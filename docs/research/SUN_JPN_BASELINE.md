# Pokémon Sun — Japanese Baseline Research Record

## Purpose

This record starts Phase 0 target definition for `PocketMonsters-Sun-Decompilation` under the project rule that the Japanese release is the investigation baseline and all other regions/languages/revisions are compared against it.

The project currently has no retail ROM/game image. Findings below therefore distinguish official/publicly documented facts from build-level facts that still require direct target verification.

## Confirmed from official/public documentation

### Core release metadata

- Title: `ポケットモンスター サン` / Pokémon Sun
- Platform: Nintendo 3DS
- Japanese release date: 2016-11-18
- Publisher/brand-side release: The Pokémon Company
- Distributor: Nintendo
- Developer: Game Freak
- Genre: RPG
- Local/internet communication support is documented by the Japanese official site.

Project verification state: **Unverified at build level**. These are externally documented release facts; no project-held retail image exists for hash-level identity checking.

### Language capability

Pokémon Sun/Moon are documented as supporting nine selectable languages:

1. Japanese
2. English
3. French
4. German
5. Italian
6. Spanish
7. Korean
8. Traditional Chinese
9. Simplified Chinese

This does **not** imply that region and language are interchangeable. Packaging, eShop distribution, displayed language metadata, and region-specific release details must be recorded separately.

### Official Japanese update history

#### Ver.1.1 — 2017-01-11

Nintendo Japan documents fixes including:

- incorrect behavior involving `Memento` and `Parting Shot`;
- an incorrect battle win/loss judgment involving `Rocky Helmet`;
- an issue where certain Pokémon could fail to learn a move they should learn on evolution;
- additional unspecified fixes for smoother play.

Nintendo also noted that online play required the update and that older Battle Videos became incompatible after updating.

#### Ver.1.2 — 2017-05-17

Nintendo Japan documents fixes including:

- an issue involving `Sky Drop` used against a Pokémon using `Spiky Shield`;
- an issue where Scatterbug could fail to have the correct Egg Move data;
- additional unspecified fixes for smoother play.

Nintendo again required the update for online play and noted Battle Video incompatibility across the update boundary.

## Public technical identifiers requiring direct verification

The following values are repeated in public 3DS catalog/tooling sources and are useful for research targeting, but this repository does not yet possess an independently verified matching build/hash:

- Application Title ID: `0004000000164800`
- Product-code family: `CTR-BNDA`

Status: **external public-source match; direct verification pending**.

Do not infer undocumented Japanese packaging suffixes or build hashes from these values.

## Source register for this batch

### Primary / official

1. The Pokémon Company — Japanese Pokémon Sun/Moon official site  
   https://www.pokemon.co.jp/ex/sun_moon/  
   Used for Japanese release date, platform, publisher/distributor/developer and communication metadata.

2. Nintendo Japan Support — Pokémon Sun/Moon update data Ver.1.2 page  
   https://support.nintendo.com/jp/3ds/soft/bnda/update/index.html  
   Used for Ver.1.1 and Ver.1.2 dates and documented fix summaries.

3. Nintendo UK — Pokémon Sun product page  
   https://www.nintendo.com/en-gb/Games/Nintendo-3DS-games/Pokemon-Sun-1092368.html  
   Used as official Nintendo evidence that Sun/Moon allow selection from nine languages.

4. The Pokémon Company corporate material  
   https://corporate.pokemon.co.jp/PostImages/850f9ea9cdecd73192ff941ced42d43bffcda492.pdf  
   Used as official corporate evidence that Sun/Moon support nine selectable languages.

### Secondary / technical lead

5. 3DSDB public catalog  
   https://3dsdb.com/  
   Used only as a lead for `0004000000164800` and `CTR-BNDA`. These values remain pending direct project verification.

## Open questions

- Exact Japanese retail cartridge product code and packaging suffix.
- Exact Japanese download distribution identifiers beyond the application Title ID lead.
- Update Title ID(s), content version metadata, and exact update package hashes.
- Retail v1.0 executable/RomFS hashes and section hashes.
- Whether any Japanese cartridge production revision exists beyond the base retail release plus downloadable updates.
- Exact region-by-region package/eShop language presentation despite the common nine-language game capability.
- Region-specific release dates, ratings, packaging, serials, bonuses and distribution differences.

## Next investigation batch

1. Resolve Japanese product/package identifiers from multiple independent public sources.
2. Resolve update identifiers/version metadata for Ver.1.1 and Ver.1.2.
3. Start the region inventory without assuming that `USA`, `EUR`, `KOR`, or other labels correspond one-to-one with language.
4. Build a source-backed region/release matrix and add only verified rows to `VERSIONS.md`.
5. Preserve unresolved values as `TBD`/`unknown` rather than guessing.
