# AIS Tools

AIS tooling is relevant for vessel tracking, anomaly detection, dark-fleet research, sanctions-evasion analysis, and defensive maritime-domain awareness.

## pyais

Labels: `data`, `defensive`, `offensive-research`, `lab`

Python library for AIS message encoding and decoding.

- [Repository](https://github.com/M0r13n/pyais)
- [PyPI](https://pypi.org/project/pyais/)

Install:

```bash
pip install pyais
```

Decode a single AIS message:

```python
from pyais import decode

raw = "!AIVDM,1,1,,B,13u@PDEPhM1P6QPBCPsoHl8N0P00,0*0D"
msg = decode(raw)

print(msg)
print("MMSI:", getattr(msg, "mmsi", None))
print("Latitude:", getattr(msg, "lat", None))
print("Longitude:", getattr(msg, "lon", None))
```

Maritime use cases:

- Decode AIS feeds from files, TCP streams, or datasets.
- Build AIS anomaly-detection pipelines.
- Flag impossible speed, position jumps, duplicate MMSI behavior, and stale tracks.
- Create training labs for AIS message structure.

## ais-decoder

Labels: `data`, `defensive`, `lab`

C++ AIS decoder with Python bindings.

- [Repository](https://github.com/aduvenhage/ais-decoder)

Maritime use cases:

- High-performance AIS decoding.
- C++ integration for maritime analytics.
- Batch processing of AIS NMEA sentences.
- Comparison against pyais and libais output.

## libais

Labels: `data`, `defensive`, `lab`

C++ AIS decoding library used in AIS tooling and research.

- [Repository](https://github.com/schwehr/libais)

Maritime use cases:

- AIS parser validation.
- Cross-checking decoder behavior.
- Research-grade AIS data pipelines.

## rtl-ais

Labels: `rf`, `data`, `defensive`, `lab`

AIS receiver using RTL-SDR hardware.

- [Repository](https://github.com/dgiardini/rtl-ais)

Build:

```bash
git clone https://github.com/dgiardini/rtl-ais.git
cd rtl-ais
make
```

Maritime use cases:

- Low-cost AIS receive station.
- Port-area AIS collection where permitted.
- Building baseline datasets for anomaly detection.
- RF learning for maritime security students.

## AIS-catcher

Labels: `rf`, `data`, `defensive`, `lab`

Modern AIS receiver supporting multiple SDR devices and output formats.

- [Repository](https://github.com/jvde-github/AIS-catcher)

Maritime use cases:

- AIS reception with RTL-SDR, Airspy, HackRF, SDRPlay, or network input.
- Forwarding decoded AIS as NMEA over UDP, TCP, HTTP, or other formats.
- Building a receive-side research station.
- Producing local AIS feeds for dashboards or labs.

## AISdb

Labels: `data`, `defensive`, `research`

AIS database and analysis tooling for storing, querying, and processing AIS data.

- [Repository](https://github.com/AISViz/AISdb)

Maritime use cases:

- Long-term AIS storage.
- Vessel trajectory analysis.
- Geospatial queries.
- Research on maritime movement patterns.

## SeaSpoofFinder

Labels: `data`, `defensive`, `research`

AIS-based framework for detecting candidate GNSS spoofing events.

- [Project](https://seaspooffinder.github.io/ais_data)
- [Paper](https://arxiv.org/abs/2602.16257)

Maritime use cases:

- GNSS spoofing research.
- Incident analysis.
- Defensive maritime-domain awareness.
- Teaching how AIS can reveal navigation deception.

Limitations:

- AIS-based detection can identify suspicious patterns.
- It does not prove attribution by itself.

## AIS_Tracker

Labels: `osint`, `data`, `defensive`

AIS-oriented OSINT project for vessel monitoring and intelligence workflows.

- [Repository](https://github.com/arandomguyhere/AIS_Tracker)

Maritime use cases:

- Dark-fleet research.
- Vessel behavior tracking.
- Sanctions-evasion research.
- AIS gap analysis.
- Vessel intelligence enrichment.

Before production use, review the license, data-source terms, and API restrictions.
