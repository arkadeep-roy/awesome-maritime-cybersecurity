# Reporting Guide

## Report structure

1. Summary
2. Affected asset and scope proof
3. Vulnerability type
4. Minimal reproduction steps
5. Evidence with sensitive data redacted
6. Impact in maritime context
7. Suggested remediation
8. Researcher safety statement

## Maritime impact examples

| Finding | Possible impact framing |
| --- | --- |
| Broken tenant isolation | Cross-company access to vessel, crew, cargo, or maintenance data |
| Exposed storage bucket | Leakage of operational documents, certificates, images, manifests, or logs |
| Weak SSO redirect validation | Account compromise across fleet-management users |
| Insecure telemetry API | Unauthorized access to vessel position or equipment status, depending on data sensitivity |
| File upload flaw | Risk to document workflows or user sessions, not necessarily OT impact |

## Safety statement example

"Testing was limited to the assets explicitly listed in scope. Evidence collection avoided unnecessary access, modification, or deletion of data. Operational technology, vessel systems, radio systems, navigation systems, distress systems, and live maritime infrastructure were not tested."
