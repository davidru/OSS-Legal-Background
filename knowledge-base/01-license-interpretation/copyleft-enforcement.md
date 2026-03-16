# Copyleft License Enforcement

> Last updated: 2026-03-15

## Summary

Copyleft licenses — principally the GPL family (GPLv2, GPLv3, LGPL, AGPL) — require that derivative works or works incorporating copyleft-licensed code be distributed under the same license terms, including making source code available. Enforcement of these obligations has generated the most significant body of open source litigation worldwide.

The enforceability of copyleft licenses is now well-established in US law. Courts have recognized that open source licenses create enforceable conditions (not mere covenants), giving licensors both copyright infringement and contract claims when conditions are violated.

## Key Principles

- Copyleft license terms are enforceable conditions on the copyright license, not merely contractual covenants
- Violation of copyleft conditions can give rise to both copyright infringement and breach of contract claims
- The copyright holder (or their assignee) has standing to enforce; third-party beneficiary enforcement remains contested
- Compliance requires providing complete corresponding source code under the same license
- Good-faith cure provisions exist in GPLv3 (§8) but not GPLv2

## Case Law

### Jacobsen v. Katzer, 535 F.3d 1373 (Fed. Cir. 2008)
- **Citation:** 535 F.3d 1373 (Fed. Cir. 2008)
- **Holding:** Open source license terms (specifically the Artistic License) are enforceable conditions on the copyright license, not mere covenants. Violation constitutes copyright infringement, not merely breach of contract, entitling the licensor to injunctive relief.
- **Significance:** The foundational US appellate decision establishing that open source license conditions are real — they restrict the scope of the license grant, and exceeding them means you have no license at all. This is the case that made open source licensing enforceable in a meaningful way in the US.
- **Key Quote:** "The choice to exact consideration in the form of compliance with the open source requirements of disclosure and explanation of changes, rather than as a dollar-denominated fee, does not vitiate the enforceability of the conditions."
- **Subsequent History:** Remanded; settled. The Federal Circuit's holding on the condition/covenant distinction remains good law.

### Artifex Software v. Hancom, Inc., No. 16-cv-06982 (N.D. Cal. 2017)
- **Citation:** No. 16-cv-06982-JSC (N.D. Cal. Dec. 5, 2017)
- **Holding:** The GPL functions as both a copyright license and a contract. Denied Hancom's motion to dismiss both the copyright infringement and breach of contract claims arising from alleged GPL violations.
- **Significance:** Established that the GPL can be enforced under both copyright and contract theories — a dual pathway that gives enforcers strategic flexibility. The contract theory matters because it opens additional remedies (damages, specific performance) beyond what copyright alone provides.
- **Key Quote:** "The GNU GPL... provides that the licensee's rights are 'conditioned on' compliance with the GPL's terms, and that if the licensee fails to comply, the license is automatically terminated."

### Versata Software v. Ameriprise Financial, No. 2:14-cv-12 (W.D. Tex. 2014)
- **Citation:** No. 2:14-cv-12-JRG (W.D. Tex. 2014)
- **Holding:** Found that Versata's commercial software incorporated GPLv2-licensed code (from XimpleWare), and this incorporation subjected Versata's software to GPLv2 obligations.
- **Significance:** Demonstrated the viral/copyleft reach of GPLv2 in a commercial context. Also raised the question of whether a third party (Ameriprise, as Versata's customer) could invoke the GPL defensively.

### XimpleWare v. Versata Software, No. 13-cv-05160 (N.D. Cal. 2014)
- **Citation:** No. 13-cv-05160-SI (N.D. Cal. 2014)
- **Holding:** Addressed whether XimpleWare (the original GPL copyright holder) could bring infringement claims against Versata for violating GPLv2 terms.
- **Significance:** Tested the boundaries of who can enforce GPL obligations and the relationship between copyright holder enforcement and downstream user rights.

### Free Software Foundation v. Cisco Systems (2008-2009)
- **Citation:** No. 08-10764 (S.D.N.Y. 2008); settled 2009
- **Holding:** Settlement — Cisco agreed to appoint a Free Software Director, notify customers of GPL rights, and publish source code.
- **Significance:** First FSF-initiated enforcement action against a major corporation. The settlement terms became a model for corporate compliance programs. Demonstrated that even large companies would settle rather than litigate GPL enforceability.

### BusyBox / Software Freedom Law Center Enforcement Actions (2007-2011)
- **Citation:** Multiple cases including SFLC v. Monsoon Multimedia (S.D.N.Y. 2007), SFLC v. Verizon (S.D.N.Y. 2007), SFLC v. Xterasys (S.D.N.Y. 2008), and others
- **Holding:** All settled with defendants agreeing to GPL compliance and, in some cases, monetary payments.
- **Significance:** The SFLC's systematic enforcement campaign using BusyBox (a widely-embedded GPLv2 utility) established a practical enforcement model and demonstrated that GPL violations in embedded systems and consumer electronics would be pursued. These cases showed the GPL had real teeth.

### Neo4j / iGov / Pure Thrills (Sweden, later US proceedings)
- **Citation:** Various proceedings 2018-2022
- **Holding:** Complex dispute involving AGPL relicensing, commercial license agreements, and attempted license changes.
- **Significance:** Illustrated the tensions around relicensing and the practical limits of copyleft enforcement when a company controls the copyright and changes licensing terms.

## Commentary & Analysis

### Heather Meeker, "Open Source for Business" (3rd ed., 2020)
- **Source:** Self-published / available commercially
- **Key Arguments:** Comprehensive treatment of copyleft enforcement from a practitioner perspective. Argues that copyleft compliance is manageable with proper processes, and that the "viral" characterization of the GPL overstates the practical risk for most use cases. Provides detailed guidance on compliance architecture.

### Eben Moglen, "Enforcing the GNU GPL" (2001, updated)
- **Source:** Free Software Foundation / SFLC
- **Key Arguments:** Articulates the FSF's enforcement philosophy — "compliance, not punishment." Explains why the FSF prefers private enforcement and settlement over litigation, and why the goal is always to bring violators into compliance rather than to extract damages.

### Bradley Kuhn & Karen Sandler, "GPL Enforcement and the Software Freedom Conservancy"
- **Source:** Software Freedom Conservancy publications
- **Key Arguments:** Advocates for principled copyleft enforcement, arguing that non-enforcement undermines the entire copyleft ecosystem. Distinguishes between "enforcement for compliance" (SFC's model) and "enforcement for profit" (Patrick McHardy model, which they criticize).

### Pamela Jones, Groklaw (archived)
- **Source:** groklaw.net (archived at various mirrors)
- **Key Arguments:** Extensive contemporaneous analysis of SCO v. IBM, GPL enforceability, and the legal foundations of open source. While not a law review, Groklaw's detailed legal analysis of open source cases was influential in shaping public understanding.

## Practical Guidance

1. **Know your obligations.** If you distribute software containing copyleft code, you must provide complete corresponding source code under the same license. This is not optional.

2. **Build compliance into your process.** Track OSS components, their licenses, and your obligations. Automated scanning tools (ScanCode, FOSSology, SPDX tools) help but are not sufficient — human review is still needed for copyleft compliance.

3. **Distinguish "conditions" from "covenants."** Under Jacobsen, violating a condition means you lose your license entirely (copyright infringement). This is more serious than a breach of contract.

4. **Cure provisions matter.** GPLv3 Section 8 provides an automatic cure for first-time violators who come into compliance within 30 days of notice. GPLv2 has no such provision — once violated, the license terminates, and only the copyright holder can reinstate it.

5. **AGPL adds network obligations.** AGPL Section 13 extends copyleft to network server use — if you modify AGPL code and users interact with it over a network, you must provide source. This is the key distinction for SaaS/cloud deployments.

6. **Enforcement standing is limited.** Only the copyright holder (or their assignee) can enforce. Third-party enforcement remains legally uncertain. This is why CLAs and copyright assignment to foundations matter for enforcement strategy.

## Open Questions

- **Scope of "derivative work" under GPLv2.** The most contested question in open source law. Does dynamic linking create a derivative work? What about kernel modules? The FSF says yes (for most cases); many disagree. No court has squarely decided this.
- **Container and microservice architectures.** How do copyleft obligations apply when GPL code runs in a container that communicates via APIs with proprietary code? The traditional linking analysis may not map cleanly.
- **AI training on copyleft code.** If an AI model is trained on GPL-licensed code, does the model output constitute a derivative work? Entirely unresolved.
- **GPLv2 "or later" relicensing.** The interaction between "GPLv2 or later" grants and GPLv3's additional patent and anti-tivoization provisions remains practically complex.

## Sources

- Jacobsen v. Katzer, 535 F.3d 1373 (Fed. Cir. 2008)
- Artifex Software v. Hancom, No. 16-cv-06982 (N.D. Cal. 2017)
- Versata Software v. Ameriprise Financial, No. 2:14-cv-12 (W.D. Tex. 2014)
- XimpleWare v. Versata Software, No. 13-cv-05160 (N.D. Cal. 2014)
- Free Software Foundation v. Cisco Systems, No. 08-10764 (S.D.N.Y. 2008)
- Heather Meeker, *Open Source for Business* (3rd ed., 2020)
- Eben Moglen, "Enforcing the GNU GPL" (FSF/SFLC, 2001)
- Bradley Kuhn & Karen Sandler, SFC Enforcement Publications
- IFOSS Law Review, various issues
