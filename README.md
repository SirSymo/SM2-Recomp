 
<div align="center">

# Spider-Man 2 — Xbox Recomp

### Experimental native recompilation for modern Windows

SM2-Recomp is an unofficial project that recompiles the original Xbox release of Spider-Man 2 for native execution on modern Windows systems.

**Early Development · In-Game · Compatibility and performance improvements ongoing**

**https://sm2-recomp.app**

</div>

---

## About

**SM2-Recomp** is an experimental native recompilation project for the original Xbox version of Spider-Man 2.

The project translates code from a user-supplied original Xbox executable into native code and provides the Xbox-facing runtime behaviour needed by the game on modern Windows systems.

The project does not distribute the original Spider-Man 2 Xbox executable, original game data, or extracted game media assets. A compatible copy of the original Xbox release is required.

Development is still active. Current builds have demonstrated sustained in-game execution through at least Chapters 1–3 during testing, and the major rendering corruption seen during early development has been resolved.

Recent development has introduced **XISO-based game-data streaming as the default method**, internal rendering resolution options up to 4K, initial mouse-look support, improved keyboard controls, and fixes for save/load functionality, animation timing, and gameplay behaviour.

Broader game compatibility, performance, rendering edge cases, and later-game stability are still being validated.

> **SM2-Recomp is experimental software and is not yet considered release-ready.**

---

## Development Status

| Component | Status |
|---|---|
| Recompiled game execution | ✅ In-game |
| Xbox runtime / kernel compatibility | 🟡 In development |
| XBE loading | 🟢 Implemented |
| XISO game-data streaming | 🟢 Implemented — Default |
| Legacy extracted-asset loading | 🟡 Available — Known compatibility issues |
| Direct3D 11 rendering | 🟢 Functional |
| Software rendering path | 🟢 Functional |
| Texture & render-target handling | 🟢 Functional |
| Internal rendering resolutions | 🟢 Native through 4K |
| Controller input | 🟢 Functional |
| Keyboard input | 🟢 Functional |
| Mouse input / mouse-look | 🟡 Implemented — Improvements ongoing |
| Audio | 🟡 Functional - Known issues including crackle under investigation |
| Save/load system | 🟢 Fixes implemented — Validation ongoing |
| Render distance settings | 🟡 Initial implementation — Not functional |
| Frame timing / performance | 🟡 Improvements required |
| Intro cutscene / shadow rendering | 🟡 Known rendering issues |
| Runtime stability | 🟢 Stable through tested Chapters 1–3 |

Current internal builds are capable of sustained in-game execution, with the major graphical rendering issues of earlier builds resolved.

Testing through **Chapters 1–3** has so far shown stable runtime behaviour. However, later portions of the game have not yet been validated to the same extent, and additional compatibility issues may still be discovered as testing progresses.

Recent fixes have addressed previously identified save/load problems, animation timing and cycling issues, and gameplay bugs. These changes are implemented but remain subject to broader testing.

Mouse-look functionality and improved keyboard controls have also been introduced, although the current implementations require further refinement.

The present focus is on **remaining rendering glitches, frame timing, performance, and game-wide compatibility validation rather than initial boot-up**.

---

## Development Progress

SM2-Recomp has progressed rapidly from initial executable analysis and recompilation to sustained in-game execution.

So far work has progressed through:

- Xbox executable analysis and recompilation
- Xbox kernel/runtime bring-up
- Game initialization
- Graphics initialization
- Game-data handling and XISO streaming
- Audio implementation
- Controller and keyboard input
- Initial mouse-look implementation
- Software rendering
- Direct3D 11 GPU rendering
- Internal rendering resolution options up to 4K
- Save/load system implementation and fixes
- Animation timing and gameplay fixes

Development since then has focused heavily on correcting rendering behaviour, improving runtime compatibility, and resolving gameplay issues.

Major graphical glitches affecting early builds have now been resolved, allowing substantially more accurate in-game rendering.

The game-data loading system has also been updated to use **XISO streaming by default**, replacing the previous reliance on extracted game assets.

The original extracted-asset method remains available as a fallback, but is known to cause unintended execution of game code and persistent gameplay issues. XISO streaming is therefore the recommended and primary method.

Runtime testing has progressed through at least **Chapters 1–3**, with current builds appearing to remain stable throughout the tested sections.

Further testing is required across the remainder of the game to identify additional runtime, rendering, performance, or compatibility issues.

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
- Configurable internal rendering resolutions

Internal rendering resolution options now range from the game's native resolution through to **4K**, allowing higher-resolution rendering on modern hardware.

These options affect internal rendering resolution and do not currently provide widescreen or ultra-widescreen aspect-ratio support.

A software rendering path is also available for development, comparison and fallback behaviour.

The major graphical corruption encountered during earlier development has now been resolved, and current builds are capable of substantially correct gameplay rendering across the portions tested so far.

Rendering work is not considered completely finished. **Intro cutscene rendering glitches and shadow-related graphical issues remain known problems**, alongside frame timing and frame-rate limitations.

An initial render-distance configuration option has also been added, although it does not yet produce the intended functional results.

---

## Save System

The save/load system has received further fixes, addressing previously identified issues with save-file handling and asynchronous read behaviour that differed from the original Xbox environment.

Both saving and loading are now implemented with these fixes in place.

Broader validation is still ongoing, particularly across later missions and longer gameplay sessions. Save functionality should therefore continue to be treated as experimental until testing confirms its reliability throughout the game.

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
| **Game-Data Streaming** | XISO (Default) |
| **Legacy Game-Data Loading** | Extracted assets (Fallback) |
| **Controller Input** | XInput |
| **Keyboard / Mouse Input** | Implemented — Experimental |
| **Internal Resolution** | Native through 4K |
| **Development Status** | Experimental |


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
- original game data archives or disc images
- extracted textures, models, audio, video, or other game media
- a complete copy of the original game

Users must provide the required game files separately from a copy to which they have lawful access.

The current build process requires a compatible Xbox executable and corresponding game data.

**XISO-based game-data streaming is now the default runtime method.** The previous extracted-asset loading method remains available as a legacy fallback but is not recommended due to known compatibility and gameplay issues.

SM2-Recomp does not grant any rights in Spider-Man 2 or other third-party game material.

---

## Current Priorities

Development is currently focused on:

1. Resolving intro cutscene and shadow rendering glitches
2. Improving frame timing, frame pacing, and overall performance
3. Validating recent save/load and gameplay fixes
4. Testing stability beyond Chapters 1–3
5. Validating game-wide rendering correctness
6. Identifying remaining Xbox runtime compatibility issues
7. Testing later missions, cutscenes, and gameplay systems
8. Refining mouse-look, keyboard, and controller input behaviour
9. Testing audio behaviour across the full game and imporving correctness
10. Establishing a stable baseline for the initial v0.1 release

---

## Development Roadmap

### Target: v0.1

The initial v0.1 milestone is focused on establishing a more reliable and functional gameplay baseline, rather than delivering every planned enhancement.

**Implemented / Under Validation**

- Save/load system fixes
- Animation timing and cycling fixes
- Gameplay bug fixes
- XISO compatibility and default game-data streaming
- Internal rendering resolution options from native through 4K
- Initial mouse-look support and improved keyboard controls

These features have been implemented, although some remain subject to wider testing and further refinement.

**Remaining v0.1 Requirements**

- Resolve intro cutscene rendering glitches
- Resolve remaining shadow rendering glitches
- Improve frame timing, frame pacing, and frame-rate performance

**Additional Features Under Investigation**

- Functional render-distance configuration (initial option added, but not yet working as intended)

### Beyond v0.1

Future development goals include:

- Widescreen and ultra-widescreen support, including correct UI scaling and positioning
- Further improvements to mouse input, mouse-look, and keyboard controls
- Configurable 60, 120, and 144 FPS limits, alongside an unlocked frame-rate option
- VSync support
- Further frame timing and frame-pacing improvements
- Mod integration and support for simple gameplay modifications
- Cheat functionality and implementation

Early investigation into mod and cheat integration is already underway, including identifying suitable game-code functions and integration points for cheats such as invulnerability (god mode) and unlimited Reflex (slow-motion) behaviour.

These capabilities are exploratory and are not currently considered implemented features.

Roadmap items and priorities may change as additional compatibility issues are discovered during development.

---

## Project Status

> **Experimental — Active Development**

SM2-Recomp is a development project, not a finished PC port.

Current builds are capable of sustained in-game execution, and major rendering issues affecting earlier builds have been resolved.

Recent development has introduced XISO streaming, higher internal rendering resolution options, input improvements, and multiple gameplay and runtime fixes.

Remaining work includes rendering glitches, frame timing and performance improvements, input refinement, and continued game-wide compatibility testing.

Testing of later portions of the game is still ongoing, and undiscovered compatibility issues should be expected.

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
