# Dual Licensing

> Last updated: 2026-03-15

## Summary

Dual licensing is a business model where a company distributes software under two licenses simultaneously: an open source license (typically copyleft) and a proprietary/commercial license. Users who can comply with the copyleft terms use the open source version for free; users who cannot or prefer not to (typically because they want to integrate the software into proprietary products without copyleft obligations) purchase a commercial license.

## Key Principles

- The dual-licensing model requires the company to hold all copyrights (or have CLA authority) — only the copyright holder can offer alternative license terms
- Copyleft is the "stick" that drives commercial license revenue — without copyleft, there's no incentive to buy a commercial license
- The model creates tension between community and commercial interests — the company benefits from copyleft fears
- Contributor agreements (CLAs with assignment or broad license grants) are essential for dual licensing

## Notable Examples

### MySQL (now Oracle)
- **Model:** GPL + commercial license
- **History:** The original and most successful dual licensing model. MySQL AB offered MySQL under GPLv2 and a commercial license. Companies embedding MySQL in proprietary products purchased commercial licenses.
- **Outcome:** Acquired by Sun (2008), then Oracle (2010). MariaDB forked as community response.

### Qt (The Qt Company)
- **Model:** LGPL/GPL + commercial license
- **History:** Initially proprietary → GPL → LGPL → dual GPL/commercial. Qt offers LGPL for most modules, GPL for some, and commercial licenses for full proprietary use.

### MongoDB (pre-SSPL)
- **Model:** AGPL + commercial license
- **History:** Used AGPL to drive commercial license adoption. Cloud providers could use AGPL MongoDB but chose not to comply with source requirements, so they bought commercial licenses. When cloud providers started running MongoDB without purchasing licenses, MongoDB switched to SSPL.

### Ghostscript (Artifex)
- **Model:** AGPL + commercial license
- **Legal significance:** Artifex v. Hancom (2017) established that the GPL can be enforced as both a copyright license and a contract in the dual-licensing context.

## Commentary & Analysis

### Heather Meeker on Dual Licensing
- **Key Arguments:** Dual licensing is a legitimate and effective business model for open source companies. The key is ensuring the commercial license provides value (typically copyleft-free use) that justifies the cost. The model works best with library/infrastructure software that gets embedded in other products.

### Critics (Bradley Kuhn, SFC)
- **Key Arguments:** Dual licensing creates perverse incentives — the company benefits from copyleft fear rather than copyleft value. CLAs that enable dual licensing concentrate power and can be used for community-hostile relicensing.

## Practical Guidance

1. **Dual licensing requires copyright control.** You must hold all copyrights or have CLAs granting you relicensing authority.

2. **Copyleft choice matters.** AGPL creates the strongest incentive for commercial licenses (covers SaaS). GPL is next. LGPL provides weak incentive (linking exception reduces copyleft pressure).

3. **Community contribution challenges.** Contributors may resist CLAs knowing their code could be sold under proprietary terms. This limits community growth.

4. **Consistent enforcement.** If you dual-license, you must actually enforce the copyleft license against non-compliant users. Selective enforcement undermines both the business model and community trust.

## Sources

- Heather Meeker, *Open Source for Business* (3rd ed., 2020)
- Artifex Software v. Hancom, No. 16-cv-06982 (N.D. Cal. 2017)
- MySQL AB dual licensing documentation (historical)
