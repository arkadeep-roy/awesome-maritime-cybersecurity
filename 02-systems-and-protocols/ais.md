# AIS

Automatic Identification System is used for vessel identification, traffic awareness, and collision-avoidance support. AIS broadcasts are intentionally open so vessels and shore stations can receive them.

## Security relevance

AIS data is not a cryptographically authenticated source of truth. Public research and security literature repeatedly note risks including spoofing, identity manipulation, false tracks, and availability disruption.

## Safe research paths

- Decode AIS messages from public datasets.
- Compare vessel movement against kinematic constraints.
- Study AIS outage and anomaly patterns.
- Use AIS-only evidence cautiously. It can support a hypothesis but usually cannot prove attribution.

## Tools and papers

- [pyais](https://github.com/M0r13n/pyais)
- [libais](https://github.com/schwehr/libais)
- [rtl-ais](https://github.com/dgiardini/rtl-ais)
- [SeaSpoofFinder paper](https://arxiv.org/abs/2602.16257)
- [AIS anomaly detection paper](https://arxiv.org/abs/2002.05013)

## Boundary

Live AIS transmission and spoofing instructions are out of scope.
