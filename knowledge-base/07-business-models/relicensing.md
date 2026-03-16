# Relicensing Controversies

> Last updated: 2026-03-15

## Summary

Relicensing — changing the license of an open source project — has become one of the most contentious issues in the open source ecosystem. A wave of companies have switched from OSI-approved licenses to source-available terms, sparking forks, community backlash, and fundamental debates about open source sustainability and corporate control.

For detailed analysis of the licenses themselves, see [Non-Standard and Source-Available Licenses](../01-license-interpretation/non-standard-licenses.md).

## Key Principles

- Relicensing requires copyright control: either holding all copyrights (via assignment CLAs) or having sufficiently broad CLA grants
- Only *future* distributions are affected — previously distributed code under the old license remains available under those terms
- The community can fork the last version under the old license (and frequently does)
- Relicensing is legally permissible if you hold the copyright; whether it's wise is a separate question
- "Just because you won doesn't mean you won" — winning the legal right to relicense doesn't mean you win the community

## Timeline of Major Relicensing Events

| Year | Company | From | To | Fork Created |
|------|---------|------|----|----|
| 2018 | Redis Labs (modules) | BSD → Commons Clause | RSAL | — |
| 2018 | MongoDB | AGPL → SSPL | SSPL | — |
| 2019 | CockroachDB | Apache 2.0 | BSL 1.1 | — |
| 2021 | Elastic | Apache 2.0 | SSPL/ELv2 | OpenSearch (AWS/LF) |
| 2023 | HashiCorp | MPL 2.0 | BSL 1.1 | OpenTofu (LF) |
| 2023 | Sentry | BSD | FSL (→ Apache 2.0 after 2yr) | — |
| 2024 | Redis | BSD | RSALv2/SSPL | Valkey (LF) |
| 2024 | Elastic | SSPL/ELv2 | AGPL/ELv2 | (OpenSearch continues) |

## The Fork Pattern

When companies relicense, the community (often backed by cloud providers or the Linux Foundation) forks the last open-source version:

- **OpenSearch (2021):** AWS forked Elasticsearch 7.10.2 (Apache 2.0). Now a major LF project.
- **OpenTofu (2023):** Community forked Terraform 1.5.x (MPL 2.0). Hosted by Linux Foundation.
- **Valkey (2024):** Linux Foundation forked Redis 7.2.4 (BSD). Backed by AWS, Google, Oracle.

## Legal Issues

### HashiCorp / OpenTofu IP Dispute
- HashiCorp accused OpenTofu of incorporating code from post-BSL Terraform versions
- OpenTofu denied the claims, asserting all code was independently developed or from pre-BSL versions
- Highlighted the risk of IP contamination claims between the original project and its fork
- No litigation filed; resolved through community process

### Standing to Relicense
- Company must hold copyright (assignment) or have broad enough CLA grants
- Contributors who contributed under the old license retain their rights to those contributions
- DCO-only projects generally *cannot* be relicensed by any single entity (contributions are under the project license only)

## Commentary

### Bruce Perens, "Post-Open" Framework (2024)
- OSI co-founder proposed a new framework acknowledging the gap between open source and proprietary
- Argued that the relicensing trend reflects genuine sustainability problems that the open source community has not adequately addressed

### Open Source Initiative Statements
- Consistently maintains that source-available licenses are not open source
- Companies should not use the term "open source" for source-available products

## Practical Guidance

1. **CLA choice determines relicensing power.** If you want to preserve the option to relicense, you need CLAs with broad grant terms. If you want to prevent relicensing, use DCO.

2. **Fork viability depends on community.** A fork only succeeds if it has sufficient contributors, users, and (often) corporate backing. Not every fork survives.

3. **Relicensing destroys trust.** Even if legally permissible, relicensing from open source to source-available permanently damages community relationships. "Don't go for the jugular — these are repeat players."

4. **The last open-source version persists.** Previously distributed code under the old license cannot be un-distributed. The community will fork.

## Sources

- Various company announcements (MongoDB, HashiCorp, Elastic, Redis, Sentry)
- Linux Foundation project announcements (OpenSearch, OpenTofu, Valkey)
- OSI Board statements on license changes
- Bruce Perens, "Post-Open" proposal (2024)
