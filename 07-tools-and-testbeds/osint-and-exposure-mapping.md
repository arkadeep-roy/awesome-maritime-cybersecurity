# OSINT and Exposure Mapping

Asset-inventory and exposure-mapping tools listed here apply to owned infrastructure, approved consulting work, VDP scope, or lab environments. These workflows are not target lists for third-party maritime infrastructure.

## Shodan

Labels: `osint`, `defensive`

- [Website](https://www.shodan.io)

Maritime use cases:

- External attack-surface inventory for authorized organizations.
- Identifying exposed management interfaces in owned infrastructure.
- Validating vendor exposure during approved assessments.
- Monitoring accidental internet exposure.

Example scoped query patterns:

```text
ssl.cert.subject.cn:"example.org"
ssl.cert.subject.alt_names:"example.org"
hostname:"example.org"
org:"Example Organization"
http.title:"fleet management"
http.title:"vessel"
http.title:"terminal"
http.title:"crew portal"
http.title:"shipmanager"
product:"OpenPLC"
port:10110
```

Replace examples with assets you own or are explicitly authorized to assess.

## Censys

Labels: `osint`, `defensive`

- [Website](https://search.censys.io)

Maritime use cases:

- Certificate transparency review.
- Internet-exposed host inventory.
- TLS and service metadata analysis.
- Owned-domain exposure validation.

Example scoped query patterns:

```text
services.tls.certificates.leaf_data.names: example.org
dns.names: example.org
services.http.response.html_title: "fleet"
services.http.response.html_title: "vessel"
services.port: 10110
```

## SecurityTrails

Labels: `osint`, `defensive`

- [Website](https://securitytrails.com)

Maritime use cases:

- Subdomain inventory.
- Historical DNS review.
- Vendor portal discovery in authorized scope.
- Acquisition and subsidiary mapping.

## crt.sh

Labels: `osint`, `defensive`

- [Website](https://crt.sh)

Maritime use cases:

- Certificate transparency recon.
- Finding forgotten subdomains.
- Mapping cloud-hosted maritime portals.
- Detecting internal hostnames accidentally exposed in certificates.

Example scoped query:

```text
%.example.org
```

## Wayback Machine

Labels: `osint`, `defensive`

- [Website](https://web.archive.org)

Maritime use cases:

- Archived endpoint discovery.
- Old API documentation.
- Deprecated portal paths.
- Historical JavaScript files.
- Forgotten upload or download endpoints.

## GitHub search

Labels: `osint`, `defensive`

- [Website](https://github.com/search)

Maritime use cases:

- Leaked API keys in owned repositories.
- Hardcoded URLs to vessel/fleet APIs.
- Exposed Swagger/OpenAPI files.
- Developer documentation leaks.
- Old infrastructure references.

Example scoped searches:

```text
"example.org"
"api.example.org"
"vessel_id" "example.org"
"fleet_id" "example.org"
"shipmanager" "example.org"
```
