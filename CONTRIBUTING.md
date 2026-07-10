# Contributing

This project prioritizes technical accuracy, source quality, and maritime relevance. Contributions are peer-reviewed before merge.
Read [STYLE_GUIDE.md](STYLE_GUIDE.md) before submitting large changes.

## Contribution types

  We welcome:
- CVE write-ups with technical analysis and reproduction steps
- Original research on AIS, GNSS, NMEA, ECDIS, VSAT exploitation and defense
- Shipboard network architecture diagrams and threat models
- Lab setup guides (OpenCPN, MaCySTe, OpenPLC, SDR-based environments)
- Incident analysis with root cause assessment and lessons learned
- Tool reviews, tutorials, and comparison matrices
- Translations that preserve technical accuracy and source context
- Regional maritime cybersecurity coverage


## Source requirements

Prefer sources in this order:

1. Official advisories, standards, regulations, CVE/NVD records, vendor statements, and official program pages
2. Academic papers and conference papers
3. ISAC, CERT, CSIRT, or government material
4. Credible industry reporting
5. Vendor threat-intelligence reports, clearly attributed
6. Media reports, clearly marked as reported, suspected, or alleged when appropriate

## Writing standards

- Use direct technical language.
- Prefer sentence-case headings.
- Keep tables short enough to read on GitHub.
- Use "reported", "suspected", "alleged", or "confirmed by" when source confidence differs.
- Do not relabel a general IT/OT CVE as maritime-specific unless the affected product is maritime-specific.
- Use "maritime-relevant" when a general component appears in maritime deployments.
- Attribute all statistics.
- Summarize copyrighted material; do not paste long excerpts.

## Pull request workflow

1. Fork the repository.
2. Create a branch named `add/<topic>` or `fix/<topic>`.
3. Add or edit the relevant file.
4. Verify links and source wording.
5. Open a pull request using the provided template.
6. Respond to review comments with source-backed changes.
