# Contributing to Virtual OSS Attorney

Thank you for your interest in contributing to this knowledge base. This project aims to be the most authoritative, well-sourced collection of open source law resources available. Maintaining quality is paramount.

## What We Accept

### Case Law
- **Court opinions only** — actual judicial decisions from recognized courts
- Full citation required (case name, court, year, reporter citation where available)
- Must include: holding, significance for OSS law, and key quotes from the opinion
- Note any subsequent history (appeals, reversals, settlements)

### Law Review Articles & Academic Commentary
- Published in recognized law journals or peer-reviewed legal publications
- Author must be identifiable and credentialed
- Preferred journals include (but are not limited to):
  - International Free and Open Source Software Law Review (IFOSS L. Rev.) / JOLTS
  - Harvard Journal of Law & Technology
  - Stanford Technology Law Review
  - Berkeley Technology Law Journal
  - Columbia Science & Technology Law Review
  - Yale Journal of Law & Technology

### Practitioner Analysis
- From recognized experts in open source law — practitioners who have:
  - Represented parties in OSS litigation
  - Drafted or contributed to major OSS licenses
  - Served in legal roles at major OSS foundations or companies
  - Published books or significant articles on OSS law
- Must be attributable to a specific author

### Institutional Publications
- From recognized organizations: FSF, OSI, SFC, FSFE, Linux Foundation, Apache Foundation, EFF, Creative Commons
- Official legal analyses, position papers, or compliance guides
- Not press releases or marketing materials

## What We Do NOT Accept

- Blog posts from unrecognized sources
- Unattributed analysis
- Marketing materials or vendor white papers
- Content aggregator summaries
- Social media posts or forum discussions
- AI-generated content without expert review and attribution
- Content that reproduces substantial portions of copyrighted works

## How to Contribute

### Adding a New Case
1. Identify the correct category in `knowledge-base/`
2. Add the case in the appropriate file using this format:

```markdown
### Case Name (Court, Year)
- **Citation:** [Full citation]
- **Holding:** [What the court decided]
- **Significance:** [Why it matters for OSS law]
- **Key Quote:** [Notable language from the opinion]
- **Subsequent History:** [If any — appeals, reversals, etc.]
```

3. Add the case to the appropriate file in `case-law-index/`
4. Submit a pull request with a clear description

### Adding Commentary or Analysis
1. Identify the correct category in `knowledge-base/`
2. Add in the Commentary & Analysis section using this format:

```markdown
### Author Name, "Title" (Year)
- **Source:** [Publication/journal with link if available]
- **Key Arguments:** [Summary of the analysis]
- **Relevance:** [How it connects to the topic]
```

3. Add to `sources/bibliography.md`
4. Submit a pull request

### Correcting Errors
- If you find an incorrect citation, superseded holding, or factual error, please open an issue or submit a PR
- Include the source for the correction

### Expanding Jurisdiction Coverage
- We especially welcome contributions covering:
  - Non-US court decisions on OSS matters
  - EU member state enforcement actions
  - Chinese, Japanese, Indian, and other Asian court decisions
  - Latin American OSS law developments

## Quality Review Process

All contributions will be reviewed for:
1. **Source quality** — Does the source meet our standards?
2. **Accuracy** — Are citations correct? Are holdings accurately stated?
3. **Completeness** — Is sufficient context provided?
4. **Objectivity** — Does the entry fairly represent the source material?
5. **Currency** — Is this the most current state of the law?

## Style Guide

- Use plain English; avoid unnecessary legalese
- Distinguish holdings from dicta
- Note circuit splits or jurisdictional disagreements
- Flag areas where the law is actively evolving
- Always attribute analysis to its source
- Use American legal citation format (Bluebook) for US cases
- Use neutral citation format for international cases where available

## Code of Conduct

Be respectful, constructive, and focused on improving the resource. Legal analysis often involves reasonable disagreements — present positions fairly and note the opposing view.
