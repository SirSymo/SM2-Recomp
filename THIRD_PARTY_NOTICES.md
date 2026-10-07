# SM2-Recomp Third-Party Notices

SM2-Recomp includes, uses, or builds upon software and assets created by third parties.

The SM2-Recomp Source-Available Personal Use License applies only to material for which Sir Symo, also known as Symo, owns the copyright or otherwise has authority to grant rights.

Third-party material remains subject to its own copyright notices and licence terms. Nothing in the SM2-Recomp licence replaces, restricts, or overrides rights granted under an applicable third-party licence.

## XboxRecomp

Project:

https://github.com/sp00nznet/xboxrecomp

SM2-Recomp uses XboxRecomp as its Xbox static-recompilation and runtime base.

The SM2-Recomp source package does not contain a complete copy of the XboxRecomp source tree. The build process obtains and uses XboxRecomp separately.

XboxRecomp currently identifies:

- most XboxRecomp code as MIT licensed
- xemu-derived MCPX APU source under src/apu as LGPL-2.1-or-later
- src/nv2a/nv2a_regs.h as LGPL-2.1-or-later

The exact list of upstream third-party files and copyright holders is maintained by XboxRecomp in its NOTICE file.

XboxRecomp's MIT-licensed material remains under the MIT License.

XboxRecomp's LGPL-covered material remains under LGPL-2.1-or-later.

Compiled SM2-Recomp builds may contain linked XboxRecomp runtime code. Any such third-party code remains subject to its applicable upstream licence regardless of the licence applied to independently authored SM2-Recomp code.

Upstream licensing information:

https://github.com/sp00nznet/xboxrecomp/blob/main/LICENSE

https://github.com/sp00nznet/xboxrecomp/blob/main/NOTICE

https://github.com/sp00nznet/xboxrecomp/tree/main/LICENSES

## NV2A Register-Combiner Code

Relevant SM2-Recomp files include:

- tools/sm2gpu/rc_body.hlsl
- tools/sm2gpu/sm2_gpu_ps.inc

The source file rc_body.hlsl identifies its register-combiner implementation as a port of nv2a_combiner.c.

The generated sm2_gpu_ps.inc file contains generated shader data based on the HLSL sources.

These portions are treated as third-party-derived material rather than exclusively licensed SM2-Recomp Project Materials.

Where the originating implementation is XboxRecomp MIT-licensed code, the applicable XboxRecomp copyright and MIT licence terms continue to apply.

The exact originating upstream file and revision should be retained in the project history when that provenance is finalised.

## Barlow Font Family

Files:

- assets/fonts/Barlow-Medium.ttf
- assets/fonts/Barlow-Regular.ttf
- assets/fonts/BarlowCondensed-SemiBold.ttf
- assets/fonts/BarlowSemiCondensed-Medium.ttf
- assets/fonts/BarlowSemiCondensed-SemiBold.ttf
- assets/fonts/OFL.txt

Copyright:

Copyright 2017 The Barlow Project Authors.

Licence:

SIL Open Font License 1.1.

The complete licence supplied with SM2-Recomp is located at:

assets/fonts/OFL.txt

The Barlow font files are not licensed under the SM2-Recomp Source-Available Personal Use License.

Upstream project:

https://github.com/jpt/barlow

## Lucide and Feather Icons

Files:

- assets/images/ui_icons.png
- assets/images/ui_icons-LICENSE.txt

The SM2-Recomp icon sheet contains Lucide icons, including icons derived by Lucide from the Feather project.

Lucide:

Copyright (c) 2026 Lucide Icons and Contributors.

Licence: ISC License.

Feather-derived icons:

Copyright (c) 2013-present Cole Bemis.

Licence: MIT License.

The complete notices supplied with SM2-Recomp are located at:

assets/images/ui_icons-LICENSE.txt

The icon artwork remains subject to those licences and is not relicensed under the SM2-Recomp Source-Available Personal Use License.

Lucide licensing information:

https://lucide.dev/license

## Mark Adler puff / DEFLATE Reference Code

Relevant SM2-Recomp file:

- src/app/main.cpp

Portions of the compact DEFLATE decoder used by the launcher are based on Mark Adler's puff reference implementation.

Upstream work:

puff.c and puff.h from the zlib project.

Copyright:

Copyright (C) 2002-2013 Mark Adler.

The puff source uses a zlib-style licence that permits use, modification, and redistribution subject to its stated conditions, including preservation of the applicable notice in source distributions and clear identification of altered source versions.

The SM2-Recomp implementation is modified and integrated into the launcher.

Upstream reference:

https://github.com/madler/zlib/tree/develop/contrib/puff

This attribution applies only to the portions derived from puff. It does not apply the puff licence to unrelated portions of src/app/main.cpp.

## Build-Time Tools and Dependencies

The SM2-Recomp build process may obtain or use external development tools and dependencies such as:

- CMake
- Ninja
- LLVM/MinGW
- Python
- Capstone
- XboxRecomp
- Microsoft Visual Studio Build Tools

These tools are not relicensed by SM2-Recomp.

Merely downloading or invoking a build tool does not make that tool part of the SM2-Recomp Project Materials. If a future release directly redistributes files from one of these projects, the applicable third-party licence and notice requirements must also be followed.

## Spider-Man 2 and Original Game Material

Spider-Man 2 and its original executable code, game data, artwork, textures, models, audio, video, scripts, text, characters, trademarks, and other original game material are third-party intellectual property.

SM2-Recomp does not grant any rights in original Spider-Man 2 material.

The project is designed to operate using game files supplied separately by the user.

The source package includes title-specific technical metadata used for compatibility and recompilation, such as executable layout information, addresses, and import information. This does not grant any ownership or distribution rights in the underlying original game.

Activision, Treyarch, Marvel, Microsoft, Xbox, Spider-Man, Spider-Man 2, and other third-party names, marks, characters, and properties remain the property of their respective rights holders.

SM2-Recomp is unofficial and is not affiliated with or endorsed by those rights holders.

## Licence Priority

Third-party material is not relicensed merely because it is included in, linked with, generated into, or used by SM2-Recomp.

If the SM2-Recomp Source-Available Personal Use License and a third-party licence appear to conflict with respect to third-party material, the applicable third-party licence controls for that material.

Copyright notices and licence notices belonging to third parties must be preserved where required by their respective licences.

---

SM2-Recomp

Copyright © 2026 Sir Symo (also known as Symo).

This notice does not alter the terms of any third-party licence.
