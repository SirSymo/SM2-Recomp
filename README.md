<div align="center">

# Spider-Man 2 — Xbox Recomp

### Experimental native recompilation for modern Windows

Recompiling the original Xbox release of **Spider-Man 2** for native execution on modern Windows systems.

**Early Development · In-Game · Major Rendering Issues Resolved · Stability Testing Ongoing**

</div>

---

## About

**SM2-Recomp** is an experimental native recompilation project for the original Xbox version of *Spider-Man 2*, targeting modern Windows systems.

The project aims to execute the original game code natively while recreating the Xbox runtime and hardware-facing behaviour required by the game on modern PC hardware.

Development remains at an early stage, but the project has progressed significantly beyond initial in-game execution. Major graphical glitches encountered during early development have now been resolved, and current builds have demonstrated stable gameplay through at least **Chapters 1–3** during testing.

Rendering accuracy, broader game compatibility and remaining runtime functionality are still being validated.

One known issue currently affects the **save system** and requires further investigation and correction.

> **This project is under active development and is not yet considered release-ready.**

---

## Development Status

| Component | Status |
|---|---|
| Recompiled game execution | ✅ In-game |
| Xbox runtime / kernel compatibility | 🟡 In development |
| XBE loading | 🟢 Implemented |
| Direct3D 11 rendering | 🟢 Functional |
| Software rendering path | 🟢 Functional |
| Texture & render-target handling | 🟢 Functional |
| Controller input | 🟢 Functional |
| Keyboard input | 🟢 Functional |
| Audio | 🟢 Functional |
| Runtime stability | 🟢 Stable through tested Chapters 1–3 |
| Save system | 🔴 Known issue |

Current internal builds are capable of sustained in-game execution, with the major graphical corruption present during earlier development now resolved.

Testing through **Chapters 1–3** has so far shown stable runtime behaviour. However, later portions of the game have not yet been validated to the same extent, and additional compatibility issues may still be discovered as testing progresses.

The **save system currently contains a known bug** and remains one of the primary issues requiring further development.

The present focus is on **game-wide validation, save functionality and remaining compatibility issues rather than initial bring-up**.

---

## Development Progress

SM2-Recomp has progressed rapidly from initial executable analysis and recompilation to sustained in-game execution.

Within the project's **first five days of development**, work progressed through:

- Xbox executable analysis and recompilation
- Xbox kernel/runtime bring-up
- Game initialization
- Graphics initialization
- Game-data handling
- Audio implementation
- Controller and keyboard input
- Software rendering
- Direct3D 11 GPU rendering
- In-game execution
- Runtime diagnostics and profiling

Development since then has focused heavily on correcting rendering behaviour and improving runtime compatibility.

Major graphical glitches affecting early builds have now been resolved, allowing substantially more accurate in-game rendering.

Runtime testing has also progressed through at least **Chapters 1–3**, with current builds remaining stable throughout the tested sections.

Further testing is required across the remainder of the game to identify any additional runtime, rendering or compatibility issues.

---

## Rendering

Graphics compatibility has been one of the project's primary areas of development.

SM2-Recomp includes a **Direct3D 11 rendering backend** that translates the rendering behaviour expected by the original Xbox title to modern Windows graphics hardware.

Graphics implementation includes support for:

- Triangle rasterisation
- Depth testing
- Alpha blending
- Texture sampling
- Alpha testing
- Fog
- Render targets
- Xbox graphics-state translation
- Register-combiner behaviour
- Visibility and occlusion behaviour
- Framebuffer and presentation handling

A software rendering path is also available for development, comparison and fallback behaviour.

The major graphical corruption encountered during earlier development has now been resolved, and current builds are capable of rendering gameplay correctly across the portions of the game tested so far.

Rendering work is not considered completely finished. Additional edge cases, effects or game-specific behaviour may still be discovered as testing expands into later chapters and less frequently encountered rendering paths.

---

## Stability

Runtime stability has improved substantially.

Current builds have been tested through at least **Chapters 1–3** without the significant runtime instability encountered during earlier development.

This represents an important milestone, although it does not yet guarantee stability across the entire game.

As additional chapters, missions, cutscenes and gameplay systems are tested, previously unexercised interactions between the original game and the recreated Xbox environment may expose further compatibility issues.

The project includes diagnostic infrastructure for investigating these issues, including:

- Runtime logging
- Graphics tracing
- Frame-level diagnostics
- Kernel-call diagnostics
- Performance profiling
- Rasteriser statistics
- Crash and stability investigation tools

These systems continue to be used for game-wide compatibility testing and regression investigation.

---

## Save System

The save system currently contains a **known bug** and is one of the primary outstanding issues.

While gameplay execution and runtime stability have improved significantly, save functionality is not yet considered reliable.

Investigation is ongoing into the interaction between the original game's save behaviour and the recreated Xbox runtime environment.

Until this issue is resolved, users should not assume that game progress can be saved or restored correctly.

---

## Technical Overview

SM2-Recomp uses **static recompilation** to translate the original Xbox game's x86 code for execution on modern Windows systems.

A compatibility runtime provides the Xbox kernel services and hardware-facing functionality expected by the original executable, while modern implementations provide graphics, audio and input functionality.

### Current Technology

| | |
|---|---|
| **Original Platform** | Microsoft Xbox |
| **Target Platform** | Modern Windows |
| **Language** | C++20 |
| **Build System** | CMake |
| **Graphics** | Direct3D 11 / Software |
| **Controller Input** | XInput |
| **Development Status** | Experimental |

Development includes a dedicated Windows launcher and supporting analysis, diagnostic and recompilation tooling.

---

## XboxRecomp

SM2-Recomp was initially bootstrapped using foundational Xbox kernel and runtime work from the **XboxRecomp** project by sp00nznet.

This provided an important starting point for executing recompiled Xbox software, with additional Spider-Man 2-specific runtime, graphics, input, audio and compatibility work being developed for this project specifically.

Proper attribution and upstream project links will be maintained as the project develops.

---

## Source Code & Builds

The source code and development builds are **not currently publicly available**.

Development is presently focused on validating the game beyond the currently tested chapters, resolving the save-system issue and identifying any remaining runtime or compatibility problems before the project is opened for broader testing and development.

The intention is to make SM2-Recomp available once it reaches a sufficiently reliable baseline for testing, experimentation and contribution.

**No release date is currently being announced.**

---

## Original Game Required

SM2-Recomp does **not** contain or distribute *Spider-Man 2*, its original Xbox executable, or copyrighted game assets.

A compatible copy of the original Xbox game data will be required to use the project.

Users are responsible for supplying game data from their own copy of the original release.

---

## Current Priorities

Development is currently focused on:

1. Fixing the save-system bug
2. Testing stability beyond Chapters 1–3
3. Validating game-wide rendering correctness
4. Identifying remaining Xbox runtime compatibility issues
5. Testing later missions, cutscenes and gameplay systems
6. Validating controller, keyboard and gameplay input behaviour
7. Testing audio behaviour across the full game
8. Establishing a stable baseline for broader testing

---

## Project Status

> **Experimental — Active Development**

SM2-Recomp is currently a development project rather than a finished PC port.

The project is capable of sustained in-game execution, and the major graphical glitches affecting earlier builds have been resolved.

Current testing has demonstrated stable gameplay through at least **Chapters 1–3**. Testing of later portions of the game remains ongoing, so undiscovered compatibility issues may still exist.

The primary known functional issue at present is the **save system**, which requires further development before save functionality can be considered reliable.

Development progress and significant milestones will continue to be documented here as the project advances.

---

## Disclaimer

SM2-Recomp is an unofficial, fan-developed project and is not affiliated with or endorsed by Activision, Treyarch, Marvel, Microsoft or any other rights holder associated with *Spider-Man 2*.

All trademarks, characters, game content and other copyrighted materials belong to their respective owners.

SM2-Recomp does not distribute copyrighted game content and is intended to operate using game data supplied separately by the user.

---

<div align="center">

**Spider-Man 2 — Xbox Recomp**

*Preserving the original Xbox release through native recompilation.*

</div>
