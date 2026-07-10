# Domain Overview: Maritime Cybersecurity

Maritime cybersecurity covers the identification, protection, assessment, and resilience of cyber-physical systems across the global maritime supply chain.

Unlike traditional enterprise IT, this domain intersects operational technology, legacy navigation protocols, radio-frequency systems, satellite communications, and modern cloud-based logistics. The result is a complex, high-availability attack surface where cyber incidents can affect safety, vessel operations, port availability, cargo movement, regulatory compliance, and national supply chains.

## Operational domains and architectural context

The maritime environment is shaped by the convergence of shipboard networks, shore-based infrastructure, third-party service providers, and global logistics platforms. Understanding the architectural boundaries and trust assumptions of each domain is a prerequisite for effective security research.

| Domain segment | Core systems and protocols | Security and architectural context |
| --- | --- | --- |
| Shipboard IT | Crew networks, administrative endpoints, email, onboard business systems, vessel management software | Characterized by high latency, low bandwidth, and intermittent connectivity. Often serves as an initial access or pivot point when segmentation between IT and OT is weak. |
| Shipboard OT | Propulsion, power generation, ballast, cargo handling, machinery control, ICS/SCADA systems | Safety-critical environment governed by availability and integrity requirements. Systems often have long lifecycles, legacy operating systems, and limited native security controls. Changes require strict operational change management. |
| Navigation and communications | ECDIS, AIS, GNSS/GPS, radar, VDR, GMDSS, NMEA networks | Relies heavily on legacy and broadcast-based protocols that often operate on implicit trust models. Many systems were not originally designed with encryption, authentication, or integrity protection as core assumptions. |
| Connectivity | VSAT, LEO satellite links, fleet broadband, LTE/5G, remote vendor access, ship-to-shore VPNs | Primary bridge between vessel networks, service providers, shore operations, and the public internet. Risk often arises from exposed edge devices, weak remote access controls, and provider-side compromise. |
| Port and shore infrastructure | Terminal operating systems, crane PLCs, gate systems, berth planning, customs integrations, logistics platforms | Critical infrastructure where availability and data integrity directly affect cargo flow and national supply chains. High-value target for ransomware, destructive attacks, and operational disruption. |
| Maritime software and data platforms | Fleet dashboards, crew management systems, procurement platforms, cargo tracking APIs, AIS data services, compliance portals | Represents the extended maritime enterprise. Web, API, identity, cloud, and multi-tenant security weaknesses can expose sensitive operational and commercial data. |

## Domain translation for security researchers

Applying traditional security research methods to the maritime domain requires mapping familiar techniques to maritime-specific systems, identifiers, operational constraints, and impact models.

| Traditional security practice | Maritime application and target vector |
| --- | --- |
| External attack surface mapping | Identifying authorized assets across shipping companies, port authorities, maritime vendors, satellite providers, and logistics platforms to understand the extended supply-chain attack surface. |
| Protocol analysis | Studying AIS, NMEA 0183, NMEA 2000, IEC 61162-450, Modbus, OPC UA, and related systems in controlled environments to understand trust assumptions, parser behavior, and monitoring opportunities. |
| Identity and access review | Assessing role boundaries between fleet operators, port users, crew managers, agents, vendors, terminal staff, and third-party service providers. |
| Impact quantification and reporting | Translating technical findings into operational, safety, regulatory, and business impact. Findings should be contextualized against maritime frameworks such as IMO cyber-risk guidance, IACS UR E26/E27, IEC 62443, and relevant port or national requirements. |

## Research methodology and onboarding

For security professionals entering maritime cybersecurity, the following methodology provides a structured way to build domain knowledge and conduct responsible research.

### 1. Architectural analysis

Study the physical and logical separation between shipboard IT, shipboard OT, navigation systems, and shore infrastructure.

Focus areas:

- vessel network zoning
- IT/OT boundary controls
- remote access paths
- vendor maintenance links
- ship-to-shore data flows
- segmentation between crew, business, navigation, and operational systems.

### 2. Protocol and system analysis

Learn the trust boundaries and design assumptions of foundational maritime systems and protocols.

Priority areas:

- AIS
- GNSS/GPS
- ECDIS
- NMEA 0183
- NMEA 2000
- IEC 61162-450
- VSAT and SATCOM connectivity
- GMDSS
- terminal operating systems
- shipboard OT and automation systems.

The goal is not only to identify weaknesses, but to understand how these systems are used operationally and how failures may affect safety and availability.

### 3. Threat intelligence and precedent analysis

Review public incidents, advisories, CVEs, and post-incident reporting to understand real-world failure modes.

Relevant examples include:

- Maersk / NotPetya
- DNV ShipManager ransomware
- port and terminal ransomware incidents
- GNSS spoofing and jamming events
- VSAT and satellite-provider compromise scenarios
- exposed maritime management systems
- maritime OT vulnerabilities and advisories.

### 4. Environment emulation

Build isolated environments before attempting any form of offensive or defensive testing.

Useful lab components include:

- MaCySTe for maritime cyber-physical simulation
- OpenCPN for navigation and chart-plotter workflows
- OpenPLC for shipboard OT-style control logic
- AIS and NMEA datasets
- local mock fleet-management APIs
- Zeek, Suricata, Wazuh, or OpenSearch for monitoring
- SDR hardware only in lawful, controlled, and properly isolated environments.

### 5. Authorized offensive research

Conduct offensive research only within clear legal and operational boundaries.

Acceptable environments include:

- owned labs
- cyber ranges
- academic testbeds
- explicitly scoped vulnerability disclosure programs
- written authorization from the asset owner
- controlled internal assessments.

Do not interact with live vessel systems, port infrastructure, navigation systems, distress communications, satellite terminals, or licensed maritime frequencies without explicit authorization.

### 6. Defensive integration

Offensive findings are more valuable when mapped to defensive controls.

For each finding, consider:

- how it could be detected
- which logs or telemetry would show it
- whether segmentation would limit impact
- how recovery would work at sea or in port
- which operational process owns the risk
- how it maps to IEC 62443, IACS UR E26/E27, IMO guidance, or local regulatory expectations.


