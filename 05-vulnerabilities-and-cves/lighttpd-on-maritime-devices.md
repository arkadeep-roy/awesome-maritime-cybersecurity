# Lighttpd CVEs observed on maritime-facing devices

## Correction

Some public writeups associate CVE-2022-22707 and CVE-2018-19052 with discovered SAILOR 900 VSAT web services. NVD classifies both as lighttpd vulnerabilities, not Sailor-specific product CVEs.

## CVEs

- CVE-2022-22707: lighttpd `mod_extforward` stack-based buffer overflow / DoS under a non-default configuration.
- CVE-2018-19052: lighttpd `mod_alias` path traversal issue under a specific alias configuration.

## Maritime relevance

If a maritime device exposes an embedded web server with vulnerable lighttpd, the maritime risk comes from the deployed context and exposure, not from the CVE being inherently maritime-specific.

## Sources

- [NVD CVE-2022-22707](https://nvd.nist.gov/vuln/detail/CVE-2022-22707)
- [NVD CVE-2018-19052](https://nvd.nist.gov/vuln/detail/CVE-2018-19052)
- [Criminal IP writeup mentioning SAILOR 900 observations](https://medium.com/@criminalip/revealing-vulnerabilities-more-than-1-600-maritime-transport-devices-found-susceptible-to-8f3600db589f)
