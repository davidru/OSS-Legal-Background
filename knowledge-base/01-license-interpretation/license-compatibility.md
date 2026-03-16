# License Compatibility

> Last updated: 2026-03-15

## Summary

License compatibility determines whether code under different open source licenses can be combined in a single work. Incompatibility arises when two licenses impose conflicting conditions — most commonly when two copyleft licenses each require the combined work to be distributed under their own terms.

License compatibility is one of the most practically important (and frequently misunderstood) areas of open source law. Getting it wrong can create legally impossible situations where you cannot distribute a combined work without violating at least one license.

## Key Principles

- Permissive licenses are generally compatible with everything (they impose no distribution-term requirements on the combined work)
- Copyleft licenses are compatible with permissive licenses (the combined work goes under the copyleft license)
- Two different copyleft licenses are generally incompatible with each other unless one includes an explicit compatibility provision
- "Compatible" means you can legally combine the code; it does not mean the licenses are identical
- Compatibility is directional in some cases — A-code can go into a B-licensed work, but not vice versa

## Compatibility Matrix (Major Licenses)

### Permissive → Copyleft (Generally Compatible)
- MIT → GPL: ✅ (combined work under GPL)
- BSD → GPL: ✅ (combined work under GPL)
- Apache 2.0 → GPLv3: ✅ (combined work under GPLv3)
- Apache 2.0 → GPLv2-only: ❌ (patent retaliation clause conflict)
- Apache 2.0 → GPLv2-or-later: ✅ (upgrade to GPLv3, then combine)

### Copyleft ↔ Copyleft (Generally Incompatible)
- GPLv2 ↔ GPLv3: ❌ (unless "or later" option exercised)
- GPL ↔ EPL 1.0: ❌ (incompatible copyleft requirements)
- GPL ↔ EPL 2.0: ✅ (if secondary license designated)
- GPL ↔ MPL 2.0: ✅ (MPL 2.0 §3.3 explicit compatibility)
- GPL ↔ CDDL: ❌ (no compatibility provision)

### Weak Copyleft Combinations
- LGPL code can be used by GPL code (LGPL is a GPL exception)
- MPL 2.0 files can coexist with proprietary files in a larger work
- MPL 2.0 code can be combined with GPL code (§3.3)

## The GPLv2/GPLv3 Split

One of the most consequential compatibility issues in open source:

- **GPLv2-only** code cannot be combined with **GPLv3** code — the licenses impose different conditions (GPLv3 adds anti-tivoization, patent provisions)
- **GPLv2-or-later** code CAN be combined with GPLv3 code by exercising the "or later" option
- The Linux kernel is GPLv2-only (Linus Torvalds deliberately chose not to include "or later"), creating a permanent incompatibility with GPLv3-only code
- This split has significant practical implications for kernel development and related toolchains

## Commentary & Analysis

### Free Software Foundation, "GPL-Compatible Free Software Licenses"
- **Source:** gnu.org/licenses/license-list.html
- **Key Arguments:** Maintains the authoritative (if sometimes contested) compatibility list. The FSF's analysis focuses on whether a license's requirements can be satisfied simultaneously with the GPL's requirements.

### David A. Wheeler, "The Free-Libre / Open Source Software (FLOSS) License Slide"
- **Source:** dwheeler.com
- **Key Arguments:** Visual representation of license compatibility as a directed graph. Code can "flow" from permissive to copyleft, but not from copyleft to more-restrictive copyleft. A widely-referenced practical tool.

## Practical Guidance

1. **Check compatibility before combining.** Before integrating a dependency, verify that its license is compatible with your project's license. Automated tools help but may miss edge cases.

2. **Permissive licenses minimize compatibility risk.** If your project uses MIT or Apache 2.0, you can incorporate almost any dependency.

3. **"Or later" matters enormously.** The difference between "GPLv2 only" and "GPLv2 or later" is the difference between GPLv3 incompatibility and compatibility. When choosing GPL, consider whether to include the "or later" option.

4. **MPL 2.0's compatibility provision is intentional.** MPL 2.0 §3.3 was specifically drafted to be GPL-compatible, solving a long-standing problem with MPL 1.1.

5. **When in doubt, don't combine.** If you're uncertain about compatibility, keep the components separate (separate processes communicating via well-defined interfaces). This may avoid creating a "combined work" under either license.

## Open Questions

- **Runtime vs. compile-time combination.** Does license compatibility analysis change depending on whether code is combined at compile time, link time, or runtime?
- **Package manager boundaries.** When npm/pip/cargo resolves dependencies, does the combined installation create a "work" for compatibility purposes?
- **Compatibility in AI contexts.** If training data includes code under incompatible licenses, does the resulting model have a compatibility problem?

## Sources

- Free Software Foundation, "Various Licenses and Comments About Them" (gnu.org)
- David A. Wheeler, "The Free-Libre / Open Source Software (FLOSS) License Slide"
- Heather Meeker, *Open Source for Business* (3rd ed., 2020), Chapter on Compatibility
- SPDX License List (spdx.org/licenses)
