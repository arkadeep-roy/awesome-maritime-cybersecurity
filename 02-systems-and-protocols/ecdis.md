# ECDIS

Electronic Chart Display and Information System integrates electronic charts with navigation inputs such as GNSS, AIS, radar, and route planning data.

## Security relevance

ECDIS risk can come from multiple layers:

- Operating-system age and patching constraints
- Chart and portrayal-catalogue update supply chains
- Network exposure and weak segmentation
- Input validation in chart, plugin, or navigation-data parsing
- USB or removable-media update workflows

## Latest

CVE-2026-22208 affects OpenS100, the reference implementation S-100 viewer, before commit 753cf29. NVD describes remote code execution through an unrestricted Lua interpreter exposed to untrusted portrayal catalogues. See [NVD CVE-2026-22208](https://nvd.nist.gov/vuln/detail/CVE-2026-22208) and [GitHub advisory GHSA-vq48-824m-7qhf](https://github.com/advisories/GHSA-vq48-824m-7qhf).

## Safe research paths

- Study OpenCPN in a local lab.
- Analyze chart update trust boundaries.
- Build mock parsers and test malformed input locally.
- Map ECDIS dependencies and update workflows.

## Boundary

Do not test operational bridge systems without explicit written authorization.
