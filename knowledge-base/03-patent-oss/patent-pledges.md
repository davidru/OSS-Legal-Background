# Patent Pledges and Non-Assertion Covenants

> Last updated: 2026-03-15

## Summary

Patent pledges are unilateral commitments by patent holders not to assert their patents against certain activities — typically open source software development or implementation of open standards. Unlike license grants embedded in OSS licenses (which attach to specific code), patent pledges are typically broader, covering entire technology areas or patent portfolios.

The legal enforceability of patent pledges as binding commitments (vs. revocable statements of intent) is an important but largely untested question.

## Key Pledges and Organizations

### Open Invention Network (OIN)
- **Founded:** 2005 by IBM, NEC, Novell, Philips, Red Hat, Sony
- **Model:** Community of 4,100+ organizations that cross-license patents royalty-free for the "Linux System Definition" — a curated, regularly expanded list of core OSS packages (Linux kernel + adjacent ecosystem: cloud-native, IoT, data platforms)
- **Scale:** Over 3 million patents/applications cross-licensed — the largest patent cross-license in history
- **Scope:** The Linux System Definition is updated every 18-24 months, currently covering thousands of packages. AI is notably *excluded* from the current definition.
- **OIN 2.0 (2026):** Introduced tiered annual fees (free for small businesses/individuals; revenue-based for larger organizations)
- **Legal mechanism:** Binding cross-license agreement among members — creates "mutually assured non-aggression"
- **Limitations:** Only protects listed software. Members retain full enforcement rights outside the defined scope.

### Microsoft Patent Pledges
- **Open Specification Promise (OSP) (2006):** Unilateral, irrevocable covenant not to sue anyone implementing covered specifications (Office Open XML, authentication standards, file formats, etc.). Not a license — a legal assurance. Mixed reception: SFLC questioned GPL compatibility if implementations diverge from spec scope.
- **Azure IP Advantage (2017+):** Makes 10,000 Microsoft patents available for Azure customers' legal defense. Includes indemnification for open source components in Azure services. Anti-troll provision: if Microsoft transfers patents to an NPE, those patents cannot be asserted against Azure customers.
- **Microsoft joining OIN (2018):** Significant symbolic and practical shift — Microsoft brought its entire patent portfolio (60,000+ patents) into the OIN cross-license for the Linux System. Represented a historic change in Microsoft's open source posture.

### Red Hat Patent Promise
- **First issued:** 2002; reaffirmed and expanded subsequently
- **Scope:** Commits not to enforce patents against anyone using, developing, or distributing software under recognized open source licenses
- **Character:** Broad unilateral pledge, not limited to specific patents or specific software — applies to any OSS under well-recognized licenses
- **Complementary actions:** Red Hat also participates in OIN and LOT Network

### Google Patent Pledges
- **Open Patent Non-Assertion Pledge (OPN):** Non-assertion pledge for specific patents
- **VP8/VP9 codec patents:** Commits not to assert patent infringement claims against anyone developing, distributing, or using open source software implementing VP8/VP9 codecs (WebM). Software must qualify under the Open Source Definition or Free Software Definition.
- **Defensive termination:** Pledge can be rescinded against anyone who sues Google for patent infringement
- **Character:** Legally binding, irrevocable (absent defensive trigger)

### IBM 500 Patent Pledge (2005)
- **Landmark:** IBM pledged 500 U.S. patents (+ international counterparts) would not be asserted against OSS. Technologies covered: text recognition, image processing, database management, networking.
- **Terms:** Intended to be irrevocable *except* against parties initiating IP-related lawsuits against open source projects (defensive termination).
- **Impact:** Empirical research (ScienceDirect, 2020) showed positive correlation between IBM's pledge and increased OSS startup activity.

### Defensive Organizations

#### LOT Network (License on Transfer)
- Nonprofit alliance (Google, IBM, Red Hat, Canon, SAP, and 2,600+ members)
- **Mechanism:** If a member's patent ends up with a patent troll (NPE), all other LOT members automatically receive a free license to that patent
- **Effect:** Neutralizes the "patent monetization by acquisition" playbook. Critical protection for OSS-heavy companies.

#### Unified Patents
- Challenges the validity of low-quality/overbroad patents through IPR (inter partes review) at the USPTO
- Provides analytics on NPE activity, patent quality, and litigation trends
- Has successfully invalidated numerous software patents used in NPE assertions

## Legal Enforceability

### Theories of Enforceability
1. **Promissory estoppel:** If developers relied on the pledge in creating software, the pledgor may be estopped from revoking
2. **Contractual obligation:** If structured as an offer accepted by use, it may create a binding contract
3. **Equitable estoppel:** A patent holder who publicly pledged may be barred from asserting patents against those who relied
4. **License:** If the pledge uses license language, it creates an irrevocable license

### Uncertainty
- **No significant case law.** Patent pledges have not been tested in court.
- **Revocability.** Unless structured as irrevocable licenses, pledges may theoretically be revocable (though estoppel theories provide protection).
- **Successor obligations.** If a company is acquired or its patents are sold, do the pledges transfer? Generally yes for licenses, uncertain for mere pledges.

## Practical Guidance

1. **OIN membership is the gold standard** for patent peace in the Linux ecosystem. If your company uses or contributes to Linux, OIN membership eliminates significant patent risk.

2. **Structure pledges as irrevocable licenses** to maximize enforceability and minimize ambiguity.

3. **Patent pledges don't eliminate all risk.** They cover the pledgor's patents only. Third-party patents (including patent trolls) are not covered.

4. **Track pledge scope carefully.** Some pledges cover specific patents or technologies, not the entire portfolio. Understand what's covered.

## Sources

- Open Invention Network (openinventionnetwork.com)
- Microsoft Patent Pledge statements
- Red Hat Patent Promise
- Google Open Patent Non-Assertion Pledge
- IBM Patent Pledge (2005)
