# Standards Organizations and Open Source

> Last updated: 2026-03-15

## Summary

The intersection of formal standards development (SDOs) and open source communities creates both opportunities and tensions. Increasingly, standards are implemented primarily in open source, and some standards development has moved entirely to open source models. But the IP policies, governance structures, and cultural norms of traditional SDOs and open source projects are fundamentally different.

## Key Principles

- "Standards don't revolutionize — they commoditize" — standards create common platforms; OSS provides the implementation
- SDOs typically use FRAND or RF patent policies; OSS licenses include their own patent provisions
- The governance models differ: SDOs use formal voting/consensus processes; OSS uses rough consensus and running code (IETF model)
- OSS implementations often precede or replace formal standards
- "He who writes the first draft wins" — applies equally to standards and to open source reference implementations

## Models of Interaction

### OSS as Reference Implementation
- A standard is developed in an SDO; an open source project provides the reference implementation
- Examples: TLS/SSL (IETF standard, implemented in OpenSSL); HTTP/2 (IETF, implemented in many OSS projects)
- Benefit: Open source ensures the standard is actually implementable and testable

### OSS-First Standards
- Development happens in open source; a formal standard is created later (or never)
- Examples: Kubernetes (CNCF), then conformance certification; Docker/OCI containers
- The code IS the standard; formal specification follows

### Hybrid Models
- W3C: Formal standards process with RF patent policy + extensive open source implementation
- OASIS: Open Projects mode allows combined standards + open source development
- Eclipse Foundation: Specification process alongside open source projects
- JDF (Linux Foundation): Joint Development Foundation for formal specifications in OSS context

## Patent Policy Tensions

See also [SEPs and OSS](../03-patent-oss/seps-and-oss.md)

- FRAND patent policies in SDOs contemplate royalties; OSS licenses expect royalty-free distribution
- RF (royalty-free) patent policies at SDOs align with OSS (W3C, IETF)
- "Every ubiquitous, open standard I'm aware of is RAND based" — but the most web-relevant standards use RF policies

## Practical Guidance

1. **Understand the SDO's IP policy before engaging.** The patent policy is the most legally consequential element.

2. **RF policies enable OSS.** If your goal is open source implementation, prefer SDOs with royalty-free patent policies.

3. **Open source can influence standards.** Contributing to open source reference implementations can shape the eventual standard.

4. **Governance interop is hard.** SDO governance (formal voting, membership requirements) and OSS governance (rough consensus, meritocracy) don't always mix well. Plan for cultural translation.

## Sources

- W3C Patent Policy (w3.org/Consortium/Patent-Policy)
- OASIS Open Projects (oasis-open-projects.org)
- IETF RFC 8179 (Intellectual Property Rights in IETF Technology)
- Linux Foundation, Joint Development Foundation
