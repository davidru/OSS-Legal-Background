# IP Ownership in Collaborative Open Source Projects

> Last updated: 2026-03-15

## Summary

Open source projects are collaborative by nature — dozens or thousands of contributors submit code. Understanding who owns the intellectual property in this context is essential for enforcement, licensing, and governance.

The default rule in most jurisdictions is that the author of a work owns the copyright. In the employment context, the employer typically owns work created within the scope of employment (work-for-hire). In open source, contributions come from individuals, employees, contractors, and automated tools — creating a complex ownership landscape.

## Key Principles

- Each contributor owns the copyright in their individual contribution (absent assignment or work-for-hire)
- Joint authorship requires intent to create a single, unified work — most OSS contributions don't meet this standard
- Employer ownership (work-for-hire) applies when contributors are employees contributing within their job scope
- Open source licenses grant downstream rights, but ownership remains with the original authors
- No one entity "owns" a large open source project unless all contributors have assigned their copyright

## Work-for-Hire and Employee Contributions

### US Law (17 U.S.C. § 101)
- Works created by employees within the scope of employment are "works made for hire" — the employer is the author and owner
- The employer-employee relationship is determined by common law agency principles
- Independent contractors generally own their work unless there's a written assignment

### Practical Impact
- Most corporate contributors are employees — their employer owns the contribution
- This is why Corporate CLAs (CCLAs) exist — to ensure the employer authorizes the contribution
- DCO sign-offs by employees may be insufficient if the employer hasn't authorized the contribution

## Practical Guidance

1. **Assume fragmented ownership.** Large OSS projects have hundreds of copyright holders. No single entity can unilaterally enforce or relicense without CLAs/assignments.
2. **Corporate CLAs address employer authorization.** If your contributors are likely employees, corporate CLAs provide employer sign-off.
3. **Track contributions.** Maintain clear records of who contributed what (version control helps) for enforcement and compliance purposes.

## Sources

- 17 U.S.C. § 101 (work-for-hire definition)
- 17 U.S.C. § 201 (ownership of copyright)
- Community Developed Ownership Guidelines (various SDO/foundation models)
