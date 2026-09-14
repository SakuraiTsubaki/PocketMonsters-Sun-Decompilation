# Pokémon Sun — Reverse-Engineering Source Inventory

## Purpose

This file inventories public reverse-engineering, format, tooling, save, model, graphics, and platform sources relevant to Pokémon Sun. It is not limited to Pokémon-specific tools: Nintendo 3DS container/runtime documentation and general 3DS tooling are also part of the evidence base.

The existence of a parser/editor does not automatically prove a format interpretation is complete or correct. Each tool/source must be traced to the specific file types, game versions, source revisions, and assumptions it implements.

## A. Pokémon-specific ROM/data tooling

### pk3DS

Repository:

- https://github.com/kwsch/pk3DS

Known directly relevant domains:

- GARC handling
- Trainer data
- Wild encounters
- Personal data
- Pokémon stats/types/abilities
- TM compatibility
- Move data
- Level-up moves
- Egg moves
- Evolutions
- TM move lists
- Special marts
- game configuration / GARC references
- Battle Royal / Battle Tree-related editors or readers in historical versions
- static encounters and other Gen VII data handlers in historical/current source

Required exhaustive sweep:

- [ ] current source tree
- [ ] complete commit history around Sun/Moon and USUM support
- [ ] tags/releases
- [ ] issues documenting Gen VII file locations and parser failures
- [ ] pull requests with format fixes
- [ ] forks containing abandoned or unmerged Gen VII research
- [ ] Project Pokémon forum release/support thread

## B. Save / legality / event structure

### PKHeX

Repository:

- https://github.com/kwsch/PKHeX

Relevant source areas include:

- `SAV7SM` / Generation VII save classes
- save-block accessors and metadata
- Gen VII personal tables
- encounter tables / legality logic
- Mystery Gift / Wonder Card formats
- region/language handling
- party/box structures
- inventory and Pokédex state
- event flags / blocks where implemented

Required exhaustive sweep:

- [ ] current SM save implementation
- [ ] historical Gen VII introduction commits
- [ ] save-block metadata revisions
- [ ] encounter/legality tables
- [ ] WC7 / mystery-gift handling
- [ ] issues/commits correcting Gen VII offsets or legality assumptions

### PKSM and PKSM-Scripts

Repositories:

- https://github.com/FlagBrew/PKSM
- https://github.com/FlagBrew/PKSM-Scripts

Useful public material already identified:

- Gen VII shortened title IDs
- save-field offsets
- script-oriented save modifications
- USUM/SM documentation history

Required exhaustive sweep:

- [ ] SM offset documentation
- [ ] USUM comparison
- [ ] script files touching Sun/Moon fields
- [ ] historical revisions and comments
- [ ] bridge/service behavior where relevant

### Project Pokémon save research

Initial source:

- https://projectpokemon.org/home/forums/topic/40732-gen-7-save-file-structure/

This thread points back to historical PKHeX source and is part of the provenance chain.

## C. 3DS executable/container/runtime documentation

### 3dbrew — NCCH / CXI / CFA

- https://3dbrew.org/wiki/NCCH

Relevant concepts:

- NCCH container
- executable CXI vs data CFA
- Extended Header
- ExeFS
- RomFS
- product code / region-lock metadata context
- compressed `.code`

### 3dbrew — RomFS

- https://3dbrew.org/wiki/RomFS

Relevant for resource layout and hash/filesystem structure.

### 3dbrew — CRO0 / CRS

- https://www.3dbrew.org/wiki/CRO0

Relevant concepts:

- `.cro` dynamic modules
- `.crs` static-module symbol information
- imports / exports
- relocation
- hash/CRR relationship

### 3dbrew — symbol-bearing titles

- https://3dbrew.org/wiki/Titles_With_Code_Symbols

Critical Pokémon-specific evidence:

- Pokémon Sun/Moon **Special Demo** is documented as containing symbol information in CROs and the ExeFS code binary.

The demo therefore needs a dedicated symbol corpus and comparison map against retail Sun/Moon.

### 3dbrew — patch/update behavior

- https://3dbrew.org/wiki/Title_list/Patches
- https://3dbrew.org/wiki/Filesystem_services

Relevant concepts:

- `0004000E` update-title behavior
- patch ExeFS/RomFS containing updated material
- base/patch mounting behavior
- program access to base vs update RomFS

### 3dbrew — save/extdata containers

- https://3dbrew.org/wiki/Savegames
- https://www.3dbrew.org/wiki/DISA_and_DIFF
- https://www.3dbrew.org/wiki/Inner_FAT
- https://3dbrew.org/wiki/Extdata

Relevant for separating game-specific save structure from the 3DS container/filesystem layer.

Required exhaustive sweep of 3dbrew:

- [ ] NCCH
- [ ] ExeFS
- [ ] RomFS
- [ ] CRO0/CRS/CRR
- [ ] Extended Header
- [ ] SMDH/icon metadata
- [ ] TMD/title/version metadata
- [ ] patch/update behavior
- [ ] Savegames
- [ ] DISA/DIFF
- [ ] Inner FAT
- [ ] Extdata
- [ ] filesystem services
- [ ] relevant title lists and historical revisions

## D. General 3DS extraction/repacking tools

### Project_CTR / ctrtool / makerom

Repositories/public sources:

- https://github.com/3DSGuy/Project_CTR
- historical/forked ProjectCTR trees where needed

ctrtool publicly documents support for:

- ExeFS
- RomFS
- NCCH/CXI/CFA
- Extended Header
- CIA
- NCSD/CCI
- TMD
- tickets
- CRR

makerom documents how NCCH/CXI/CFA/CIA/CCI outputs are composed.

Required sweep:

- [ ] source format structs
- [ ] release history
- [ ] parsing assumptions
- [ ] CRR/CRO-related support
- [ ] metadata/version handling

### 3dstool

- https://github.com/dnasdw/3dstool

Public source implements extraction/creation for CCI/CXI/CFA/ExeFS/RomFS/banner/code and includes region/language handling.

Required sweep:

- [ ] NCCH implementation
- [ ] RomFS implementation
- [ ] ExeFS implementation
- [ ] code compression
- [ ] diff/patch functionality
- [ ] version history around 2016–2019

### 3DSkit

- https://github.com/Tyulis/3DSkit

Relevant public modules include extraction/repacking support for NCCH/ExeFS and GARC, plus multiple Nintendo resource formats.

Required sweep:

- [ ] GARC parser/repacker
- [ ] NCCH/ExeFS support
- [ ] BCLIM/image-related formats
- [ ] font/resource handlers relevant to Pokémon
- [ ] plugin/format history

### ninfs

- https://github.com/ihaveamac/ninfs

Relevant as a public implementation for mounting/extracting 3DS cart images, CIA, NCCH, ExeFS, RomFS, installed title contents and SD data.

## E. Models / graphics / animation

### Ohana3DS Rebirth

- https://github.com/gdkchan/Ohana3DS-Rebirth

Publicly supports viewing/extracting models, textures and some animations from decrypted 3DS game data. Source contains format parsers such as BCH.

Important caveat: individual parsers include completeness/accuracy warnings; parser behavior must be verified per Sun/Moon format revision.

Required sweep:

- [ ] BCH parser
- [ ] texture/image handlers
- [ ] animation handlers
- [ ] Pokémon-specific file support
- [ ] issues documenting Sun/Moon compatibility
- [ ] forks and successor tools

### SPICA

Project Pokémon's 3DS R&D forum records SPICA as a model tool tagged for Ultra Sun/Moon and other 3DS Pokémon titles.

Forum entry point:

- https://projectpokemon.org/home/forums/forum/127-rom-3ds-research-and-development/

Required sweep:

- [ ] original SPICA source/repository if publicly available
- [ ] BCH/model format documentation
- [ ] animation/material/shader support
- [ ] issues/limitations on Sun/Moon assets

## F. Pokémon-specific file-location research

### Project Pokémon GARC-location research

- https://projectpokemon.org/home/forums/topic/39695-solved-sun-and-moon-important-garc-file-locations/

This and linked/replied research is useful for mapping text, story text, trainer data, battle models, overworld models, images, and other GARCs.

Related technical/community areas requiring sweep:

- 3DS ROM Research & Development forum
- 3DS ROM Discussion & Help forum
- translation/modding threads that document otherwise undocumented GARCs
- Battle Tree/Battle Maison restriction research
- overworld/script research
- UI/type/Z-Move graphic research

Community findings remain `Unverified` until tied to direct technical evidence or reproducible source code.

## G. RNG / battle-generation research

Initial Project Pokémon source:

- https://projectpokemon.org/home/forums/topic/40013-sun-moon-rng-manipulation-research-tools/

Required sweep includes:

- encounter RNG
- stationary/event RNG
- egg/breeding RNG
- SOS chain behavior where documented
- PRNG state / algorithm research
- legality implications

## H. Emulator / runtime-source research

Public 3DS emulator source (Citra and forks/successors) may document:

- CRO loader behavior
- NCCH/ExeFS/RomFS mounting
- filesystem services
- save/extdata handling
- GPU/shader behavior relevant to rendering reconstructed assets

This is supporting platform evidence rather than Pokémon-specific game-code evidence and should be kept clearly separated.

Required sweep:

- [ ] loader / NCCH parsing
- [ ] CRO/RO module behavior
- [ ] filesystem service behavior
- [ ] save/extdata implementation
- [ ] relevant historical commits from the Sun/Moon era

## I. Source-history requirement

For every major repository above, survey must include more than current HEAD:

- commit history
- tags/releases
- deleted/renamed files discoverable through history
- branches
- forks
- issues
- pull requests
- linked forum posts / documentation

A useful format discovery that existed in a 2016–2018 revision but was later refactored or removed remains relevant to Generation VII reconstruction.

## Current status

This inventory establishes the reverse-engineering source classes and initial major repositories. It is **not yet an exhaustive repository-by-repository historical sweep**.

Next concrete outputs should split this inventory into technical maps for:

1. executable / CRO / symbol sources;
2. GARC/data locations;
3. save blocks;
4. models/graphics/animation;
5. audio;
6. scripts/maps/events;
7. RNG/battle mechanics;
8. update/base-title overlay behavior.
