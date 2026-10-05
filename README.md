<div align="center">

# Spider-Man 2 — Xbox Recomp

### Experimental native recompilation for modern Windows

Recompiling the original Xbox release of **Spider-Man 2** for native execution on modern Windows systems.

**Early Development · In-Game · Rendering & Stability Work in Progress**

</div>

---

## About

**SM2-Recomp** is an experimental native recompilation project for the original Xbox version of *Spider-Man 2*, targeting modern Windows systems.

The project aims to execute the original game code natively while recreating the Xbox runtime and hardware-facing behaviour required by the game on modern PC hardware.

Development is currently at an early stage. The recompiled game is capable of reaching **in-game execution**, representing a major initial milestone, but significant graphical issues and runtime instability remain.

Rendering accuracy, Xbox graphics compatibility and overall stability are the current development priorities.

> **This project is under active development and is not currently considered playable.**

---

## Development Status

| Component | Status |
|---|---|
| Recompiled game execution | ✅ In-game |
| Xbox runtime / kernel compatibility | 🟡 In development |
| XBE loading | 🟢 Implemented |
| Direct3D 11 rendering | 🟡 In development |
| Software rendering path | 🟡 In development |
| Texture & render-target handling | 🟡 In development |
| Controller input | 🟡 In development |
| Keyboard input | 🟡 In development |
| Audio | 🟡 In development |
| Runtime stability | 🔴 Early development |

Current internal builds can execute the game environment, but users should expect significant rendering errors, incomplete graphical behaviour and crashes.

The present focus is **correctness and stability rather than release readiness**.

---

## Development Progress

SM2-Recomp has progressed rapidly from initial executable analysis and recompilation to in-game execution.

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

Reaching the game environment is an important milestone, but substantial engineering work remains before the recompilation accurately reproduces the behaviour of the original Xbox release.

---

## Rendering

Graphics compatibility is currently one of the project's primary areas of development.

SM2-Recomp includes an experimental **Direct3D 11 rendering backend** intended to translate the rendering behaviour expected by the original Xbox title to modern Windows graphics hardware.

Current graphics development includes work on:

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

A software rendering path is also used for development, comparison and fallback behaviour.

The game can currently render in-game scenes; however, **rendering is not yet accurate**. Significant graphical corruption, missing or incorrect effects and other visual issues remain under investigation.

---

## Stability

Runtime stability remains an active area of development.

As progressively more of the original game becomes executable, additional interactions between the game and the recreated Xbox environment are exposed. Some of this behaviour is incomplete or not yet accurately reproduced.

Current development builds may therefore crash or encounter unexpected behaviour during execution.

The project includes diagnostic infrastructure for investigating these issues, including:

- Runtime logging
- Graphics tracing
- Frame-level diagnostics
- Kernel-call diagnostics
- Performance profiling
- Rasteriser statistics
- Crash and stability investigation tools

These systems are being used to progressively improve runtime correctness.

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

## XboxDecomp

SM2-Recomp was initially bootstrapped using foundational Xbox kernel and runtime work from the **XboxDecomp** project.

This provided an important starting point for executing recompiled Xbox software, with additional Spider-Man 2-specific runtime, graphics, input, audio and compatibility work being developed as the project progresses.

Proper attribution and upstream project links will be maintained as the project develops.

---

## Source Code & Builds

The source code and development builds are **not currently publicly available**.

Development is presently focused on improving rendering accuracy and runtime stability before the project is opened for broader testing and development.

The intention is to make SM2-Recomp available once it reaches a more useful baseline for testing, experimentation and contribution.

**No release date is currently being announced.**

---

## Original Game Required

SM2-Recomp does **not** contain or distribute *Spider-Man 2*, its original Xbox executable, or copyrighted game assets.

A compatible copy of the original Xbox game data will be required to use the project.

Users are responsible for supplying game data from their own copy of the original release.

---

## Current Priorities

Development is currently focused on:

1. Improving rendering correctness
2. Improving Xbox graphics compatibility
3. Identifying and resolving in-game crashes
4. Improving overall runtime stability
5. Validating controller and gameplay input
6. Improving audio and runtime compatibility
7. Establishing a stable baseline for broader testing

---

## Project Status

> **Experimental — Active Development**

SM2-Recomp is currently a development project rather than a finished PC port.

In-game execution has been achieved, but significant rendering and stability work remains. Current builds should be expected to contain graphical errors, crashes, incomplete functionality and behaviour that differs from the original Xbox release.

Development progress and significant milestones will be documented here as the project advances.

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
