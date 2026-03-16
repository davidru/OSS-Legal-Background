# Trademarks in Open Source Projects

> Last updated: 2026-03-15

## Summary

Trademark law in open source operates differently from copyright and patent law. While open source licenses grant broad rights to use, modify, and redistribute software, they typically do NOT grant trademark rights. A project's name, logo, and branding remain under the control of the trademark holder (typically the original developer or the hosting foundation), even though the code itself is freely available.

This creates an important distinction: anyone can fork and modify the code, but they may not be able to use the project's name or logo for their modified version.

## Key Principles

- Open source licenses grant copyright and (sometimes) patent rights — NOT trademark rights
- Trademark rights are separate from and independent of copyright licenses
- Trademarks protect consumers (preventing confusion about the source of goods/services)
- Foundations typically hold project trademarks and enforce them through trademark guidelines
- Forking code is a license right; using the project's name for the fork is a trademark question

## Case Law

### Planetary Motion v. Techsplosion, 261 F.3d 1188 (11th Cir. 2001)
- **Citation:** 261 F.3d 1188 (11th Cir. 2001)
- **Holding:** Distribution of open source software under the "Coolmail" name constituted sufficient use in commerce to establish trademark rights, even though the software was distributed for free.
- **Significance:** Established that free distribution of open source software can create trademark rights. You don't need to charge money to have a protectable trademark.
- **Key Principle:** Trademark rights arise from use in commerce — distribution of open source software qualifies.

### Other Relevant Cases
- **Mozilla / Firefox trademark disputes:** Mozilla maintained strict trademark policies even while distributing Firefox under MPL. Debian renamed Firefox to "Iceweasel" (2006-2016) when it couldn't comply with Mozilla's trademark requirements for modified versions.
- **Linux trademark:** Linux is a registered trademark of Linus Torvalds, managed by the Linux Mark Institute. Sublicensing is available but use must comply with trademark guidelines.

## Foundation Trademark Policies

### Apache Software Foundation
- All project names (Apache Hadoop, Apache Kafka, etc.) are trademarks of the ASF
- Strict trademark guidelines govern use of Apache project names
- Third parties can use the software but must comply with trademark guidelines when referencing

### Linux Foundation
- Linux is a registered trademark of Linus Torvalds
- LF projects have varying trademark policies (Kubernetes, Node.js, etc.)
- Conformance programs (Kubernetes certification, for example) are trademark-driven

### Eclipse Foundation
- Eclipse project names are trademarks of the Eclipse Foundation
- Compatibility requirements for use of the name "Eclipse" with modified versions

## Practical Guidance

1. **Open source ≠ open trademark.** Having the right to fork code does not give you the right to use the project's name. If you fork Firefox, you can't call your fork "Firefox."

2. **Register your project trademark.** If your project gains traction, register the name and logo. Trademark rights are stronger with registration.

3. **Create a trademark policy.** Document how others may (and may not) use your project name. Most foundations have templates.

4. **Forks must rename.** When a project is forked, the fork typically must use a different name (unless the trademark holder permits it). OpenSearch, OpenTofu, and Valkey all chose new names.

5. **Trademark vs. descriptive use.** Fair use of a trademark for descriptive purposes ("compatible with Linux") is generally permitted. Using a trademark as your own product name is not.

## Sources

- Planetary Motion v. Techsplosion, 261 F.3d 1188 (11th Cir. 2001)
- Pamela Chestek, "Trademark Usage Guidelines for Open Source Projects"
- Apache Software Foundation Trademark Policy
- Linux Foundation Trademark Usage Guidelines
- Model Trademark Guidelines (modeltrademarkguidelines.org)
