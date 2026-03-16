# Standard-Essential Patents and Open Source

> Last updated: 2026-03-15

## Summary

Standard-essential patents (SEPs) — patents that are necessarily infringed by implementing a technical standard — create a fundamental tension with open source software. SEP holders typically commit to license on FRAND (fair, reasonable, and non-discriminatory) terms, which traditionally contemplates royalty-bearing licenses. Open source licenses, however, require royalty-free distribution. This creates a structural conflict: how can open source projects implement standards encumbered by FRAND-committed SEPs?

## Key Principles

- FRAND commitments require licensing on fair, reasonable, and non-discriminatory terms — but don't necessarily mean royalty-free
- Open source licenses (especially copyleft) cannot include per-unit royalty obligations
- The tension is structural: FRAND permits royalties; OSS distribution models cannot pass through per-unit royalties
- Some SDOs offer royalty-free (RF) patent policies (W3C, OASIS in some modes), which are inherently compatible with OSS
- FRAND-encumbered standards can be implemented in OSS, but the patent licensing question shifts to the user/distributor level

## The FRAND-OSS Tension

### The Problem
1. Implementer creates open source implementation of a FRAND-encumbered standard
2. The OSS license permits royalty-free redistribution by anyone
3. SEP holder expects royalties from implementers
4. Who pays? The original developer? Each distributor? Each end user?
5. Copyleft licenses (GPLv3 §11) may prohibit distribution if patent royalties attach

### Proposed Solutions
- **Royalty-free patent policies** at the SDO level (eliminates the problem)
- **Patent pledges** by SEP holders for OSS implementations
- **Licensing at the end-product level** (royalties paid by device manufacturers, not OSS distributors)
- **Patent pools** with OSS-friendly terms
- **FRAND-zero** commitments (FRAND with royalty rate of zero)

## Case Law

### Huawei v. ZTE, Case C-170/13 (CJEU 2015)
- **Citation:** Case C-170/13, ECLI:EU:C:2015:477
- **Holding:** Established the framework for when SEP holders can seek injunctive relief. FRAND-committed SEP holders must follow specific procedural steps before seeking injunctions against willing licensees.
- **Relevance to OSS:** While not an OSS case, the Huawei v. ZTE framework affects how SEPs are enforced generally, which impacts OSS implementations of standards.

*[Additional case law to be populated from research]*

## Commentary & Analysis

### The Royalty Stacking Problem
When a standard involves hundreds of SEPs held by dozens of entities, cumulative royalties can become prohibitive — especially for open source implementations distributed at no charge. This "royalty stacking" problem is one of the primary economic arguments for royalty-free patent policies in standards.

## Practical Guidance

1. **Prefer RF standards for OSS implementations.** When possible, implement standards developed under royalty-free patent policies (W3C, IETF, some OASIS projects).

2. **Understand the patent landscape before implementing.** If implementing a FRAND-encumbered standard in OSS, understand which patents are essential and what licensing terms are available.

3. **GPLv3 has specific provisions.** GPLv3 Section 11's patent provisions may create complications for distributing GPLv3 implementations of FRAND-encumbered standards. Analyze carefully.

4. **Permissive licenses have more flexibility.** Apache 2.0 or MIT-licensed implementations of FRAND standards face fewer structural conflicts, since the patent licensing burden can be passed to commercial distributors.

## Open Questions

- **Can FRAND obligations be satisfied by licensing at the implementation level rather than distribution level?** This is the core structural question.
- **Are FRAND commitments compatible with copyleft distribution?** GPLv3 arguably prohibits distribution if doing so requires downstream recipients to pay patent royalties.
- **How do SEP pledges interact with OSS license patent grants?** If a contributor to an Apache 2.0 project holds SEPs on the standard being implemented, does the Apache patent grant cover those SEPs?

## Sources

- Huawei v. ZTE, Case C-170/13 (CJEU 2015)
- W3C Patent Policy (royalty-free)
- OASIS IPR Modes (including RF mode)
- IEEE-SA Patent Policy
