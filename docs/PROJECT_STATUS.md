# Project Status

**Current stage:** Phase 0 — Target definition (in progress)

This document tracks decompilation progress, target-version coverage, validation level, and the next major milestones.

## Project constraints

- No retail ROM/game image is currently available to the project.
- Publicly accessible official documentation, reverse-engineering research, tooling, catalogs, and independently checkable technical sources are therefore used to build the target inventory.
- The Japanese release is the investigation baseline. Other regions, languages, revisions, and updates are compared against it rather than being silently merged.
- Retail ROM/game images, decrypted distribution images, console keys, and other redistributable game binaries remain outside the repository.

## Version inventory

| Target | Region | Language | Revision / update | Verification | Notes |
| --- | --- | --- | --- | --- | --- |
| Pokémon Sun Japanese baseline | JPN | 9-language capability documented; region/language mapping still under investigation | Retail base / v1.0 | Unverified | Official release metadata recorded; exact build/hash unavailable. |
| Pokémon Sun update | JPN | Multi-language | Ver.1.1 (2017-01-11) | Unverified | Update history confirmed from Nintendo Japan; build/hash pending. |
| Pokémon Sun update | JPN | Multi-language | Ver.1.2 (2017-05-17) | Unverified | Update history confirmed from Nintendo Japan; build/hash pending. |
| Pokémon Sun regional releases | NA / AU / EUR / KOR / HK / TW / unresolved PRC | Region and language tracked independently | Retail base targets | Unverified | First region matrix established; first-party evidence captured for JPN, NA, EUR, KOR metadata, HK and TW. |

See `VERSIONS.md` for the authoritative target inventory.

Current Phase 0 research records:

- `research/SUN_JPN_BASELINE.md`
- `research/SUN_REGION_MATRIX.md`
- `research/SUN_UPDATE_MATRIX.md`

## Progress

- [x] Begin authoritative version/revision inventory with the Japanese baseline
- [x] Establish the first source-backed regional release matrix
- [x] Establish the first regional update-history comparison
- [ ] Complete Japanese product/build identifier inventory
- [ ] Complete region-by-region cartridge/eShop product identifiers
- [ ] Complete update Title ID/content-version inventory by distribution region
- [ ] Resolve Europe/Australia/Korea update archival gaps
- [ ] Resolve mainland-China retail/distribution status separately from Simplified-Chinese language support
- [ ] Document executable and section layout
- [ ] Map symbols, functions, and major subsystems
- [ ] Document game-data formats and resource containers
- [ ] Reconstruct scripts, events, and behavior
- [ ] Reconstruct asset pipelines and metadata
- [ ] Add reproducible extraction/repacking tooling
- [ ] Add automated verification where practical

## Validation levels

- **Unverified** — proposed or recorded but not independently checked against the target build.
- **Observed** — confirmed directly in a specific target build, executable, extracted file, or runtime observation.
- **Reproduced** — behavior or data can be recreated with documented steps.
- **Matched** — reconstructed output is verified against the intended target.

Official/public documentation can establish release history and research leads without automatically promoting a build-level claim to `Observed` or `Matched`.

## Next milestones

1. Resolve the Japanese retail/download product identifiers and update identifiers from independent public sources.
2. Finish the Sun region/distribution inventory, including packaging and eShop distinctions.
3. Resolve update package identities by region rather than assuming globally shared packages.
4. Begin executable/container mapping only after the relevant target identifiers are sufficiently constrained.

Update this file whenever the project reaches a meaningful milestone or adds a new supported target.
