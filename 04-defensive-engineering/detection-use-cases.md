# Detection Use Cases

## Shipboard network use cases

| Use case | Signal | Operational relevance |
| --- | --- | --- |
| Unauthorized remote access | New VPN/RDP/VNC source or vendor account use | Remote support is a common trust boundary |
| IT-to-OT connection attempt | Traffic from crew/admin networks to navigation or control zones | Possible segmentation failure or lateral movement |
| Removable media event | New USB device on bridge or engineering workstation | Air-gap bridging risk |
| Unexpected service exposure | SMB/RDP/web admin interface appears in OT zone | Legacy systems may be exposed accidentally |
| DNS or beaconing from OT | OT host contacting unusual internet domains | Malware or misconfigured remote management |

## AIS/GNSS use cases

| Use case | Signal | Operational relevance |
| --- | --- | --- |
| Implausible vessel jump | AIS position movement exceeds expected speed/distance | Possible data artifact or GNSS spoofing indicator |
| Multi-vessel coherent jump | Several vessels show consistent source/target clustering | Stronger candidate for regional GNSS spoofing |
| GNSS/AIS/radar disagreement | Navigation sources disagree materially | Requires bridge-team investigation |

See [SeaSpoofFinder](https://arxiv.org/abs/2602.16257) and [AIS-derived GNSS interference monitoring](https://arxiv.org/abs/2603.11055).
