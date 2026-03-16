# Patent Grants in Open Source Licenses

> Last updated: 2026-03-15

## Summary

Open source licenses take varying approaches to patent rights. Some include express patent grants (Apache 2.0, GPLv3, MPL 2.0), while others are silent on patents (MIT, BSD). The presence or absence of patent provisions is one of the key differentiators among open source licenses and has significant practical implications for both licensors and licensees.

A patent grant in an open source license permits licensees to practice the licensor's patents that are necessarily infringed by the licensed software, without paying royalties or seeking separate permission. This eliminates a major source of risk in using open source software.

## Key Principles

- Express patent grants provide certainty; implied grants depend on legal theory
- The scope of a patent grant is typically limited to "necessary claims" or "essential claims" — patents necessarily infringed by the software as contributed
- Patent grants typically cover only the contributor's own patents, not third-party patents
- Patent grants generally apply to the software as contributed, not to subsequent modifications by others
- The absence of an express grant does not necessarily mean no patent rights — implied license theories may apply

## License-by-License Analysis

### Apache License 2.0 (Section 3)
**Express patent grant:** "Subject to the terms and conditions of this License, each Contributor hereby grants to You a perpetual, worldwide, non-exclusive, no-charge, royalty-free, irrevocable... patent license to make, have made, use, offer to sell, sell, import, and otherwise transfer the Work"

- **Scope:** "Patent claims licensable by such Contributor that are necessarily infringed by their Contribution(s) alone or by combination of their Contribution(s) with the Work"
- **Patent retaliation (Section 3, final paragraph):** If you file a patent infringement lawsuit against any contributor alleging the Work infringes your patents, your patent license from all contributors terminates
- **Strength:** Clear, well-drafted, widely understood

### GPLv3 (Section 11)
**Express patent grant:** "Each contributor grants you a non-exclusive, worldwide, royalty-free patent license under the contributor's essential patent claims, to make, use, sell, offer for sale, import and otherwise run, modify and propagate the contents of its contributor version."

- **Scope:** "Essential patent claims" — claims that would be infringed by making, using, or selling the contributor version
- **Anti-patent provisions:** Section 11 also includes provisions against patent aggression, including prohibiting making the software subject to patent licenses that discriminate against GPL users
- **Downstream protection:** GPLv3 attempts to protect downstream users from patent claims by upstream contributors

### GPLv2 (No Express Grant)
- **GPLv2 has no express patent grant.** This is a significant gap.
- **Implied license theory:** Some argue that distributing software under GPLv2 creates an implied patent license (you can't grant a copyright license to use software and then sue for patent infringement for using it)
- **This gap was a major motivation for GPLv3's express patent provisions**

### MPL 2.0 (Section 2.1)
**Express patent grant:** Grants a "world-wide, royalty-free, non-exclusive license... under Patent Claims of such Contributor to make, use, sell, offer for sale, have made, import, and otherwise transfer either its Contributions or its Contributor Version"

- **Scope:** "Patent Claims" of a contributor — claims infringed by the contributor's contribution
- **Patent retaliation (Section 5.2):** If you file a patent infringement claim against a contributor, your rights under the license from that contributor terminate

### MIT / BSD (No Express Grant)
- **No express patent grant.** The licenses are silent on patents.
- **Implied license debate:** Does the broad permission to "use, copy, modify, merge, publish, distribute" implicitly include a patent license? Legal scholars disagree.
- **Practical risk:** A contributor could theoretically contribute code under MIT, then assert patents covering that code. The implied license theory is the primary defense.

## Implied Patent License Debate (MIT/BSD)

The MIT license's broad permissions ("to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies") use verbs that correspond to exclusive patent rights under 35 U.S.C. § 271. Some commentators argue this language creates an implied patent license under the doctrine that a patent holder who distributes a product for unrestricted use implicitly licenses relevant patents.

US courts recognize implied patent licenses where the patent holder's conduct would otherwise create infringement liability but is knowingly permitted. Key factors include intent of the parties, the nature of the dealing, and whether the patentee's actions are inconsistent with an intent to enforce. However, no binding case law tests this theory specifically for MIT/BSD-licensed software.

## Case Law

### XimpleWare v. Versata Software/Cisco
- **Facts:** XimpleWare released an XML parser under GPLv2, then sued Versata and Cisco for both GPL violation (copyright) and patent infringement — asserting patents covering the same technology.
- **Significance:** First prominent case where a GPL licensor asserted *both* patent and copyright claims. Raised the question: Does releasing code under GPL implicitly license the author's own patents? (GPLv2 has no express patent grant.)
- **Outcome:** Settled. No binding precedent, but it remains a cautionary illustration that patent and copyright claims can coexist even for GPL-licensed code.

### Alice Corp. v. CLS Bank International, 573 U.S. 208 (2014)
- **Citation:** 573 U.S. 208 (2014)
- **Holding:** Patent claims directed to abstract ideas implemented on generic computers are not patent-eligible under 35 U.S.C. § 101. Established the "Alice/Mayo two-step test."
- **Significance for OSS:** Made it harder to enforce broad, abstract software patents — beneficial for OSS projects facing patent troll assertions. Led to significant increase in § 101 invalidity challenges.
- **Status:** Still controlling law as of 2025; legislative reform proposals pending but not enacted.

## Commentary & Analysis

### Heather Meeker, "Open Source for Business" (3rd ed., 2020)
- **Source:** *UC Hastings Science & Technology Law Journal*, Vol. 4, Issue 2 (also *Open Source for Business* patent chapter)
- **Key Arguments:** Recommends Apache 2.0 when patent protection matters. Notes that the MIT license's silence on patents is a "drafting gap" that creates risk. The Apache 2.0 patent grant is the clearest and most tested. Reviews evolution of OSS license enforcement.

### Van Lindberg, "Intellectual Property and Open Source" (O'Reilly, 2008)
- **Key Arguments:** Detailed analysis of patent provisions across open source licenses. Covers patent law fundamentals for developers, patent exhaustion doctrine, patent retaliation clauses, and freedom-to-operate analysis. Argues that implied patent licenses exist under MIT/BSD based on estoppel and implied grant theories, but that express grants are always preferable.

### Mark Lemley, "Software Patents and the Return of Functional Claiming" (Wisconsin Law Review, 2013)
- **Source:** Wisconsin Law Review (2013); SSRN
- **Key Arguments:** Argues that overbroad functional claiming in software patents violates the 1952 Patent Act's restrictions and creates patent thickets that stymie innovation. Proposes limiting claims to disclosed implementations and equivalents. Among the most-cited IP scholars on software patent reform.

### Jorge L. Contreras, Patent Pledge Scholarship
- **Source:** Utah Law Review (2015); Edward Elgar (2025)
- **Key Works:**
  - "A Market Reliance Theory for FRAND Commitments and Other Patent Pledges" — proposed market-wide presumption of reliance for public patent pledges
  - "Patent Pledges as Portfolio Management Tools" — taxonomy of pledge types and enforceability analysis
  - Created the Patent Pledge Database (now maintained by University of Copenhagen) cataloging 300+ patent pledges globally

## Practical Guidance

1. **Use Apache 2.0 when patents matter.** If your project involves patented technology, Apache 2.0's express grant and retaliation clause provide the strongest protection.

2. **GPLv3 > GPLv2 for patent protection.** GPLv3's express patent grant addresses GPLv2's significant gap.

3. **MIT/BSD patent risk is real but manageable.** The implied license theory provides some protection, but it's untested in the open source context. For patent-heavy domains, consider Apache 2.0.

4. **Patent retaliation clauses work both ways.** If you file patent litigation against contributors to Apache 2.0 or MPL 2.0 projects, you lose your patent license. Plan accordingly.

## Open Questions

- **Scope of "necessarily infringed."** How broadly do courts interpret "necessarily infringed" or "essential patent claims" in open source licenses? No case law directly on point.
- **Implied patent license under MIT/BSD.** Would a court find an implied patent license? No court has decided this for open source licenses.
- **Patent retaliation scope.** Does the Apache 2.0 retaliation clause apply only to patents covering the Work, or to all patents? The text says "alleging that the Work... constitutes... patent infringement" — limited to Work-related claims.

## Sources

- Apache License 2.0, Section 3
- GNU General Public License v3, Section 11
- GNU General Public License v2 (full text, noting absence of patent grant)
- Mozilla Public License 2.0, Section 2.1
- MIT License (full text)
- Heather Meeker, *Open Source for Business* (3rd ed., 2020)
- Van Lindberg, *Intellectual Property and Open Source* (2008)
