# Fair Use and Open Source Software

> Last updated: 2026-03-15

## Summary

Fair use (17 U.S.C. § 107) is a defense to copyright infringement that permits certain uses of copyrighted works without the copyright holder's permission. In the open source context, fair use is most significant in cases involving API reimplementation, interoperability, and reverse engineering — areas where functional necessities may justify copying that would otherwise infringe.

The Supreme Court's decision in Oracle v. Google (2021) is the landmark ruling applying fair use to software, finding that Google's copying of Java API declarations for reimplementation in Android was fair use.

## Key Principles

- Fair use is a four-factor balancing test, not a bright-line rule
- The four factors: (1) purpose and character of the use, (2) nature of the copyrighted work, (3) amount and substantiality used, (4) market effect
- "Transformative" use weighs heavily in favor of fair use — using the work for a different purpose or context
- Software's functional character makes fair use analysis different from literary or artistic works
- Interoperability and compatibility purposes are strongly favored

## The Four Factors Applied to Software

### Factor 1: Purpose and Character of the Use
- Reimplementing APIs for platform compatibility is transformative (Oracle v. Google)
- Commercial use is not dispositive but weighs against fair use
- Educational, research, and interoperability uses are favored

### Factor 2: Nature of the Copyrighted Work
- Software has a "functional" character that is "further from the core of copyright" (Oracle v. Google)
- API declarations are "inherently bound together with uncopyrightable ideas" and organizational systems
- Creative code with significant expressive choices weighs against fair use

### Factor 3: Amount and Substantiality
- Copying only what is necessary for the purpose weighs in favor
- Google copied ~11,500 lines of API declarations out of 2.86 million total lines — "virtually all of the copied lines are inherently bound up with the idea of the API" (Oracle v. Google)
- Qualitative analysis matters — copying the "heart" of the work can weigh against fair use even if the quantity is small

### Factor 4: Market Effect
- The relevant market is the copyright holder's actual or potential market
- If the copying enables a new platform or product that doesn't substitute for the original, this weighs in favor
- Loss of licensing revenue alone is not sufficient to defeat fair use if the use is transformative

## Case Law

### Oracle America v. Google LLC, 593 U.S. 1 (2021)
- **Citation:** 593 U.S. 1, 141 S. Ct. 1183 (2021)
- **Holding:** Google's copying of Java SE API declaring code for use in Android was fair use.
- **Analysis:** All four factors weighed in Google's favor. The opinion emphasized that the declaring code was "inherently bound up with a general system" and that Google's purpose was to create a "new and transformative" platform (mobile phones vs. desktop/embedded Java).
- **Key Quote:** "Google's purpose was to create a different task-related system for a different computing environment (smartphones) and to create a platform — the Android platform — that would help achieve and popularize that objective."

### Sega v. Accolade, 977 F.2d 1510 (9th Cir. 1992)
- **Citation:** 977 F.2d 1510 (9th Cir. 1992)
- **Holding:** Reverse engineering of Sega Genesis console software to develop compatible games was fair use.
- **Significance:** Established that reverse engineering for interoperability purposes is fair use, even when it requires copying the entire program as an intermediate step.

### Sony Computer Entertainment v. Connectix, 203 F.3d 596 (9th Cir. 2000)
- **Citation:** 203 F.3d 596 (9th Cir. 2000)
- **Holding:** Copying PlayStation BIOS as an intermediate step in creating a compatible emulator was fair use.
- **Significance:** Extended Sega v. Accolade to permit intermediate copying for the purpose of creating compatible products.

## Practical Guidance

1. **API reimplementation has strong fair use support after Oracle v. Google.** But the holding was fact-specific — the Supreme Court emphasized the particular circumstances (established API, new platform, programmer investment in learning the API).

2. **Reverse engineering for interoperability is fair use.** Sega and Sony establish that you can reverse-engineer software to understand its interfaces for the purpose of creating compatible products.

3. **Document your purpose.** Fair use analysis is purpose-driven. If you're copying for interoperability, compatibility, or to create something new, document that purpose.

4. **Copy only what's necessary.** The amount factor matters. Copy the minimum needed to achieve the fair use purpose.

5. **Don't compete in the same market.** Fair use is strongest when you're creating something for a different market or purpose, not a direct substitute.

## Open Questions

- **AI training as fair use.** Is training an AI model on copyrighted code fair use? The Oracle v. Google framework supports arguments on both sides. Active litigation is ongoing.
- **Scope of Oracle v. Google beyond APIs.** How broadly does the fair use holding apply? To all APIs? To software interfaces generally? To data formats?
- **Fair use and copyleft.** Can fair use be a defense to a claim that someone violated GPL terms? Technically yes (fair use is a defense to infringement), but no court has addressed this in the copyleft context.

## Sources

- 17 U.S.C. § 107 (fair use)
- Oracle v. Google, 593 U.S. 1 (2021)
- Sega v. Accolade, 977 F.2d 1510 (9th Cir. 1992)
- Sony v. Connectix, 203 F.3d 596 (9th Cir. 2000)
