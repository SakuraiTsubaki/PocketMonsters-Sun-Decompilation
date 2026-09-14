# Pokémon Sun — Exhaustive Public-Source Survey

## Purpose

This document is the master survey for publicly accessible material relevant to reconstructing, comparing, and documenting **Pokémon Sun** without access to a retail ROM/game image.

The project baseline is the **Japanese release**. All regional, language, revision, update, service, distribution, and technical evidence is compared against that baseline rather than silently merged.

This survey is deliberately broader than a version-ID inventory. A category is not considered fully surveyed merely because one authoritative source has been found. The goal is to enumerate all material source classes that can contribute to reconstruction, then track representative and newly discovered sources until each class has been systematically exhausted as far as public evidence permits.

## Survey rules

- Preserve the repository's existing verification vocabulary: `Unverified`, `Observed`, `Reproduced`, `Matched`.
- External documentation can establish facts and research leads without automatically making a target-build claim `Observed`.
- Prefer first-party Japanese material first, then first-party regional material, then independent technical/reverse-engineering sources, then secondary reference sources.
- Record region and language separately.
- Record revision/update context whenever known.
- Keep historical/deprecated material when it documents a Generation VII-era service or behavior.
- Search archived and historical versions of source sites when current pages are incomplete.
- Search GitHub history, forks, issues, pull requests, and old revisions where current HEAD has removed useful research.
- Do not commit retail ROM/game images, decrypted distribution images, keys, or redistributable game binaries.
- Do not infer missing file names, offsets, symbols, addresses, package identities, or regional builds.

## Source classes

| Class | Required coverage | Current state |
| --- | --- | --- |
| Japanese first-party game site | All index pages, dated news, product pages, feature pages, screenshots, videos, distributions, update notices | In progress |
| Japanese Nintendo support | Base title support, update history, eShop/download metadata, service notices | In progress |
| Regional first-party sites | North America, Europe, Australia, Korea, Hong Kong, Taiwan and any other verified distribution target | In progress |
| Official manuals / PDFs / press kits | Manuals, downloadable guides, corporate PDFs, press releases, media kits, screenshots | In progress |
| Demo / prerelease / promotional material | Special Demo, Direct footage, trailers, prerelease screenshots, downloadable demo metadata | In progress |
| Pokémon Global Link | Battle Spot, competitions, QR rental teams, global missions, regulations, service changes | In progress |
| Pokémon Bank / Poké Transporter | Compatibility, migration rules, supported origins, service updates, event-linked rewards | In progress |
| Official events / distributions | Serial code, Internet, local wireless, store, tournament, magazine, Bank-linked, QR and other distributions by region/language | In progress |
| 3DS platform documentation | NCCH/NCSD, ExeFS, RomFS, CRO/CRS, title/update metadata, symbols, save/extdata context | In progress |
| ROM/data reverse engineering | GARC locations, data schemas, text, encounters, trainers, personal, moves, evolution, shops, scripts, maps | In progress |
| Save reverse engineering | Save block maps, offsets, checksums/crypto, Pokédex, party/boxes, Festival Plaza, Pelago, Battle Tree, Mystery Gift | In progress |
| Models / graphics / animation | BCH/model tooling, textures, BCLIM, skeletal animation, overworld assets, UI graphics | In progress |
| Audio | BCSAR/BCSTM/stream/archive research, sequence/bank tooling, music/sound identifiers | Not yet exhaustively swept |
| Scripting / events | Event-script formats, field objects, triggers, flags, map/event research | In progress |
| Battle mechanics / RNG | SOS, Z-Moves, Battle Royal, Battle Tree, RNG, encounter generation, legality details | In progress |
| Unused / development leftovers | Unused maps, models, graphics, items, battle backgrounds, text, GO remnants, debug/symbol artifacts | In progress |
| Event databases | Wonder Cards, event Pokémon/items, region/language legality, redemption metadata | In progress |
| Encyclopedic reference | Bulbapedia, Serebii and similar references used only with provenance and cross-checking | In progress |
| Historical forums / community research | Project Pokémon, ROM-hacking threads, tool discussions, old discoveries and unresolved questions | In progress |
| Web archives | Dead official PGL pages, regional pages, old support articles, removed downloads and documentation | Not yet exhaustively swept |
| Source-code history | GitHub commits, tags, branches, forks, issues, PRs for relevant tools | Not yet exhaustively swept |
| Media evidence | Official videos, screenshots, package scans where legally/publicly hosted, press imagery | In progress |

## First-party Japanese corpus — initial map

The Japanese Pokémon Sun/Moon official site is a major primary corpus and must be treated as a site tree, not a single citation.

Known top-level areas include:

- Product information / release / download-size notes
- `story/` — island challenge, grand trials, Pokémon League, Ultra Beasts, legendary Pokémon and story features
- `character/` — protagonist, Kukui, Lillie, Hau, Samson Oak, captains, kahunas, Team Skull, Aether Foundation and guests
- `pokemon/` — newly revealed species, Alolan forms, previously known Pokémon and special entries such as Ash-Greninja
- `collect/` — Rotom Pokédex, QR Scan, Island Scan, Poké Finder, Pokémon Bank, Poké Pelago
- `fight/` — Z-Moves, Mega Evolution, Battle Royal, SOS battles, Battle Tree, online battle functions, QR rental teams, Friendly Competitions
- communication / Festival Plaza / exchange-related pages
- customization / world / field-feature pages
- `topics/` and `update/` — dated news, serial-code distributions, Mega Stone passwords, Bank support, launch notices, update notices
- `movie/` — trailers and game-footage index

Primary entry points currently captured:

- https://www.pokemon.co.jp/ex/sun_moon/
- https://www.pokemon.co.jp/ex/sun_moon/update/
- https://www.pokemon.co.jp/ex/sun_moon/story/
- https://www.pokemon.co.jp/ex/sun_moon/character/
- https://www.pokemon.co.jp/ex/sun_moon/pokemon/
- https://www.pokemon.co.jp/ex/sun_moon/collect/
- https://www.pokemon.co.jp/ex/sun_moon/fight/
- https://www.pokemon.co.jp/ex/sun_moon/movie/

These indexes and every reachable dated/detail page need separate enumeration and archival recording.

## First-party system/service corpus

### Nintendo update/support

- Nintendo Japan Sun/Moon update Ver.1.2 page, including Ver.1.1 history:
  - https://support.nintendo.com/jp/3ds/soft/bnda/update/index.html

### Pokémon Bank / Poké Transporter

- Official Sun/Moon Bank compatibility page:
  - https://www.pokemon.co.jp/ex/sun_moon/collect/160920_01.html

This corpus must also include historic Bank/Transporter notices, Virtual Console transfer rules, Pokédex additions, service fee/status changes, and event-linked rewards.

### Pokémon Global Link

Known official Sun/Moon pages document:

- Rating Battles and rule categories
- WCS rules
- Global Missions / global attractions
- QR rental teams
- Friendly Competitions
- Regulation-data distribution

Example primary source:

- https://www.pokemon.co.jp/ex/sun_moon/fight/161004_02.html

The original PGL site is historical and requires web-archive coverage.

## Reverse-engineering / technical corpus — initial map

### pk3DS

Repository:

- https://github.com/kwsch/pk3DS

Known supported research/editing domains include:

- Trainer data
- Wild encounters
- Personal data: types, stats, abilities, TM compatibility
- Move data
- Level-up / egg learnsets
- Evolutions
- TM moves
- Special marts
- GARC handling and game configuration

The complete repository history, source paths, issues, forks and older revisions must be surveyed, not only the README.

### PKHeX

Repository:

- https://github.com/kwsch/PKHeX

Relevant areas include Generation VII save classes, save-block accessors, legality data, encounters, personal tables, Mystery Gift handling, language/region data and related format definitions.

### PKSM / PKSM-Scripts

Repositories / historical documentation include:

- https://github.com/FlagBrew/PKSM
- https://github.com/FlagBrew/PKSM-Scripts

Known useful material includes shortened 3DS Title IDs and Generation VII save offsets / script-oriented field maps.

### 3dbrew

Relevant technical evidence includes 3DS executable/container documentation and the important record that the **Pokémon Sun and Moon Special Demo contains symbols in CROs and the ExeFS code binary**.

- https://3dbrew.org/wiki/Titles_With_Code_Symbols

This makes the Special Demo a distinct reverse-engineering evidence target rather than merely promotional software.

### Project Pokémon research

Major source areas:

- 3DS ROM Research & Development forum
- Sun/Moon GARC-location research
- Gen VII save research
- RNG research/tools
- model tooling such as SPICA
- historical ROM-hack research that incidentally documents file locations and engine behavior

Entry points currently captured:

- https://projectpokemon.org/home/forums/forum/127-rom-3ds-research-and-development/
- https://projectpokemon.org/home/forums/topic/39695-solved-sun-and-moon-important-garc-file-locations/
- https://projectpokemon.org/home/forums/topic/40732-gen-7-save-file-structure/
- https://projectpokemon.org/home/forums/topic/40013-sun-moon-rng-manipulation-research-tools/

Research threads are evidence leads and must be separated from direct target observation.

## Save-data corpus — initial map

Sources currently identified include PKHeX's Generation VII save implementations and PKSM documentation/scripts.

Coverage target includes at minimum:

- Trainer identity and region/language
- Money / BP / Festival Coins
- Party and boxes
- Pokédex
- inventory categories
- event flags and work values where documented
- Festival Plaza
- Poké Pelago
- Battle Tree / Battle Royal state
- QR / Poké Finder state
- Zygarde cells
- Mystery Gift / Wonder Card storage
- battle teams
- play time / clock fields
- checksum/encryption/block metadata

Offsets from public source code are not automatically assumed identical across SM and USUM; each title family must be handled separately.

## Event / distribution corpus — initial map

### Project Pokémon Event Gallery

Generation VII 3DS archive:

- https://projectpokemon.org/home/files/category/6-generation-7-3ds/

The archive is organized by language and currently exposes large per-language collections, including Japanese, English, Korean, European languages, and both Chinese scripts.

The survey must record, per event where possible:

- distribution name
- distribution region
- language behavior
- distribution dates
- method
- eligible games
- species/item
- OT/TID/SID
- level
- moves
- ability
- held item
- ball
- ribbon
- met location
- Wonder Card identifiers
- serial/local/Internet/store/tournament provenance

### Serebii Event Database

- https://www.serebii.net/events/

Use for cross-checking dates, methods and event variations, not as sole authoritative evidence.

## Unused / development-leftover corpus — initial map

Known public reference areas include:

- Pokémon Sun/Moon development-leftover / beta documentation on Bulbapedia
- TCRF where available
- Special Demo symbol evidence on 3dbrew
- reverse-engineering threads documenting inaccessible/unused GARCs or data

Known classes already reported publicly include unused locations, battle backgrounds, items, inverse-battle remnants, Pokémon GO-related remnants, unused global missions, graphics, models, and other development leftovers.

Every unused claim must be traced back to a technical observation where practical; encyclopedic summaries alone are not enough for `Observed` project status.

## Mechanics / gameplay corpus — initial map

The Japanese official site itself provides primary documentation for many systems, including:

- Z-Moves and species-specific Z-Moves
- Mega Evolution in Sun/Moon
- Battle Royal
- SOS battles
- Battle Tree
- QR Scan and Island Scan
- Poké Finder
- Poké Pelago
- Festival Plaza
- communication battle modes
- QR rental teams
- Friendly Competitions
- Island Challenge / Trials / Grand Trials
- Ultra Beasts
- Alolan forms

These official descriptions must then be cross-checked against in-game/mechanical research for exact numerical rules and edge cases.

## Regional/language corpus

The following axes must remain independent:

- distribution region / hardware region
- physical package SKU
- eShop/title metadata
- selectable in-game language
- text/localization variant
- update package / revision
- event/distribution region

Current Sun region inventory is tracked in:

- `SUN_REGION_MATRIX.md`
- `SUN_UPDATE_MATRIX.md`
- `SUN_IDENTIFIERS.md`
- `../VERSIONS.md`

## Historical-source requirements

Current live pages are insufficient for a complete Generation VII survey. The following must also be searched systematically:

- Internet Archive snapshots of Pokémon Global Link
- archived regional Nintendo/Pokémon pages
- removed support pages
- historical GitHub revisions
- deleted/moved forum attachments where metadata remains publicly documented
- old release notes for reverse-engineering tools
- issue trackers and pull requests that document format discoveries
- historical event announcements and local store/tournament pages

## Completion rule

The public-source survey is **not complete** when identifiers are complete, nor when a single decompilation subsystem is mapped.

For Pokémon Sun, completion requires a documented sweep of every source class above, with:

1. source discovered or explicitly searched with no result;
2. scope and relevance recorded;
3. region/language/revision context recorded when known;
4. useful claims extracted into the relevant research/format/data document;
5. unresolved contradictions retained rather than collapsed;
6. archival or historical follow-up recorded where live sources are incomplete.

This file is a living index and should expand as new source classes or repositories are discovered.
