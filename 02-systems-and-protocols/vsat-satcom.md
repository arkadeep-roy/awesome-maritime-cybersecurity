# VSAT and SATCOM

VSAT and satellite communications provide ship connectivity for operations, crew services, remote monitoring, and vendor access.

## Security relevance

Common risk themes:

- Exposed management interfaces
- Weak remote access controls
- Outdated embedded web services
- Flat networks behind satellite gateways
- Vendor access without strong identity controls
- Difficulty patching equipment while vessels are at sea

## CVE caution

Some public materials associate CVE-2022-22707 and CVE-2018-19052 with discovered Sailor 900 VSAT web services. NVD identifies these CVEs as lighttpd vulnerabilities, not Sailor-specific vulnerabilities. In this repo they are treated as "third-party component exposure observed on maritime devices," not as Sailor 900 product CVEs. Sources: [NVD CVE-2022-22707](https://nvd.nist.gov/vuln/detail/CVE-2022-22707), [NVD CVE-2018-19052](https://nvd.nist.gov/vuln/detail/CVE-2018-19052), [Criminal IP writeup](https://medium.com/@criminalip/revealing-vulnerabilities-more-than-1-600-maritime-transport-devices-found-susceptible-to-8f3600db589f).

## Safe research paths

- Review vendor hardening guides.
- Study network segmentation and remote-access architecture.
- Analyze public advisories and exposed-service trends without touching live systems.
- Test only in owned labs or explicit VDP scope.
