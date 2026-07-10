# Style Guide

Use a technical reference style: source-backed, concise, and careful about confidence. Avoid marketing language, sales framing, and unreviewed link collections.

## Tone

Use precise language.

Prefer:

- `reported by`
- `confirmed by`
- `suspected`
- `maritime-relevant where deployed`
- `lab-only`
- `authorized testing`
- `source not independently verified`
- `status requires periodic verification`

Avoid unsupported claims:

- `guaranteed`
- `first ever`
- `unhackable`
- `military grade`
- `catastrophic` without evidence
- `weaponized` unless the source supports it

## Source hierarchy

Use the strongest available source. If a stronger source is unavailable, state the limitation.

1. Official advisories, standards, regulations, CVE/NVD records, vendor statements, and official program pages
2. Academic papers and conference papers
3. ISAC, CERT, CSIRT, and government material
4. Credible industry reporting
5. Vendor threat-intelligence reports, explicitly attributed
6. Media reports, marked as reported or suspected where necessary

## Incident confidence labels

| Label | Use when |
| --- | --- |
| `confirmed` | Primary or official source confirms the incident or vulnerability |
| `reported` | Credible reports exist, but no full official technical confirmation is available |
| `suspected` | The event is plausible but causality or attribution is not proven |
| `contested` | Sources disagree or an important source cautions against accepting the claim |
| `illustrative` | The file is not a cyber incident; it is included to explain operational impact |

## CVE classification

Do not convert a general IT/OT CVE into a maritime-specific CVE unless the affected product is specifically maritime. Use `maritime-relevant` when the component appears in maritime deployments but is not exclusive to maritime.

Examples:

- Correct: `CVE-2016-5817: Cargotec Navis WebAccess SQL injection; port and terminal software relevance.`
- Incorrect: `CVE-2016-5817: ECDIS vulnerability.`
- Correct: `CVE-2022-22707: lighttpd issue observed in maritime-facing device context.`
- Incorrect: `CVE-2022-22707: Sailor 900 product CVE.`

## File structure

For most entries, use this order:

1. Summary
2. Classification or scope
3. Maritime relevance
4. Operational relevance
5. Limitations or confidence notes
6. Sources

For incident files, use:

1. Summary
2. What is confirmed
3. What is reported or suspected
4. Affected systems
5. Impact
6. Lessons for researchers and defenders
7. Sources

## Markdown presentation

- Use sentence-case headings.
- Avoid emojis in headings and filenames.
- Avoid decorative dividers.
- Avoid long raw URL walls when a short source list works better.
- Keep README files navigational; keep technical detail in child files.
- Prefer short paragraphs and compact tables.
- Do not add screenshots unless they are necessary, licensed, and source-attributed.
- Do not publish target lists of real maritime infrastructure.
