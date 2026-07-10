# Maritime Offensive Research Map

Maritime offensive research areas are organized by system to support lab work, CVE analysis, authorized assessments, and responsible disclosure. Procedures for disrupting live vessels, ports, radio systems, satellite systems, or navigation infrastructure are out of scope.

## Research model

Maritime offensive research should answer four questions:

1. What maritime function depends on the system?
2. What trust boundary is crossed?
3. What failure mode would matter operationally?
4. Can the issue be reproduced safely in a lab, simulator, cyber range, or scoped engagement?

## AIS research

Relevant functions:

- vessel identification and tracking;
- collision-avoidance awareness;
- port traffic monitoring;
- sanctions and dark-fleet analysis;
- maritime domain awareness.

Research areas:

- AIS message parsing and validation;
- impossible movement and duplicate-MMSI detection;
- stale tracks, identity inconsistency, and position jumps;
- receiver-side trust assumptions;
- AIS data broker API integrity and provenance;
- defensive anomaly pipelines using public or licensed AIS datasets.

Safe artifacts:

- offline AIS parsers;
- anomaly-detection notebooks;
- simulator-only AIS feeds;
- detection rules and validation datasets.

Do not publish live AIS transmission instructions or target live AIS infrastructure.

## GNSS and navigation-integrity research

Relevant functions:

- ECDIS position input;
- AIS position source;
- timing;
- dynamic positioning;
- fleet telemetry;
- incident reconstruction.

Research areas:

- receiver trust and cross-checking logic;
- GNSS anomaly detection using AIS, radar, visual bearings, or inertial inputs;
- spoofing/jamming indicators in historical datasets;
- bridge workflow under navigation-data inconsistency;
- alerting gaps when position drift is gradual.

Safe artifacts:

- analysis of public interference maps;
- lab-only receiver tests in RF-contained environments;
- sensor-fusion detection prototypes;
- incident-analysis templates.

Do not publish live GNSS transmit/replay procedures.

## ECDIS, S-100, and chart-supply-chain research

Relevant functions:

- route planning;
- chart display;
- navigation alerts;
- ingestion of Electronic Navigational Charts and portrayal catalogues;
- update distribution.

Research areas:

- chart and portrayal-catalogue parser security;
- S-100/S-101 supply-chain assumptions;
- unsafe scripting or rendering logic;
- plugin/update trust boundaries;
- legacy OS exposure in bridge workstations;
- USB-mediated update workflows;
- file-format fuzzing in local viewers.

Key source anchor:

- [CVE-2026-22208, OpenS100 remote code execution via unrestricted Lua interpreter in portrayal catalogue handling](https://nvd.nist.gov/vuln/detail/CVE-2026-22208)

Safe artifacts:

- CVE analysis;
- patched/unpatched behavior notes where legally available;
- defensive validation guidance;
- mock chart/update pipeline labs.

## NMEA 0183, NMEA 2000, and IEC 61162-450 research

Relevant functions:

- GPS input;
- heading and speed data;
- depth and wind data;
- AIS integration;
- autopilot and bridge-network data exchange.

Research areas:

- parser robustness;
- checksum and field validation;
- device trust on shared buses;
- gateway security between serial/CAN and IP networks;
- monitoring for unexpected talkers, PGNs, or Ethernet bridge behavior;
- protocol translation into Signal K or other web-native formats.

Safe artifacts:

- parser unit tests;
- local fuzzing harnesses;
- passive decoding labs;
- mock NMEA feeds;
- monitoring logic for lab traffic.

Do not inject frames into operational vessel networks.

## VSAT, SATCOM, and remote-connectivity research

Relevant functions:

- ship-to-shore communications;
- remote diagnostics;
- crew internet;
- fleet operations;
- weather and voyage updates;
- emergency communications backup paths.

Research areas:

- provider-side compromise as fleet-level risk;
- terminal management-plane exposure;
- credential and configuration handling;
- segmentation between communications equipment and onboard networks;
- firmware/update lifecycle;
- failover and recovery when terminals are unavailable;
- satellite-linked edge devices and VPN concentrators.

Safe artifacts:

- architecture reviews;
- CVE-to-device mapping;
- lab-only management-plane assessment;
- provider-risk questionnaires;
- recovery-time and physical-access analysis.

## Shipboard OT research

Relevant functions:

- propulsion;
- steering;
- machinery and power management;
- ballast;
- cargo handling;
- dynamic positioning;
- alarm and monitoring systems.

Research areas:

- segmentation between crew IT, business IT, navigation, OT, and vendor access;
- exposed Modbus TCP, OPC UA, SMB, RDP, or web management interfaces in labs or authorized assessments;
- insecure remote maintenance workflows;
- endpoint age and patch constraints;
- incident response where bandwidth, sea state, and physical access limit recovery.

Safe artifacts:

- OpenPLC labs;
- MaCySTe scenarios;
- detection engineering;
- tabletop exercises;
- CVE impact mapping for marine automation products.

## Port and terminal-system research

Relevant functions:

- terminal operating systems;
- gate and truck appointment systems;
- container tracking;
- berth planning;
- customs and single-window integrations;
- crane and yard operations;
- port community systems.

Research areas:

- authorization flaws across terminal, shipper, carrier, customs-broker, and port-authority roles;
- API access to cargo, container, appointment, or billing objects;
- document-generation and file-storage workflows;
- integration security between TOS, PCS, customs, EDI, and customer portals;
- ransomware resilience and manual fallback.

Safe artifacts:

- mock terminal APIs;
- role-model analysis;
- report templates for cargo/port impact;
- resilience tabletop exercises.

## GMDSS and safety communications research

Relevant functions:

- distress alerting;
- maritime safety information;
- ship-to-shore emergency communication;
- SAR coordination.

Research areas:

- dependence on GNSS position and timing;
- authentication and operator-verification workflows;
- false alert handling;
- fallback procedures;
- integration with bridge systems and logs.

Safe artifacts:

- process analysis;
- incident tabletop scenarios;
- defensive logging checklists;
- awareness material.

Do not publish distress-signal abuse procedures.

## Reporting impact

A maritime offensive finding should map to at least one operational category:

| Category | Example impact |
| --- | --- |
| Navigation integrity | incorrect position, route, alert, or chart data |
| Communications availability | loss of ship-to-shore data, remote support, or backup channels |
| Port throughput | gate, yard, berth, container, or customs disruption |
| Shipboard OT | degraded monitoring, control, or recovery capability |
| Safety management | inability to prove cyber risk is addressed in SMS or equivalent controls |
| Regulatory exposure | mismatch with IACS, IMO, USCG, NIS2, TMSA3, or class expectations |
| Supply-chain trust | compromised chart, firmware, update, or vendor-access pathway |
