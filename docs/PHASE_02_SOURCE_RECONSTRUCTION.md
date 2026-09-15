# Phase 02 — Source Reconstruction Bootstrap

## Objective

Turn verified local extraction metadata into the first stable source-reconstruction map for **Pokémon Sun** without committing ROM images or proprietary executable payloads.

## Required local inputs

- extracted `exheader.bin`
- extracted ExeFS `.code`
- decompressed `.code` when the exheader compression flag is set
- extracted RomFS directory

## Generated metadata

1. `inventory_extracted_tree.py` → complete path/size/SHA-256 inventory
2. `inspect_3ds_exheader.py` → text/rodata/data/BSS/stack/dependency map
3. `map_3ds_code_layout.py` → virtual-address ↔ `.code` file-offset map
4. `classify_romfs.py` → extension/top-directory/magic/hash clustering

Recommended generated paths:

- `analysis/executable/exheader.json`
- `analysis/executable/code_layout.json`
- `analysis/romfs/classification.json`

Only metadata reports belong in Git. Local game binaries remain outside the repository.

## Reconstruction queues

Do not invent subsystem addresses before the executable map is verified. After verification, classify functions/data into these queues:

- process startup and runtime
- filesystem/resource loading
- script/event execution
- field/map systems
- battle systems
- Pokémon/species/move/item data access
- UI/text/localization
- save data
- communications/network features
- graphics/audio/resource management

## Sun ↔ Moon comparison

Once both inventories exist, compare them with `Sakurai/tools/compare_gen7_inventories.py`. Record:

- identical files
- same-path changed files
- version-only files
- identical content at different paths

Do not assume every difference is gameplay-related; classify evidence before naming the subsystem.

## Exit criteria

Phase 02 is complete when:

- target revision is identified
- `.code` section layout is internally consistent
- RomFS has a reproducible full inventory
- the first executable regions and resource families have evidence-backed labels
- Sun/Moon version differences have a machine-generated baseline
