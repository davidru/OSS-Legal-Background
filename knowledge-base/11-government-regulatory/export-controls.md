# Export Controls and Open Source Software

> Last updated: 2026-03-15

## Summary

The intersection of export control law and open source software involves an important carve-out: publicly available open source software is generally exempt from US Export Administration Regulations (EAR) under the "publicly available" exception. However, the details matter, and some types of technology (encryption, certain hardware designs) require careful analysis even in the open source context.

## Key Principles

- Publicly available open source software is generally exempt from EAR controls under 15 C.F.R. § 734.3(b)(3)
- The exemption applies to software that is "published" and "available to the public without restrictions upon its further dissemination"
- Encryption software has special rules — while the general exemption applies, a notification to BIS (Bureau of Industry and Security) may be required
- Export control analysis should focus on: (1) is the software publicly available? (2) does it include controlled encryption? (3) is it being provided to sanctioned entities?
- Sanctions programs (OFAC) apply regardless of the public availability exemption

## The EAR "Publicly Available" Exception

### 15 C.F.R. § 734.3(b)(3)
"Publicly available technology and software that... are already published or will be published... and are or will be available to the public" are not subject to the EAR.

### What Qualifies
- Source code posted on GitHub, GitLab, or other public repositories
- Code distributed under open source licenses
- Published standards and specifications with open source reference implementations

### What Doesn't Qualify
- Software that is not publicly available (e.g., distributed only to specific recipients)
- Software with access restrictions (e.g., registration required for access)
- Proprietary software, even if distributed widely

## Encryption and Open Source

### EAR Category 5, Part 2
- Encryption software has separate export control provisions
- **Open source encryption notification:** Under 15 C.F.R. § 742.15(b), publicly available encryption source code may be exported without a license, but the exporter should provide BIS and NSA with a notification (including the URL where the code is available)
- In practice, major open source projects with encryption (OpenSSL, GnuPG, etc.) comply with this notification requirement

## Sanctions Compliance

### OFAC (Office of Foreign Assets Control)
- Sanctions programs (SDN list, country-specific sanctions) apply regardless of the EAR public availability exemption
- Making software available on a public repository is generally not a "transaction" with a sanctioned entity
- However, providing technical support, customization, or services to sanctioned entities may violate sanctions
- GitHub, GitLab, and other platforms have implemented sanctions compliance programs that restrict access from certain countries

## Practical Guidance

1. **Public open source is generally EAR-exempt.** If your source code is publicly available on GitHub without access restrictions, it's likely exempt from EAR.

2. **Encryption notification is easy.** If your open source project includes encryption, send the notification to BIS/NSA. It's a simple email/filing.

3. **Sanctions are separate from EAR.** Even if your software is EAR-exempt, you cannot provide it as a service or provide support to sanctioned entities.

4. **Don't add access restrictions.** If you restrict access to your open source repository (e.g., requiring registration, gating downloads), you may lose the public availability exemption.

5. **Get advice for dual-use technology.** If your open source project involves technology with military or intelligence applications, consult export control counsel.

## Sources

- 15 C.F.R. § 734.3(b)(3) (publicly available exception)
- 15 C.F.R. § 742.15(b) (encryption source code)
- OFAC Sanctions Programs
- BIS, "Encryption and Export Controls FAQ"
