# Open Core Business Model

> Last updated: 2026-03-15

## Summary

Open core is a business model where a company maintains a core open source project but adds proprietary features, extensions, or management tools on top, sold as an "enterprise edition." The open source core provides community adoption and developer trust; the proprietary layer provides revenue.

## Key Principles

- The core product is genuinely open source; premium features are proprietary
- The dividing line between open and proprietary features is the key business and community decision
- Open core avoids copyleft complications — the proprietary layer doesn't need to be open source because it's separate from the open source core
- Typically uses permissive licenses (Apache 2.0, MIT) for the core to avoid copyleft complications with the proprietary layer
- Community perception depends on where you draw the line — putting too many features behind the paywall alienates contributors

## Notable Examples

- **GitLab:** Core (MIT) + Enterprise Edition (proprietary). Clear feature matrix distinguishing CE from EE.
- **Elastic:** Elasticsearch core (formerly Apache 2.0, now AGPL/ELv2) + proprietary X-Pack features
- **Redis:** Core (formerly BSD, now dual RSALv2/SSPL) + proprietary modules
- **Confluent:** Apache Kafka (Apache 2.0) + Confluent Platform (proprietary enterprise features)

## Practical Guidance

1. **Draw the line thoughtfully.** Security features behind a paywall alienate the community. Governance, management, and scale features behind a paywall are more accepted.

2. **Permissive licenses simplify open core.** Apache 2.0 or MIT for the core means no copyleft complications with the proprietary add-ons.

3. **Be transparent about the business model.** Openly document which features are open source and which are proprietary. Don't surprise your community.

## Sources

- Heather Meeker, *Open Source for Business* (3rd ed., 2020)
- Joseph Jacks, "Open Core Summit" presentations
- Various company documentation (GitLab, Elastic, Redis, Confluent)
