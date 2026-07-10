# Defensive Monitoring Tools

## Zeek

Labels: `defensive`, `lab`

- [Website](https://zeek.org)

Maritime use cases:

- Network security monitoring.
- Extract metadata from shipboard lab traffic.
- Monitor unexpected cleartext telemetry.
- Build detections for unauthorized management access.
- Create logs for maritime SOC training.

Logs:

- `conn.log`
- `dns.log`
- `http.log`
- `ssl.log`
- `files.log`
- `weird.log`

## Suricata

Labels: `defensive`, `lab`

- [Website](https://suricata.io)

Maritime use cases:

- IDS/IPS lab monitoring.
- Detect scanning in shipboard segmentation labs.
- Alert on exposed SMB/RDP/Modbus/OPC UA behavior.
- Validate detection rules against simulated traffic.

## Sigma

Labels: `defensive`

- [Website](https://sigmahq.io)

Maritime use cases:

- Windows event detection.
- Ransomware behavior detection.
- Suspicious PowerShell on ship-management workstations.
- Lateral movement detection.
- Admin login anomaly rules.

## YARA

Labels: `defensive`

- [Website](https://virustotal.github.io/yara/)

Maritime use cases:

- Malware triage.
- USB malware detection.
- Incident-response scanning.
- File classification during maritime ransomware incidents.

## Velociraptor

Labels: `defensive`

- [Website](https://docs.velociraptor.app)

Maritime use cases:

- Endpoint triage.
- Remote artifact collection.
- Ransomware investigation.
- USB insertion timeline reconstruction.
- Fleet-wide hunting where bandwidth allows.

## Wazuh

Labels: `defensive`

- [Website](https://wazuh.com)

Maritime use cases:

- Lightweight SIEM/XDR for labs.
- Endpoint monitoring.
- File integrity monitoring.
- Compliance-oriented alerting.
- Centralized security logs for simulated ship networks.

## OpenSearch

Labels: `defensive`, `lab`

- [Website](https://opensearch.org)

Maritime use cases:

- Log storage.
- Security dashboards.
- AIS anomaly visualization.
- Zeek/Suricata log search.
- Training SOC analysts on maritime scenarios.
