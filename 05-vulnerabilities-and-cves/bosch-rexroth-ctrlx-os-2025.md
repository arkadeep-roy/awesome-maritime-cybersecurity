# Bosch Rexroth ctrlX OS vulnerabilities, 2025

## Summary

Bosch Rexroth published BOSCH-SA-640452 for multiple ctrlX OS vulnerabilities. Two examples relevant to OT risk discussions:

- CVE-2025-24346: A remote authenticated low-privileged attacker can manipulate `/etc/environment` via the Proxy functionality.
- CVE-2025-24349: A remote authenticated low-privileged attacker can delete the configuration of physical network interfaces via Network Interfaces functionality.

## Correct classification

These are industrial automation OS vulnerabilities. They are maritime-relevant where ctrlX OS or derived automation components are used in maritime or port environments. They are not maritime-exclusive CVEs.

## Sources

- [Bosch Rexroth security advisories](https://www.boschrexroth.com/en/de/company/product-security/security-advisories/)
- [BOSCH-SA-640452 advisory](https://psirt.bosch.com/security-advisories/bosch-sa-640452.html)
- [Nozomi Networks analysis](https://www.nozominetworks.com/blog/nozomi-networks-labs-discovers-15-new-vulnerabilities-affecting-bosch-rexroth-ctrlx-core)
