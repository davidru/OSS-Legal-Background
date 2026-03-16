# Open Source Foundation Models

> Last updated: 2026-03-15

## Summary

Open source foundations provide governance infrastructure for collaborative software projects. They serve as neutral homes for IP, provide legal protection (including indemnification) for contributors, and establish governance frameworks that enable participation by competing companies. The choice of foundation — or whether to use one at all — has significant legal and strategic implications.

## Key Principles

- Foundations serve as neutral IP holding entities, reducing single-company control risk
- Most foundations are US 501(c)(6) business leagues (not charities) — member-funded, not donor-funded
- Foundation governance models range from corporate-controlled to community-driven
- The foundation's IP policy (who owns what, how it's licensed) is the most legally consequential element
- "Joining a foundation is like joining a gym — you get to use the equipment, but you're not responsible for the gym itself"

## Major Foundations

### Apache Software Foundation (ASF)
- **Structure:** 501(c)(3) charitable organization (unusual — most foundations are 501(c)(6))
- **IP model:** Apache License 2.0 for all projects; Individual CLA (ICLA) + Corporate CLA (CCLA)
- **Governance:** Merit-based. Projects self-govern with elected PMC (Project Management Committee). "Community over code" philosophy.
- **Key feature:** All projects must use Apache License 2.0 — no copyleft
- **Significance:** One of the oldest and most respected foundations. Home to 350+ projects.

### Linux Foundation (LF)
- **Structure:** 501(c)(6) business league
- **IP model:** Varies by project — LF hosts projects under many different licenses. Each project defines its own IP policy.
- **Governance:** Federated model. Individual projects have significant autonomy. LF provides infrastructure, legal, marketing, and event support.
- **Joint Development Foundation (JDF):** Template for creating new projects with standardized governance
- **Key feature:** Largest foundation ecosystem. Hosts Linux kernel, Kubernetes, Node.js, CNCF, OpenTofu, and hundreds more.
- **Significance:** The dominant foundation for corporate-backed open source.

### Eclipse Foundation
- **Structure:** Belgian AISBL (international nonprofit) since 2021 (formerly US 501(c)(6))
- **IP model:** Eclipse Public License 2.0 (default) with option for other licenses. Eclipse Contributor Agreement (ECA).
- **Governance:** Specification process (Eclipse Foundation Specification Process) enables creating standards alongside code.
- **Key feature:** Strong European presence. Moved to Brussels partly for EU regulatory proximity.
- **Significance:** Home to Jakarta EE, MicroProfile, and automotive (Eclipse SDV) projects.

### Open Source Initiative (OSI)
- **Structure:** 501(c)(3) charity
- **Role:** License stewardship — maintains the Open Source Definition and approves licenses as "open source"
- **Does not host projects** — focused on license standards and advocacy
- **Key feature:** The authoritative body for what constitutes an "open source" license
- **Current controversy:** Open Source AI Definition (OSAID) debate

### Free Software Foundation Europe (FSFE)
- **Structure:** German nonprofit (Verein)
- **Role:** Advocacy, legal support, compliance assistance in Europe
- **Key feature:** European Legal Network (400+ FOSS lawyers); REUSE initiative for license compliance
- **Significance:** Key voice in EU regulatory processes (CRA, Product Liability Directive)

## Governance Models Compared

| Feature | Apache | Linux Foundation | Eclipse |
|---------|--------|-----------------|---------|
| Legal structure | 501(c)(3) | 501(c)(6) | Belgian AISBL |
| License policy | Apache 2.0 only | Project chooses | EPL 2.0 default |
| CLA model | ICLA + CCLA | Varies (often DCO) | Eclipse Contributor Agreement |
| Membership dues | Sponsorship-based | Tiered corporate | Tiered corporate |
| Project autonomy | High (PMC model) | Very high | Moderate (spec process) |
| Specification capability | No | JDF provides this | Yes (built-in) |

## Practical Guidance

1. **Foundation choice depends on your needs.** Apache for community-driven development under permissive terms. LF for corporate-backed projects needing flexible licensing. Eclipse for specification-adjacent work.

2. **IP policy is the most important factor.** Before joining or hosting a project, understand the foundation's IP policy — who owns contributions, what licenses are used, and what patent commitments apply.

3. **Foundations cost money.** Membership dues range from free (individual/small company) to hundreds of thousands of dollars (platinum/founding members of LF projects).

4. **Governance protects against forks.** Good foundation governance reduces the risk of community fragmentation. "The best way to avoid forking is to allow forking."

## Sources

- Apache Software Foundation, Governance documentation (apache.org)
- Linux Foundation, Charter and Governance (linuxfoundation.org)
- Eclipse Foundation, Governance documents (eclipse.org/org)
- Open Source Initiative (opensource.org)
