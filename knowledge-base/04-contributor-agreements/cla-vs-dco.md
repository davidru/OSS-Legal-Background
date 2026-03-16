# CLAs vs. DCO: Contributor Agreement Models

> Last updated: 2026-03-15

## Summary

When developers contribute code to an open source project, the project needs a mechanism to ensure it has the legal right to distribute those contributions. Two primary models have emerged: Contributor License Agreements (CLAs) and the Developer Certificate of Origin (DCO). Each reflects different philosophical, legal, and practical tradeoffs.

The CLA vs. DCO debate is one of the most actively contested governance questions in open source, touching on corporate control, community trust, contributor friction, and the ability to relicense projects.

## Key Principles

- Both CLAs and DCO address the same problem: ensuring the project has rights to distribute contributed code
- CLAs are agreements (contracts) that grant specific rights to the project or entity
- DCO is a lightweight attestation that the contributor has the right to make the contribution
- The choice affects contributor friction, relicensing flexibility, corporate control, and community trust
- Neither model is inherently "better" — the right choice depends on the project's needs and values

## Contributor License Agreements (CLAs)

### How CLAs Work
A CLA is a legal agreement between the contributor and the project (or the entity managing the project). The contributor grants specific rights — typically a broad copyright license, patent license, and representations about the contribution's originality.

### Types of CLAs
1. **Copyright assignment CLAs** (e.g., FSF, Canonical): Transfer copyright ownership to the entity. The entity becomes the copyright holder.
2. **Copyright license CLAs** (e.g., Apache ICLA, Google CLA): Grant a broad license but contributor retains copyright.
3. **Corporate CLAs (CCLAs)**: Signed by employers to cover all employees' contributions.

### The Apache Model (ICLA/CCLA)
- Individual Contributor License Agreement (ICLA) + Corporate CLA (CCLA)
- Grants Apache a "perpetual, worldwide, non-exclusive, no-charge, royalty-free, irrevocable copyright license" plus patent license
- Does NOT assign copyright — contributor retains ownership
- Widely used as a template by other projects

### Advantages of CLAs
- Clear legal chain of title
- Enables relicensing (if the CLA grants broad enough rights)
- Patent license grant from contributors
- Corporate CLAs ensure employer sign-off
- Defensible in court (written agreement)

### Disadvantages of CLAs
- Contributor friction (signing legal documents deters casual contributors)
- Perceived corporate control (the entity can relicense, but contributors cannot)
- Asymmetry — the entity gets broad rights, contributors get the project license
- Complexity — managing CLA tracking, corporate vs. individual, updates
- Can be used for license changes that harm the community (see relicensing controversies)

## Developer Certificate of Origin (DCO)

### How the DCO Works
The DCO is a lightweight attestation, not a license agreement. Contributors "sign off" on each commit with a `Signed-off-by` line, certifying that they have the right to submit the contribution under the project's license.

### The DCO Text (v1.1)
```
Developer Certificate of Origin
Version 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

### Advantages of DCO
- Minimal contributor friction (just add `Signed-off-by` to commits)
- No legal agreement to sign or manage
- Distributed trust model — consistent with OSS philosophy
- No single entity gains special rights over contributions
- Used by the Linux kernel (the largest OSS project)

### Disadvantages of DCO
- No express patent grant from contributors
- Does not enable relicensing (contributions are under the project's existing license only)
- No employer sign-off mechanism (employer may own the code; employee's DCO may be ineffective)
- Weaker legal chain of title than a CLA
- Harder to enforce — attestation vs. agreement

## The Relicensing Connection

The CLA vs. DCO choice directly affects whether a project can change its license:

- **With CLA (broad license grant):** The entity holding CLA rights can relicense. This is how MongoDB (AGPL → SSPL), HashiCorp (MPL → BSL), and others relicensed.
- **With DCO:** Relicensing requires consent of every contributor (or removal of their contributions). Practically impossible for large projects with many contributors.

The relicensing controversy has made many developers suspicious of CLAs, viewing them as tools for eventual proprietary relicensing.

## Commentary & Analysis

### Bradley Kuhn (SFC) on DCO
- **Key Arguments:** Advocates for DCO over CLA. Argues that CLAs concentrate power in a single entity and enable community-hostile relicensing. The DCO's distributed model better serves community interests.

### Heather Meeker on CLAs
- **Key Arguments:** CLAs provide legal certainty and are sometimes necessary (e.g., for dual licensing business models). The Apache ICLA is a good model. Corporate CLAs address the employer-ownership problem.

### Luis Villa on CLA Reform
- **Key Arguments:** Traditional CLAs are too broad and create asymmetric power. Argues for narrower CLA terms or DCO + supplemental patent grant as a middle path.

## Practical Guidance

1. **DCO is sufficient for most community projects.** If you don't need relicensing flexibility and want maximum contributor participation, DCO is the lighter-weight choice.

2. **CLAs are needed for dual-licensing business models.** If your business model depends on offering both open source and proprietary licenses, you need CLAs that grant you the right to do so.

3. **If using a CLA, use the Apache model.** The Apache ICLA is the best-drafted, most widely understood CLA template. Don't create your own.

4. **Consider the trust signal.** For community-driven projects, requiring CLAs signals corporate control. For corporate-backed projects, CLAs may be expected and accepted.

5. **Automate CLA management.** CLA bot tools (CLA Assistant, etc.) reduce friction by automating the signing process through GitHub/GitLab.

## Open Questions

- **DCO and employer ownership.** If an employee signs the DCO but their employer owns the code (work-for-hire), is the DCO effective? The DCO doesn't address this directly.
- **CLA enforceability for AI-generated contributions.** If a contributor uses AI to generate code, does their CLA certification of originality hold?
- **Middle path: DCO + patent grant.** Some projects are exploring combining DCO with a separate, lightweight patent commitment. Viability is unclear.

## Sources

- Developer Certificate of Origin v1.1 (developercertificate.org)
- Apache Individual Contributor License Agreement v2.0
- FSF Copyright Assignment Agreement
- Bradley Kuhn, SFC publications on DCO
- Heather Meeker, *Open Source for Business* (3rd ed., 2020)
