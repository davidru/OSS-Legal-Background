# AI and Open Source Software: Legal Issues Knowledge Base

**Last Updated:** January 2026
**Scope:** Comprehensive analysis of legal issues at the intersection of AI and open source software, including definitions, copyright, licensing, litigation, regulation, and key commentary.

---

## 1. OPEN SOURCE AI DEFINITION

### 1.1 OSI's Open Source AI Definition (OSAID)

**Status:** OSAID v1.0 released October 2024 by the Open Source Initiative.

**Core Requirements for "Open Source AI":**
- **Transparency:** Sufficiently detailed information about model design, especially training data origin, collection, processing, and access/licensing—enough for skilled individuals to substantially recreate the model
- **Code Availability:** Complete source code (data processing, model training) under OSI-approved open source licenses
- **Parameters/Weights:** Access to model weights and intermediate artifacts under "OSI-approved terms"
- **Four Freedoms:** Users can freely use, study, modify, and share the system for any purpose

**Critical Limitation:** OSAID does **not** mandate that all training data be made public—only that enough detail is shared to enable recreation. This is the single most controversial design choice.

**Adoption:** Referenced by Mozilla, Eclipse Foundation, and the Digital Public Goods Alliance. OSI lacks enforcement power—relies on community norms and exposure of "open-washing."

**Sources:**
- TechCrunch, "We finally have an 'official' definition for open source AI" (Oct 2024): https://techcrunch.com/2024/10/28/we-finally-have-an-official-definition-for-open-source-ai/
- InfoQ, "OSI Releases New Definition for Open Source AI" (Nov 2024): https://www.infoq.com/news/2024/11/open-source-ai-definition/
- ZDNET, "We have an official open-source AI definition now, but the fight is far from over": https://www.zdnet.com/article/we-have-an-official-open-source-ai-definition-now-but-the-fight-is-far-from-over/
- OSI blog, "Report from OSS EU 2025: What's next for OSAID": https://opensource.org/blog/report-from-oss-eu-2025-and-ai_dev-whats-next-for-osaid

### 1.2 OSAID Controversy and Criticism

**Software Freedom Conservancy (Bradley Kuhn, Oct 2024):**
- OSAID "erodes the meaning of open source"
- Without training data access, the community cannot fully inspect, audit, or improve AI systems
- OSI's drafting process was rushed and overly influenced by commercial interests
- The rationale that "no existing AI system could currently meet" open data criteria is a capitulation, not a compromise

**Bruce Perens (co-author of the original Open Source Definition):**
- Training data exclusion creates a "data barrier" perpetuating dominance of large organizations
- Labeling proprietary-data AI as "open source" waters down the established meaning
- Privacy concerns: if using an "open" AI means user inputs become public contributions, that's incompatible with real-world expectations
- Proposed alternative: the **"Post-Open" framework** (see Section 1.5)

**Amanda Brock (OpenUK CEO):**
- A separate AI definition is unnecessary and harmful
- Creates confusion and undermines the existing Open Source Definition

**Free Software Foundation:**
- OSAID does not align with the four freedoms central to free software
- Users don't get meaningful control over AI systems under OSAID

**Sources:**
- SFC blog, "Open Source AI Definition Erodes the Meaning of 'Open Source'" (Oct 31, 2024): https://sfconservancy.org/blog/2024/oct/31/open-source-ai-definition-osaid-erodes-foss/
- FOSS Force, "Avoiding OSAID: Brock and Perens Reflect on a Year of Open Source AI Debate" (Sep 2025): https://fossforce.com/2025/09/avoid-osaid-brock-and-perens-reflect-on-a-year-of-open-source-ai-debate/
- The New Stack, "The Case Against OSI's Open Source AI Definition": https://thenewstack.io/the-case-against-osis-open-source-ai-definition/
- Slashdot, "New 'Open Source AI Definition' Criticized for Not Opening Training Data" (Nov 2024): https://news.slashdot.org/story/24/11/03/0257241/new-open-source-ai-definition-criticized-for-not-opening-training-data

### 1.3 Meta's LLaMA License Controversy

**Key Facts:**
- Meta markets LLaMA models as "open source" but uses custom community licenses
- OSI has explicitly stated: "Meta's LLaMA license is still not Open Source"
- Restrictions increase with each version (Llama 2 → 3 → 4)

**Notable Restrictions Across Llama Versions:**
- Commercial use limited for companies with >700 million monthly active users
- Mandatory "Built with Meta Llama" attribution on derivative products
- Certain application restrictions (biometric surveillance, unlawful content)
- Llama 4: EU users reportedly excluded without clear explanation
- Restrictions against circumventing safety/usage controls
- Compliance with biological and chemical weapons laws

**2025 Shift:** Zuckerberg signaled Meta may not open-source "superintelligent" models at all, citing safety, regulatory, and business concerns. Marks a significant retreat from earlier open rhetoric.

**Sources:**
- OSI blog, "Meta's LLaMa license is still not Open Source": https://opensource.org/blog/metas-llama-license-is-still-not-open-source
- TechCrunch, "Zuckerberg signals Meta won't open source all of its 'superintelligence' AI models" (Jul 2025): https://techcrunch.com/2025/07/30/zuckerberg-says-meta-likely-wont-open-source-all-of-its-superintelligence-ai-models/
- ITProToday, "Meta's Llama LLMs Spark Debate Over Open Source AI": https://www.itprotoday.com/it-operations/meta-s-llama-llms-spark-debate-over-open-source-ai

### 1.4 The Spectrum of AI Model Licensing

| Category | Examples | Key Characteristics |
|----------|----------|-------------------|
| **Fully Open Source** (OSI-style) | Rare; small/academic models only | Apache 2.0 or MIT, no field-of-use restrictions |
| **Open Weights + Responsible Use** | DeepSeek, Falcon, BLOOM | Downloadable weights, commercial use OK, but prohibited uses (military, surveillance, discrimination). Derivatives must carry restrictions |
| **Open Weights + Commercial Thresholds** | Meta Llama, Mistral (larger models) | Open for smaller-scale/non-commercial; revenue/user thresholds require separate licensing |
| **API-Only / Proprietary** | OpenAI GPT, Anthropic Claude | No self-hosting, all restrictions via ToS |

**Mistral:** Smaller models Apache 2.0; larger models use Mistral Non-Production License (MNPL) or modified MIT with >$20M revenue threshold.

**DeepSeek:** Dual-license: code is MIT; model weights under custom "DeepSeek License" based on OpenRAIL principles. No royalties, but prohibited military/harmful uses.

**Falcon (TII):** Apache 2.0 variant with additional acceptable use policies restricting high-risk applications.

**Sources:**
- SoftwareSeni, "Llama Mistral DeepSeek and Qwen Licence Terms Compared for Commercial Use": https://www.softwareseni.com/llama-mistral-deepseek-and-qwen-licence-terms-compared-for-commercial-use/
- DeepSeek License FAQ: https://deepseeklicense.github.io/
- Mistral help docs on licensing: https://help.mistral.ai/en/articles/347393-under-which-license-are-mistral-s-open-models-available

### 1.5 Bruce Perens' "Post-Open" Framework

**Concept:** Alternative licensing and organizational paradigm to address limitations of OSAID and longstanding open source funding problems.

**Key Features:**
- Developer compensation when work is used by companies above a revenue threshold
- ASCAP-inspired once-a-year audit and payment mechanisms
- Provisions against using covered content to train proprietary AI models
- "Post-Open Zero Cost License" draft released April 2024

**Sources:**
- The Register, "Bruce Perens proposes draft Post-Open Zero Cost License" (Apr 2024): https://www.theregister.com/2024/04/30/bruce_perens_post_open_license/
- The New Stack, "What Comes After Open Source? Bruce Perens Has Some Ideas": https://thenewstack.io/what-comes-after-open-source-bruce-perens-has-some-ideas/
- PostOpen.org: https://postopen.org/press

---

## 2. COPYRIGHT AND AI TRAINING DATA

### 2.1 Can Copyleft Licenses Restrict AI Training?

**Current Legal Status:** No legal consensus or court precedent (as of early 2026) that an AI model trained on GPL code automatically becomes a derivative work.

**Key Arguments:**

*Against GPL propagation to models:*
- Training uses code as input for statistical learning—model parameters don't directly copy code, they extract patterns
- Most copyleft licenses were not designed with AI training in mind (Institute for Information Law, University of Amsterdam study)
- GPL mechanisms focus on copying and distributing source code, not learning from it
- "Derivative work" traditionally means software that incorporates or directly builds on the original's codebase

*For GPL propagation:*
- If AI outputs reproduce GPL code verbatim or near-verbatim, this is almost certainly a derivative
- Free software advocates argue functional equivalency may still trigger copyleft if structure, sequence, and organization are copied
- Concern about "license laundering" through AI technologies

**Risk Assessment:** Medium legal risk. Training itself likely does not trigger GPL obligations on a model, but outputting GPL code or clear derivatives is more dangerous.

**Best Practices:**
- Implement robust filtering to avoid verbatim output of GPL code
- Keep records of training data sources
- If output is "heavily inspired" by GPL code, consider following GPL obligations
- Watch for new licenses with explicit AI training provisions

**Sources:**
- Terms.Law, "Training on open source code: what GPL, MIT and other licenses actually say about AI" (Dec 2025): https://www.terms.law/2025/12/05/training-on-open-source-code-what-gpl-mit-and-other-licenses-actually-say-about-ai/
- Open Future, "The Impact of Share Alike/CopyLeft Licensing on Generative AI": https://openfuture.eu/publication/the-impact-of-share-alike-copyleft-licensing-on-generative-ai/
- Shujisado.org, "The Current State of the Theory that GPL Propagates to AI Models" (Nov 2025): https://shujisado.org/2025/11/27/gpl-propagates-to-ai-models-trained-on-gpl-code/
- arXiv, "An Exploratory Investigation into Code License Infringements in Large Language Model Training Datasets": https://arxiv.org/html/2403.15230v1

### 2.2 Key Litigation

#### Doe v. GitHub (Copilot Litigation)

**Status (early 2026):** Pending in the U.S. Court of Appeals for the Ninth Circuit.

**Procedural History:**
- Filed by anonymous developers against GitHub, Microsoft, and OpenAI
- June 2024: Judge Tigar (N.D. Cal.) dismissed most claims, including DMCA §1202(b) claims—Copilot outputs not shown to be "identical" to protected works
- Limited claims survived: breach of contract related to open-source licenses
- September 27, 2024: Court certified interlocutory appeal to Ninth Circuit on whether DMCA §§1202(b)(1) and (b)(3) require "identicality"
- April 9, 2025: Plaintiffs filed opening brief to Ninth Circuit

**Central Legal Question:** Must AI-generated output be identical to original code for DMCA violation? Federal courts are split.

**Significance:** The Ninth Circuit's ruling will set precedent for copyright, attribution, and OSS license compliance for AI models trained on third-party code.

**Sources:**
- GitHub Copilot Litigation case updates: https://githubcopilotlitigation.com/case-updates.html
- CourtListener docket: https://www.courtlistener.com/docket/69495342/doe-et-al-v-github-inc-et-al/
- JD Supra, "DMCA Question Certified for Appellate Court" (Sep 2024): https://www.jdsupra.com/legalnews/dmca-question-certified-for-appellate-7537654/
- Syracuse Law Review, "Update in Copilot Copyright Claim" (2025): https://lawreview.syr.edu/update-in-copilot-copyright-claim-may-affect-future-challenges-of-artificial-intelligence/

#### New York Times v. OpenAI

**Status:** Active in federal court (S.D.N.Y.); filed December 2023.

**Key Issues:**
- Whether large-scale ingestion of copyrighted works for AI training is fair use
- Fair use factors: transformative purpose vs. commercial use; market substitution effect
- 2025: Unprecedented data preservation order requiring OpenAI to retain all output log data, including deleted chats and API-generated outputs
- Scope of liability for both users and platform providers if AI outputs cross from "inspired by" to "substantially similar"

**Implications for Code:**
- Legal reasoning directly applicable to training code-generation AI on copyrighted code
- If NYT wins, AI companies could be compelled to exclude protected code from training or pay royalties
- May accelerate dataset segmentation: "safe for training" (properly licensed/open source) vs. "risky" (commercial, paywalled)

**Sources:**
- Global Law Today, "The New York Times v. OpenAI and Microsoft: A Pivotal Copyright Battle" (Jun 2025): https://www.globallawtoday.com/law/case-law/2025/06/the-new-york-times-v-openai-and-microsoft-a-pivotal-copyright-battle-in-the-ai-era/
- Harvard Law Review blog, "NYT v. OpenAI: The Times's About-Face" (Apr 2024): https://harvardlawreview.org/blog/2024/04/nyt-v-openai-the-timess-about-face/
- Fordham IPLJ, "The Ongoing Legal Battle: New York Times vs. OpenAI" (Apr 2025): http://www.fordhamiplj.org/2025/04/09/the-ongoing-legal-battle-new-york-times-vs-openai/

#### Thomson Reuters v. Ross Intelligence

**Status:** Summary judgment for Thomson Reuters (February 2025, D. Del., Judge Bibas).

**Holding:** First major U.S. court decision explicitly ruling that training an AI model with copyrighted text from a competitor is **not fair use** as a matter of law.

**Fair Use Analysis:**
1. **Purpose and Character:** Commercial, not transformative—Ross's purpose was to compete with Westlaw
2. **Nature of the Work:** Headnotes contain enough creativity to be protected despite factual components
3. **Amount and Substantiality:** Over 2,000 headnotes copied (via intermediary "Bulk Memos")
4. **Market Effect:** Clear risk of undermining Westlaw's licensing market

**Significance:** Narrow but important—applies most directly to competitive uses. Does not directly address non-competing or transformative uses. ROSS shut down due to litigation costs.

**Sources:**
- National Law Review, "Fair Warning: AI's First Copyright Fair Use Ruling" (Feb 2025): https://natlawreview.com/article/fair-warning-ais-first-copyright-fair-use-ruling-thomson-reuters-v-ross
- DWT, "Thomson Reuters v. Ross Intelligence: Copyright, Fair Use, and AI" (Feb 2025): https://www.dwt.com/blogs/artificial-intelligence-law-advisor/2025/02/reuters-ross-court-ruling-ai-copyright-fair-use
- Authors Alliance, "Thomson Reuters v. Ross: The First AI Fair Use Ruling Fails to Persuade" (Feb 2025): https://www.authorsalliance.org/2025/02/13/thomson-reuters-v-ross-the-first-ai-fair-use-ruling-fails-to-persuade/

#### Andersen v. Stability AI

**Status:** Pending in N.D. Cal. (Judge Orrick); in discovery phase as of early 2026.

**Key Rulings (August 2024):**
- Direct copyright infringement and inducement claims against Stability AI **survived** dismissal
- Court accepted plausible allegation that Stable Diffusion may embed compressed copies of training images
- DMCA claims for distributing false copyright management information **dismissed with prejudice**
- "VCR defense" (tool with many lawful uses) rejected for models built from copyrighted content without permission

**Significance:** Leading test case for visual copyright and generative AI. If artists succeed, AI developers may need to license training data. Principles directly applicable to code.

**Sources:**
- Copyright Alliance, "Takeaways from the Andersen v. Stability AI Copyright Case": https://copyrightalliance.org/andersen-v-stability-ai-copyright-case/
- Expert Institute, "Artists Win Landmark Intellectual Property Case Against AI": https://www.expertinstitute.com/resources/insights/artists-victory-intellectual-property-case-ai-generated-content-companies/
- CourtListener docket: https://www.courtlistener.com/docket/66732129/andersen-v-stability-ai-ltd/

### 2.3 Fair Use Analysis for AI Training on OSS

**Four-Factor Framework Applied to AI Training:**

| Factor | Analysis | Risk Level |
|--------|----------|-----------|
| **Purpose and Character** | Transformative if model creates new outputs; less so if competitive or substitutive | Medium—depends on use case |
| **Nature of the Work** | Code is both functional and creative; functional aspects less protected | Lower for purely functional code |
| **Amount Used** | AI training uses entire corpora—weighs against fair use | Higher risk |
| **Market Effect** | If AI outputs replace demand for original code/libraries, weighs against fair use | Varies by context |

**Key Consideration:** Thomson Reuters v. Ross shows competitive use is high-risk. Non-competitive, transformative uses (e.g., code completion that doesn't reproduce substantial chunks) may fare better, but no court has ruled definitively on code-specific AI training.

---

## 3. AI-GENERATED CODE AND LICENSING

### 3.1 Copyright Office Guidance on AI Authorship

**Core Principle (reaffirmed January 2025):** Copyright protection requires human authorship. AI-generated works where expressive elements are determined by AI are not eligible.

**Key Rules:**
| Scenario | Copyright Protection? | Notes |
|----------|----------------------|-------|
| Purely AI-generated code | **No** | No human creative authorship |
| Human edits, arranges, or modifies AI output | **Yes** (for human parts) | Must be significant, creative contribution |
| Prompts only (even detailed ones) | **No** | Prompts are analogous to broad instructions |
| Mixed work (AI + human) | **Yes** (human portions only) | Must disclose AI use in registration; disclaim AI portions |

**Registration Practices:** Applicants must disclose AI-generated content and describe their own creative contribution.

**Thaler v. Perlmutter (2025):** Court held copyright must originate from a human being, not an autonomous AI system.

**Sources:**
- U.S. Copyright Office AI initiative: https://www.copyright.gov/ai/
- DLA Piper, "Copyrightability of genAI outputs in the US: Key developments" (Mar 2025): https://www.dlapiper.com/en-us/insights/publications/2025/03/copyrightability-of-genai-outputs-in-the-us-key-developments
- Jones Day, "U.S. Copyright Office Analyzes Human Authorship Requirement" (Feb 2025): https://www.jonesday.com/en/insights/2025/02/copyrightability-of-ai-outputs-us-copyright-office-analyzes-human-authorship-requirement
- Congressional Research Service, "Generative Artificial Intelligence and Copyright Law": https://www.congress.gov/crs-product/LSB10922

### 3.2 Can AI-Generated Code Be Licensed Under Open Source Licenses?

**The Paradox:** If AI-generated code is not copyrightable (no human author), then:
- There is nothing to license—the code may be effectively in the public domain
- Open source licenses require copyright to operate (they are copyright licenses with conditions)
- Anyone could use AI-generated code without restriction, which might seem "open" but eliminates the enforceability of copyleft or attribution requirements

**Practical Approach:** When a human meaningfully selects, arranges, edits, or integrates AI-generated code, the human contributions may be copyrightable and licensable. The AI-generated portions may not carry enforceable license obligations.

**Implication for Copyleft:** If AI generates code that resembles GPL-licensed training data:
- If the output is verbatim or near-verbatim: likely a derivative work of the original, subject to GPL
- If the output is sufficiently transformed: may not be a derivative—but the legal line is unclear
- If the output is not copyrightable at all (purely AI-generated): GPL cannot attach because there's no copyright to license
- **Practical risk:** Using AI-generated code that closely tracks GPL code without GPL compliance could expose the user to infringement claims from the original authors

### 3.3 The "Stochastic Parrot" vs. "Transformation" Debate

**Stochastic Parrot Hypothesis (Bender et al., 2021):**
- LLMs do not understand language or meaning—they mimic human patterns probabilistically
- Outputs are statistical recombinations, not genuinely creative works
- **Legal implication:** If models are just parroting, outputs are closer to copies, increasing infringement risk

**Transformation/World Model View:**
- Modern LLMs may develop rudimentary "world models" and combine concepts in novel ways
- Outputs can be genuinely new combinations that stretch the definition of "mere parroting"
- **Legal implication:** If models truly transform input into new expression, fair use arguments strengthen and infringement claims weaken

**Current State:** No court has adopted either theory as dispositive. The debate informs—but does not control—the legal analysis.

**Sources:**
- Bender et al., "On the Dangers of Stochastic Parrots: Can Language Models Be Too Big?" (2021)
- arXiv, "The Dark Side of ChatGPT: Legal and Ethical Challenges from Stochastic Parrots" (2023): https://arxiv.org/abs/2304.14347
- Robometrics AGI, "Generative AI & Law: Diffusion Models are not Stochastic Parrots": https://www.robometricsagi.com/blog/ai-policy/generative-ai-law-diffusion-models-are-not-stochastic-parrots

---

## 4. AI MODEL LICENSING

### 4.1 Apache 2.0 for AI

**Usage:** Common choice for AI model code (not weights). Mistral (smaller models), many Hugging Face projects.

**Advantages:** Maximally permissive; allows commercial use, modification, distribution. Includes patent grant. No field-of-use restrictions.

**Limitation:** Cannot restrict harmful/unethical uses. Not technically designed for model weights or training data (which may not be copyrightable).

### 4.2 Responsible AI Licenses (RAIL)

**Concept:** Licenses designed specifically for AI models, datasets, and code. Include behavioral-use restrictions while allowing access, use, distribution, and adaptation.

**Key Features:**
- Prohibit certain harmful uses (surveillance, weapons, discrimination)
- Restrictions must carry forward to derivatives
- **Not** considered "open source" by traditional definitions (field-of-use restrictions violate OSD)
- Used by: Stable Diffusion, BLOOM, many Hugging Face models

**OpenRAIL Variants:**
- OpenRAIL-M: for model weights
- OpenRAIL-D: for datasets
- OpenRAIL-S: for source code

**IEEE 2840-2024:** New IEEE standard for Responsible AI Licensing, seeking global standardization of RAIL principles.

**Kate Downing's Critique (2023):** "AI Licensing Can't Balance 'Open' with 'Responsible'"—argues the tension is fundamental, not resolvable through license design alone.

**Sources:**
- Licenses.AI (RAIL): https://www.licenses.ai/
- OECD, "Responsible AI licenses: a practical tool for implementing trustworthy AI": https://oecd.ai/en/wonk/rails-licenses-trustworthy-ai
- IEEE 2840-2024: https://ieeexplore.ieee.org/document/10982423
- Kate Downing, "AI Licensing Can't Balance 'Open' with 'Responsible'" (Jul 2023): https://katedowninglaw.com/2023/07/13/ai-licensing-cant-balance-open-with-responsible/

### 4.3 Creative Commons and AI Training

**CC's Position:** Creative Commons is piloting **"CC Signals"**—a standardized way for creators and platforms to declare preferences regarding AI training.

**Current State:**
- CC licenses were not designed with AI training in mind
- No existing CC license explicitly permits or prohibits AI training
- CC is working to balance openness with author control
- "CC Signals" would add metadata/web-based signals indicating whether AI/data mining use is permitted, conditioned, or refused

**Opt-Out Mechanisms (2024–2025):**

| Region | Mechanism | Technical Format |
|--------|-----------|-----------------|
| **EU** | DSM Art. 4, AI Act | Machine-readable (HTML/HTTP/metadata) |
| **UK** | Proposed rights reservation | TBA (consultation ongoing) |
| **US** | No federal standard—case law and licensing focused | Explicit license terms, DMCA takedown |
| **GitHub/Code** | Repo settings, explicit license | Platform opt-out + legal text |
| **Creative Commons** | "CC Signals," license updates | Metadata, site-wide flags (in beta) |

**U.S. Copyright Office (May 2025 Report):** Building AI training datasets from copyrighted works constitutes reproduction—thus infringement—unless covered by fair use or licensing.

**Sources:**
- Creative Commons, "AI and the Commons": https://creativecommons.org/ai-and-the-commons/
- Berkeley Technology Law Journal, "Opt-Out Approaches to AI Training: A False Compromise" (Apr 2025): https://btlj.org/2025/04/opt-out-approaches-to-ai-training/
- Kate Downing, "The Enforceability of AI Training Opt-Outs" (May 2025): https://katedowninglaw.com/2025/05/28/the-enforceability-of-ai-training-opt-outs/
- Copyright Clearance Center, "AI Systems Training License" (2025): https://www.copyright.com/media-press-releases/ccc-announces-ai-systems-training-license-for-the-external-use-of-copyrighted-works-coming-soon/

### 4.4 Model Cards and Documentation Requirements

Emerging norm (not yet legally mandated in most jurisdictions, but required under EU AI Act for certain models):
- Training data provenance and composition
- Model architecture and capabilities
- Intended use cases and limitations
- Evaluation results and known biases
- License terms and permitted/prohibited uses

---

## 5. REGULATORY INTERSECTION

### 5.1 EU AI Act (Regulation 2024/1689)

**Published:** July 12, 2024. Phased implementation through 2025–2026.

**Open Source Provisions:**

**General Exception (Article 2):** AI systems under free/open-source licenses are generally outside scope, **EXCEPT:**
- High-risk AI systems (Articles 6–23)
- Prohibited AI systems (Article 5)
- Individual-user-facing systems

**General-Purpose AI Models (GPAIMs):**
- Open source GPAIMs (all weights/parameters published under free/open license): Some requirements waived (technical documentation, transparency documents)
- **Exception does NOT apply** if the model presents "systemic risk" (large-scale, high-impact)

**Definition of "Open Source":** Recital 102 (non-binding) references software/licenses where users can "freely access, use, modify and redistribute"

**Bottom Line:** The open source exception is quite limited. Most significant regulatory requirements still apply for high-risk or large-scale models, regardless of license.

**Sources:**
- EUR-Lex, Regulation 2024/1689 full text: https://eur-lex.europa.eu/eli/reg/2024/1689/oj/eng
- Orrick, "The EU AI Act: Application to Open-Source Projects" (Sep 2024): https://www.orrick.com/en/Insights/2024/09/The-EU-AI-Act-Application-to-Open-Source-Projects
- ArtificialIntelligenceAct.eu: https://artificialintelligenceact.eu/the-act/

### 5.2 U.S. Executive Orders on AI

**Biden Executive Order 14110 (October 2023):**
- Mandated safety results sharing with government for systems with national security/public health impact
- Required testing for bias, discrimination, security
- Open-source AI in sensitive sectors subject to same risk mitigation as proprietary
- **Repealed January 2025**

**Trump Executive Order 14179 + AI Action Plan (January 2025 – July 2025):**
- Deregulation: Removal of pre-deployment safety testing, mandatory transparency, government review requirements
- Single streamlined federal AI policy, preempting state regulations
- NIST directed to strip guidance about misinformation, DEI, climate from AI governance frameworks
- Favors rapid innovation in both open-source and closed-source domains
- Efforts to challenge state laws (e.g., anti-bias requirements) that might "burden" AI innovation

**Open Source Impact:**
- Fewer formal federal constraints on open source AI → wider adoption but higher risk of unvetted deployment
- Federal procurement requires "unbiased" AI but with vague "neutrality" standards
- State-level AI regulation may be preempted, creating more uniform (and more permissive) federal approach

**Sources:**
- Darrow.AI, "AI Policy in 2025: The Diverging Visions of Biden & Trump": https://www.darrow.ai/resources/federal-ai-policy-biden-trump
- National Law Review, "Trump's AI Executive Order: A Shift Toward Deregulation": https://natlawreview.com/article/key-insights-president-trumps-new-ai-executive-order-and-policy-regulatory
- Orrick, "How Trump's AI Action Plan and Executive Orders Will Impact U.S. Technology" (Aug 2025): https://www.orrick.com/en/Insights/2025/08/How-Trumps-AI-Action-Plan-and-Executive-Orders-Will-Impact-US-Technology-and-Federal-Procurement
- Cato Institute, "Biden, Trump, and AI" (Fall 2025): https://www.cato.org/regulation/fall-2025/biden-trump-ai

### 5.3 International AI Governance and OSS

- **EU:** Most prescriptive approach; AI Act creates tiered obligations with limited OSS exceptions
- **US:** Shifted from oversight-focused (Biden) to deregulation (Trump); no federal OSS-specific AI provisions
- **UK:** Consulting on rights-reservation (opt-out) model for AI training; no comprehensive AI law yet
- **China:** State control emphasis; legal evolution ongoing with specific AI regulations
- Broadly, jurisdictions are diverging on whether and how to regulate AI, with OSS treatment varying significantly

---

## 6. KEY COMMENTARY AND SCHOLARSHIP

### 6.1 Luis Villa

**Position:** One of the most influential voices at the intersection of open source, AI policy, and legal considerations.

**Key Themes (2024–2025):**
- The evolving meaning of "open" in AI—push to clarify how open source ideals apply when infrastructure, data, and models are proprietary or "open-ish"
- Compliance, security, and privacy concerns in burgeoning AI industry
- Blog: "Open+ML: Updates from the jagged frontier" at openml.fyi
- RedMonk interview (Sep 2024): "The AI Compliance Dumpster Fire"—critiqued inconsistent privacy/security practices in AI startups
- Conference talks: "Open in a Regulated Age: Open Source, AI, and the Law in 2024" (Duke); State of Open Conference 2025
- Individual/small-team developers can still have impact in era dominated by large organizations

**Sources:**
- Blog: http://openml.fyi/
- RedMonk, "Luis Villa on the AI Compliance Dumpster Fire" (Sep 2024): https://redmonk.com/blog/2024/09/16/rmc-luis-villa-on-the-ai-compliance-dumpster-fire-and-doing-the-right-thing/
- Duke CS event: https://cs.duke.edu/events/open-regulated-age-open-source-ai-and-law-2024

### 6.2 Heather Meeker

**Position:** Leading open source licensing attorney; author of "Open (Source) for Business" (4th edition 2025).

**Key Themes (2024–2025):**
- Most open source licenses (especially permissive) allow using code for model training—restrictions generally activate on distribution, not use
- Distinguishes input risk (training) from output risk (what AI produces)
- Whether training on copyrighted works is "fair use" remains unsettled
- Stresses critical need for genuine open source AI, not "source available" or "open weights" models with significant restrictions
- Warns against mislabeling restrictive AI as "open source"
- Conference co-chair: PLI "Open Source Software 2024 – From Compliance to Cooperation"
- TED Talk: "Why we need open-source AI"

**Sources:**
- FOSSA blog, "Heather Meeker on AI Coding Assistants and OSS License Compliance": https://fossa.com/blog/heather-meeker-ai-coding-assistants-oss-license-compliance/
- TED Talk: https://www.ted.com/talks/heather_meeker_why_we_need_open_source_ai
- OSA Con 2025, "How Open Source Businesses Will Thrive in the Age of AI": https://osacon.io/sessions/2025/how-open-source-businesses-will-thrive-in-the-age-of-ai/
- BrightTALK, "When 'Open Source' Isn't Open Source": https://www.brighttalk.com/webcast/17752/597834

### 6.3 Pamela Samuelson

**Position:** Leading copyright scholar (UC Berkeley); prolific on AI and fair use.

**Key Works and Positions (2024–2025):**
- "Fair Use Defenses in Disruptive Technology Cases" (UCLA Law Review, 2024)
- "Does Using In-Copyright Works as Training Data Infringe?" (Communications of the ACM, 2025)
- "Thinking About Possible Remedies in the Generative AI Copyright Cases" (2024)
- Upcoming article on feasibility of collective licensing for AI training
- Argues outcomes depend heavily on specific uses and the four fair use factors
- Warns remedies could include statutory damages, mandatory destruction of trained models, or forced regulatory regimes
- Emphasizes that 35+ lawsuits in the U.S. and several internationally are challenging unauthorized use of copyrighted works for AI training
- Transparency about training data helps but won't resolve core disputes

**Sources:**
- Lawfare, "Scaling Laws: AI Copyright Lawsuits with Pam Samuelson": https://www.lawfaremedia.org/article/scaling-laws--ai-copyright-lawsuits-with-pam-samuelson
- CACM, "Does Using In-Copyright Works as Training Data Infringe?": https://cacm.acm.org/opinion/does-using-in-copyright-works-as-training-data-infringe/
- UCLA Law Review (2024): https://www.uclalawreview.org/wp-content/uploads/securepdfs/2024/12/02-Samuelson-No-Bleed.pdf
- Private Law Theory, "Thinking About Possible Remedies" (Apr 2024): https://www.private-law-theory.org/2024/04/11/pamela-samuelson-thinking-about-possible-remedies-in-the-generative-ai-copyright-cases/

### 6.4 Mark Lemley

**Position:** Leading IP scholar (Stanford Law School); prolific on AI and copyright.

**Key Works (2024–2025):**

**"How Generative AI Turns Copyright Law Upside Down"** (Columbia Science & Technology Law Review, Vol. 25, No. 2, 2024):
- Generative AI strains the idea-expression dichotomy and substantial similarity test
- Creativity shifts from generating answers to formulating questions (prompt engineering)
- Current frameworks for assessing infringement may become inadequate
- Courts may need to radically alter longstanding tests

**"Plagiarism, Copyright, and AI"** (with Lisa Larrimore Ouellette, U. Chicago Law Review Online, Oct 2025):
- AI-facilitated plagiarism is a genuine problem but not necessarily copyright infringement
- Copyright limits should not punish mere appropriation of ideas
- Extralegal academic norms need strengthening for attribution in the AI era

**"The Mirage of Artificial Intelligence Terms of Use Restrictions"** (with Peter Henderson, Indiana Law Journal, Vol. 100, Iss. 4, Jun 2025):
- ToU restrictions on AI models are difficult to enforce because model outputs and weights are not ordinarily copyrightable
- Legislative—rather than private—enforcement models are better suited for regulating AI use

**Sources:**
- Columbia STLR: https://journals.library.columbia.edu/index.php/stlr/article/view/12761
- U. Chicago Law Review Online (Oct 2025): https://lawreview.uchicago.edu/sites/default/files/2025-10/Lemley%2C%20Ouellette_Copyright%2C%20Plagiarism%2C%20AI.pdf
- Indiana Law Journal: https://www.repository.law.indiana.edu/ilj/vol100/iss4/2/

### 6.5 Other Notable Commentary and Scholarship

**Kate Downing:**
- "AI Licensing Can't Balance 'Open' with 'Responsible'" (Jul 2023): https://katedowninglaw.com/2023/07/13/ai-licensing-cant-balance-open-with-responsible/
- "The Enforceability of AI Training Opt-Outs" (May 2025): https://katedowninglaw.com/2025/05/28/the-enforceability-of-ai-training-opt-outs/
- PLI CLE co-chair: "Open Source and Machine Learning—Practical Licensing Issues" (Oct 2024): https://katedowninglaw.com/2024/10/22/pli-cle-open-source-and-machine-learning-practical-licensing-issues/

**Bradley Kuhn (Software Freedom Conservancy):**
- "Open Source AI Definition Erodes the Meaning of 'Open Source'" (Oct 2024): https://sfconservancy.org/blog/2024/oct/31/open-source-ai-definition-osaid-erodes-foss/

### 6.6 Significant Law Review Articles (2023–2026)

| Article | Journal | Year | Key Contribution |
|---------|---------|------|-----------------|
| Lemley, "How Generative AI Turns Copyright Law Upside Down" | Columbia Sci. & Tech. L. Rev. | 2024 | Fundamental challenge to idea-expression dichotomy |
| Samuelson, "Fair Use Defenses in Disruptive Technology Cases" | UCLA L. Rev. | 2024 | Historical fair use analysis applied to AI |
| Samuelson, "Does Using In-Copyright Works as Training Data Infringe?" | Communications of the ACM | 2025 | Comprehensive four-factor analysis of AI training |
| Lemley & Ouellette, "Plagiarism, Copyright, and AI" | U. Chi. L. Rev. Online | 2025 | Separating plagiarism from infringement in AI context |
| Lemley & Henderson, "The Mirage of AI Terms of Use Restrictions" | Indiana L.J. | 2025 | Unenforceability of contractual AI restrictions |
| Ard, "Copyright's Latent Space: Generative AI and the Limits of Fair Use" | Cornell L. Rev. | 2025 | Rethinking which "market" copyright protects |
| "AI and Copyright Upgrade" (special issue) | J. Intell. Prop. L. & Practice | 2025 | International perspectives on copyright reform |
| "Copyright Protection for AI-Generated Works" | Asian J. Int'l L. | 2024 | Comparative analysis (Berne Convention, EU, national law) |
| RAND, "AI Impacts on Copyright Law" | RAND Perspectives | 2024 | Policy-focused briefing on copyrightability and TDM |
| ABA, "Generative AI and Copyright Law: Current Trends" | Communications Lawyer | 2025 | Practice-focused litigation and legislative trends |
| Samuelson, "Copyright and AI training data—transparency to the rescue?" | J. Intell. Prop. L. & Practice | 2025 | Limits of transparency as solution |

---

## 7. PRACTICAL RISK MATRIX

| Scenario | Legal Risk | Key Factor |
|----------|-----------|-----------|
| Training AI model on permissively licensed OSS (MIT, Apache) | **Low** | Permissive licenses don't restrict use; fair use arguments strong |
| Training AI model on GPL-licensed code | **Medium** | GPL propagation to models unsettled; output filtering critical |
| AI output reproduces verbatim GPL code | **High** | Almost certainly a derivative work; GPL obligations attach |
| AI output is functionally similar but independently expressed | **Medium-Low** | Unlikely to be derivative unless structure/sequence/organization copied |
| Using AI-generated code in commercial product | **Medium** | Copyright status uncertain; no author = no copyright = no license |
| Competing with training data source | **High** | Thomson Reuters v. Ross—competitive use is not fair use |
| Calling proprietary-restricted model "open source" | **Medium** (reputational) | OSI, SFC, community pushback; regulatory relevance under EU AI Act |

---

## 8. KEY OPEN QUESTIONS (as of early 2026)

1. **Will the Ninth Circuit require "identicality" for DMCA violations in Doe v. GitHub?** This will reshape AI code-generation compliance nationwide.

2. **Does training on copyrighted code constitute fair use?** No definitive ruling for code-specific AI training. Thomson Reuters suggests competitive use is not fair use, but transformative non-competitive use may be different.

3. **Can copyleft propagate through AI models?** No court has ruled. Most legal analysis suggests training alone does not trigger GPL, but the question remains open.

4. **Who owns AI-generated code?** If purely AI-generated, likely no one (not copyrightable). Human-modified portions may be protectable. Creates a paradox for open source licensing.

5. **Will OSAID gain broader acceptance or be superseded?** Community remains divided. Bruce Perens' Post-Open and other alternatives are gaining traction.

6. **How will the EU AI Act's open source exceptions work in practice?** Implementation details and enforcement mechanisms still being developed.

7. **Will new licenses emerge specifically for AI training rights?** CC Signals, CCC AI Systems Training License, and Post-Open are early attempts. Market is moving faster than legal frameworks.

---

*This document is a knowledge base for research and analysis purposes. It reflects the state of law, commentary, and scholarship as of January 2026. This is a rapidly evolving area—verify current status of all litigation and regulatory developments before relying on this analysis.*
