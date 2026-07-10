# KEPServerEX vulnerabilities affecting ABB Marine ITMonitoring

## Summary

ABB published an advisory explaining that vulnerabilities in PTC KEPServerEX affect ABB Marine ITMonitoring versions 1.0.2 and 1.0.3. The advisory states that specially crafted OPC UA messages could crash the server and leak data transmitted to it.

## CVEs

- CVE-2022-2825: KEPServerEX stack-based buffer overflow; NVD and Claroty describe remote code execution risk in affected KEPServerEX installations.
- CVE-2022-2848: Related KEPServerEX vulnerability referenced in ABB and vendor advisories.

## Sources

- [ABB advisory PDF](https://search.abb.com/library/Download.aspx?Action=Launch&DocumentID=8MAL100030-0015&DocumentPartId=&LanguageCode=en)
- [NVD CVE-2022-2825](https://nvd.nist.gov/vuln/detail/CVE-2022-2825)
- [Claroty CVE-2022-2825 dashboard](https://claroty.com/team82/disclosure-dashboard/cve-2022-2825)

## Defensive notes

- Identify whether KEPServerEX is present in marine monitoring systems.
- Confirm version and vendor patch guidance.
- Segment OPC UA services from untrusted networks.
- Monitor unexpected OPC UA traffic and crashes.
