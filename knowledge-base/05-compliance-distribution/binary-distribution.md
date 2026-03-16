# Binary Distribution Compliance

> Last updated: 2026-03-15

## Summary

Distributing compiled binary code containing open source components triggers license obligations that differ from source-code-only distribution. Most compliance challenges arise in binary distribution contexts — embedded systems, mobile apps, desktop applications, and container images — where the original source code is not directly visible to the recipient.

## Key Principles

- Binary distribution triggers copyleft source code obligations (GPLv2 §3, GPLv3 §6)
- All open source licenses with attribution requirements apply to binary distribution
- Binary distribution does NOT include SaaS/cloud deployment (see [SaaS/Cloud](saas-cloud.md))
- Compliance requires: correct notices, license texts, source code availability (for copyleft), and NOTICE files (Apache 2.0)

## Common Distribution Contexts

### Embedded Systems / IoT Devices
- Highest compliance risk — devices ship with Linux + hundreds of OSS packages
- BusyBox enforcement cases targeted this category
- Source must be provided for the specific binary shipped on the device
- Written offer (GPLv2) or download URL (GPLv3) required

### Mobile Applications
- App store distribution is "distribution" for license purposes
- Must include license/attribution information within the app
- Common practice: "Licenses" section in app settings
- Copyleft-licensed code in mobile apps requires source availability

### Container Images
- Docker/OCI container images containing OSS components are distributions
- Each layer may contain different licensed components
- SBOM for container images helps track obligations

### Desktop Applications / Installers
- Standard distribution — include NOTICES/LICENSE files in the installation
- Copyleft source must be available for the duration of the written offer period

## Practical Guidance

1. **Automate notice generation.** Integrate license notice collection into your build system. Don't rely on manual processes.

2. **Provide source alongside binaries.** The simplest copyleft compliance path is providing source code alongside the binary (on the same download page, in the same package, etc.).

3. **Test source completeness.** Build from the source you provide to verify it produces the binary you distribute.

4. **Container images need attention.** Just because your code is in a container doesn't exempt you from license obligations. The container is a distribution mechanism.

## Sources

- GNU GPL v2 §3 (source code requirements for binary distribution)
- GNU GPL v3 §6 (conveying non-source forms)
- Apache License 2.0 §4 (redistribution requirements)
- OpenChain Specification (ISO/IEC 5230)
