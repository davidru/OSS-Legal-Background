# Weak Copyleft Licenses

> Last updated: 2026-03-15

## Summary

Weak copyleft licenses occupy a middle ground between permissive licenses and strong copyleft (GPL). They require that modifications to the licensed component itself be shared under the same terms, but permit the component to be combined with proprietary code without the copyleft obligation extending to the larger work. The principal weak copyleft licenses are the LGPL (Lesser General Public License), MPL 2.0 (Mozilla Public License), and EPL 2.0 (Eclipse Public License).

The boundary between "the licensed component" and "the larger work" is the central legal and architectural question for weak copyleft compliance.

## Key Principles

- Weak copyleft applies to modifications of the licensed files/libraries, not to the entire combined work
- The boundary definition varies by license: LGPL uses linking concepts, MPL uses file-level scope, EPL uses module-level scope
- Weak copyleft enables library and component reuse in proprietary products while preserving improvements to the component itself
- Compliance architecture (how you integrate the component) can determine your obligations

## The Licenses

### LGPL (Lesser General Public License)
- **Versions:** LGPLv2.1 (1999), LGPLv3 (2007)
- **Scope mechanism:** Based on "work that uses the Library" vs. "work based on the Library." Modifications to the library itself are copyleft; the application using the library via its interface is not.
- **Key obligation:** Must allow users to re-link with modified versions of the LGPL library (the "relinking" requirement in LGPLv2.1 §6)
- **Complexity:** The LGPL's reliance on linking concepts (static vs. dynamic) creates architectural dependencies on compliance

### MPL 2.0 (Mozilla Public License)
- **Version:** MPL 2.0 (2012), replacing MPL 1.1
- **Scope mechanism:** File-level copyleft. Modifications to MPL-licensed files must be shared; new files in the same project can be under any license.
- **Key features:** Explicit compatibility provisions with GPL/LGPL/AGPL (§3.3); patent grant (§2.1); clear "Larger Work" exception (§3.3)
- **Simplicity advantage:** File-level scope is much easier to understand and comply with than LGPL's linking-based scope

### EPL 2.0 (Eclipse Public License)
- **Version:** EPL 2.0 (2017), replacing EPL 1.0
- **Scope mechanism:** Module-level copyleft, similar conceptually to MPL but using "Module" terminology
- **Key features:** Optional GPL-2.0 secondary license designation; patent grant; commercial distribution provisions

## Case Law

Limited published case law specifically on weak copyleft licenses. The general principles from Jacobsen v. Katzer (license conditions are enforceable) and Artifex v. Hancom (dual copyright/contract enforcement) apply.

### Relevant Proceedings

#### Various LGPL Compliance Disputes
- Most LGPL disputes have been resolved through private enforcement by the FSF and SFLC, typically resulting in compliance agreements without published opinions.
- The BusyBox enforcement campaign included some LGPL claims alongside GPLv2 claims.

## Commentary & Analysis

### Richard Fontana, "The Weak Copyleft Landscape" (Various publications)
- **Key Arguments:** Argues that MPL 2.0 represents the best-drafted weak copyleft license due to its clear file-level scope and explicit compatibility provisions. Notes that LGPL's linking-based scope creates unnecessary complexity.

### Heather Meeker on LGPL Compliance
- **Key Arguments:** LGPL compliance requires careful attention to the relinking requirement. Dynamic linking is generally safer than static linking for compliance purposes. The LGPL was designed for libraries and works best in that context.

## Practical Guidance

1. **MPL 2.0 is the clearest weak copyleft license.** If you're choosing a weak copyleft license, MPL 2.0's file-level scope is unambiguous and easy to comply with.

2. **LGPL compliance depends on integration architecture.** Dynamic linking to an LGPL library generally preserves the "work that uses the Library" status. Static linking may trigger additional obligations (providing object files to allow relinking).

3. **File boundaries matter for MPL 2.0.** Keep MPL-licensed code in its own files. If you modify an MPL file, that file stays under MPL. New files you create can be under any license.

4. **EPL 2.0's secondary license option.** EPL 2.0 allows the initial contributor to designate a "Secondary License" (GPL-2.0-only, GPL-2.0-or-later, or LGPL-2.1-or-later) for GPL compatibility.

## Open Questions

- **LGPL and modern language ecosystems.** How does the LGPL's linking concept apply to languages without traditional compilation (JavaScript, Python)? What about language-level module systems, package managers, or dynamic imports?
- **Container boundaries.** If LGPL code runs in a container that communicates via IPC/API with proprietary code, what are the obligations?
- **Header file inclusion.** The LGPL permits including header files (up to 10 lines) without triggering copyleft. How does this interact with modern header-only libraries?

## Sources

- GNU Lesser General Public License v2.1 (1999) and v3 (2007)
- Mozilla Public License 2.0 (2012)
- Eclipse Public License 2.0 (2017)
- Heather Meeker, *Open Source for Business* (3rd ed., 2020)
- Richard Fontana, various publications on weak copyleft licensing
- Free Software Foundation, "LGPL Frequently Asked Questions"
