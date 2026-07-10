# Maritime Attack Surface

Maritime attack surface is not one network. It is a set of connected operational functions: ship navigation, communications, machinery, port logistics, cargo documentation, remote maintenance, and regulatory evidence. A useful assessment starts from those functions, then maps systems and trust boundaries.

## High-value maritime asset classes

| Asset class | Examples | Primary risk question |
| --- | --- | --- |
| Navigation systems | ECDIS, GNSS receivers, AIS receivers, radar integration, voyage planning | Can data integrity be trusted and cross-checked? |
| Marine data networks | NMEA 0183, NMEA 2000, IEC 61162-450, Signal K gateways | Who can publish, bridge, or transform navigation and sensor data? |
| SATCOM and remote access | VSAT terminals, VPNs, vendor access, fleet operations links | Can shore-side or provider compromise reach vessels? |
| Shipboard OT | propulsion, steering, ballast, cargo, power management, dynamic positioning | Are control and monitoring zones segmented and recoverable? |
| Port and terminal systems | TOS, PCS, gate systems, berth planning, crane/yard integrations | Can data or availability failures affect cargo flow? |
| Chart and update supply chain | ENC/S-63/S-100 data, firmware, ECDIS updates, USB workflows | Can update trust be abused? |
| Maritime enterprise systems | fleet dashboards, crew management, procurement, certificates, maintenance | Can tenant isolation or operational confidentiality fail? |
| Maritime data platforms | AIS data brokers, vessel intelligence, sanctions screening, telemetry APIs | Can data provenance, authorization, or enrichment logic be abused? |

## System-specific vulnerability classes

| Area | Research class | Maritime impact |
| --- | --- | --- |
| AIS | parser trust, identity inconsistency, impossible movement, data-provenance gaps | maritime-domain-awareness integrity |
| GNSS | spoofing/jamming detection gaps, weak sensor fusion, poor operator alerting | navigation integrity and bridge decision support |
| ECDIS/S-100 | file parser flaws, unsafe portrayal logic, update trust, legacy OS exposure | chart display integrity and navigation availability |
| NMEA / IEC 61162 | weak validation, unauthenticated data streams, gateway exposure | bridge data integrity and device trust |
| VSAT / SATCOM | exposed management plane, weak credentials, provider-side cascade, poor segmentation | communications availability and shore-to-ship trust |
| Shipboard OT | flat networks, legacy services, unsafe remote maintenance, weak logging | machinery, propulsion, cargo, and recovery risk |
| Port systems | broken authorization, ransomware exposure, integration trust, weak manual fallback | terminal throughput and supply-chain disruption |
| Maritime SaaS | BOLA/IDOR, tenant isolation, document leakage, telemetry API exposure | fleet confidentiality, operational privacy, compliance evidence |

## Common maritime web/API bug classes

Web and API bugs remain relevant, but only when tied to maritime workflows.

| Bug class | Maritime example | Impact |
| --- | --- | --- |
| IDOR/BOLA | Changing `vessel_id`, `crew_id`, `cargo_id`, `port_call_id` | Cross-tenant access to vessel, crew, cargo, or operations data |
| Broken RBAC | Viewer role can download certificates, manifests, or maintenance records | Compliance, privacy, and operational confidentiality |
| Insecure object storage | Public documents, manifests, images, maintenance exports | Data exposure and third-party risk |
| API key leakage | Frontend keys for maps, telemetry, storage, analytics | Abuse depends on key scope and restrictions |
| Weak SSO/OAuth | Misconfigured redirect or tenant binding | Account takeover or tenant switching |
| File upload flaws | Document portal accepts unsafe files | Malware or stored XSS in operations workflows |
| SSRF or unsafe fetch | Chart/document processor fetches attacker-controlled URLs | internal metadata, document pipeline, or network exposure |
| CSV/Excel injection | Exported manifests or cargo tables execute formulas | downstream analyst or operations workstation risk |

## Trust boundaries to document

A maritime assessment should explicitly map these boundaries:

- shore network to vessel network.
- vendor remote-access path to shipboard systems.
- crew IT to navigation or OT networks.
- SATCOM terminal to internal network.
- serial/CAN bus to IP gateway.
- port community system to terminal operator.
- terminal operator to shipping-line customer portal.
- chart/update provider to ECDIS workstation.
- public AIS/GNSS data to operational decision-making.

## Research boundaries

Use only assets explicitly in scope for a VDP, employer engagement, lab, cyber range, academic testbed, or written authorization. Do not scan or test live ship, port, VSAT, ECDIS, GNSS, AIS, GMDSS, or navigation infrastructure discovered through internet search.
