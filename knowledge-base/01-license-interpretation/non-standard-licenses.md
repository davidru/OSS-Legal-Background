# Non-Standard and Source-Available Licenses

> Last updated: 2026-03-15

## Summary

A growing category of licenses that are not approved by the Open Source Initiative (OSI) but share some characteristics with open source licenses. These include "source-available" licenses that make source code accessible but impose restrictions incompatible with the Open Source Definition — such as limiting commercial use, competitive use, or requiring eventual open-source release after a time delay.

This category has become one of the most contested areas in the open source ecosystem, as several prominent companies have relicensed from OSI-approved licenses to source-available terms, sparking debates about sustainability, community trust, and the definition of "open source" itself.

## Key Principles

- "Source available" ≠ "open source" — the OSI Open Source Definition requires freedom from field-of-use restrictions and non-discrimination
- Companies relicensing from OSS to source-available terms can only do so if they hold all copyrights (or have CLA/assignment authority)
- The relicensing trend reflects tension between OSS sustainability and cloud provider economics
- These licenses may create compliance complexity because they look like OSS but impose additional restrictions

## The Licenses

### Server Side Public License (SSPL) — MongoDB (2018)
- **Type:** Modified AGPLv3 with expanded network-use copyleft
- **Key restriction:** Section 13 requires that anyone offering the software "as a service" must release the complete source code for the entire service stack (management, monitoring, deployment, etc.) under SSPL
- **OSI status:** Not approved — OSI concluded it fails OSD §6 (no discrimination against fields of endeavor) and the copyleft scope is impractically broad
- **Adopted by:** MongoDB, Graylog (later reverted), Elastic (later switched to proprietary + AGPL dual)

### Business Source License (BSL / BUSL) — MariaDB (2013)
- **Type:** Time-delayed open source. Code is source-available with usage restrictions; restrictions automatically expire after a specified period (typically 3-4 years), at which point the code becomes available under a specified open source license (the "Change License")
- **Key feature:** Built-in sunset — every release eventually becomes open source
- **OSI status:** Not approved (usage restrictions during the restricted period)
- **Adopted by:** MariaDB, HashiCorp (Terraform, Vault, etc.), CockroachDB, Sentry, Couchbase

### Elastic License 2.0 (ELv2) — Elastic (2021)
- **Type:** Source-available with competitive-use restriction
- **Key restrictions:** Cannot provide the software as a managed service; cannot circumvent license key functionality
- **OSI status:** Not approved
- **Context:** Elastic relicensed Elasticsearch and Kibana from Apache 2.0 to dual SSPL/ELv2 in 2021 (then to AGPL + ELv2 in 2024)

### PolyForm Licenses — Kyle Mitchell (2019)
- **Type:** Family of standardized source-available licenses with various restriction levels
- **Variants:** PolyForm Noncommercial, PolyForm Small Business, PolyForm Free Trial, PolyForm Internal Use, PolyForm Shield (no competitive use), PolyForm Strict
- **Key feature:** Professional drafting with clear, consistent terms across the family
- **OSI status:** Not approved (intentionally — designed to be source-available, not open source)

### Functional Source License (FSL) — Sentry (2023)
- **Type:** Similar to BSL — source-available with competitive-use restriction that converts to Apache 2.0 or MIT after 2 years
- **Key feature:** Shorter delay period than typical BSL (2 years vs. 3-4)
- **Adopted by:** Sentry, GitButler

### Commons Clause (2018)
- **Type:** Addendum to existing open source licenses adding a commercial restriction
- **Key restriction:** "The Software is provided to you by the Licensor under the License, as defined below, subject to the following condition: Without limiting other conditions in the License, the grant of rights under the License will not include, and the License does not grant to you, the right to Sell the Software."
- **Problems:** Ambiguous scope ("Sell" is broadly defined); confusing when combined with permissive licenses; not a standalone license
- **OSI status:** Not approved; widely criticized for confusion

## The Relicensing Controversy

### Timeline of Major Relicensing Events
1. **2018:** Redis Labs adds Commons Clause to certain Redis modules (later switches to RSAL, then dual RSALv2 + SSPL in 2024)
2. **2018:** MongoDB relicenses from AGPL to SSPL
3. **2019:** Cockroach Labs relicenses from Apache 2.0 to BSL
4. **2021:** Elastic relicenses from Apache 2.0 to dual SSPL/ELv2
5. **2023:** HashiCorp relicenses Terraform and other products from MPL 2.0 to BSL 1.1
6. **2023:** Sentry moves to FSL
7. **2024:** Redis relicenses to dual RSALv2/SSPL

### Community Response — The Fork Pattern
- **OpenSearch** (2021): AWS forked Elasticsearch under Apache 2.0 after Elastic's relicensing
- **OpenTofu** (2023): Linux Foundation project forked Terraform under MPL 2.0 after HashiCorp's relicensing
- **Valkey** (2024): Linux Foundation project forked Redis after Redis Labs' relicensing
- **Pattern:** Major cloud providers or foundations fork the last open-source version, creating a competing project

## Commentary & Analysis

### Heather Meeker, "The Open Source Alternative" and related writing
- **Key Arguments:** Source-available licenses serve a legitimate market need. Companies that built businesses on open source need sustainable revenue models. The BSL's time-delay mechanism is an elegant compromise.

### Kyle Mitchell, "PolyForm Project" and blog writing
- **Key Arguments:** The gap between open source and proprietary is too wide. Source-available licenses provide a middle ground. Standardized source-available terms (PolyForm) are better than ad hoc restrictions.

### Bruce Perens (OSI co-founder), Various statements (2023-2024)
- **Key Arguments:** Source-available licenses that restrict commercial use are not open source and should not be called open source. The relicensing trend threatens the open source ecosystem.

### Open Source Initiative, Official Positions
- **Key Arguments:** SSPL, BSL, ELv2, and Commons Clause are not open source licenses. Companies using these licenses should not describe their software as "open source." The Open Source Definition's prohibition on field-of-use restrictions is a core principle, not a technicality.

## Practical Guidance

1. **Don't call source-available "open source."** Using these licenses is a legitimate business choice, but mislabeling them erodes trust and causes confusion.

2. **Compliance complexity.** These licenses often have restrictions that look simple but are hard to apply in practice ("competitive use," "as a service," "sell"). Review carefully with counsel.

3. **Dependency risk.** If your project depends on source-available software, understand that you may face usage restrictions that open source dependencies do not impose.

4. **Relicensing risk for contributors.** If you contribute to a CLA-governed project, the company may relicense your contributions under non-open-source terms. Understand the CLA before contributing.

5. **Fork viability.** The last open-source version of relicensed projects can be forked. Evaluate whether the fork has sufficient community support and investment to be viable long-term.

## Open Questions

- **"As a service" scope.** SSPL's Section 13 requires disclosure of the entire service stack. What exactly constitutes the service stack? No court has tested this.
- **BSL "Additional Use Grant" scope.** BSL permits the licensor to grant additional usage rights. The scope and interpretation of these grants varies by adopter.
- **Competition with forks.** Can a company that relicensed use trademark or patent claims against the open-source fork? The OpenTofu/HashiCorp dispute touched on this.
- **EU implications.** How do source-available restrictions interact with EU competition law and digital markets regulation?

## Sources

- Server Side Public License v1 (2018)
- Business Source License 1.1 (2013/2017)
- Elastic License 2.0 (2021)
- PolyForm Project (polyformproject.org)
- Functional Source License 1.1 (2023)
- OSI Board statements on SSPL and related licenses
- Heather Meeker, various publications
- Kyle Mitchell, writing.kemitchell.com
