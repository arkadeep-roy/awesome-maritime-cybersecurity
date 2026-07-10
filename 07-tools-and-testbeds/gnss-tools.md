# GNSS and GPS Tools

GNSS security matters because GPS/GNSS feeds ECDIS, AIS position data, timing, bridge systems, dynamic positioning, and fleet telemetry.

## GNSS-SDR

Labels: `rf`, `defensive`, `research`, `lab`

Open-source software-defined GNSS receiver.

- [Website](https://gnss-sdr.org)
- [Repository](https://github.com/gnss-sdr/gnss-sdr)

Install:

```bash
sudo apt-get update
sudo apt-get install gnss-sdr
```

Build:

```bash
git clone https://github.com/gnss-sdr/gnss-sdr.git
cd gnss-sdr
mkdir build
cd build
cmake ..
make
sudo make install
```

Maritime use cases:

- GNSS receiver research.
- Spoofing and jamming detection research.
- Multi-constellation signal analysis.
- Defensive navigation-resilience testing.

## GPS-SDR-SIM

Labels: `rf`, `offensive-research`, `lab`

GPS signal simulation tool used in GNSS security research.

- [Repository](https://github.com/osqzss/gps-sdr-sim)

Build:

```bash
git clone https://github.com/osqzss/gps-sdr-sim.git
cd gps-sdr-sim
make
```

Maritime use cases:

- Controlled GPS receiver testing.
- ECDIS/GNSS receiver behavior research.
- Defensive spoofing-detection validation.
- Cyber-range exercises.
- Understanding GPS signal-generation attack classes.

## bladeGPS

Labels: `rf`, `offensive-research`, `lab`

Real-time GPS signal-generation research tool for bladeRF.

- [Repository](https://github.com/osqzss/bladeGPS)

Maritime use cases:

- Real-time GNSS simulation in controlled lab environments.
- Dynamic receiver behavior testing.
- Defensive validation for navigation resilience.

## GPSJam

Labels: `data`, `defensive`, `osint`

Public GNSS interference visualization project.

- [Website](https://gpsjam.org)

Maritime use cases:

- Track broad GNSS interference areas.
- Compare vessel anomaly reports with regional GNSS interference.
- Support incident writeups and threat-landscape monitoring.
