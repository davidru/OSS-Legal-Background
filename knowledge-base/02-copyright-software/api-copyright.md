# API Copyright

> Last updated: 2026-03-15

## Summary

Whether application programming interfaces (APIs) are protectable by copyright is one of the most consequential and contested questions in software law. The Supreme Court's decision in Oracle v. Google (2021) addressed this question but deliberately declined to resolve it, instead holding that even assuming APIs are copyrightable, Google's use was fair use.

The API copyright question is particularly important for open source because many projects reimplment existing APIs for compatibility (e.g., Mono reimplementing .NET APIs, Wine reimplementing Windows APIs, various Java SE reimplementations).

## Key Principles

- API "declaring code" (method signatures, class hierarchies, interface definitions) has a functional character
- The Supreme Court assumed without deciding that API declarations are copyrightable
- Even if copyrightable, reimplementation of APIs for compatibility purposes has strong fair use support
- The distinction between "declaring code" (interface) and "implementing code" (functionality) is critical

## Case Law

### The Oracle v. Google Saga (Full History)

#### Oracle v. Google, N.D. Cal. (2012) — District Court
- **Judge:** William Alsup
- **Holding:** Java API declarations (structure, sequence, and organization of 37 API packages) are not copyrightable because they constitute a "method of operation" under 17 U.S.C. § 102(b).
- **Notable:** Judge Alsup learned to write Java code during the trial.

#### Oracle v. Google, 750 F.3d 1339 (Fed. Cir. 2014) — First Appeal
- **Holding:** Reversed. The Federal Circuit held that the Java API declarations are copyrightable. The structure, sequence, and organization of the APIs reflected creative choices that went beyond mere functional requirements.
- **Significance:** Split from the Ninth Circuit's more functional approach to software copyright.

#### Oracle v. Google, Fed. Cir. (2018) — Second Appeal
- **Holding:** Reversed the jury's fair use finding. Held that Google's use was not fair use as a matter of law.
- **Significance:** Raised alarm in the software industry about the scope of API copyright protection.

#### Oracle America v. Google LLC, 593 U.S. 1 (2021) — Supreme Court
- **Holding:** Assuming copyrightability, Google's use was fair use. Reversed the Federal Circuit.
- **Significance:** The definitive statement on API fair use, though the copyrightability question remains technically open.

*[To be enriched with research from background agent]*

## Practical Guidance

1. **Reimplementing APIs is defensible.** After the Supreme Court's Oracle v. Google decision, reimplementing APIs for compatibility and interoperability purposes has strong legal support under fair use.

2. **The copyrightability question is not resolved.** The Supreme Court did not say APIs are uncopyrightable. Future cases may still need to address this threshold question.

3. **Purpose matters.** The fair use analysis was highly dependent on Google's purpose (creating a new platform). A different purpose might yield a different result.

4. **Implement, don't copy.** The strongest position is to reimplement API functionality from specifications/documentation without copying literal code. Clean-room processes remain the gold standard.

## Sources

- Oracle America v. Google LLC, 593 U.S. 1 (2021)
- Oracle v. Google, 750 F.3d 1339 (Fed. Cir. 2014)
- Oracle v. Google, No. C 10-03561 (N.D. Cal. 2012)
