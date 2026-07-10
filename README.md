# Maritime Cybersecurity Knowledge Base

> A comprehensive resource for maritime cybersecurity research, vulnerability analysis, and defensive operations across vessel systems, ports, and maritime infrastructure.

[![License](https://img.shields.io/badge/License-CC%20BY%204.0-blue)](https://creativecommons.org/licenses/by/4.0/)
[![Research](https://img.shields.io/badge/Scope-Offensive%20%2B%20Defense-red)]()
[![Updated](https://img.shields.io/badge/Updated-2026-green)]()

## About
This repository serves as a centralized, peer-reviewed resource for maritime cybersecurity research spanning vessel systems, port infrastructure, satellite communications, navigation protocols, regulatory frameworks, disclosed vulnerabilities, historical incidents, open-source tooling, vendor ecosystems, and regional threat landscapes.

Intended audience: Security researchers, defensive practitioners, maritime engineers, incident responders, policy analysts, and students working with cyber risk in the maritime domain.

Governance: Community-maintained under CC BY 4.0. All contributions are peer-reviewed. See CONTRIBUTING.md for submission guidelines.

---

## 🚀 Getting Started

| Stage | Start with |
| --- | --- |
| Domain orientation | [What is maritime cybersecurity?](00-start-here/what-is-maritime-cybersecurity.md) |
| Research boundary | [Scope and ethics](00-start-here/scope-and-ethics.md) |
| Learning sequence | [Learning roadmap](00-start-here/learning-roadmap.md) |
| Technical systems | [Systems and protocols](02-systems-and-protocols/README.md) |
| Offensive research | [Offensive research](03-offensive-research/README.md) |
| Defensive work | [Defensive engineering](04-defensive-engineering/README.md) |
| Disclosure work | [Disclosure and VDPs](09-disclosure-and-vdps/README.md) |
| Evidence and sources | [Sources index](data/sources.yml) |

---

## 🎯 What's Inside

This knowledge base covers:

- **Vessel Systems**: ECDIS, AIS, GNSS, NMEA, VSAT, GMDSS
- **OT Security**: PLCs, SCADA, propulsion, ballast systems
- **Threat Intelligence**: Real incidents, CVEs, TTPs
- **Compliance**: IMO, IACS UR E26/E27, USCG, NIS2
- **Research Tools**: Testbeds, simulators, decoding tools
- **Bug Bounty**: VDPs, safe harbor programs, maritime SaaS

---

## Coverage

| Area | Coverage |
| --- | --- |
| Systems and protocols | AIS, GNSS, ECDIS, NMEA, VSAT/SATCOM, GMDSS, shipboard OT, port systems |
| Offensive research | Maritime attack-surface taxonomy, system-specific research areas, authorized testing methodology, advisory mapping |
| Standards | IMO, IACS UR E26/E27, USCG MTS rule, NIS2, TMSA3, BIMCO guidelines, ISPS context, India-specific references |
| Vulnerabilities | OpenS100/S-100, Navis WebAccess, KEPServerEX, ctrlX OS, lighttpd in maritime-facing contexts |
| Incidents | Maersk, DNV ShipManager, CMA CGM, Port of Nagoya, DP World Australia, MSC Antonia, Lab Dookhtegan, dark-fleet risk |
| Tools and labs | AIS, GNSS, NMEA, OpenCPN, OpenPLC, MaCySTe, cyber ranges, defensive monitoring, RF hardware |
| Organizations | Classification societies, cyber vendors, ISACs, legal/insurance advisory, India ecosystem, legacy vendors |
| Regional coverage | Initial coverage for Europe/North Atlantic, India/IOR, Southeast Asia, Middle East/Red Sea, East Asia, Russia/Baltic/Black Sea, and Oceania/Pacific |

---

## Repository map

```text
00-start-here/                 Field overview, scope, and learning path
01-standards-and-regulations/  IMO, IACS, USCG, NIS2, TMSA3, BIMCO, ISPS, India
02-systems-and-protocols/      AIS, GNSS, ECDIS, NMEA, VSAT, GMDSS, OT, port systems
03-offensive-research/         Maritime offensive research maps and authorized methodology
04-defensive-engineering/      Monitoring, detection, hardening, and response use cases
05-vulnerabilities-and-cves/   CVEs, vulnerability classes, and classification notes
06-real-world-incidents/       Case studies with confidence labels and sources
07-tools-and-testbeds/         Tools, datasets, simulators, cyber ranges, RF hardware, lab ideas
08-research-papers/            Academic papers, whitepapers, and threat-intelligence reports
09-disclosure-and-vdps/        Verified VDPs, safe-harbor references, and report guidance
10-companies-and-orgs/         Vendors, classification societies, ISACs, research groups, advisory firms
11-regional-coverage/          Regional maritime cyber context
templates/                     Contribution templates
data/                          Source and reference index
.github/                       Issue and pull-request templates
```



## Current Source

Core official and primary references include:

- IMO maritime cyber-risk guidance: [MSC-FAL.1/Circ.3/Rev.3](https://wwwcdn.imo.org/localresources/en/OurWork/Security/Documents/MSC-FAL.1-Circ.3-Rev.3.pdf) and [IMO Maritime Cyber Risk](https://www.imo.org/en/ourwork/security/pages/cyber-security.aspx)
- IACS ship cyber-resilience requirements: [UR E26/E27 press release](https://iacs.org.uk/news/iacs-ur-e26-and-e27-press-release) and [ClassNK summary](https://www.classnk.or.jp/hp/en/activities/cybersecurity/ur-e26e27.html)
- U.S. Coast Guard MTS cybersecurity rule: [USCG Maritime Cybersecurity Resource Center](https://www.uscg.mil/MaritimeCyber/) and [Federal Register final rule](https://www.federalregister.gov/documents/2025/01/17/2025-00708/cybersecurity-in-the-marine-transportation-system)
- CISA and USCG cyber-hygiene advisory: [AA25-212A](https://www.cisa.gov/news-events/cybersecurity-advisories/aa25-212a)
- CISA MTS resilience resources: [Port Resilience Index](https://www.cisa.gov/mts-resilience-resources/port-resilience-index) and [MTS Resilience Assessment Guide](https://www.cisa.gov/news-events/news/cisa-releases-marine-transportation-system-resilience-assessment-guide-0)
- GAO review of Coast Guard maritime cybersecurity efforts: [GAO-25-107244](https://www.gao.gov/products/gao-25-107244)
- Industry Guidelines on Cyber Security On Board Ships v5: [Guidelines PDF](https://www.maritimeglobalsecurity.org/media/g3qlxdaw/2024-11-14-guidelines_on_cyber_security-v5-final.pdf)

Vendor and industry incident statistics are placed in [Threat intelligence reports](08-research-papers/threat-intelligence-reports.md) and are treated as attributed reporting, not as universal incident totals.

## Core research references

- [MaCySTe](https://github.com/CRACK-MCR/MaCySTe)
- [SeaSpoofFinder paper](https://arxiv.org/abs/2602.16257)
- [Literature Review: Cyber Security Monitoring in Maritime](https://arxiv.org/abs/2503.18173)
- [A Sea of Cyber Threats](https://arxiv.org/abs/2506.15842)
- [An In-Depth Security Assessment of Maritime Container Terminal Software Systems](https://arxiv.org/abs/2006.12056)
- [NVD CVE-2026-22208](https://nvd.nist.gov/vuln/detail/CVE-2026-22208)
- [ABB advisory on KEPServerEX impact on Marine ITMonitoring](https://search.abb.com/library/Download.aspx?Action=Launch&DocumentID=8MAL100030-0015&DocumentPartId=&LanguageCode=en)

## Regional coverage

Regional pages provide initial context rather than exhaustive country coverage. Each page identifies source anchors and avoids live target lists or operational scanning details. See [11-regional-coverage/](11-regional-coverage/).

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) and [STYLE_GUIDE.md](STYLE_GUIDE.md) before opening a pull request. New entries should include a source, a concise explanation.
