# Software Copyright & Open Source: Case Law and Commentary Knowledge Base

*Compiled for Virtual David Rudin Knowledge Base — Last Updated: 2025*

---

## Table of Contents
1. [Oracle v. Google (SCOTUS 2021)](#1-oracle-v-google)
2. [Software Copyrightability — Foundational Cases](#2-software-copyrightability)
3. [Reverse Engineering & Interoperability Cases](#3-reverse-engineering--interoperability)
4. [Open Source License Enforcement Cases](#4-open-source-license-enforcement)
5. [Derivative Works in Open Source — The Linking Question](#5-derivative-works-in-open-source)
6. [Fair Use in Software](#6-fair-use-in-software)
7. [Leading Commentary & Scholarship](#7-leading-commentary--scholarship)
8. [Key Law Review Articles](#8-key-law-review-articles)

---

## 1. Oracle v. Google

### Full Citation
**Google LLC v. Oracle America, Inc.**, 593 U.S. 1, 141 S. Ct. 1183, 209 L. Ed. 2d 311 (2021).

### Complete Procedural History

| Year | Court | Copyrightability Ruling | Fair Use Ruling |
|------|-------|------------------------|-----------------|
| 2010 | N.D. Cal. (Alsup, J.) | Case filed by Oracle (having acquired Sun Microsystems) | — |
| 2012 | N.D. Cal. (Trial) | **Not copyrightable** — API declaring code and SSO are functional "methods of operation" under §102(b) | Jury deadlocked |
| 2014 | Federal Circuit | **Reversed** — Declaring code and SSO are copyrightable expression; Google could have designed its own API | Remanded for fair use trial |
| 2016 | N.D. Cal. (Jury) | — | **Google wins** — Jury finds fair use |
| 2018 | Federal Circuit | **Reaffirmed copyrightability** | **Reversed** — Not fair use as a matter of law |
| 2021 | U.S. Supreme Court (6-2) | **Assumed copyrightability** without deciding | **Google wins** — Fair use as a matter of law |

### The Facts
- Google copied approximately 11,500 lines of Java SE API **declaring code** (out of millions of lines total) and the **structure, sequence, and organization (SSO)** of 37 Java API packages for use in building the Android platform.
- Google wrote its own **implementing code** — the actual functional code behind the API declarations.
- The declaring code defines the names, parameters, and organization that Java programmers already know; the implementing code does the actual work.

### Supreme Court Holding
The Court held, 6–2, that Google's copying of the Java API declaring code was **fair use** as a matter of law. The Court **assumed without deciding** that the API was copyrightable, resolving the case entirely on fair use grounds.

### Four-Factor Fair Use Analysis

**Factor 1 — Purpose and Character of the Use:**
Google's use was **transformative**. Google reimplemented a user interface in a new and different computing platform (smartphones), enabling programmers to use their existing skills in a new context. This was not mere market substitution.

**Factor 2 — Nature of the Copyrighted Work:**
Declaring code is "inherently different" from most copyrighted works. It is primarily **functional** — an organizational tool that enables programmers to call upon implementing code. It is "further from the core of copyright" than most works.

**Factor 3 — Amount and Substantiality:**
Google copied only what was needed to allow programmers to use their accrued talents — roughly 11,500 lines of declaring code out of 2.86 million total lines in Java SE. The copying was limited to what was necessary for interoperability.

**Factor 4 — Market Effect:**
Oracle was not well-positioned to compete in the smartphone market. Android created a new platform rather than serving as a market substitute for Java SE. The relevant market was smartphone platforms, not Java SE licensing.

### Key Quotes

> "Where Google reimplemented a user interface, taking only what was needed to allow users to put their accrued talents to work in a new and transformative program, Google's copying of the Sun Java API was a fair use of that material as a matter of law."
> — Majority Opinion (Breyer, J.), Slip Op. at 35

> "We do not believe that an approach close to 'all or nothing' would be faithful to the Copyright Act's overall design."
> — Majority Opinion

> "To the extent that these interfaces are copyrightable, the fair use doctrine can play a significant role in determining whether and when their use (or their reuse) by others is lawful."
> — Majority Opinion

### Dissent (Thomas, J., joined by Alito, J.)
Argued the majority failed to settle the threshold copyrightability issue and that none of the four fair use factors favored Google. Warned the majority's approach renders functional code "less worthy of protection," potentially reducing incentives for software development.

### Significance
1. **API copyrightability remains formally unresolved.** The Court deliberately ducked this question, leaving the Federal Circuit's copyrightability holding intact for that case but setting no precedent on the general question.
2. **Fair use provides a safety valve.** Even assuming APIs are copyrightable, reimplementation for interoperability in a transformative new context is likely fair use.
3. **"Declaring code" is a new category.** The Court created a conceptual distinction between declaring code (functional, organizational) and implementing code (creative expression), suggesting different copyright treatment.
4. **Industry impact.** The decision supports the longstanding software industry practice of reimplementing APIs for compatibility, giving legal comfort to practices that power cloud computing, open source ecosystems, and cross-platform development.

### What the Case Did NOT Decide
- Whether APIs are copyrightable subject matter (left open)
- Whether all API reimplementation is fair use (case-specific)
- The relationship between §102(b) (methods of operation) and API declaring code

---

## 2. Software Copyrightability — Foundational Cases

### 2A. Whelan Associates, Inc. v. Jaslow Dental Laboratory, Inc.
**Citation:** 797 F.2d 1222 (3d Cir. 1986)

**Holding:** Copyright protection extends to a computer program's **structure, sequence, and organization (SSO)**, not just its literal code. The "idea" of a program is its purpose or function; everything else is protectable "expression."

**Facts:** Whelan developed dental lab management software (Dentalab). Jaslow created a functionally identical program (Dentlab) in a different programming language, replicating the overall structure, logic flow, and module arrangement without copying any literal code.

**Significance:**
- Established the **broadest view** of software copyright protection — SSO is protectable expression.
- Applied a simple dichotomy: one "idea" per program (its purpose), everything else is expression.
- Drew on Baker v. Selden (1879) idea-expression dichotomy.

**Criticism:**
- Overly broad — essentially gave copyright protection to program architecture.
- Conflated creative choices with functional necessities.
- **Largely superseded** by Computer Associates v. Altai but still cited as the high-water mark for broad software copyright protection.

### 2B. Computer Associates International, Inc. v. Altai, Inc.
**Citation:** 982 F.2d 693 (2d Cir. 1992)

**Holding:** Introduced the **Abstraction-Filtration-Comparison (AFC) test** for evaluating copyright infringement of non-literal elements of computer programs. After applying the test, found Altai's rewritten program did not infringe.

**The Abstraction-Filtration-Comparison Test:**

**Step 1 — Abstraction:**
Break the program into successive levels of generality — from specific code, to individual modules, to the program's overall structure, up to its most abstract purpose. (Analogous to Judge Learned Hand's "abstractions test" from Nichols v. Universal Pictures.)

**Step 2 — Filtration:**
At each level, filter out elements that are NOT protectable:
- **Merger doctrine:** Where an idea can be expressed in only one or a limited number of ways, the expression merges with the idea and is unprotectable.
- **Scènes à faire:** Elements dictated by external factors (hardware requirements, interoperability standards, widely accepted programming practices).
- **Public domain:** Previously published or well-known elements.

**Step 3 — Comparison:**
Compare only the **remaining protectable elements** with the accused work to determine substantial similarity.

**Significance:**
- **The dominant test** for non-literal software copyright infringement in U.S. courts.
- Effectively narrowed Whelan's broad protection by requiring courts to strip away functional, externally dictated, and public domain elements before comparing.
- Widely adopted across circuits (though not universally — the Federal Circuit in Oracle v. Google took a different approach to copyrightability).

**Key Insight:** Much of what appears to be creative "structure" in software is actually dictated by efficiency, hardware constraints, interoperability requirements, or standard programming conventions — and thus unprotectable.

### 2C. Lotus Development Corp. v. Borland International, Inc.
**Citation:** 49 F.3d 807 (1st Cir. 1995), *aff'd by equally divided court*, 516 U.S. 233 (1996).

**Holding:** The **menu command hierarchy** of Lotus 1-2-3 is an uncopyrightable **"method of operation"** under 17 U.S.C. §102(b), even though creative choices went into designing it.

**Facts:** Borland copied the entire Lotus 1-2-3 menu command hierarchy (not the underlying code) to ensure user compatibility — allowing Lotus users to switch to Borland's spreadsheet without learning new commands or rewriting macros.

**Key Quote:**
> "Just as it would be impossible to operate a VCR without buttons, it would be impossible to operate Lotus 1-2-3 without using its menu command hierarchy. Therefore, the Lotus command terms are equivalent to the buttons themselves, which are an uncopyrightable method of operating the VCR."

**Significance:**
- Applied §102(b)'s "method of operation" exclusion directly to software user interfaces.
- Established that some software elements, even if reflecting creative choices, are **functional** and thus uncopyrightable.
- **Affirmed by equally divided Supreme Court** (4-4, Justice Stevens recused) — left the First Circuit's holding intact but set no national precedent.
- Strong precursor to the arguments in Oracle v. Google.
- The 1st Circuit explicitly rejected applying the AFC test for this question, finding §102(b) is a threshold exclusion, not a similarity test.

**Relationship to Oracle v. Google:** Judge Alsup relied heavily on Lotus v. Borland in holding Java API declaring code uncopyrightable. The Federal Circuit rejected this analogy. The Supreme Court sidestepped the issue entirely.

### 2D. Additional Significant Cases

**Apple Computer, Inc. v. Franklin Computer Corp.**, 714 F.2d 1240 (3d Cir. 1983)
- Held that both **source code and object code** are copyrightable as "literary works."
- Established that an operating system, not just application software, is copyrightable.
- Foundational case for software copyright protection.

**Lexmark International, Inc. v. Static Control Components, Inc.**, 387 F.3d 522 (6th Cir. 2004)
- Lexmark's embedded toner cartridge authentication code was **not sufficiently creative** for copyright protection — largely functional and dictated by hardware requirements.
- DMCA anti-circumvention provisions cannot be used to create de facto monopolies over functional product components.
- Important for interoperability and right-to-repair in the software context.

---

## 3. Reverse Engineering & Interoperability Cases

### 3A. Sega Enterprises Ltd. v. Accolade, Inc.
**Citation:** 977 F.2d 1510 (9th Cir. 1992)

**Holding:** Reverse engineering copyrighted software through disassembly (intermediate copying) to discover unprotected functional requirements for interoperability constitutes **fair use** — where no other means of accessing unprotectable elements exists.

**Facts:** Accolade disassembled Sega Genesis game cartridge code to discover the interface specifications needed to make compatible games, without being a Sega licensee.

**Key Principle:** If reverse engineering is the only way to access unprotected functional elements necessary for interoperability, the intermediate copying required is fair use. Without this rule, copyright owners could obtain **de facto monopolies** over functional aspects of their software.

**Fair Use Factors:** All four factors favored Accolade — legitimate, non-exploitative purpose (interoperability), functional nature of code, and minimal market harm.

### 3B. Sony Computer Entertainment, Inc. v. Connectix Corp.
**Citation:** 203 F.3d 596 (9th Cir. 2000)

**Holding:** Intermediate copying of Sony PlayStation BIOS during reverse engineering to create a compatible emulator (Virtual Game Station) is **fair use**.

**Key Distinction:** Even though the entire BIOS was temporarily copied during development, the final product contained none of Sony's code. The use was transformative — enabling PlayStation games to run on a new platform (personal computers).

**Significance Together with Sega v. Accolade:**
- Established a robust fair use doctrine for reverse engineering in the 9th Circuit.
- Protected intermediate copying as a necessary step to access unprotectable functional elements.
- Drew a clear line: the final product must not contain copied code; the copying is justified only as a means to an end (interoperability).
- Both cases are heavily cited in Oracle v. Google and in open source contexts.

---

## 4. Open Source License Enforcement Cases

### 4A. Jacobsen v. Katzer
**Citation:** 535 F.3d 1373 (Fed. Cir. 2008)

**Holding:** Open source license conditions (attribution, source disclosure, license notice) are **enforceable copyright conditions**, not merely contractual covenants. Violating them constitutes **copyright infringement**, not just breach of contract.

**Facts:** Katzer incorporated Jacobsen's code (distributed under the Artistic License) into commercial products without following attribution and license notice requirements.

**Significance:**
- **The foundational case** for open source license enforceability in U.S. law.
- Established that open source license conditions are **conditions** on the copyright license grant, not mere contractual promises. This distinction matters enormously: copyright infringement triggers statutory damages, injunctive relief, and attorney's fees. Breach of contract typically provides only actual damages.
- Makes clear that "free" software is not "public domain" — the license conditions are real and enforceable.

**Key Quote from Harvard JOLT Commentary:**
The Federal Circuit "affirmed the economic interest of open source copyright holders," recognizing that the value of open source distribution lies precisely in the conditions (attribution, share-alike, source availability) attached to the license.

### 4B. Artifex Software, Inc. v. Hancom, Inc.
**Citation:** No. 16-cv-06982-JSC (N.D. Cal. 2017)

**Holding:** The GPL is legally enforceable as both a **copyright license** and a **contract**. Artifex's claims for copyright infringement and breach of contract both survived a motion to dismiss.

**Facts:** Artifex distributes Ghostscript under a dual-license model (GPL or commercial). Hancom incorporated Ghostscript into commercial products without releasing source code (as GPL requires) and without purchasing a commercial license.

**Significance:**
- Reaffirmed that GPL obligations are enforceable and that ignoring them exposes companies to both copyright infringement and breach of contract claims.
- Demonstrates the practical enforceability of copyleft requirements.
- Confirmed that dual-licensing models have legal teeth.

### 4C. BusyBox GPL Enforcement Cases (2007–2012)
The Software Freedom Law Center (SFLC), on behalf of BusyBox developers, brought multiple enforcement actions against companies distributing BusyBox in embedded products without complying with the GPL (failing to provide source code). Most settled with compliance agreements. These cases established practical precedent that GPL enforcement is real and that companies cannot ignore source code obligations.

---

## 5. Derivative Works in Open Source — The Linking Question

### The Central Question
What makes a program a "derivative work" of GPL-licensed software? This is THE central unresolved question in open source licensing, because the GPL's copyleft obligations extend to "derivative works" and "works based on the Program."

### Statutory Framework
17 U.S.C. §101 defines a "derivative work" as "a work based upon one or more preexisting works, such as a translation, musical arrangement, dramatization, fictionalization, motion picture version, sound recording, art reproduction, abridgment, condensation, or any other form in which a work may be recast, transformed, or adapted."

### The Three Positions

#### Position 1: FSF / Eben Moglen — Broad Interpretation
**Claim:** Both static and dynamic linking to GPL-covered code create a "combined work based on the GPL covered work," triggering full copyleft obligations.

**FSF GPL FAQ (authoritative statement):**
> "Linking a GPL covered work statically or dynamically with other modules is making a combined work based on the GPL covered work. Thus, the terms and conditions of the GNU General Public License cover the whole combination."

**Rationale:**
- The user receives a single combined work that cannot function without the GPL component.
- The distinction between static and dynamic linking is a technical implementation detail, not a copyright law distinction.
- The GPL's purpose — ensuring software freedom for end users — supports treating tightly coupled code as a single work.

**Moglen's position:** No bright-line rule exists, but the policy intention of the GPL supports treating linked combinations as combined works. Static linking "almost certainly" creates a derivative work; dynamic linking "may also" trigger copyleft depending on the degree of integration.

#### Position 2: Lawrence Rosen — Derivative Work vs. Collective Work
**Claim:** Merely linking to an open source library (especially dynamically) creates a **collective work**, not a **derivative work**, and copyleft should not extend to the entire combination.

**Key Distinction:**
- **Derivative work** = actual modification of or substantive integration with the original code; the new work is "based on" the original.
- **Collective work** = assembly of separate, independent works into a whole where each component retains its independence.

**Rosen's Analysis (from "Geek Law" columns and *Open Source Licensing*):**
- Dynamic linking connects independent codebases through well-defined interfaces (APIs). The calling program and the library remain separate works.
- The calling program is not "based on" the library in any meaningful copyright sense — it uses the library's functionality through a standard interface.
- The OSL (Open Software License, authored by Rosen) explicitly distinguishes between derivative works and collective works, and limits copyleft to true derivative works.
- Static linking is more ambiguous because the code is physically combined into one binary, but even here, the analysis should focus on whether the new work is "based on" the library.

| Action | Rosen's View | License Impact |
|--------|-------------|----------------|
| Code modification/integration | Derivative work | Copyleft applies |
| Unmodified component in package | Collective work | No copyleft on whole |
| Static linking | Context-dependent | Possibly copyleft |
| Dynamic linking | Usually collective | Minimal copyleft risk |

**Source:** Rosen, Lawrence. "Derivative Works," Linux Journal (2003); Rosen, *Open Source Licensing: Freedom and Enforcement* (Prentice Hall, 2004), Chapter 5.

#### Position 3: Heather Meeker — Practical Compliance Focus
**Claim:** The "derivative work" question is often a red herring. Focus on practical license compliance, not doctrinal categories.

**Key Points from Meeker:**
- The GPL uses its own terms ("work based on the Program") that go beyond the formal copyright law definition of "derivative work."
- The critical question is: **"Is it one program or two?"** — can the user see and replace the component independently, or is it distributed as a single binary?
- For **GPL:** Both static and dynamic linking are typically treated by the community as creating a single combined program. This is the community expectation and the prudent compliance approach.
- For **LGPL:** Designed specifically for libraries — allows dynamic linking from proprietary code without triggering copyleft on the whole. Static linking may trigger obligations (user must be able to relink with modified library).
- **Distribution triggers obligations.** SaaS/cloud use does not constitute distribution unless the license says so (AGPL).
- **Permissive licenses (MIT, BSD, Apache):** Linking creates no copyleft risk — only notice requirements.

**Source:** Meeker, Heather. *Open (Source) for Business: A Practical Guide to Open Source Software Licensing* (3rd ed., 2020).

### The Legal Reality: No Court Has Decided This
**There is no U.S. (or global) court decision** squarely holding that dynamic linking to a GPL library creates a derivative work. The question remains genuinely unresolved as a matter of copyright law.

**Factors courts would likely consider:**
1. Does the accused work incorporate copyrightable expression from the GPL code, or only functional interfaces?
2. Is the combination so tightly integrated that the accused work cannot function independently?
3. Has the accused work merely used the GPL code through standard, well-defined APIs (like any other library)?
4. Could the GPL library be replaced with a different implementation without altering the accused work?
5. What is the physical form of distribution — single binary or separate components?

**Practical takeaway:** The FSF's interpretation is the most conservative (safest from a compliance perspective) but may overreach as a matter of copyright law. Rosen's distinction between derivative and collective works has sound doctrinal support but has not been tested in court. Meeker's practical approach ("is it one program or two?") is probably the best operational framework.

---

## 6. Fair Use in Software

### The Fair Use Cascade
U.S. courts have built a consistent body of fair use law for software, centered on **interoperability** and **transformative use**:

| Case | Year | Key Fair Use Principle |
|------|------|-----------------------|
| **Sega v. Accolade** | 1992 | Reverse engineering for interoperability is fair use (9th Cir.) |
| **Sony v. Connectix** | 2000 | Intermediate copying during reverse engineering is fair use if final product is clean (9th Cir.) |
| **Google v. Oracle** | 2021 | Reimplementing API declarations for a transformative new platform is fair use (SCOTUS) |

### Common Threads
1. **Interoperability purpose strongly favors fair use.** Copying that enables software to work with existing systems, standards, or programmer knowledge is transformative.
2. **Functional code gets less copyright protection.** Declaring code, interface specifications, and API structures are "further from the core of copyright."
3. **Amount must be proportional.** Copying only what is necessary for interoperability — not wholesale reproduction of implementing code.
4. **Market substitution weighs against fair use.** If the copy replaces the original in its primary market, fair use is unlikely. If it creates a new market or platform, fair use is more likely.

### Fair Use in Open Source Contexts
- **No significant case law** directly applies fair use as a defense to GPL or other open source license violations. The typical enforcement framework is copyright infringement (Jacobsen v. Katzer), not fair use defense.
- Fair use is more likely relevant in the **reimplementation context** (building compatible alternatives) than in the **license violation context** (distributing GPL code without source).
- The Oracle v. Google decision provides significant comfort for **clean-room reimplementation** of APIs — a practice common in open source (e.g., WINE, Mono, OpenJDK alternative implementations).

---

## 7. Leading Commentary & Scholarship

### Heather Meeker
**Affiliation:** Partner, OSS Capital; formerly partner at O'Melveny & Myers.
**Key Work:** *Open (Source) for Business: A Practical Guide to Open Source Software Licensing* (3rd ed., 2020).
**Blog:** Copyleft Currents (https://heathermeeker.com/)

**Core Positions:**
- The most practical and business-oriented voice in open source licensing.
- Focus on compliance, not doctrinal purity. "Derivative work" is often the wrong question — focus on what the license says and how the community interprets it.
- Distinguishes strong copyleft (GPL) from weak copyleft (LGPL, MPL, EPL) and permissive (MIT, BSD, Apache).
- Emphasizes that **distribution** is the trigger for most open source obligations; cloud/SaaS deployment is not distribution (except AGPL).
- The "one program or two?" test for linking boundaries.
- Comprehensive treatment of LGPL dynamic linking safe harbor.

### Pamela Samuelson
**Affiliation:** Richard M. Sherman Distinguished Professor of Law, UC Berkeley School of Law; co-director, Berkeley Center for Law & Technology.

**Core Positions:**
- The most influential academic voice arguing for **narrow software copyright protection**.
- Functional elements (APIs, interfaces, methods of operation) should not be copyrightable.
- The Federal Circuit's Oracle v. Google copyrightability holding was wrong — inconsistent with §102(b) and the weight of regional circuit authority.
- The AFC test (Computer Associates v. Altai) correctly filters out functional and externally dictated elements.
- Concerned that Oracle v. Google's failure to resolve copyrightability leaves dangerous uncertainty.

**Key Publications:**
- "Functionality and Expression in Computer Programs: Refining the Tests for Software Copyright Infringement," 31 Berkeley Tech. L.J. 1215 (2016).
- "Staking the Boundaries of Software Copyrights in the Shadow of Patents," 71 Fla. L. Rev. 243 (2019).
- "Interfaces and Interoperability After Google v. Oracle," 100 Texas L. Rev. 1 (2021) (with Mark Lemley).

### Mark Lemley
**Affiliation:** William H. Neukom Professor, Stanford Law School; Director, Stanford Program in Law, Science & Technology.

**Core Positions:**
- Software interfaces should not be copyrightable; denying fair use in reimplementation contexts would "entrench monopolies and harm innovation."
- Strong advocate for robust fair use in software, extending to API reimplementation, reverse engineering, and (recently) AI training.
- The idea-expression dichotomy must be applied aggressively in software — much of what looks like creative structure is actually functional or dictated by external factors.

**Key Publications:**
- "Interfaces and Interoperability After Google v. Oracle," 100 Texas L. Rev. 1 (2021) (with Pamela Samuelson).
- "Fair Learning," Stanford Law School (2023) — extends fair use analysis to AI training data.
- "How Generative AI Turns Copyright Law Upside Down," Columbia Science & Technology Law Review (2024).

### Lawrence Rosen
**Affiliation:** Attorney; former General Counsel, Open Source Initiative (OSI); author of the OSL and AFL.
**Key Work:** *Open Source Licensing: Freedom and Enforcement* (Prentice Hall, 2004).

**Core Positions:**
- The derivative work / collective work distinction is the key analytical framework for linking questions.
- Dynamic linking generally creates a collective work, not a derivative work — copyleft should not extend to the entire combination.
- License text controls — courts should look at what the license actually says, not what the community "expects."
- The OSL was designed to be clearer than the GPL on the scope of copyleft.

**Key Publications:**
- *Open Source Licensing: Freedom and Enforcement* (Prentice Hall, 2004), esp. Chapter 5 on derivative works.
- "Derivative Works," Linux Journal (2003).

### Eben Moglen
**Affiliation:** Professor of Law, Columbia Law School; founder, Software Freedom Law Center (SFLC); former General Counsel, Free Software Foundation.

**Core Positions:**
- The broadest interpretation of copyleft obligations. Both static and dynamic linking trigger GPL copyleft.
- Copyright law should be interpreted to maximize software freedom for end users.
- GPL enforcement is a practical necessity — without enforcement, copyleft is meaningless.
- Helped draft GPLv3.
- No bright-line rule, but the policy intention of GPL supports treating linked combinations as combined works.

**Key Publications and Activities:**
- Co-drafter, GPLv3 (2007).
- Founding Director, Software Freedom Law Center.
- "Freeing the Mind: Free Software and the Death of Proprietary Culture" (lecture/essay).
- SFLC, "A Practical Guide to GPL Compliance."

---

## 8. Key Law Review Articles

### Essential Reading List

| Citation | Authors | Key Contribution |
|----------|---------|-----------------|
| "Interfaces and Interoperability After Google v. Oracle," 100 Texas L. Rev. 1 (2021) | Lemley & Samuelson | Most authoritative post-SCOTUS analysis of API copyrightability; argues interfaces should not be copyrightable |
| "Functionality and Expression in Computer Programs," 31 Berkeley Tech. L.J. 1215 (2016) | Samuelson | Definitive analysis of how to distinguish protectable expression from unprotectable function in software |
| "Staking the Boundaries of Software Copyrights in the Shadow of Patents," 71 Fla. L. Rev. 243 (2019) | Samuelson | Critiques Federal Circuit's Oracle copyrightability holding as inconsistent with §102(b) |
| "Google LLC v. Oracle America, Inc.," 135 Harv. L. Rev. 431 (2021) | Harvard Law Review (student note) | Leading case comment on the SCOTUS decision |
| "How Generative AI Turns Copyright Law Upside Down," Columbia Sci. & Tech. L. Rev. (2024) | Lemley | Extends software copyright analysis to AI training — disrupts traditional idea-expression dichotomy |
| "Fair Learning," Stanford Law (2023) | Lemley | Fair use applied to AI training data; builds on software interoperability principles |
| "Copyright, Contract, and Licensing in Open Source," in *Open Source Law, Policy and Practice* (Oxford, 2022) | Various | Comprehensive academic treatment of copyright mechanics in open source licensing |
| "Jacobsen v. Katzer: Federal Circuit Affirms Economic Interest of Open Source Copyright Holders" | Harvard JOLT Digest | Analysis of the foundational OSS enforcement case |
| "Open Source Software: Litigation Windfall or Landmine?" (Dentons, 2020) | Dentons LLP | Practical litigation risk analysis for open source copyright |

### Themes in Current Scholarship (2020–2025)
1. **Post-Oracle uncertainty.** The copyrightability of APIs remains formally unresolved. Scholars overwhelmingly view the Federal Circuit's 2014 copyrightability holding as wrong but acknowledge the Supreme Court did not overrule it.
2. **AI and open source convergence.** As AI systems train on open source code, new questions arise about fair use, license compliance, and derivative works in the AI context.
3. **Collaborative authorship.** Joint works vs. collective works in open source projects — who owns what in a project with hundreds of contributors?
4. **License compatibility.** The proliferation of open source licenses creates combinatorial complexity for projects that use components under different licenses.
5. **Copyleft's declining market share.** Permissive licenses (MIT, Apache) now dominate new projects, while copyleft (GPL) is declining — raising questions about whether copyleft's legal theories will ever be fully tested.

---

## Quick Reference: Case Citation Table

| Case | Citation | Court | Year | Key Principle |
|------|----------|-------|------|--------------|
| Apple v. Franklin | 714 F.2d 1240 | 3d Cir. | 1983 | Source and object code are copyrightable |
| Whelan v. Jaslow | 797 F.2d 1222 | 3d Cir. | 1986 | SSO broadly protectable (largely superseded) |
| Computer Assocs. v. Altai | 982 F.2d 693 | 2d Cir. | 1992 | AFC test for non-literal infringement |
| Sega v. Accolade | 977 F.2d 1510 | 9th Cir. | 1992 | Reverse engineering for interop = fair use |
| Lotus v. Borland | 49 F.3d 807 | 1st Cir. | 1995 | Menu hierarchy = uncopyrightable method of operation |
| Sony v. Connectix | 203 F.3d 596 | 9th Cir. | 2000 | Intermediate copying for emulation = fair use |
| Lexmark v. Static Control | 387 F.3d 522 | 6th Cir. | 2004 | Functional embedded code not sufficiently creative; DMCA limits |
| Jacobsen v. Katzer | 535 F.3d 1373 | Fed. Cir. | 2008 | OSS license conditions = copyright conditions, not just contract |
| Oracle v. Google (FC I) | 750 F.3d 1339 | Fed. Cir. | 2014 | API declaring code and SSO are copyrightable |
| Artifex v. Hancom | No. 16-cv-06982 | N.D. Cal. | 2017 | GPL enforceable as both copyright license and contract |
| Oracle v. Google (FC II) | 886 F.3d 1179 | Fed. Cir. | 2018 | Google's use was not fair use |
| Google v. Oracle (SCOTUS) | 141 S. Ct. 1183 | SCOTUS | 2021 | API reimplementation is fair use (copyrightability assumed) |

---

*This document is a research compilation for knowledge base purposes. It summarizes publicly available case law and legal commentary. It is not legal advice.*
