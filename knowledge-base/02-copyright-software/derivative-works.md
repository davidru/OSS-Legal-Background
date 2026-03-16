# Derivative Works in Software

> Last updated: 2026-03-15

## Summary

The concept of "derivative work" is the fulcrum of copyleft licensing. The GPL and similar licenses require that "derivative works" be distributed under the same license terms. But what constitutes a derivative work of software is one of the most contested and unresolved questions in open source law.

Under US copyright law, a "derivative work" is "a work based upon one or more preexisting works, such as a translation, musical arrangement, dramatization, fictionalization, motion picture version, sound recording, art reproduction, abridgment, condensation, or any other form in which a work may be recast, transformed, or adapted" (17 U.S.C. § 101). Applying this definition to software — particularly to questions of linking, loading, and interaction between programs — has proven deeply contentious.

## Key Principles

- A derivative work must incorporate protectable expression from the original work (not just ideas or functional elements)
- Merely using a program does not create a derivative work of it
- Modifying source code clearly creates a derivative work
- The harder questions involve linking, compilation, and runtime interaction between separately-written programs
- The GPL's definition of "work based on the Program" is broader than the copyright law definition of "derivative work" — creating a gap between legal and license requirements

## The Linking Debate

### The Core Question
Does a proprietary program that links (statically or dynamically) to a GPL-licensed library become a derivative work of that library, triggering copyleft obligations?

### FSF Position
The Free Software Foundation maintains that both static and dynamic linking generally create a "work based on" the GPL library, triggering copyleft. The FSF's position is that the GPL's scope is defined by the license text ("work based on the Program"), not solely by the copyright law definition of "derivative work."

### Industry/Practitioner Position
Many practitioners (including Heather Meeker, Lawrence Rosen, and others) argue that dynamic linking does not create a derivative work under copyright law, because the calling program does not incorporate protectable expression from the library — it merely uses the library's functional interface. Under this view, the GPL can only extend as far as copyright law's derivative work concept.

### The Unresolved Middle Ground
- **Static linking:** Generally considered more likely to create a derivative work (the library code is physically incorporated into the binary)
- **Dynamic linking:** Contested — the program calls the library at runtime but does not contain the library's code
- **IPC/sockets/pipes:** Generally considered not to create a derivative work (separate processes communicating via interfaces)
- **Kernel modules:** Highly contested — the Linux kernel's MODULE_LICENSE() macro distinguishes between GPL and proprietary modules

## Case Law

No court has squarely decided the linking question in the GPL context. The relevant case law comes from general software derivative works analysis:

### Micro Star v. Formgen, 154 F.3d 1107 (9th Cir. 1998)
- **Citation:** 154 F.3d 1107 (9th Cir. 1998)
- **Holding:** User-created levels for the game Duke Nukem 3D were derivative works because they incorporated the game's protected audiovisual elements when played.
- **Relevance:** Suggests that programs designed to interoperate with and depend upon another program can be derivative works, even if they don't contain the original program's literal code.

### Galoob v. Nintendo, 964 F.2d 965 (9th Cir. 1992)
- **Citation:** 964 F.2d 965 (9th Cir. 1992)
- **Holding:** The Game Genie device, which modified Nintendo games' output without altering the underlying code, did not create derivative works.
- **Relevance:** Suggests that modifying a program's behavior at runtime (without changing its code) does not create a derivative work.

## Commentary & Analysis

### Eben Moglen, "The GPL and Derivative Works"
- **Source:** FSF/SFLC publications
- **Key Arguments:** The GPL's concept of "work based on the Program" is intentionally broader than the copyright law definition. The license creates a contractual scope that extends beyond what copyright alone would require.

### Lawrence Rosen, "Open Source Licensing" (2004), Chapter 5
- **Source:** Prentice Hall
- **Key Arguments:** Strongly argues that dynamic linking does not create a derivative work. The copyright law definition should control, not the FSF's expansive interpretation. If there's no copying of protectable expression, there's no derivative work.

### Heather Meeker, "Open Source for Business" (3rd ed., 2020)
- **Source:** Self-published
- **Key Arguments:** Takes a pragmatic middle position. Notes the legal uncertainty and recommends that companies design their architectures to avoid the question where possible. Provides practical guidance on how to structure software integration to minimize copyleft risk.

### Pamela Samuelson, "The Strange Odyssey of Software Interfaces as Intellectual Property"
- **Source:** Various Berkeley publications
- **Key Arguments:** Interfaces should be unprotectable (functional elements), which would resolve many linking questions — if the interface isn't protectable, then using it can't create a derivative work.

## Practical Guidance

1. **Modification is clear.** If you modify GPL source code, your modified version is a derivative work. Full stop.

2. **Avoid the linking question by architecture.** If possible, separate GPL components from proprietary components using well-defined process boundaries (IPC, sockets, REST APIs). This is the safest approach.

3. **Dynamic linking is defensible but not certain.** Many practitioners believe dynamic linking doesn't create a derivative work, but no court has confirmed this in the GPL context. If you rely on this position, understand the risk.

4. **LGPL was designed for this.** If a library wants to be used by proprietary programs, it should use LGPL, which explicitly permits this use pattern.

5. **The "mere aggregation" exception.** Bundling GPL software alongside proprietary software on the same medium (without integration) is not creating a derivative work. The GPL explicitly permits this.

## Open Questions

- **No court decision on linking.** The central question — does linking create a derivative work? — has never been decided by a court in the GPL context. This is the biggest open question in open source law.
- **Modern architectures.** How does the derivative work analysis apply to containers, microservices, serverless functions, and other modern deployment patterns?
- **AI training.** Is a model trained on GPL code a "derivative work" of that code? This would have enormous implications.
- **The contract vs. copyright theory gap.** If the GPL is enforced as a contract (Artifex v. Hancom), the scope of "work based on the Program" could be broader than the copyright law derivative work definition. This gap hasn't been explored in litigation.

## Sources

- 17 U.S.C. § 101 (definition of "derivative work")
- Micro Star v. Formgen, 154 F.3d 1107 (9th Cir. 1998)
- Galoob v. Nintendo, 964 F.2d 965 (9th Cir. 1992)
- Eben Moglen, "The GPL and Derivative Works"
- Lawrence Rosen, *Open Source Licensing* (2004)
- Heather Meeker, *Open Source for Business* (3rd ed., 2020)
