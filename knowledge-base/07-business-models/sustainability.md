# Open Source Sustainability

> Last updated: 2026-03-15

## Summary

Open source sustainability — ensuring that open source projects have the resources (financial, human, organizational) to continue operating effectively — has become a central concern in the software industry. High-profile incidents like the Heartbleed vulnerability (OpenSSL), the Log4Shell crisis, and the XZ Utils backdoor have demonstrated that critical digital infrastructure often depends on under-resourced volunteer maintainers.

## Key Principles

- Modern digital infrastructure depends heavily on open source, but funding models haven't kept pace
- "10% of the people do 90% of the effort" — maintainer burnout is a systemic risk
- Sustainability is not just about money — it's about governance, succession planning, and community health
- There is no single solution; multiple funding models coexist and complement each other

## Funding Models

### Foundation-Based Funding
- Corporate membership dues fund foundation operations and project support
- Examples: Linux Foundation, Apache, Eclipse, CNCF
- Strengths: Stable, institutional, enables professional staff
- Weaknesses: Favors large corporate projects; small projects may not qualify

### Corporate Employment
- Companies employ developers to work on open source full-time
- Examples: Red Hat (Linux kernel), Google (Chromium, Kubernetes), Microsoft (VS Code, .NET)
- Strengths: Professional development, full-time focus
- Weaknesses: Company priorities may diverge from community priorities; developer leaves = contribution stops

### Individual Sponsorship
- Platforms: GitHub Sponsors, Open Collective, Patreon, Tidelift
- Strengths: Direct community support, individual developer empowerment
- Weaknesses: Typically small amounts, unreliable, creates tax/administrative burden

### Government Funding
- EU's Next Generation Internet (NGI) initiative
- Germany's Sovereign Tech Fund
- US government investment through CISA and NSF
- Strengths: Large grants, public interest alignment
- Weaknesses: Bureaucratic, political, not sustainable long-term

### Commercial Support Contracts
- Companies pay for support, training, and custom development
- Examples: Tidelift (subscription model for maintainer income), various consulting firms
- Strengths: Aligns incentives (users pay for what they value)
- Weaknesses: Scale limitations, not all projects lend themselves to support contracts

## Key Initiatives

### OpenSSF (Open Source Security Foundation)
- Linux Foundation project focused on securing open source software
- Funded by major tech companies post-Log4Shell
- Initiatives: Scorecard (project security metrics), Sigstore (code signing), Alpha-Omega (security investment in critical projects)

### Tidelift
- Subscription model: companies pay Tidelift, which distributes payments to maintainers of dependencies they use
- Maintainers commit to security, maintenance, and licensing standards in return

### Sovereign Tech Fund (Germany)
- Government-funded program supporting critical open source infrastructure
- Provides direct grants to maintainers and projects

## Practical Guidance

1. **Track your dependencies.** Know what open source you depend on. Consider supporting the projects you rely on most.

2. **Sustainability is a supply chain issue.** If a critical dependency is unmaintained, that's a supply chain risk — not just an altruism opportunity.

3. **Multiple models work together.** No single funding model solves sustainability. Foundation support + corporate employment + community sponsorship creates resilience.

## Sources

- Nadia Eghbal, *Working in Public: The Making and Maintenance of Open Source Software* (Stripe Press, 2020)
- OpenSSF (openssf.org)
- Tidelift (tidelift.com)
- Sovereign Tech Fund (sovereigntechfund.de)
- Ford Foundation, "Roads and Bridges: The Unseen Labor Behind Our Digital Infrastructure" (2016)
