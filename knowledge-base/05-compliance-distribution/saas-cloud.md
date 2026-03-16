# SaaS, Cloud, and Network Use

> Last updated: 2026-03-15

## Summary

Traditional copyleft licenses (GPLv2, GPLv3) are triggered by "distribution" — providing copies of the software to others. Using software to provide a service over a network (SaaS model) generally does not constitute "distribution," creating what is known as the "SaaS loophole" or "ASP loophole." The GNU Affero General Public License (AGPL) was created specifically to close this gap.

## Key Principles

- GPLv2/v3 copyleft obligations require "distribution" or "conveying" — running software on your own servers for SaaS is generally not distribution
- The AGPL (Section 13) extends copyleft to network interaction: if users interact with AGPL software remotely, the operator must provide source code
- The "SaaS loophole" is a feature (of GPLv2/v3), not a bug (from the FSF's perspective) — AGPL exists for projects that want network copyleft
- Cloud providers' use of open source code to provide competing services was a major driver of the source-available license movement

## The AGPL (Section 13)

"Notwithstanding any other provision of this License, if you modify the Program, your modified version must prominently offer all users interacting with it remotely through a computer network... an opportunity to receive the Corresponding Source of your version."

### Key Elements
- **Trigger:** Modification + remote user interaction over a network
- **Obligation:** Provide corresponding source to remote users
- **Scope:** Only the modified version; not the entire service stack (unlike SSPL)
- **Unmodified use:** Running unmodified AGPL software as a service does NOT trigger Section 13 (no modification = no obligation beyond what GPLv3 already requires)

## The Cloud Provider Controversy

### The Problem
Companies like MongoDB, Redis Labs, and Elastic argued that major cloud providers (AWS, Azure, GCP) were taking their open source software, running it as a managed service, and capturing the commercial value without contributing back. Even AGPL was insufficient because:
1. Cloud providers could run the software unmodified (no Section 13 trigger)
2. Cloud providers' service management infrastructure was separate from the AGPL code
3. Users interacted with the cloud provider's API, not directly with the AGPL software

### The Response: Source-Available Licenses
This perceived gap drove the creation of SSPL, BSL, and other source-available licenses (see [Non-Standard Licenses](../01-license-interpretation/non-standard-licenses.md)).

## Practical Guidance

1. **GPLv2/v3 for SaaS is low-risk.** If you run GPL software on your own servers to provide a service, you generally have no source code disclosure obligation (no "distribution").

2. **AGPL requires attention.** If you modify AGPL software and users interact with it over a network, you must provide source code. Understand whether your use triggers this.

3. **Unmodified AGPL is safer than modified.** Running unmodified AGPL software as a service does not trigger Section 13. But verify — configuration changes that modify source code count as modifications.

4. **Many companies ban AGPL.** Google, Apple, and others prohibit AGPL in their codebases due to compliance complexity. Evaluate your organization's risk tolerance.

## Open Questions

- **What constitutes "interacting remotely"?** Is an API call sufficient? What about indirect interaction through a load balancer or reverse proxy?
- **"Modification" scope.** Does applying patches, configuration changes, or environment-specific adaptations constitute "modification" under AGPL?
- **Container and microservice boundaries.** If AGPL code runs in one container and proprietary code in another, communicating via API — does Section 13 apply to the proprietary code?

## Sources

- GNU Affero General Public License v3, Section 13
- FSF, "Why the Affero GPL" (gnu.org)
- Heather Meeker, *Open Source for Business* (3rd ed., 2020), AGPL chapter
