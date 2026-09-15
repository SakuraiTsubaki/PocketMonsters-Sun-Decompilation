# Phase 3 — Evidence Extraction and Binary Diff

This phase begins after the exact target build and executable layout have been verified.

## Goals

- Build a reproducible evidence index from the decompressed ExeFS `.code` image.
- Narrow Sun/Moon code differences without embedding executable bytes in reports.
- Generate pointer candidates only inside verified mapped address ranges.
- Keep all labels provisional until a reference is confirmed by code/data behavior.

## Required inputs

- verified `exheader.json`
- verified `code_layout.json`
- locally extracted/decompressed ExeFS `.code`
- paired-version `.code` when performing Sun ↔ Moon comparison

## Tools

### `tools/extract_binary_evidence.py`

Indexes ASCII and ASCII-subset UTF-16LE string candidates. Default reports contain only offsets, lengths, encodings, and SHA-256 hashes. Literal text is excluded unless `--include-text` is explicitly used for local/private analysis.

### `tools/compare_binary_blocks.py`

Compares two local binaries in fixed-size blocks (default `0x1000`) and records same/changed/left-only/right-only blocks using hashes only.

### `tools/scan_pointer_candidates.py`

Scans aligned little-endian integers for values inside a researcher-supplied verified address interval. Candidate values are not considered confirmed pointers until validated by surrounding code/data and mapped sections.

## 3DS workflow

1. Run `inspect_3ds_exheader.py`.
2. Run `map_3ds_code_layout.py` on a decompressed `.code` image.
3. Use the mapped `.text/.rodata/.data` ranges to select address intervals.
4. Generate binary evidence indexes.
5. Compare Sun ↔ Moon only when both exact target revisions are known.
6. Generate pointer candidates inside verified section ranges.
7. Create function/data labels only after direct evidence or reproducible cross-version correspondence.

## Evidence rules

- Do not copy function names or addresses between Sun/Moon merely because binaries are similar.
- Do not copy addresses from Ultra Sun/Ultra Moon into Sun/Moon.
- A numeric value inside an address range is only a candidate pointer.
- A string candidate does not establish function purpose on its own.
- Changed 4 KiB blocks are localization targets, not function boundaries.
- Unknowns remain unknown until verified.

## Repository policy

Do not commit ROM/CXI images, encrypted title content, proprietary executable payloads, keys, or literal extracted text dumps. Commit tooling, hashes, metadata, reconstructed source, analysis tables, and verification records according to project policy.
