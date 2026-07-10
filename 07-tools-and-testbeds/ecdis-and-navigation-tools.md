# ECDIS and Navigation-System Tools

## OpenCPN

Labels: `lab`, `defensive`, `offensive-research`

Open-source chart plotter and navigation platform.

- [Website](https://opencpn.org)
- [Repository](https://github.com/OpenCPN/OpenCPN)

Maritime use cases:

- Learn chart-plotter workflows.
- Test AIS display behavior in a local lab.
- Study plugin attack surface.
- Feed simulated NMEA/AIS data.
- Build ECDIS-like training scenarios.

## OpenS100

Labels: `offensive-research`, `defensive`, `cve-analysis`, `lab`

OpenS100 is relevant because of S-100 portrayal and chart-processing security research.

Known issue:

```text
CVE-2026-22208
OpenS100 remote code execution via unrestricted Lua interpreter in portrayal-catalogue handling.
```

- [NVD](https://nvd.nist.gov/vuln/detail/CVE-2026-22208)

Recommended repo use:

- CVE summary.
- Affected component.
- Root cause.
- Patch reference.
- Defensive recommendations.
- Supply-chain implications.
