# Scope and Ethics

The project covers both offensive and defensive maritime cybersecurity. Offensive research is valuable when it is controlled, sourced, and authorized.

## Practical boundary

Content can explain attack classes, protocol weaknesses, research methods, and defensive mitigations. Operational instructions for disrupting real maritime systems are out of scope.

## Safe examples

- AIS message decoding from public datasets
- AIS anomaly detection using historical data
- GNSS spoofing case-study analysis
- NMEA parser robustness testing in a local mock parser
- OpenCPN training in an isolated lab
- MaCySTe or cyber-range exercises
- Security research testing on explicitly in-scope assets

## Unsafe examples

- Transmitting false AIS messages on live maritime frequencies
- GNSS jamming or spoofing outside a shielded, authorized test environment
- Testing exposed ship systems found by internet search
- Denial-of-service against port or vessel infrastructure
- Attempting access to ECDIS, VSAT, GMDSS, propulsion, or port systems without authorization

## Language rules

Use accurate language:

- "Confirmed" only when an official source confirms it.
- "Reported" when credible media or a vendor report says it.
- "Suspected" when causality is not proven.
- "Maritime-relevant" when a general IT/OT CVE appears in maritime deployments but is not maritime-specific.
