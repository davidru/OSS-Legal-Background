# Nonprofit Law for Open Source Organizations

> Last updated: 2026-03-15

## Summary

Most open source foundations are organized as US nonprofits or international equivalents. The choice of legal structure affects taxation, governance requirements, fundraising, and the organization's relationship with its members and the public. Understanding nonprofit law is essential for anyone creating or managing an open source foundation.

## Key Structures

### US 501(c)(3) — Charitable Organization
- **Tax treatment:** Tax-exempt; donations are tax-deductible for donors
- **Examples:** Apache Software Foundation, Free Software Foundation, Software Freedom Conservancy
- **Requirements:** Must operate exclusively for charitable, educational, or scientific purposes
- **OSS rationale:** Software development for the public benefit can qualify as educational/scientific
- **Constraints:** Cannot engage in substantial lobbying; must serve public interest, not private benefit
- **Advantage:** Donor tax deductibility makes fundraising easier

### US 501(c)(6) — Business League
- **Tax treatment:** Tax-exempt; member dues may be deductible as business expenses (not charitable donations)
- **Examples:** Linux Foundation, Eclipse Foundation (pre-2021), OASIS
- **Requirements:** Must promote common business interests of members
- **OSS rationale:** Promoting open source development serves common business interests of the technology industry
- **Constraints:** Must serve member interests collectively; less restrictive than 501(c)(3) on lobbying
- **Advantage:** Better suited for industry consortia with corporate membership

### Fiscal Sponsorship
- **How it works:** An existing nonprofit provides legal and financial infrastructure for a project without the project forming its own entity
- **Examples:** Software Freedom Conservancy sponsors ~40 projects (Git, Homebrew, Selenium, etc.)
- **Advantage:** Projects get nonprofit status, legal protection, and administrative support without forming their own organization
- **Disadvantage:** Less autonomy than having your own foundation; shared resources

### International Structures
- **Belgian AISBL:** Eclipse Foundation (since 2021). International nonprofit under Belgian law. Provides EU legal presence.
- **German e.V. (Verein):** FSFE, KDE e.V. Registered association under German law.
- **UK Community Interest Company (CIC):** Some UK-based open source projects use this structure.

## Key Legal Issues

### Fiduciary Duties
- Directors of nonprofit foundations owe fiduciary duties (care, loyalty, obedience)
- Must act in the organization's best interest, not their employer's interest
- Conflict of interest policies are essential when directors represent competing companies

### D&O Insurance
- Directors & Officers insurance protects board members from personal liability
- Essential for any foundation with a board of directors
- "These things tend not to be important until they're important, and then they become very, very important"

### Antitrust Compliance
- Foundation meetings where competitors gather create antitrust risk
- Must avoid discussions of pricing, market allocation, boycotts, or competitive strategy
- Antitrust guidelines should be reviewed at the start of every meeting

## Practical Guidance

1. **501(c)(6) is the default for industry foundations.** Unless you specifically need donor tax deductibility, 501(c)(6) provides more flexibility for corporate-funded open source.

2. **Fiscal sponsorship before incorporation.** For new projects, fiscal sponsorship (e.g., through SFC or NumFOCUS) provides nonprofit benefits without the cost and complexity of forming a new entity.

3. **Get D&O insurance.** Any foundation with a board needs this. Don't skip it.

4. **Plan for governance costs.** Foundations need legal counsel, accounting, and administration. Budget accordingly. "If it's not worth it to the engineering group to cover the dues, it's probably not worth it for Microsoft to be a member."

## Sources

- IRS, "Tax-Exempt Status for Your Organization" (Publication 557)
- 26 U.S.C. §§ 501(c)(3), 501(c)(6)
- Software Freedom Conservancy, Fiscal Sponsorship Overview
- Linux Foundation, Governance and Structure Documentation
