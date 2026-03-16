# Attribution and Notice Requirements

> Last updated: 2026-03-15

## Summary

Nearly all open source licenses require some form of attribution — preserving copyright notices, license texts, or other identifying information when distributing the software. While attribution requirements are simpler than copyleft source code obligations, they apply to virtually every open source license (including permissive licenses) and are frequently violated.

## Key Principles

- Attribution requirements exist in both permissive and copyleft licenses
- Typically require: preserving copyright notices, including license text, and (for some licenses) maintaining a NOTICE file
- Violation of attribution requirements is a license violation — under Jacobsen v. Katzer, this can constitute copyright infringement
- Attribution compliance should be automated where possible

## License-Specific Requirements

### MIT License
"The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software."

### BSD Licenses
- **2-clause:** Retain copyright notice and license in source and binary distributions
- **3-clause:** Same as 2-clause plus prohibition on using author's name for endorsement

### Apache License 2.0 (Section 4)
- Retain NOTICE file contents in any distribution
- Provide a copy of the license
- State modifications in modified files
- Preserve all copyright, patent, trademark, and attribution notices

### GPL (all versions)
- Keep intact all copyright notices
- Provide a copy of the license
- Display appropriate legal notices in interactive programs
- State changes made to the files (GPLv2 §2(a))

## Practical Guidance

1. **Automate notice collection.** Tools like FOSSology, ScanCode Toolkit, and SPDX tools can scan your codebase and extract license/notice information.

2. **Create a consolidated NOTICES file.** For binary distributions, include a single file collecting all required attributions and license texts.

3. **Don't strip copyright headers.** When modifying open source files, preserve existing copyright headers and add your own.

4. **SPDX identifiers simplify tracking.** Use SPDX license identifiers in source files (`SPDX-License-Identifier: MIT`) to make license identification machine-readable.

## Sources

- MIT License (full text)
- BSD 2-Clause and 3-Clause Licenses
- Apache License 2.0, Section 4
- GNU GPL v2/v3, notice requirements
- SPDX Specification (spdx.dev)
