# Virtual OSS Attorney

A world-class, open-source knowledge base of open source software law — curated case law, legal commentary, law reviews, and practitioner analysis organized by topic and distilled into a Virtual OSS Attorney powered by AI.

## What This Is

This project provides two things:

1. **A comprehensive knowledge base** of open source law, covering licensing, copyright, patents, compliance, governance, business models, and more — drawn exclusively from high-quality primary and secondary sources.

2. **A Virtual OSS Attorney** — a system prompt and knowledge routing architecture that enables AI assistants (GitHub Copilot, ChatGPT, Claude, etc.) to provide informed, well-sourced guidance on open source legal questions.

## ⚠️ Important Disclaimer

**This is not legal advice.** This knowledge base and Virtual OSS Attorney are educational resources. No attorney-client relationship is created by using this tool. The information provided may not reflect the current state of the law in all jurisdictions. **Always consult qualified legal counsel for specific legal matters.**

## Knowledge Base Structure

The knowledge base is organized into 12 topical categories:

| Category | Topics |
|----------|--------|
| [01 — License Interpretation](knowledge-base/01-license-interpretation/) | Copyleft enforcement, permissive licenses, weak copyleft, non-standard licenses, compatibility |
| [02 — Copyright in Software](knowledge-base/02-copyright-software/) | Copyrightability, derivative works, fair use, API copyright |
| [03 — Patents & OSS](knowledge-base/03-patent-oss/) | Patent grants, retaliation clauses, patent pledges, SEPs |
| [04 — Contributor Agreements](knowledge-base/04-contributor-agreements/) | CLAs vs DCO, copyright assignment, IP ownership |
| [05 — Compliance & Distribution](knowledge-base/05-compliance-distribution/) | Source obligations, notices, binary distribution, SaaS, SBOMs |
| [06 — Governance & Organizations](knowledge-base/06-governance-organizations/) | Foundation models, project governance, nonprofit law |
| [07 — Business Models](knowledge-base/07-business-models/) | Dual licensing, open core, relicensing, sustainability |
| [08 — Trademark](knowledge-base/08-trademark/) | Project trademarks, community use policies |
| [09 — International](knowledge-base/09-international/) | EU enforcement, China OSS law, cross-border, EU regulatory |
| [10 — Antitrust & Competition](knowledge-base/10-antitrust-competition/) | OSS and competition law, standards interaction |
| [11 — Government & Regulatory](knowledge-base/11-government-regulatory/) | Government use, export controls, sovereign OSS strategies |
| [12 — AI & Open Source](knowledge-base/12-ai-and-oss/) | AI model licensing, training data, AI-generated code |

Plus:
- [Case Law Index](case-law-index/) — Cross-referenced case summaries by jurisdiction
- [Sources](sources/) — Bibliography, key authors, and institutions
- [Appendices](appendices/) — Glossary, license text references, historical timeline

## How to Use

### As a Knowledge Base
Browse the `knowledge-base/` directory by topic. Each file contains:
- Executive summary of the legal landscape
- Key case law with holdings and significance
- Synthesized commentary from leading practitioners
- Practical guidance
- Open questions where the law is unsettled

### As a Virtual OSS Attorney
Load the system prompt from `system-prompt/Virtual-OSS-Attorney-System-Prompt.md` into your AI assistant of choice. The prompt includes knowledge routing that automatically loads relevant knowledge files based on the user's question.

### With GitHub Copilot CLI
```
# Point the CLI at the system prompt
copilot --system-prompt system-prompt/Virtual-OSS-Attorney-System-Prompt.md
```

## Source Quality Standards

This project only includes sources that meet these standards:

- **Case law:** Actual court opinions (federal, state, international) — not blog summaries
- **Law reviews:** Published in recognized journals (Harvard, Stanford, Berkeley, Columbia, etc.)
- **Commentary:** From recognized practitioners in the OSS legal field
- **Institutional:** Publications from FSF, OSI, SFC, FSFE, Linux Foundation, Apache Foundation, EFF
- **Academic:** IFOSS Law Review / JOLTS, Berkman Klein Center, Stanford CIS

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed quality criteria.

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on:
- Adding new case law or commentary
- Correcting errors or updating holdings
- Expanding coverage to new jurisdictions
- Improving practical guidance sections

## License

- **Content** (knowledge base, documentation): [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/)
- **Code** (scripts, tooling): [MIT License](https://opensource.org/licenses/MIT)

## Acknowledgments

This project was created by by AI without formal human review.  Use accordingly.
