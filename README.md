<div align="center">

# Spider-Man 2 — Xbox Recomp

### Experimental native recompilation for modern Windows

SM2-Recomp is an unofficial project that recompiles the original Xbox release of Spider-Man 2 for native execution on modern Windows systems.

**Early Development · In-Game · Bug fixes ongoing**

**https://sm2-recomp.app**

</div>

---

## About

**SM2-Recomp** is an experimental native recompilation project for the original Xbox version of Spider-Man 2.

The project translates code from a user-supplied original Xbox executable into native code and provides the Xbox-facing runtime behaviour needed by the game on modern Windows systems.

The project does not distribute the original Spider-Man 2 Xbox executable, original game data, or extracted game media assets. A compatible copy of the original Xbox release is required.

Development is still active. Current builds have demonstrated sustained in-game execution through at least Chapters 1–3 during testing, and the major rendering corruption seen during early development has been resolved.

Broader game compatibility, save behaviour, rendering edge cases, and later-game stability are still being validated.

> **SM2-Recomp is experimental software and is not yet considered release-ready.**

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
| Mouse input | 🔴 Not Implimented |
| Audio | 🟢 Functional |
| Runtime stability | 🟢 Stable through tested Chapters 1–3 |
| Save system | 🟢 Implimented |

Current internal builds are capable of sustained in-game execution, with the major graphical render issues of earlier builds resolved.

Testing through **Chapters 1–3** has so far shown stable runtime behaviour. However, later portions of the game have not yet been validated to the same extent, and additional compatibility issues may still be discovered as testing progresses.

The **save system currently contains a known bug** and remains one of the primary issues requiring further development.

The present focus is on **game-wide validation, save functionality and remaining compatibility issues rather than initial bring-up**.

---

## Development Progress

SM2-Recomp has progressed rapidly from initial executable analysis and recompilation to sustained in-game execution.

So far work has progressed through:

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

Runtime testing has also progressed through at least **Chapters 1–3**, with current builds appearing to remain stable throughout the tested sections.

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

## Save System

The save system has been under active investigation.

A fix has been implemented for asynchronous save-file read behaviour that differed from the original Xbox environment. Broader validation is still ongoing, so save functionality should currently be treated as experimental.

---

## Technical Overview

SM2-Recomp uses static recompilation.

The build process analyses a user-supplied Spider-Man 2 Xbox executable and uses that input to generate native code locally. The repository itself does not need to contain a copy of the original XBE.

A compatibility runtime supplies the Xbox kernel services and hardware-facing functionality expected by the game, while modern implementations provide graphics, audio, input, and host integration.

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

SM2-Recomp builds on XboxRecomp by sp00nznet and its contributors.

XboxRecomp provides the underlying Xbox static-recompilation toolchain and runtime components used during the build and execution process.

SM2-Recomp adds Spider-Man 2-specific integration, compatibility work, graphics behaviour, input and audio fixes, launcher functionality, diagnostics, and title-specific runtime handling.

XboxRecomp and its third-party components remain subject to their own upstream licences.

Upstream project:

https://github.com/sp00nznet/xboxrecomp

See THIRD_PARTY_NOTICES.md for attribution and licensing details.

---

## Original Game Required

SM2-Recomp does **not** include or distribute:

- the original Spider-Man 2 Xbox executable
- original game data archives
- extracted textures, models, audio, video, or other game media
- a complete copy of the original game

Users must provide the required game files separately from a copy to which they have lawful access.

The current build process expects a compatible Xbox executable and the corresponding game data.

SM2-Recomp does not grant any rights in Spider-Man 2 or other third-party game material.


---

## Current Priorities

Development is currently focused on:

1. Animation and additional render bugs
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

SM2-Recomp is a development project, not a finished PC port.

Current builds are capable of sustained in-game execution, and major rendering issues affecting earlier builds have been resolved. Testing of later portions of the game is still ongoing, and undiscovered compatibility issues should be expected.

Development milestones and public release information will be documented through the project's official channels.

---

## Source Availability

SM2-Recomp's original project code and project-owned assets will initially be released under the SM2-Recomp Source-Available Personal Use License.

This initial licence is intended to support public access to the source for personal use, study, experimentation, private modification, and contribution while the project remains under active development.

The licensing model may change as SM2-Recomp matures and reaches a more stable state. Future versions of SM2-Recomp may therefore be released under different or more permissive licence terms.

Any future change in licensing will apply as stated to the relevant release and does not, by itself, alter the licence terms that applied to an earlier copy or version when it was provided.

Redistribution and other uses of SM2-Recomp Project Materials are governed by LICENSE.md.

Third-party components are not relicensed under the SM2-Recomp licence and remain subject to their respective upstream licences.

See:

- LICENSE.md
- THIRD_PARTY_NOTICES.md

---

## Disclaimer

SM2-Recomp is an unofficial, fan-developed project.

It is not affiliated with, authorised by, sponsored by, or endorsed by Activision, Treyarch, Marvel, Microsoft, or any other rights holder associated with Spider-Man 2.

Spider-Man, Spider-Man 2, Xbox, and all other third-party names, characters, trademarks, game content, and intellectual property remain the property of their respective rights holders.

The SM2-Recomp licence applies only to material for which the SM2-Recomp licensor has authority to grant rights. Third-party material remains subject to its own applicable rights and licence terms.

---

<div align="center">

**Spider-Man 2 — Xbox Recomp**

*Exploring native recompilation of the original Xbox release on modern Windows.*

</div>
