# International Open Source Software Case Law & Legal Developments

## Knowledge Base — Non-US Jurisdictions

*Last updated: July 2025*
*Sources: Web research, court records, legal commentary, JOLTS/IFOSSLR*

---

## 1. GERMANY — The Global Center of GPL Enforcement

Germany has the most developed GPL enforcement case law outside the US. Three reasons: (1) German copyright law provides strong statutory protections for software (UrhG §§69a–69g); (2) preliminary injunctions are relatively easy to obtain; (3) a small group of dedicated lawyers (notably Dr. Till Jaeger) and activists (Harald Welte) systematically pursued enforcement for over two decades.

### 1.1 Legal Framework: German Copyright Act (UrhG)

**Sections 69a–69g UrhG** implement the EU Software Directive and provide the backbone for OSS enforcement:

- **§69a**: Computer programs are protected as literary works if they constitute a personal intellectual creation. Both source and object code are protected, as well as preparatory design materials.
- **§69b**: Employer ownership of employee-created software (work-for-hire equivalent).
- **§69c**: Exclusive rights — reproduction, distribution, adaptation, public communication.
- **§69d**: Exceptions — lawful users may reproduce/adapt as necessary for intended purpose; backup copies permitted.
- **§69e**: Decompilation — permitted solely to achieve interoperability with independently created programs, subject to strict conditions (mirrors EU Software Directive Art. 6).
- **§69f**: Enforcement remedies — destruction of infringing copies, injunctions.
- **§69g**: Application of general copyright provisions.

**Key legal principles for OSS enforcement in Germany:**
- OSS licenses are legally enforceable contracts under German law. Breach of license conditions = copyright infringement (not merely breach of contract), which triggers stronger remedies including injunctions.
- Both individual developers and organizations with assigned copyright can enforce.
- Moral rights (attribution) remain with the original developer(s) and cannot be waived.
- Criminal prosecution is available in extreme cases under §106 UrhG.

**Full English text**: https://www.gesetze-im-internet.de/englisch_urhg/

### 1.2 Welte / gpl-violations.org — Pioneering Enforcement (2004–2013)

Harald Welte, a core Linux kernel developer (netfilter/iptables), founded **gpl-violations.org** in 2004 after discovering widespread GPL non-compliance in embedded devices. Working with attorney **Dr. Till Jaeger** (then JBB Rechtsanwälte, Berlin), Welte brought the first successful GPL enforcement actions in any court worldwide.

**Landmark cases:**

| Year | Case | Court | Key Outcome |
|------|------|-------|-------------|
| 2004 | Sitecom | LG München I | First preliminary injunction enforcing GPL worldwide. Sitecom enjoined from distributing wireless router firmware containing GPL code without source. |
| 2005 | **Fortinet** | LG München I | Fortinet used GPL code in FortiOS and attempted to mask violations using encryption. Court issued temporary injunction halting sales. Fortinet forced to release required source code. |
| 2006 | **D-Link** | LG Frankfurt | D-Link distributed products with embedded Linux without source code or license documentation. Court ruled against D-Link, affirming GPL enforceability in civil proceedings. Landmark "acid test" for GPL in German courts. |
| 2007 | Skype | LG München I | Skype's WLAN phone contained GPL code. Court granted injunction. |
| 2013 | **Fantec** | LG Hamburg | Fantec, a German electronics distributor, repeatedly failed to supply complete corresponding source code for GPLv2 components. Court held distributors (not just manufacturers) must fulfill GPL obligations regardless of supplier assurances. |

**Legacy:**
- By 2006, gpl-violations.org had resolved 100+ infringement cases, all successfully.
- Welte received the **2007 FSF Award for the Advancement of Free Software**.
- Established that GPL is a valid, enforceable license instrument in German/EU law.
- Created the template for enforcement procedure: cease-and-desist → declaration to cease → source code delivery → costs → injunction if non-compliant.

**Sources:**
- https://gpl-violations.org/about/
- https://wiki.fsfe.org/Migrated/GPL%20Enforcement%20Cases
- Jaeger, "GPL Enforcement and License Compliance in Europe" (Linux Foundation, 2013)
- https://www.linux.com/news/gpl-passes-acid-test-german-court/

### 1.3 Hellwig v. VMware (2015–2019) — The Big One That Wasn't

**Parties:** Christoph Hellwig (Linux kernel developer) v. VMware Inc.
**Backed by:** Software Freedom Conservancy (SFC)
**Courts:** LG Hamburg (2016), OLG Hamburg (2017–2019)

**Facts:** VMware's ESXi hypervisor included a compatibility module called "vmklinux" that contained Linux kernel code. Hellwig argued vmklinux and VMware's proprietary kernel (vmkernel) formed a derivative work under GPLv2, requiring VMware to release vmkernel source code. VMware maintained vmkernel was independent — the "shim layer" argument.

**Procedural history:**
- **2015**: Hellwig filed suit in LG Hamburg.
- **July 2016**: LG Hamburg **dismissed** the case on evidentiary grounds — Hellwig had not sufficiently demonstrated that *his specific copyrighted code* was present in the disputed portions of VMware's software.
- **2017–2019**: OLG Hamburg (Higher Regional Court) upheld the dismissal on procedural/evidentiary grounds.
- **April 2019**: Hellwig declined further appeal. Case closed.

**What the court DID NOT decide:**
- Whether combining GPL kernel modules with proprietary code via a shim layer creates a "derivative work"
- The scope of GPLv2 copyleft in the context of loadable kernel modules
- Any substantive question about GPL interpretation

**Practical outcome:** VMware eventually removed vmklinux (Linux-derived code) from vSphere, achieving de facto compliance by eliminating the GPL code rather than open-sourcing vmkernel.

**David's take:** This is the paradigmatic "won on process, not substance" case. The most important GPL question in the embedded/enterprise space — what constitutes a derivative work when you have shim layers and dynamic linking — remains judicially unresolved in any jurisdiction. From an enforcement perspective, it highlights the standing and evidentiary burden challenges: individual developers must prove their *specific* code is in the accused product. That's expensive, technically demanding, and procedurally risky. VMware's practical response (removing the code) is actually the enforcement outcome Welte's approach always aimed for — behavioral change, not damages.

**Sources:**
- https://sfconservancy.org/news/2019/apr/02/vmware-no-appeal/
- https://lwn.net/Articles/784673/
- https://opensource.com/law/16/8/gpl-enforcement-action-hellwig-v-vmware
- https://www.ifross.org/?q=artikel/hellwig-vs-vmware-gpl-enforcement-lawsuit-hamburg-district-court

### 1.4 Patrick McHardy — The GPL Copyright Troll Problem (2011–2022)

Patrick McHardy, a former core developer of the Linux Netfilter project, became the most controversial figure in GPL enforcement history.

**What he did:**
- From ~2011 onwards, initiated **50+ lawsuits or legal warnings** against companies for GPL non-compliance related to Linux kernel/netfilter code.
- Demanded companies sign cease-and-desist declarations with **contractual penalty clauses** that would benefit him personally upon future violations.
- Reportedly extracted up to **€2 million** in settlements.
- Acted unilaterally, without coordination with the Netfilter project or broader community.

**Why it was problematic:**
- Focus on financial extraction rather than achieving compliance.
- Secretive litigation — companies weren't given reasonable opportunity to cure.
- Exploited Germany's favorable injunction procedures for personal gain.
- Described by critics (including SFC) as "copyright trolling."
- Damaged the reputation of community-led GPL enforcement.

**Community response:**
1. **Netfilter core team suspended McHardy** (2016).
2. **"Principles of Community-Oriented GPL Enforcement"** published by SFC, FSF, and gpl-violations.org — emphasizing compliance and cooperation over litigation and monetary penalties.
3. **Linux Kernel Enforcement Statement** (2017) — kernel developers adopted GPLv3-style cure provisions, giving violators a "cure period" to come into compliance before license termination becomes permanent. Signed by hundreds of kernel contributors.
4. **GPL Cooperation Commitment** — major companies (Red Hat, IBM, Google, Facebook, etc.) committed to providing cure opportunities even under GPLv2.
5. **2022 Settlement**: Netfilter project obtained a legally binding settlement requiring that any future enforcement actions involving Netfilter code must be decided by **majority vote of the active core team**, ending McHardy's ability to act solo.

**McHardy v. Geniatech (LG Mannheim, 2018):** One of the publicly reported cases. Court hearing documented by Harald Welte at https://laforge.gnumonks.org/blog/20180307-mchardy-gpl/. Analysis in JOLTS: "Opposing the Monetization of Linux: McHardy v. Geniatech" — https://www.jolts.world/index.php/jolts/article/view/128

**David's take:** McHardy is the textbook example of why "process is substance" in enforcement. Legally, everything he did was arguably within his rights as a copyright holder — German law gives individual contributors standing. But his approach was corrosive to the ecosystem. The community's response was masterful governance engineering: the Kernel Enforcement Statement, the GPL Cooperation Commitment, and the Netfilter settlement together created a framework that channels enforcement through community process rather than individual action. This is governance design at its best — "create the rules, once they're playing on your gameboard, you've already won."

**Sources:**
- https://sfconservancy.org/blog/2016/jul/19/patrick-mchardy-gpl-enforcement/
- https://lwn.net/Articles/882397/ (Netfilter settlement)
- https://docs.kernel.org/process/kernel-enforcement-statement.html
- https://gplcc.github.io/gplcc/

---

## 2. EU CASE LAW & REGULATORY FRAMEWORK

### 2.1 SAS Institute v. World Programming Ltd (CJEU, Case C-406/10, 2012)

The most important EU-level decision on the scope of software copyright protection.

**Facts:** SAS Institute developed the SAS System, including a proprietary programming language. World Programming Ltd (WPL) created a competing product that emulated SAS functionality — running SAS scripts on WPL's platform — without copying source code.

**CJEU held:**
1. **Functionality not protected**: Neither the functionality of a computer program, the programming language, nor the format of data files constitutes copyrightable expression. These are ideas and principles — not expression.
2. **Observation/study/testing rights**: A lawful user may observe, study, and test a program to discover its underlying ideas and principles, *even if the license attempts to restrict this* (per Software Directive Art. 5(3)).
3. **User manuals**: Reproducing elements from a manual may constitute infringement only if the reproduction reflects the *expression of the intellectual creation*, not just underlying ideas.

**Significance for OSS:**
- Confirms the idea/expression dichotomy as core EU software copyright law.
- Supports clean-room reimplementation of functionality — critical for open source projects creating compatible alternatives to proprietary software.
- License restrictions on observation/study are overridden by statute — important for understanding how software works for interoperability purposes.
- Strongly pro-competition and pro-interoperability.

**Sources:**
- https://ipcuria.eu/case?reference=C-406/10
- https://en.wikipedia.org/wiki/SAS_Institute_Inc_v_World_Programming_Ltd
- https://www.europeanlawblog.eu/pub/c-40610-sas-institute-v-world-programming-ltd-wpl

### 2.2 EU Software Directive (2009/24/EC)

Codified version of the original 1991 Computer Programs Directive (91/250/EEC). Harmonizes software copyright across EU member states.

**Key provisions relevant to OSS:**

- **Art. 1**: Copyright protection extends to the expression of a computer program, not ideas/principles/interfaces.
- **Art. 4**: Exclusive rights — reproduction, translation, adaptation, distribution.
- **Art. 5**: Exceptions — lawful users may reproduce/adapt as necessary; backup copies; observation/study/testing to understand ideas and principles.
- **Art. 6**: **Decompilation exception** — permitted *solely* to achieve interoperability with independently created programs, subject to strict conditions:
  - Information not previously readily available
  - Confined to parts necessary for interoperability
  - Results cannot be used for competing/similar programs
  - Results cannot be shared except as necessary for interoperability

**Interaction with OSS licensing:**
- The Directive is technology/license-neutral — applies equally to proprietary and OSS.
- OSS licenses operate *within* the Directive's copyright framework, granting additional permissions.
- Where OSS source is available, the decompilation exception is largely moot (information is readily available).
- The Art. 5(3) right to observe/study/test cannot be contracted away — even by a proprietary license, and by extension, this right exists regardless of OSS license terms.
- There is active discussion (2025) about whether the Directive needs updating for AI-generated code and evolving OSS practices.

**Source:** https://eur-lex.europa.eu/eli/dir/2009/24/oj/eng

### 2.3 EU Cyber Resilience Act (CRA) — Regulation (EU) 2024/2847

**Adopted:** December 2024
**Full application:** December 2027 (vulnerability reporting obligations from September 2026)

The CRA is the most significant EU regulation affecting open source since the Software Directive.

**Scope & OSS carve-out:**
- Applies to "products with digital elements" placed on the EU market.
- **Non-commercial OSS is excluded**: If FOSS is distributed without commercial intent (no payment, no personal data exchange), the CRA does not apply to the maintainer/contributor.
- **"Open Source Software Steward"** — new legal category for entities (typically foundations) that systematically manage commercial open source distributions. These face "light-touch" obligations:
  - Cybersecurity policy
  - Vulnerability reporting (severe vulnerabilities within 24 hours)
  - Cooperation with regulatory authorities
  - *Exempt from administrative fines* if nonprofit
- **Commercial integrators** bear full CRA obligations for products incorporating OSS.

**Key concerns for OSS community:**
- Indirect pressure: Downstream commercial users will push compliance requirements upstream to maintainers.
- SBOM requirements will proliferate — commercial vendors must document all OSS components.
- The boundary between "commercial" and "non-commercial" is not always clear (e.g., OSS maintainer who accepts donations, or whose employer benefits commercially).
- Foundations must determine whether they qualify as "stewards."

**Industry response:**
- Heavy lobbying by GitHub, Linux Foundation, Eclipse Foundation, FSFE, and others secured the OSS exemptions.
- OpenSSF developing guidance and training for CRA readiness.
- Open Regulatory Compliance Working Group (ORCWG) tracking implementation: https://orcwg.org/cra/

**Sources:**
- https://digital-strategy.ec.europa.eu/en/policies/cra-open-source
- https://github.blog/open-source/maintainers/what-the-eus-new-software-legislation-means-for-developers/
- https://www.redhat.com/en/blog/eu-cyber-resilience-acts-impact-open-source-security

### 2.4 EU Product Liability Directive (2024/2853)

**Adopted:** Late 2024. Replaces the 1985 Product Liability Directive.

**Major change:** Software (standalone, embedded, and digital files) is now explicitly a "product" subject to strict liability.

**OSS treatment:**
- **Non-commercial FOSS excluded from strict liability**: If distributed without commercial intent and not in exchange for personal data.
- **Commercial integrators bear liability**: If OSS is bundled into a commercial product that causes harm due to a defect, the manufacturer/integrator — not the original OSS developer — is liable.
- **Boundary cases**: If OSS is provided as part of a business activity (paid product, commercial service, or in exchange for personal data used commercially), the exclusion is lost.

**Practical implications:**
- Non-commercial OSS contributors are generally safe from strict product liability.
- Commercial vendors must exercise due diligence on all OSS components — they are responsible for defects regardless of origin.
- Increased pressure for SBOMs, vulnerability tracking, and active maintenance of OSS dependencies.
- Aligns with CRA in creating a "liability chain" that stops at the commercial integrator, not the upstream volunteer.

**Sources:**
- https://eur-lex.europa.eu/eli/dir/2024/2853/oj/eng
- https://www.ibanet.org/European-Product-Liability-Directive-liability-for-software
- https://zenodo.org/records/16211917 (OSS-specific analysis)

### 2.5 FSFE Legal Network & European Legal Infrastructure

**FSFE Legal Network:**
- Network of 400+ legal experts specializing in Free Software law.
- Operates under Chatham House Rule — confidential exchange environment.
- Organizes the annual **Free Software Legal & Licensing Workshop (LLW)** — the world's largest gathering of FOSS lawyers (held in Gothenburg, Sweden).
- 2023–2024 focus areas: AI/ML legal implications, CRA compliance, open data, OSPO governance.

**Key publications and outlets:**
- **JOLTS** (Journal of Open Law, Technology & Society) — successor to IFOSS Law Review (rebranded 2019). Peer-reviewed, open access (CC-BY 4.0). Premier scholarly journal for FOSS legal analysis. https://jolts.world
- **IFOSS Law Review** (2009–2019) — archived at JOLTS. Foundational body of European FOSS legal scholarship.

---

## 3. CHINESE OSS LAW — Rapid Maturation (2021–2025)

China has emerged as a significant jurisdiction for OSS enforcement, with the Supreme People's Court issuing several landmark decisions.

### 3.1 Key Court Decisions

#### Wangjing v. Yibang (Supreme People's Court, 2021, Final Judgment No. 51)

**Facts:** Wangjing Technology built proprietary software on OpenWRT (GPLv2). Former employees copied and modified the software, partnering with Yibang to distribute it.

**Holdings:**
1. Wangjing's copyright in its original contributions recognized *despite* being built on GPL-licensed code.
2. **GPL defense rejected in part**: Even if Wangjing violated GPLv2 by not releasing source, it could still pursue copyright infringement claims against the copiers.
3. Court acknowledged GPL's enforceability — GPL contributors could sue Wangjing separately for non-compliance.
4. **Key principle**: Copyright ownership and OSS license compliance are distinct legal questions.

**English translation:** https://www.ifross.org/sites/default/files/CN_to_EN-Wangjing_vs_Yibang_Judgment%20_2023.pdf
**Analysis:** https://www.ifross.org/?q=node/1676

#### Virtual App (罗盒) Case (2023)

**Holdings:**
1. **GPL3.0 has the force of contract under Chinese law.**
2. Violating GPL terms (failing to release derivative source) triggers automatic license termination.
3. Unlicensed use after termination constitutes copyright infringement.
4. Project lead/primary rights holder does not need explicit authorization from every contributor to sue violators — practical recognition of how OSS projects operate.

**Source:** https://zhuanlan.zhihu.com/p/408916516

#### Changsha Mitop Cases (2022)

**Issue:** Abusive "fishing" litigation — mass lawsuits seeking inflated damages for OSS violations.

**Outcome:** Court reduced damage awards but **affirmed** the legal validity of OSS licenses (GPL, Creative Commons) in China.

### 3.2 Chinese Regulatory & Ecosystem Developments

**Legal framework:**
- OSS licenses enforced under both Chinese Copyright Law and Civil Code (contract law).
- Supreme People's Court has established that GPL is contractual — breach triggers both copyright and contractual remedies.
- OpenAtom Foundation (开放原子开源基金会) — China's primary OSS foundation, maintains a legal database: https://www.openatom.org/law/database

**Governance standards:**
- Ministry of Industry and Information Technology (MIIT) formalized governance metrics for OSS projects (T/CESA 1270.3-2023, T/CESA 1270.5-2023).
- "China's Law-Based Cyberspace Governance in the New Era" (2023 white paper) emphasizes rule-based approach including for OSS.

**Gitee and ecosystem:**
- Gitee (China's primary GitHub alternative) subject to regulatory scrutiny and content review requirements.
- Censorship events (2022–2023) caused community disruption but no mass migration to GitHub due to Great Firewall friction.
- OSS Compass adopted as primary ecosystem evaluation tool (replacing Gitee Index).
- 30M+ OSS projects tracked; 100+ universities with OSS courses.

**Geopolitical context:**
- China frames OSS as critical to national technological sovereignty.
- OSS policies increasingly align with international practices while maintaining stronger government involvement.
- Supply chain security (post-XZ Utils incident) is a major focus.

**Sources:**
- https://kaiyuanshe.github.io/2023-China-Open-Source-Report/en/
- https://blog.fossity.com/limit-open-source-software-licensing-landmark-china/
- https://cssl.socsc.cuhk.edu.hk/2025/05/02/the-impact-of-regulation-on-open-source-development-evidence-from-gitee/

---

## 4. OTHER JURISDICTIONS

### 4.1 Japan

**Legal framework:** Copyright Act + Civil Code (contract law). No specific OSS legislation.

**Court decisions:** No landmark Supreme Court precedents on OSS license enforcement. Disputes resolved using standard copyright/contract principles. Courts recognize OSS licenses as binding agreements.

**Policy:**
- No unified national OSS mandate, but METI (Ministry of Economy, Trade and Industry) and the Digital Agency promote OSS.
- IPA (Information-technology Promotion Agency) published 2024 Open Source Promotion Report recommending national OSS strategy.
- Gap between strong private-sector adoption and limited government-led OSS mandates.
- Tokyo metropolitan government independently promoting OSS for digital transformation.
- IPA provides "OSPO Starter Kit" and compliance guidance.

**Sources:**
- https://www.ipa.go.jp/digital/kaihatsu/oss/about/report2024/index.html
- https://interoperable-europe.ec.europa.eu/sites/default/files/inline-files/OSS%20Country%20Intelligence%20Report%20Japan.pdf

### 4.2 India

**Legal framework:** Indian Copyright Act, Patent Act, IT Act. OSS licenses operate as contracts under general IP law.

**Policy:**
- "Policy on Adoption of Open Source Software for Government of India" under Digital India initiative — government must consider OSS as preferred option for all new e-Governance solutions.
- 2025 NLSIU/FOSS United report recommends mandating OSS in public procurement.

**Litigation:**
- No landmark OSS license enforcement cases comparable to German precedent.
- SFLC India (Software Freedom Law Center, India) litigates primarily on indirect issues: government app bans affecting FOSS, content blocking, intermediary liability.
- Most OSS-related litigation centers on government digital policy effects rather than license enforcement per se.
- Permissive licenses (MIT, Apache, BSD) increasingly favored; copyleft licenses (GPL, AGPL) approached with caution.

**Sources:**
- https://www.meity.gov.in/static/uploads/2024/05/policy_on_adoption_of_oss.pdf
- https://sflc.in/litigation-tracker-old/
- https://www.nls.ac.in/news-events/nlsiu-releases-report-on-the-rise-of-foss-in-india/

### 4.3 Brazil

**Legal framework:**
- Software Protection Act (Law No. 9.609/98) — governs licensing and protection.
- Copyright Act (Law No. 9.610/98) — general copyright.
- Software copyright infringement can trigger both civil and criminal proceedings.

**Policy:**
- Since 2003, government has prioritized OSS for public sector: reduce costs, promote digital inclusion, ensure technological autonomy.
- Agencies instructed to prefer OSS, promote interoperability, avoid vendor lock-in.
- Proposals for laws requiring exclusive government use of OSS — more advanced than most jurisdictions.

**Litigation:** High litigation culture with frequent preliminary injunctions. Courts recognize OSS licenses may conflict with traditional licensing, requiring nuanced interpretation. No landmark GPL enforcement case analogous to German precedent.

**Broader framework:** Marco Civil da Internet (internet civil rights), LGPD (data protection), ongoing AI regulation debates create pro-openness regulatory environment.

**Sources:**
- https://link.springer.com/content/pdf/10.1007/978-3-319-21560-0_3 (Springer, FOSS in Brazil)
- https://www.timreview.ca/article/250

### 4.4 South Korea

**Legal framework:**
- Software Promotion Act + Enforcement Decree — general regulatory environment.
- No dedicated OSS compliance law. Organizations observe international OSS licenses under general IP law.
- MSIT (Ministry of Science and ICT) + NIPA (National IT Industry Promotion Agency) drive OSS policy.

**Policy:**
- "Open Source Software Invigoration Plan" — primary OSS policy initiative.
- Public sector projects increasingly mandate OSS license compliance, attribution, and code-sharing.
- AI Basic Act (2025) may affect open source AI deployment and monitoring.

**Enforcement:** Sector-specific regulations (finance, healthcare) require robust supply chain management including OSS components. No reported landmark OSS license enforcement litigation.

**Sources:**
- https://interoperable-europe.ec.europa.eu/sites/default/files/inline-files/OSS%20Country%20Intelligence%20report_KR.pdf
- https://elaw.klri.re.kr/eng_mobile/viewer.do?hseq=62266&type=sogan&key=54

---

## 5. CROSS-BORDER ENFORCEMENT

### 5.1 Choice of Law

OSS licenses rarely specify governing law. This creates significant uncertainty:

- **GPL/LGPL**: No choice of law clause. GPLv3 contains a limited jurisdiction reference (FSF as steward) but no explicit governing law provision.
- **Apache 2.0, MIT, BSD**: Silent on governing law.
- **MPL 2.0**: Unusual in specifying California law for disputes with the initial developer.

**In practice:**
- Courts apply the copyright law of the country where protection is sought (lex loci protectionis) — the standard approach under the Berne Convention and most national conflict-of-laws rules.
- Contract claims (license breach) may follow different conflict rules — in the EU, Rome I Regulation may apply, often pointing to the law of the party performing the characteristic obligation.
- Result: The same license violation can be analyzed under different substantive law depending on where suit is filed.

### 5.2 Jurisdictional Challenges

- No harmonized international mechanism for software license enforcement.
- Determining which court has jurisdiction is rarely straightforward when parties are on different continents.
- Even if judgment obtained in one country, enforcement in another may require additional proceedings.
- Some jurisdictions require license agreements to be registered, translated, or follow specific formalities.

### 5.3 Practical Strategies

- **Explicit governing law and dispute resolution clauses** in contributor agreements and commercial license terms (even if upstream OSS license is silent).
- **International arbitration** may offer more predictable and enforceable outcomes than litigation for cross-border disputes.
- **Community standards and voluntary compliance** (OpenChain, Kernel Enforcement Statement) reduce the need for formal cross-border enforcement.
- **TRIPS and Berne Convention** provide baseline mutual recognition but do not harmonize procedures or substantive OSS-specific law.

### 5.4 The Enforcement Gap

**Key insight:** There is a fundamental mismatch between the global nature of OSS distribution and the territorial nature of copyright enforcement. Most OSS enforcement has succeeded in Germany precisely because one jurisdiction was chosen and the defendants had a German nexus. Cross-border enforcement of OSS licenses against parties with no local presence remains largely theoretical.

**The practical reality is that OSS compliance is driven more by:**
- Industry norms and community pressure (OpenChain, SPDX)
- Supply chain requirements from commercial customers
- Reputational risk
- Community governance mechanisms (Kernel Enforcement Statement)

...than by cross-border litigation, which remains expensive, unpredictable, and jurisdiction-specific.

---

## 6. KEY INTERNATIONAL COMMENTATORS & PUBLICATIONS

### 6.1 Dr. Till Jaeger (JBViniol, formerly JBB Rechtsanwälte, Berlin)

- Co-founder, ifrOSS (Institute for Legal Issues of Free and Open Source Software)
- Lead attorney for gpl-violations.org enforcement actions
- Participated in GPLv3 drafting process
- Co-author (with Axel Metzger): "Open Source Software – Rechtliche Rahmenbedingungen der Freien Software" (5th ed.)
- Co-author: "The International FOSS Law Book"
- Presentation: "GPL Enforcement and License Compliance in Europe" (Linux Foundation, 2013)
- Profile: https://jbviniol.de/en/lawyer/till-jaeger/

### 6.2 Andrew Katz (Moorcrofts LLP / Orcro Limited, UK)

- Joint Managing Partner and Head of Technology, Moorcrofts LLP
- CEO, Orcro Limited (OSS compliance)
- Qualified in UK and Ireland; former software developer
- Co-author: "Open Source Law, Policy and Practice" (OUP, 2022)
- Lead author: EU Commission study "The Impact of Open Source Software and Hardware on Technological Independence, Competitiveness and Innovation in the EU Economy" (2021) — key policy input for EU OSS legislation
- Drafted Solderpad Hardware License; key drafter of CERN Open Hardware Licence
- OpenChain UK Work Group chair
- Visiting scholar, University of Skövde, Sweden
- Regular speaker at EU Open Source Policy Summit
- Google Scholar: https://scholar.google.com/citations?user=S-ZwHAoAAAAJ

### 6.3 JOLTS / IFOSS Law Review

- **IFOSS L. Rev.** (2009–2019): Founded by FSFE Legal Network experts. Peer-reviewed, open access. First dedicated scholarly journal for FOSS legal issues.
- **JOLTS** (2019–present): Rebranded/expanded successor. Covers FOSS, open standards, open science, open data, open governance. CC-BY 4.0. Rolling publication. https://jolts.world
- Notable recent article: "Opposing the Monetization of Linux: McHardy v. Geniatech" — https://www.jolts.world/index.php/jolts/article/view/128

### 6.4 ifrOSS (Institute for Legal Issues of Free and Open Source Software)

- German research institute co-founded by Till Jaeger
- Maintains comprehensive collection of OSS legal materials and case law
- Published English translations of Chinese court decisions (e.g., Wangjing v. Yibang)
- https://www.ifross.org/

### 6.5 FSFE (Free Software Foundation Europe)

- Legal Network (400+ experts)
- Annual Legal & Licensing Workshop (LLW) — Gothenburg, Sweden
- Legal support activities and compliance assistance
- https://fsfe.org/activities/ln/
- https://fsfe.org/activities/legal.html

### 6.6 OpenChain Project (Linux Foundation)

- ISO/IEC 5230:2020 — international standard for OSS license compliance
- ISO/IEC 18974 — standard for OSS security assurance
- Provides framework for organizational compliance programs
- Self-certification and third-party conformance options
- https://www.openchainproject.org/

---

## 7. COMMUNITY ENFORCEMENT FRAMEWORKS

### 7.1 Linux Kernel Enforcement Statement (2017)

Adopted by hundreds of kernel contributors. Key principles:
1. **Cure period**: Violators who correct non-compliance promptly after notification get license reinstated (adopting GPLv3 cure provisions for GPLv2-licensed kernel code).
2. **Compliance as goal**: Enforcement aims for compliance, not punishment.
3. **Legal action as last resort**: All other avenues must be exhausted first.
4. **Community benefit over individual lawsuits**: Discourages actions for personal financial gain.
- https://docs.kernel.org/process/kernel-enforcement-statement.html

### 7.2 Principles of Community-Oriented GPL Enforcement (SFC)

Published by Software Freedom Conservancy, supported by FSF and others:
- Careful verification before making violation claims
- Prioritize user freedoms and community health
- Full transparency and integrity in enforcement
- https://sfconservancy.org/copyleft-compliance/principles.html

### 7.3 GPL Cooperation Commitment

Major companies (Red Hat, IBM, Google, Facebook, Microsoft, Amazon, etc.) committed to extending GPLv3-style cure provisions to GPLv2 violations:
- Violators receive notice and 30-day cure period
- If cured, license reinstated
- Promotes predictability and fairness
- https://gplcc.github.io/gplcc/

---

## 8. SYNTHESIS: KEY THEMES FOR MICROSOFT

### 8.1 Where the Law Is Settled

- GPL is legally enforceable in Germany (copyright + contract), China (contract/copyright), and almost certainly in all Berne Convention jurisdictions.
- Software functionality, programming languages, and data formats are not copyrightable in the EU (SAS v. WPL).
- Distributors (not just manufacturers) bear GPL compliance obligations (Fantec).
- Non-commercial OSS contributors are largely shielded from EU product liability and CRA obligations.

### 8.2 Where the Law Remains Unsettled

- **Derivative work scope under GPL**: No court has ruled on the shim layer / dynamic linking / kernel module question (Hellwig v. VMware was dismissed on procedure).
- **Cross-border enforcement mechanisms**: No harmonized international approach.
- **"Commercial" vs. "non-commercial" boundary** under CRA and Product Liability Directive — many edge cases unresolved.
- **OSS license as contract vs. bare license** — different characterizations in different jurisdictions with different remedial consequences.

### 8.3 Practical Takeaways

1. **Germany remains the enforcement venue of choice** — favorable procedures, developed case law, experienced practitioners.
2. **China is now a real enforcement jurisdiction** — Supreme People's Court has affirmed GPL enforceability with sophistication.
3. **Community governance mechanisms** (Kernel Enforcement Statement, GPL Cooperation Commitment, OpenChain) are more effective than litigation for driving compliance at scale.
4. **The EU regulatory wave** (CRA + Product Liability Directive) will create significant indirect compliance pressure on OSS maintainers through downstream commercial users.
5. **India, Japan, South Korea, Brazil** — strong policy support for OSS but limited enforcement precedent. Compliance driven by industry norms rather than litigation.
