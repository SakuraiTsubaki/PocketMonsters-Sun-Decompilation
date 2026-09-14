# Roadmap

This roadmap defines the recommended order for turning this repository from an initial research scaffold into a reproducible decompilation project.

## Cross-phase requirement — exhaustive public-source survey

Because this project does not have a retail ROM/game image, the public-source survey is a continuous requirement across every phase rather than a one-time preliminary task.

- [ ] Systematically enumerate Japanese first-party material as the baseline corpus.
- [ ] Systematically enumerate all verified regional and language-specific first-party material.
- [ ] Survey official manuals, PDFs, press materials, videos, demos, updates, distributions, services, and archived/deprecated pages.
- [ ] Survey relevant reverse-engineering repositories, source history, forks, issues, pull requests, research forums, save research, format research, and technical documentation.
- [ ] Survey event/distribution databases, unused/development-leftover documentation, and encyclopedic reference sources with independent cross-checking.
- [ ] Record sources that were searched but yielded no usable evidence so absence is not mistaken for an unperformed search.
- [ ] Keep `research/SUN_PUBLIC_SOURCE_SURVEY.md` current as the master source-class census.

Source discovery continues during Phases 1–5; no phase transition implies that public-source collection is complete.

## Phase 0 — Target definition
- [ ] Identify authoritative game versions, regions, languages, revisions, and updates.
- [ ] Record hashes and provenance for each supported target.
- [ ] Define the primary matching target.

## Phase 1 — Binary and container mapping
- [ ] Document executable layout, sections, overlays, archives, and resource containers.
- [ ] Build file manifests and extraction notes.
- [ ] Record known compression, packing, and serialization formats.

## Phase 2 — Symbol and subsystem mapping
- [ ] Name functions, symbols, tables, and major data structures.
- [ ] Identify engine subsystems and dependencies.
- [ ] Track confidence and evidence for each finding.

## Phase 3 — Source reconstruction
- [ ] Reconstruct code into readable, maintainable source.
- [ ] Reconstruct scripts, data tables, and asset metadata.
- [ ] Add extraction/repacking tools where needed.

## Phase 4 — Verification
- [ ] Add repeatable tests and comparison workflows.
- [ ] Track matching or behavioral-equivalence status by subsystem.
- [ ] Document remaining mismatches and unknowns.

## Phase 5 — Reproducible project workflow
- [ ] Provide documented setup and build/repack steps.
- [ ] Add CI or automated verification where practical.
- [ ] Keep generated outputs reproducible from repository sources and tooling.