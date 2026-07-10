# NMEA and Marine Protocol Tools

NMEA protocols carry navigation, sensor, engine, AIS, and instrument data across vessel systems.

## Canboat

Labels: `data`, `defensive`, `offensive-research`, `lab`

NMEA 2000 and NMEA 0183 utilities, including PGN decoding.

- [Repository](https://github.com/canboat/canboat)
- [Documentation](https://canboat.github.io/canboat/canboat.html)

Maritime use cases:

- Decode NMEA 2000 PGNs.
- Analyze lab CAN/NMEA traffic.
- Build defensive monitoring for marine electronics.
- Understand how NMEA 2000 messages are structured.

## Signal K Server

Labels: `data`, `defensive`, `lab`

Signal K is a modern open marine data format and server ecosystem built around JSON, HTTP, WebSockets, and boat data integration.

- [Website](https://signalk.org)
- [Repository](https://github.com/SignalK/signalk-server)

Maritime use cases:

- Convert marine data into web-native formats.
- Build lab dashboards.
- Bridge NMEA 0183, NMEA 2000, Seatalk, and other inputs.
- Study how marine telemetry is exposed over modern web protocols.

## Wireshark

Labels: `data`, `defensive`, `offensive-research`, `lab`

Network protocol analyzer.

- [Website](https://www.wireshark.org)

Maritime use cases:

- Inspect NMEA over TCP/UDP.
- Analyze IEC 61162-450 traffic.
- Review Modbus TCP and OPC UA traffic in shipboard OT labs.
- Build packet captures for training and detection engineering.

Example lab-only capture:

```bash
tshark -i eth0 -f "tcp port 10110" -w nmea-lab.pcapng
```

Example offline analysis:

```bash
tshark -r nmea-lab.pcapng -Y "tcp.port == 10110"
```

## NMEA 0183 checksum helper

Labels: `offensive-research`, `defensive`, `lab`

Use this helper for parser unit tests and simulator data generation.

```python
def nmea_checksum(body: str) -> str:
    checksum = 0
    for char in body:
        checksum ^= ord(char)
    return f"{checksum:02X}"

def build_nmea_sentence(body: str) -> str:
    return f"${body}*{nmea_checksum(body)}"

if __name__ == "__main__":
    body = "GPGGA,120000,3750.789,N,12230.999,W,1,08,1.0,10.0,M,,,"
    print(build_nmea_sentence(body))
```

## Local NMEA parser robustness harness

Labels: `offensive-research`, `lab`

This produces test strings for local parser testing. It does not talk to serial devices or live systems.

```python
import random

def checksum(body: str) -> str:
    value = 0
    for char in body:
        value ^= ord(char)
    return f"{value:02X}"

def sentence(body: str) -> str:
    return f"${body}*{checksum(body)}"

def generate_validish_gga() -> str:
    lat = f"{random.randint(0, 89):02d}{random.randint(0, 59):02d}.{random.randint(0, 9999):04d}"
    lon = f"{random.randint(0, 179):03d}{random.randint(0, 59):02d}.{random.randint(0, 9999):04d}"

    fields = [
        "GPGGA", "120000", lat, random.choice(["N", "S"]), lon,
        random.choice(["E", "W"]), "1", str(random.randint(0, 12)),
        "1.0", "10.0", "M", "", "",
    ]
    return sentence(",".join(fields))

def generate_malformed_cases() -> list[str]:
    return [
        "$GPGGA,,,,,,,,,,,,*00",
        "$GPGGA," + "A" * 5000 + "*00",
        "$GPGGA,not-a-time,not-lat,N,not-lon,E,1,08,1.0,10.0,M,,,*00",
        "$GPGGA,120000,3750.789,N,12230.999,W,1,08,1.0,10.0,M,,,*ZZ",
        "GPGGA,120000,3750.789,N,12230.999,W,1,08,1.0,10.0,M,,,",
        "$PTEST,\x00\x01\x02*00",
    ]

if __name__ == "__main__":
    for _ in range(10):
        print(generate_validish_gga())
    for item in generate_malformed_cases():
        print(item)
```

Maritime applications:

- Parser robustness testing.
- Unit tests.
- CI pipeline checks for NMEA parsers.
- Training on malformed navigation data.
