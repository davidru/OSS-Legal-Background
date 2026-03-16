# Software Supply Chain and SBOMs

> Last updated: 2026-03-15

## Summary

Software supply chain security and transparency have become major regulatory and industry concerns, driven by high-profile incidents (SolarWinds, Log4Shell, XZ Utils) and new regulations (US Executive Orders, EU Cyber Resilience Act). Software Bills of Materials (SBOMs) — machine-readable inventories of software components — are at the center of both compliance and security efforts.

## Key Principles

- Modern software is built from hundreds or thousands of open source components, creating complex dependency chains
- SBOMs provide transparency into what components are in a software product
- Regulatory requirements for SBOMs are increasing in both the US and EU
- SBOMs serve dual purposes: license compliance AND security vulnerability tracking
- The primary SBOM formats are SPDX (ISO/IEC 5962:2021) and CycloneDX

## Regulatory Landscape

### US Executive Order 14028 (May 2021)
- "Improving the Nation's Cybersecurity"
- Requires SBOMs for software sold to the federal government
- NTIA established minimum elements for SBOMs
- Led to OMB M-22-18 and CISA guidance on SBOM adoption

### EU Cyber Resilience Act (2024)
- Requires manufacturers to identify and document vulnerabilities in software components
- SBOM requirements for products with digital elements
- Open source stewards have lighter obligations but must support vulnerability reporting
- Full application by December 2027

### NTIA Minimum Elements for SBOMs
1. Supplier name
2. Component name
3. Version
4. Unique identifier
5. Dependency relationships
6. Author of SBOM data
7. Timestamp

## SBOM Formats

### SPDX (Software Package Data Exchange)
- Developed by Linux Foundation
- ISO/IEC 5962:2021 international standard
- Covers both license and security information
- Widely adopted in open source ecosystems

### CycloneDX
- Developed by OWASP
- Focused on security and vulnerability tracking
- Supports VEX (Vulnerability Exploitability eXchange)
- Growing adoption in security-focused environments

## Supply Chain Security Incidents

### Log4Shell (December 2021)
- Critical vulnerability (CVE-2021-44228) in Apache Log4j
- Demonstrated that a vulnerability in a widely-used OSS library can affect millions of systems
- Highlighted the need for SBOMs — many organizations couldn't quickly determine if they used Log4j

### XZ Utils Backdoor (March 2024)
- Social engineering attack: a long-term contributor inserted a backdoor into XZ compression library
- Caught before widespread deployment but demonstrated supply chain attack vectors
- Led to renewed focus on maintainer trust, contributor verification, and build reproducibility

## Practical Guidance

1. **Generate SBOMs as part of your build process.** Don't treat SBOMs as an afterthought — integrate SBOM generation into CI/CD pipelines.

2. **Choose a format.** SPDX for license compliance focus; CycloneDX for security focus. Both are acceptable; consistency matters more than format choice.

3. **Track transitive dependencies.** Your direct dependencies have their own dependencies. An SBOM should capture the complete dependency tree.

4. **Keep SBOMs current.** An SBOM is only useful if it reflects the actual shipped software. Regenerate with every release.

5. **Use SBOMs for license compliance.** An SBOM that includes license information makes it possible to identify all open source obligations automatically.

## Sources

- Executive Order 14028 (May 2021)
- NTIA, "The Minimum Elements for a Software Bill of Materials" (2021)
- EU Cyber Resilience Act (Regulation 2024/2847)
- SPDX Specification (spdx.dev)
- CycloneDX Specification (cyclonedx.org)
- OpenSSF, Supply Chain Security Best Practices
