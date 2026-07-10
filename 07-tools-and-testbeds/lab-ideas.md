# Lab Ideas

These labs are intended for local systems, public datasets, mock applications, simulators, and cyber ranges.

## Lab 1: AIS decoding and sanity checks

Goal: decode AIS messages and flag basic anomalies.

Tools:

- pyais
- AISdb
- pandas
- geopandas
- folium or kepler.gl

Checks:

- Invalid coordinates
- Impossible speed
- Sudden long-distance jumps
- MMSI reuse
- Repeated stale positions
- Track gaps

Output:

- CSV of anomalies
- Map visualization
- Short analyst note

## Lab 2: NMEA 0183 parser robustness

Goal: test a local parser against malformed or unexpected NMEA sentences.

Checks:

- Missing checksum
- Invalid checksum
- Oversized fields
- Non-numeric latitude or longitude
- Unsupported talker IDs
- Null fields
- Unicode or binary characters

Output:

- Unit tests
- Parser crash report
- Defensive validation recommendations

## Lab 3: OpenCPN AIS display lab

Goal: use OpenCPN in a local environment to understand how navigation displays consume AIS data.

Tools:

- OpenCPN
- pyais
- local TCP feed
- sample AIS data

Checks:

- How vessels appear on the display
- How stale updates are handled
- How unusual tracks are represented
- How alarms or warnings behave in simulation

Output:

- Screenshots
- Observations
- Detection ideas

## Lab 4: Shipboard OT segmentation lab

Goal: simulate IT, OT, and navigation zones and test monitoring controls.

Tools:

- VirtualBox or VMware
- OpenPLC
- Zeek
- Suricata
- mock NMEA service
- Linux routers or pfSense

Zones:

- Crew IT
- Business IT
- Navigation
- OT
- Vendor remote access
- SOC monitoring

Output:

- Network diagram
- Firewall policy
- Detection rules
- Incident-response notes

## Lab 5: Maritime SOC scenario

Goal: build a small SOC workflow around simulated vessel activity.

Inputs:

- AIS anomaly dataset
- Zeek logs
- Suricata alerts
- mock Windows endpoint logs
- incident timeline

Output:

- Triage notes
- Detection improvements
- Lessons learned
- Incident report using `templates/incident-template.md`
