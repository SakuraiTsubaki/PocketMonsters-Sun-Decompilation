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
| Pokémon Sun Japanese baseline | JPN | 9-language capability documented; region/language tracked separately | Retail base / v1.0 | Unverified | Official release metadata recorded. Physical code/JAN and public application identifiers now cross-checked; exact build/hash unavailable. |
| Pokémon Sun update | JPN | Multi-language | Ver.1.1 (2017-01-11) | Unverified | Official history plus public update Title-ID lead recorded; exact Ver.1.1 content-version/hash pending. |
| Pokémon Sun update | JPN | Multi-language | Ver.1.2 (2017-05-17) | Unverified | Official history; update Title ID/product code/final content-version cross-checked from public catalogs; exact package hash pending. |
| Pokémon Sun regional releases | NA / AU / EUR / KOR / HK / TW | Region and language tracked independently | Retail base targets | Unverified | First region matrix established; first-party evidence captured for JPN, NA, EUR, KOR metadata, HK and TW. |
| Simplified Chinese localization | Language axis | zh-Hans | Available within documented JPN/Traditional-Chinese-region software | Reference only | Current official evidence does not establish a separate mainland-China/iQue Sun build. |

See `VERSIONS.md` for the authoritative target inventory.

Current Phase 0 research records:

- `research/SUN_JPN_BASELINE.md`
- `research/SUN_REGION_MATRIX.md`
- `research/SUN_UPDATE_MATRIX.md`
- `research/SUN_IDENTIFIERS.md`

## Progress

- [x] Begin authoritative version/revision inventory with the Japanese baseline
- [x] Establish the first source-backed regional release matrix
- [x] Establish the first regional update-history comparison
- [x] Cross-check core Japanese physical identifiers (`CTR-P-BNDJ`, JAN `4902370534009`)
- [x] Cross-check public base/update Title-ID leads and final Ver.1.2 catalog metadata
- [x] Separate Simplified-Chinese language support from an unproven mainland-China retail build
- [ ] Locate first-party/preserved manufacturer evidence for all Japanese physical/eShop identifiers where possible
- [ ] Recover exact Ver.1.1 content-version metadata
- [ ] Complete region-by-region cartridge/eShop product identifiers
- [ ] Resolve Europe/Australia/Korea update archival gaps
- [ ] Determine exact HK/TW Japanese-system versus Traditional-Chinese-system package identifiers
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

1. Finish Sun Phase 0 identity work: package/eShop/update metadata by distribution target.
2. Resolve remaining first-party archive gaps for Australia, Korea and regional updates.
3. Determine whether public evidence can distinguish regional executable/RomFS builds from shared content plus regional wrappers.
4. Begin Phase 1 executable/container mapping once target identities are sufficiently constrained.

Update this file whenever the project reaches a meaningful milestone or adds a new supported target.
