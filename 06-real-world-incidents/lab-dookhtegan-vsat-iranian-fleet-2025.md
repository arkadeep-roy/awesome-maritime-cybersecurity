# Lab Dookhtegan VSAT Attacks on Iranian Shipping Fleets, 2025

## Summary

In March 2025 and again in August 2025, a self-described hacktivist group calling itself Lab Dookhtegan claimed disruptive attacks against Iranian maritime communications. Public reporting describes the March wave as affecting 116 vessels and the August wave as affecting more than 60 vessels, including 39 NITC tankers and 25 IRISL cargo ships. Some later summaries round this to roughly 180 vessels across both waves.

Treat these figures as reported, not confirmed. The reviewed public sources do not include an official confirmation from Fanava, NITC, IRISL, or the Iranian government.

## What is reported

- Lab Dookhtegan claimed disruption of external and internal communications for Iranian vessels associated with NITC and IRISL.
- Cydome assessed the second wave as a provider-level compromise of Fanava infrastructure rather than isolated exploitation of individual vessels.
- Reporting describes destructive actions against iDirect Falcon VSAT terminal software, including partition wiping and disabling Falcon processes.
- The reported operational effect was loss of ship-to-shore communications and disruption of maritime satellite connectivity.
- The targeted entities are associated with sanctioned Iranian maritime activity, so several outlets frame the event as hacktivism or geopolitical sabotage rather than financially motivated cybercrime.

## What is not confirmed

- The precise initial-access technique into Fanava's environment has not been independently verified from a public technical incident-response report.
- Vessel counts come from attacker claims and third-party reporting.
- NORMA Cyber stated that it had not found corroborating open-source confirmation that the alleged March attack on 116 Iranian vessels took place, while also assessing some published vessel-name evidence as likely genuine.

## Operational relevance

This case is valuable because it illustrates a maritime-specific supply-chain risk: compromising a satellite or communications provider can create fleet-wide effects without attacking each vessel one by one.

It connects directly to:

- VSAT and SATCOM risk
- provider-side single points of failure
- vessel communications resilience
- destructive attacks against embedded communications infrastructure
- geopolitical maritime cyber operations
- recovery difficulty when physical hardware access is required

## Lessons

- A satellite or communications provider can become a single point of failure for an entire fleet.
- Recovery from destructive attacks against embedded VSAT terminals can be slower than typical IT recovery because vessels may require physical hardware replacement or onboard intervention.
- Loss of ship-to-shore communications has safety and operational implications beyond confidentiality.
- Treat hacktivist self-reporting cautiously. Use ranges and confidence labels until official or independent technical confirmation is available.

## Sources

- [cydome.io](https://cydome.io/lab-dookhtegan-cyber-attack-on-iranian-oil-tankers-disrupts-operations/)
- [cydome.io](https://cydome.io/lab-dookhtegan-cyberattack-second-wave-findings-aug-2025/)
- [industrialcyber.co](https://industrialcyber.co/transport/cydome-analyzes-lab-dookhtegan-cyber-attack-on-iranian-oil-tankers-provides-mitigation-action/)
- [iranintl.com](https://www.iranintl.com/en/202503182119)
- [iranintl.com](https://www.iranintl.com/en/202508226637)
- [maritime-executive.com](https://maritime-executive.com/article/hackers-disable-iranian-merchant-shipping-communications)
- [thedigitalship.com](https://thedigitalship.com/news/maritime-satellite-communications/norma-cyber-perspective-on-cyber-attack-of-116-iranian-vessel-vsats/)
- [maritimecybersecurity.nl](https://maritimecybersecurity.nl/incident/PDJoR3w6W4)
- [maritimecybersecurity.nl](https://maritimecybersecurity.nl/incident/e54zZOxo3l)
