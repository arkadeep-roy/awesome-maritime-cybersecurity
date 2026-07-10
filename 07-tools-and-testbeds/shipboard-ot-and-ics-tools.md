# Shipboard OT and ICS Tools

## OpenPLC

Labels: `ot`, `defensive`, `offensive-research`, `lab`

Open-source PLC runtime and research platform.

- [Repository](https://github.com/thiagoralves/OpenPLC_v3)
- [Project](https://openplcproject.com)

Install:

```bash
git clone https://github.com/thiagoralves/OpenPLC_v3.git
cd OpenPLC_v3
./install.sh
```

Maritime use cases:

- Simulate ballast pump logic.
- Simulate engine-room alarms.
- Build Modbus TCP training labs.
- Test segmentation between IT, OT, and navigation zones.
- Generate traffic for Zeek/Suricata detection labs.

## GRFICSv2

Labels: `ot`, `defensive`, `offensive-research`, `lab`

General ICS/SCADA training lab.

- [Repository](https://github.com/Fortiphyd/GRFICSv2)

Maritime use cases:

- Teach ICS fundamentals before moving into maritime-specific OT.
- Build generic attacker/defender workflows.
- Practice segmentation and monitoring.
- Adapt process-control scenarios into shipboard analogies.

## ModbusPal

Labels: `ot`, `lab`, `defensive`

Modbus simulator.

- [Repository](https://github.com/epsilonrt/modbuspal)

Maritime use cases:

- Simulate Modbus devices.
- Build mock shipboard automation labs.
- Generate traffic for IDS rules.
- Teach insecure-by-design OT protocol behavior.

## OPC UA tools

Labels: `ot`, `lab`, `defensive`, `offensive-research`

Projects:

- [open62541](https://github.com/open62541/open62541)
- [UA-.NETStandard](https://github.com/OPCFoundation/UA-.NETStandard)

Maritime use cases:

- Understand OPC UA in marine automation and monitoring systems.
- Build lab servers and clients.
- Validate security modes and certificates.
- Study CVE impact in systems using OPC UA stacks.
