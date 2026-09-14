# Project Status

**Current stage:** Phase 0 — Target definition (in progress)

This document tracks decompilation progress, target-version coverage, validation level, and the next major milestones.

## Project constraints

- No retail ROM/game image is currently available to the project.
- Publicly accessible official documentation, reverse-engineering research, tooling, catalogs, archived material, historical source-code revisions, event databases, technical forums, and independently checkable reference sources are therefore part of the reconstruction evidence base.
- The Japanese release is the investigation baseline. Other regions, languages, revisions, updates, services, and distributions are compared against it rather than being silently merged.
- The public-source survey is continuous across all roadmap phases; completing version identification does **not** mean source collection is complete.
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

Current research records:

- `research/SUN_PUBLIC_SOURCE_SURVEY.md` — master exhaustive public-source census
- `research/SUN_JPN_BASELINE.md`
- `research/SUN_REGION_MATRIX.md`
- `research/SUN_UPDATE_MATRIX.md`
- `research/SUN_IDENTIFIERS.md`

## Public-source survey workstreams

The active survey covers, in parallel:

- Japanese first-party site tree and dated news/detail pages
- regional first-party Nintendo/Pokémon sites
- official manuals, PDFs, press releases, videos and demo material
- Pokémon Global Link, Pokémon Bank, Poké Transporter and related historical services
- official distributions/events by region and language
- 3DS executable/container/platform documentation
- pk3DS, PKHeX, PKSM/PKSM-Scripts and other reverse-engineering/tool repositories
- GitHub history, forks, issues and pull requests relevant to format discoveries
- Project Pokémon ROM/save/RNG/model research
- save structure, event-script, GARC, model/graphics, audio and map research
- Wonder Card/event archives and distribution databases
- unused/development-leftover documentation and technical evidence
- Bulbapedia, Serebii and similar secondary references for cross-checking
- Internet Archive and other preserved copies of removed Generation VII-era pages

No single source class is treated as complete merely because one good source has been found.

## Progress

- [x] Begin authoritative version/revision inventory with the Japanese baseline
- [x] Establish the first source-backed regional release matrix
- [x] Establish the first regional update-history comparison
- [x] Cross-check core Japanese physical identifiers (`CTR-P-BNDJ`, JAN `4902370534009`)
- [x] Cross-check public base/update Title-ID leads and final Ver.1.2 catalog metadata
- [x] Separate Simplified-Chinese language support from an unproven mainland-China retail build
- [x] Establish master exhaustive public-source survey categories and initial source corpus
- [x] Identify the Sun/Moon Special Demo symbol-bearing CRO/ExeFS code as a dedicated reverse-engineering evidence target
- [x] Register major technical corpora: pk3DS, PKHeX, PKSM/PKSM-Scripts, 3dbrew and Project Pokémon research/event archives
- [ ] Enumerate every reachable page of the Japanese Sun/Moon official site and record coverage
- [ ] Enumerate regional official site trees and archived equivalents
- [ ] Sweep historical Pokémon Global Link pages and archived competition/regulation/global-mission material
- [ ] Sweep Pokémon Bank/Poké Transporter compatibility/history material
- [ ] Build full Generation VII event/distribution inventory for Sun by region/language/method
- [ ] Sweep reverse-engineering repository history, forks, issues and PRs rather than only current HEAD
- [ ] Build GARC/file-location and format research inventory
- [ ] Build save-structure evidence inventory
- [ ] Build model/graphics/animation/audio research inventory
- [ ] Build unused/development-leftover evidence inventory
- [ ] Record negative searches / unresolved source gaps
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

1. Continue the exhaustive public-source census across every source class; do not stop at version identifiers.
2. Enumerate the Japanese official Sun/Moon site tree and event/update pages as the first-party baseline corpus.
3. Build parallel technical corpora for demo symbols, GARC/data locations, save structures, events/distributions, and unused content.
4. Continue region/update identity work in parallel rather than treating it as the whole project.
5. Begin Phase 1 executable/container mapping as evidence becomes sufficient while public-source collection continues.

Update this file whenever the project reaches a meaningful milestone or adds a new supported target.