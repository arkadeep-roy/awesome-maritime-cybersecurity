# Standards and Regulations

This section maps cybersecurity requirements and guidance that affect ships, ports, maritime operators, vendors, and researchers.

## Core files

| File | What it covers |
| --- | --- |
| [India Maritime Cybersecurity](india-maritime-cybersecurity.md) | DG Shipping, IRClass, Bureau of Port Security, C3iHub/IPA training |
| [NIS2 and Maritime Transport](nis2-maritime.md) | EU transport-sector cybersecurity obligations and maritime relevance |
| [TMSA 3 Element 13](tmsa3-element-13.md) | Tanker maritime security and cyber-risk assurance context |
| [BIMCO / Industry Guidelines v5](bimco-guidelines-v5.md) | Cyber Security On Board Ships, version 5, published November 2024 |
| [ISPS Code and Cybersecurity](isps-code-and-cyber.md) | How ship and port-facility security intersects with digital systems |

## Core references

| Reference | What it covers | Source |
| --- | --- | --- |
| IMO maritime cyber risk guidance | High-level cyber risk recommendations for shipping | [IMO cyber risk page](https://www.imo.org/en/ourwork/security/pages/cyber-security.aspx), [MSC-FAL.1/Circ.3/Rev.3 PDF](https://wwwcdn.imo.org/localresources/en/OurWork/Security/Documents/MSC-FAL.1-Circ.3-Rev.3.pdf) |
| IACS UR E26 | Cyber resilience of ships | [IACS press release](https://iacs.org.uk/news/iacs-ur-e26-and-e27-press-release), [ClassNK summary](https://www.classnk.or.jp/hp/en/activities/cybersecurity/ur-e26e27.html) |
| IACS UR E27 | Cyber resilience of onboard systems and equipment | [IACS press release](https://iacs.org.uk/news/iacs-ur-e26-and-e27-press-release), [ClassNK summary](https://www.classnk.or.jp/hp/en/activities/cybersecurity/ur-e26e27.html) |
| USCG MTS final rule | Baseline cybersecurity requirements for the U.S. Marine Transportation System | [USCG resource center](https://www.uscg.mil/MaritimeCyber/), [Federal Register](https://www.federalregister.gov/documents/2025/01/17/2025-00708/cybersecurity-in-the-marine-transportation-system) |
| Cyber Security Onboard Ships v5 | Industry guidance for cyber risk on ships | [Guidelines PDF](https://www.maritimeglobalsecurity.org/media/g3qlxdaw/2024-11-14-guidelines_on_cyber_security-v5-final.pdf), [Intercargo page](https://www.intercargo.org/publications/guidelines-cyber-security-onboard-ships/) |
| IEC 62443 | Industrial automation and control system security | [IEC 62443 overview](https://www.iec.ch/blog/understanding-iec-62443) |
| NIST SP 800-82 Rev. 3 | Guide to OT security | [NIST SP 800-82 Rev. 3](https://csrc.nist.gov/pubs/sp/800/82/r3/final) |

## How researchers can use this

For responsible disclosure, map a finding to operational and governance impact.

Examples:

- Broken tenant isolation in a fleet dashboard can affect confidentiality of vessel, crew, or cargo data.
- Weak remote-access controls can affect cyber risk management under IMO-style processes.
- Poor segmentation between IT and OT can conflict with IACS-style cyber-resilience principles for newbuilds or onboard systems.

Do not claim a legal violation unless you understand the vessel, flag, class, date, and applicable contractual requirements.
