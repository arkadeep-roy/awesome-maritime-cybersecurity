# Authorized Testing Methodology

This methodology structures maritime security testing without crossing into live safety-system interference.

## Acceptable testing contexts

Work only within one of these conditions:

- owned lab or simulator.
- contracted assessment.
- official VDP or safe-harbor program.
- academic cyber range.
- public-data analysis that does not touch live systems.

## Maritime scoping questions

Before testing, confirm:

- Which assets are in scope?
- Which operational functions are explicitly out of scope?
- Are vessel, port, radio, satellite, navigation, GMDSS, and OT systems excluded unless separately authorized?
- Are rate limits, scan types, and test windows defined?
- What evidence is acceptable without accessing sensitive cargo, crew, vessel, or operational data?
- Who receives urgent safety-impact notifications?

## Maritime-specific impact model

A maritime finding should explain the affected operational function, not only the technical bug class.

| Security finding | Maritime impact framing |
| --- | --- |
| IDOR in vessel records | Cross-fleet data exposure, tenant-isolation failure, possible operational privacy impact |
| Exposed document storage | Leakage of manifests, certificates, maintenance records, cargo evidence, or compliance records |
| Weak remote-access control | Vendor access pathway into shipboard, port, terminal, or fleet operations |
| Insecure telemetry API | Unauthorized visibility into vessel position, equipment state, ETA, or operational schedule |
| Exposed update portal | Supply-chain risk for chart, firmware, vessel software, or application distribution |
| Weak segmentation finding | Potential pathway from business IT, crew IT, or SATCOM into navigation or OT zones |
| Poor logging | Reduced ability to investigate ransomware, remote-access abuse, or operational disruption |

## Evidence standard

A maritime report should include:

1. scope reference;
2. affected asset and operational function;
3. vulnerability summary;
4. reproduction steps within permitted scope;
5. minimal proof of impact;
6. data minimization notes;
7. safety or regulatory relevance, if applicable;
8. remediation recommendation;
9. testing limitations.

## Research discipline

- Do not test systems that are not explicitly in scope.
- Do not run disruptive scans against maritime infrastructure.
- Do not access live navigation, distress, propulsion, cargo, or port-control systems without explicit authorization.
- Do not include target lists in public writeups.
- Prefer lab reproduction for protocol, RF, navigation, or OT claims.
