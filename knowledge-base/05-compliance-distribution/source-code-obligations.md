# Source Code Obligations Under Copyleft Licenses

> Last updated: 2026-03-15

## Summary

The defining obligation of copyleft licenses is providing complete corresponding source code when distributing binaries. This requirement — simple in concept — creates significant compliance challenges in practice, particularly for embedded systems, consumer electronics, and complex software supply chains.

## Key Principles

- Copyleft obligations are triggered by **distribution** (GPLv2/v3) or **network interaction** (AGPL)
- "Complete corresponding source" must include everything needed to build the binary from source
- Source must be provided in a timely manner, in a usable format
- Incomplete source code (missing build scripts, configuration files, or dependencies) is a common compliance failure
- GPLv3 expanded the definition of "Corresponding Source" to explicitly include build scripts, installation information, and encryption keys needed for installation

## GPLv2 Source Code Requirements (Section 3)

Three options for providing source code:
1. **Accompany the binary** with complete corresponding source code on a physical medium
2. **Written offer** (valid for 3 years) to provide source code to any third party, for no more than the cost of distribution
3. **Pass along the written offer** received from upstream (non-commercial distributors only)

## GPLv3 Source Code Requirements (Sections 1, 6)

**"Corresponding Source"** includes:
- Source code for the work
- All interface definition files
- Scripts used to control compilation and installation
- System libraries and general-purpose tools used in building (identified but not required to be included)
- Installation information necessary to install modified versions on the user's hardware (the anti-tivoization provision)

**Distribution methods (Section 6):**
1. Source with the binary (physical or digital)
2. Written offer valid for 3 years
3. Network server access (e.g., download URL alongside binary)
4. Peer-to-peer distribution
5. Additional methods for user products (installation information)

## Common Compliance Failures

1. **Incomplete source code** — missing build scripts, patches, configuration files, or toolchain specifications
2. **Delayed source delivery** — providing source months after binary distribution
3. **Incorrect version** — providing source that doesn't match the distributed binary
4. **Missing third-party components** — failing to include source for all copyleft dependencies
5. **Dead download links** — source code URLs that stop working after product discontinuation

## Commentary & Analysis

### Software Freedom Conservancy, "Copyleft and the GNU General Public License: A Comprehensive Tutorial and Guide"
- **Source:** copyleft.org
- **Key Arguments:** The most detailed practical guide to GPL compliance. Walks through each obligation with examples. Emphasizes that "complete corresponding source" means everything needed to reproduce the binary — if your build requires proprietary tools, you have a compliance problem.

### OpenChain Project (ISO/IEC 5230:2020)
- **Source:** openchainproject.org
- **Key Arguments:** International standard for open source license compliance programs. Defines the key requirements for a compliance program including: policy, training, contribution management, and SBOM/component tracking. Adopted as ISO standard in 2020.

## Practical Guidance

1. **Build from source regularly.** The test for complete corresponding source is: can a competent developer build the binary from the source you provide? Test this periodically.

2. **Automate source code packaging.** Integrate source code collection into your build pipeline. Don't try to assemble source packages manually after the fact.

3. **Use SPDX and SBOMs.** Machine-readable software bills of materials make it possible to track what's in your product and what source obligations attach.

4. **Written offers must be honored.** If you use the written offer mechanism, be prepared to fulfill requests for 3 years. Budget for this.

5. **AGPL adds network obligations.** If you modify AGPL-licensed software and users interact with it over a network, you must provide source code even without traditional "distribution."

## Sources

- GNU General Public License v2, Section 3
- GNU General Public License v3, Sections 1, 6
- GNU Affero General Public License v3, Section 13
- Software Freedom Conservancy, *Copyleft Guide* (copyleft.org)
- OpenChain Project (ISO/IEC 5230:2020)
