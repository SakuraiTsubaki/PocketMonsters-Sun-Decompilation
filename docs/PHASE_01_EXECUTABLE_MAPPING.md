# Phase 01 — Executable Mapping

## Goal

Establish a reproducible executable baseline for the exact local Pokémon Sun target before function naming or source reconstruction begins.

## Inputs

Use only a locally owned/extracted target. Do not commit ROM/CXI/CCI/3DS images, encrypted title packages, keys, or extracted proprietary executable binaries.

Expected local inputs include:

- extracted game tree
- `exheader.bin` (or equivalent extracted NCCH extended header)
- ExeFS `.code` / `code.bin`
- RomFS tree

## Step 1 — Inventory

```bash
python tools/inventory_extracted_tree.py /path/to/extracted-game \
  --project "Pokemon Sun" --platform "Nintendo 3DS" \
  -o manifests/local/inventory.json
```

Commit only the generated metadata report if it contains no game content.

## Step 2 — Map System Control Info

```bash
python tools/inspect_3ds_exheader.py /path/to/exheader.bin \
  -o manifests/local/exheader-map.json
```

Record:

- application title
- remaster version
- ExeFS `.code` compression flag
- `.text` address / size
- `.rodata` address / size
- `.data` address / size
- BSS size
- stack size
- dependency program IDs

## Step 3 — Establish code image

If the exheader reports compressed ExeFS code, decompress the local `.code` before instruction-level analysis. Do not commit the proprietary code image.

The decompiler/disassembler base map must use the addresses from the verified exheader report rather than guessed addresses or values copied from another title.

## Step 4 — First reconstruction outputs

Repository-safe outputs may include:

- function and symbol maps
- address ranges and section maps
- call-graph metadata
- data-structure notes
- reconstructed source
- scripts and tests
- hashes and verification manifests

## Evidence status

Until a real local target has been inventoried, all game/revision-specific values remain **Unverified**. Platform-format facts may be documented separately from target-specific observations.
