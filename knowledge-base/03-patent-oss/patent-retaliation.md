# Patent Retaliation Clauses in Open Source Licenses

> Last updated: 2026-03-15

## Summary

Patent retaliation clauses terminate a licensee's patent rights (and sometimes all rights) under an open source license if the licensee initiates patent infringement litigation against a contributor. These clauses serve as a defensive mechanism, creating a mutual-deterrence structure within open source communities.

## Key Principles

- Patent retaliation clauses are defensive — they only activate if the licensee sues first
- The scope varies: some terminate only patent rights, others terminate the entire license
- Retaliation clauses create a "patent peace" within open source ecosystems
- They are untested in court — their enforceability is theoretical but widely assumed

## License Provisions

### Apache License 2.0 (Section 3)
"If You institute patent litigation against any entity (including a cross-claim or counterclaim in a lawsuit) alleging that the Work or a Contribution incorporated within the Work constitutes direct or contributory patent infringement, then any patent licenses granted to You under this License for that Work shall terminate as of the date such litigation is filed."
- **Trigger:** Filing patent infringement lawsuit alleging the Work infringes
- **Effect:** Loss of patent licenses only (copyright license survives)
- **Scope:** Limited to claims about the Work itself

### GPLv3 (Section 10)
Broader anti-patent provisions. Section 10's "automatic licensing of downstream recipients" and Section 11's patent provisions collectively create strong patent deterrence.

### MPL 2.0 (Section 5.2)
"If You initiate litigation against any entity by asserting a patent infringement claim... alleging that a Contributor Version directly or indirectly infringes any patent, then the rights granted to You by any and all Contributors... under Sections 2.1 and 2.2 of this License shall terminate."
- **Trigger:** Patent infringement claim against Contributor Version
- **Effect:** Loss of both copyright and patent grants from all contributors

## Practical Guidance

1. **Patent retaliation clauses are real constraints.** If your company holds patents and uses open source software with retaliation clauses, litigation strategy must account for potential loss of open source rights.

2. **Scope matters.** Apache 2.0 only terminates patent rights for claims about the Work. MPL 2.0 terminates both copyright and patent rights. Know which you're dealing with.

3. **Portfolio considerations.** Companies with large patent portfolios should track which open source projects they use and understand the retaliation clause exposure.

## Sources

- Apache License 2.0, Section 3
- GNU GPLv3, Sections 10-11
- Mozilla Public License 2.0, Section 5.2
- Eclipse Public License 2.0, patent provisions
