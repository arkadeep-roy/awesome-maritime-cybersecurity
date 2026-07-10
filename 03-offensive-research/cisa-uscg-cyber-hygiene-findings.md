# CISA and USCG Cyber Hygiene Findings

CISA and the U.S. Coast Guard published Advisory AA25-212A on 31 July 2025 after a proactive threat-hunting engagement at a U.S. critical infrastructure organization. The advisory is not limited to maritime, but it is directly relevant to maritime offensive research because it describes real cyber-hygiene weaknesses defenders should expect to find in critical infrastructure environments.

Source: [CISA Advisory AA25-212A](https://www.cisa.gov/news-events/cybersecurity-advisories/aa25-212a)

## Why this belongs in maritime offensive research

Maritime assessments often fail when they stay at the level of generic vulnerability scanning. AA25-212A is relevant because it translates into concrete research questions for ports, ship operators, terminal operators, and maritime service providers.

## Research areas derived from the advisory

| Advisory theme | Maritime research question |
| --- | --- |
| Asset and network visibility | Can the operator prove which systems belong to crew IT, business IT, navigation, OT, remote access, and SATCOM paths? |
| Segmentation | Can an incident in enterprise IT, crew Wi-Fi, vendor access, or SATCOM management reach navigation or OT networks? |
| Identity and access | Are remote-maintenance, administrator, and service accounts separated, logged, and regularly reviewed? |
| Logging and monitoring | Would the operator detect lateral movement, unauthorized remote access, unusual authentication, or changes to critical configuration? |
| Patch and configuration management | Are internet-facing, remote-access, and edge systems managed despite vessel bandwidth and access constraints? |
| Incident response | Can the operator isolate affected systems without losing essential safety and communications functions? |

## Maritime-specific test planning

For authorized assessments, turn the themes above into evidence questions:

- Is there a current zone-and-conduit diagram for vessel networks?
- Are SATCOM, crew, business, navigation, and OT segments separated by enforceable controls?
- Are vendor remote-access paths inventoried and time-bound?
- Are logs collected from VPNs, identity systems, firewalls, EDR, and critical management interfaces?
- Are bridge workstations, chart-update systems, and OT engineering stations included in asset inventory?
- Is there a recovery plan for loss of remote communications or satellite-linked management systems?
- Are cyber incidents reportable under relevant national MTS rules, SMS processes, or port-facility procedures?

## Related official resources

- [CISA Port Resilience Index](https://www.cisa.gov/mts-resilience-resources/port-resilience-index)
- [CISA Marine Transportation System Resilience Assessment Guide](https://www.cisa.gov/news-events/news/cisa-releases-marine-transportation-system-resilience-assessment-guide-0)
- [USCG Maritime Cybersecurity Resource Center](https://www.uscg.mil/MaritimeCyber/)
- [GAO-25-107244, Coast Guard: Additional Efforts Needed to Address Cybersecurity Risks to the Maritime Transportation System](https://www.gao.gov/products/gao-25-107244)

## Boundary

Use this material for assessment planning and control validation, not unsolicited scanning or testing of maritime infrastructure.
