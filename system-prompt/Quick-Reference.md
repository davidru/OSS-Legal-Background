# Virtual OSS Attorney — Quick Reference

## Top 10 Things Everyone Should Know About Open Source Law

1. **Open source licenses are enforceable.** Courts in the US, Germany, and China have all confirmed this. Jacobsen v. Katzer (Fed. Cir. 2008) is the foundational US case.

2. **"Free" doesn't mean "no obligations."** Even permissive licenses (MIT, BSD) require attribution. Copyleft licenses (GPL) require providing source code when you distribute the software.

3. **The derivative works question is unresolved.** Does linking to a GPL library make your program a derivative work? The FSF says yes; many practitioners say no for dynamic linking. No court has decided this.

4. **API reimplementation is protected.** After Oracle v. Google (SCOTUS 2021), reimplementing APIs for interoperability has strong fair use support.

5. **Copyleft is triggered by distribution, not use.** Running GPL software on your servers (SaaS) generally doesn't trigger source code obligations. AGPL changes this for network use.

6. **Patent grants vary by license.** Apache 2.0 has an express patent grant. MIT/BSD do not. GPLv3 does; GPLv2 does not. This matters for patent risk.

7. **CLAs vs. DCO determines who controls the project.** CLAs enable relicensing; DCO prevents it. This has driven major forks (OpenTofu, Valkey, OpenSearch).

8. **Source-available ≠ open source.** SSPL, BSL, and Elastic License are NOT open source by the OSI definition. Using these licenses is legitimate, but calling them "open source" is not.

9. **Compliance is achievable.** Most open source compliance boils down to: preserve notices, provide source code (if copyleft), and don't violate additional restrictions. Build it into your process.

10. **When in doubt, ask a lawyer.** This knowledge base is educational. Real legal questions deserve real legal counsel.

---

## Common Questions — Quick Answers

### "Can I use GPL code in my proprietary product?"
You can USE it (run it on your servers). You cannot DISTRIBUTE a combined work without complying with GPL terms (providing source code, licensing under GPL). Consider using the GPL code as a separate service communicating via API, or use an LGPL/permissive alternative.

### "Do I need to open-source my code if I use MIT-licensed code?"
No. MIT is permissive. You must preserve the copyright notice and license text. You do NOT need to release your source code.

### "What's the difference between GPL and AGPL?"
GPL copyleft is triggered by distribution (giving copies to others). AGPL adds network copyleft — if users interact with modified AGPL software over a network, you must provide source code.

### "Can I change the license of my open source project?"
Only if you hold all copyrights (or have CLAs granting broad enough rights). If you used DCO, relicensing requires consent of every contributor.

### "Is it safe to use AGPL-licensed software?"
It depends on how you use it. Running unmodified AGPL software as a service has minimal risk. Modifying it and deploying it for network use triggers source code obligations. Many companies ban AGPL as a precaution.

### "Does AI training on GPL code create obligations?"
Unresolved. No court has addressed this. The "derivative work" and "fair use" analyses both apply but in novel ways. This is one of the biggest open questions in OSS law.

---

## Key Cases — One-Line Summaries

| Case | One-Line Summary |
|------|-----------------|
| **Jacobsen v. Katzer** (Fed. Cir. 2008) | OSS license conditions are enforceable copyright conditions |
| **Oracle v. Google** (SCOTUS 2021) | API reimplementation can be fair use |
| **Artifex v. Hancom** (N.D. Cal. 2017) | GPL enforceable as both copyright license AND contract |
| **Computer Associates v. Altai** (2d Cir. 1992) | AFC test for non-literal software infringement |
| **Wallace v. IBM** (7th Cir. 2006) | Open source licensing is pro-competitive |
| **Alice v. CLS Bank** (SCOTUS 2014) | Abstract software ideas on generic computers are not patentable |
| **Hellwig v. VMware** (Germany, 2016-19) | GPL derivative works question — dismissed on procedure, unresolved |
| **SAS v. WPL** (CJEU 2012) | Software functionality and languages are not copyrightable |

---

## License Quick Reference

| License | Type | Copyleft | Patent Grant | Key Feature |
|---------|------|----------|-------------|-------------|
| MIT | Permissive | No | No (implied?) | Simplest; most popular |
| BSD-2 | Permissive | No | No | Minimal conditions |
| Apache 2.0 | Permissive | No | Yes + retaliation | Best for patent protection |
| GPLv2 | Strong copyleft | Yes (distribution) | No | Linux kernel license |
| GPLv3 | Strong copyleft | Yes (distribution) | Yes | Anti-tivoization + patent |
| AGPL | Strong copyleft | Yes (network use) | Yes | SaaS copyleft |
| LGPL | Weak copyleft | Library modifications | Varies | For libraries |
| MPL 2.0 | Weak copyleft | File-level | Yes | GPL-compatible |
| EPL 2.0 | Weak copyleft | Module-level | Yes | Eclipse ecosystem |
| SSPL | Source-available | Extreme | N/A | NOT open source (OSI) |
| BSL | Source-available | Time-limited | N/A | NOT open source (until conversion) |
