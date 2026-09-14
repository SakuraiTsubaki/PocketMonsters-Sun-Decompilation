# Version Coverage

Use this document as the authoritative inventory of game versions targeted by this decompilation project.

## Baseline policy

The project uses the Japanese release as the investigation baseline. Other regions, languages, revisions, and updates are compared against that baseline as they are independently identified. Because no retail ROM/game image is available to this project, externally documented release/update facts may be recorded before exact build hashes are available; such rows remain **Planned** until target identity and hashes are independently verified.

| Status | Region | Language | Revision / update | Platform / build | Hashes | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Planned | JPN | Multi-language; 9 selectable languages documented for Sun/Moon | Retail base / v1.0 | Nintendo 3DS; application Title ID lead `0004000000164800` | TBD | Japanese baseline. Official release date: 2016-11-18. Japanese physical code `CTR-P-BNDJ` and JAN `4902370534009` agree across multiple independent Japanese retailers/catalogs; direct build hash remains unavailable. |
| Planned | JPN | Multi-language | Update Ver.1.1 | Nintendo 3DS update; update Title ID lead `0004000E00164800`; 2017-01-11 | TBD | Update existence/date/fixes documented by Nintendo Japan. Exact Ver.1.1 content-version/hash still TBD. |
| Planned | JPN | Multi-language | Update Ver.1.2 | Nintendo 3DS update; update Title ID lead `0004000E00164800`; 2017-05-17 | TBD | Official update history. Public catalogs agree on update product code `CTR-U-BNDA` and final content version `2112`; exact project-verified package hash unavailable. |
| Planned | North America | Multi-language capability; package-language presentation TBD | Retail base / v1.0 | Nintendo 3DS; application Title ID lead `0004000000164800` | TBD | Official Pokémon Company North America launch date: 2016-11-18. Public physical product-code lead: `CTR-BNDE-USA`. |
| Planned | Australia | Multi-language capability; package-language presentation TBD | Retail base / v1.0 | Nintendo 3DS; exact build identity TBD | TBD | 2016-11-18 release supported by public cross-checks; primary Nintendo AU archival source still required. Public lead: `CTR-BNDP-AUS`. |
| Planned | Europe | Multi-language capability; package-language presentation varies by listing | Retail base / v1.0 | Nintendo 3DS European distribution; application Title ID lead `0004000000164800` | TBD | Official Nintendo Europe release date: 2016-11-23. Public physical product-code lead: `CTR-BNDP-EUR`. |
| Planned | South Korea | Nine-language game capability; Korean distribution metadata tracked separately | Retail base / v1.0 | Nintendo 3DS; application Title ID lead `0004000000164800` | TBD | Pokémon Korea confirms Nov. 2016 and Korean Nintendo as distributor; exact 2016-11-18 date supported by contemporary Korean-Nintendo-sourced reporting. Public physical lead: `CTR-BNDK-KOR`. |
| Planned | Hong Kong | Both Traditional-Chinese-system and Japanese-system software offerings documented; each supports all 9 selectable languages | Retail base / v1.0 | Nintendo 3DS; application Title ID lead `0004000000164800` | TBD | Nintendo (Hong Kong) official launch date: 2016-11-18. Traditional-Chinese distribution physical lead: `CTR-BNDW-CHT`. |
| Planned | Taiwan | Both Traditional-Chinese-system and Japanese-system software offerings documented; each supports all 9 selectable languages | Retail base / v1.0 | Nintendo 3DS; application Title ID lead `0004000000164800` | TBD | Nintendo (Hong Kong) Taiwan material confirms 2016-11-18 launch. Exact package/build identity still unresolved. |
| Reference only | Mainland China / CHN-specific target | Simplified Chinese is officially selectable | No distinct CHN retail/update target identified | No distinct CHN/iQue build established by current first-party evidence | N/A | Official Simplified-Chinese material tells users of JPN- and Traditional-Chinese-region 3DS systems to use the corresponding regional software. Keep Simplified Chinese as a language axis, not a presumed CHN build. |

## Current public identifiers under investigation

These identifiers are useful research targets but are not yet promoted to project-verified build identity because no matching retail/update image is held for direct comparison.

| Identifier | Value | Evidence state | Notes |
| --- | --- | --- | --- |
| Base application Title ID | `0004000000164800` | Multiple public technical-source match | Repeated across regional public 3DS catalogs/tools. |
| Japanese physical product code | `CTR-P-BNDJ` | Multiple independent Japanese retailer/catalog match | Distinguish from eShop/title metadata codes. |
| Japanese physical JAN | `4902370534009` | Multiple independent Japanese retailer/catalog match | Standard Japanese physical release. |
| Base eShop/title metadata code | `CTR-N-BNDA` | Public technical-catalog match | Meaning/field provenance still being documented. |
| Generic base product family | `BNDA` / `CTR-BNDA` | Public catalog match | Do not conflate with regional physical package codes. |
| Update Title ID | `0004000E00164800` | Multiple public technical-source match | Listed for Pokémon Sun update data in multiple regional catalog datasets. |
| Update product code | `CTR-U-BNDA` | Multiple public technical-source match | Public update metadata. |
| Ver.1.2 content version | `2112` | Multiple public technical-source match | Catalog metadata; exact package hash is not project-verified. |

## Documented selectable languages

Official Nintendo material states that Pokémon Sun and Pokémon Moon can be played in nine languages:

- Japanese
- English
- French
- German
- Italian
- Spanish
- Korean
- Traditional Chinese
- Simplified Chinese

Region packaging and per-distribution language presentation must still be investigated separately; region and language are not assumed to be equivalent. Nintendo (Hong Kong) explicitly documents both Traditional-Chinese-system and Japanese-system software offerings for the Hong Kong/Taiwan markets while stating that either offering can select all nine game languages.

The official Simplified-Chinese Sun/Moon website likewise describes Japanese-region and Traditional-Chinese-region software as the applicable 3DS products and says that either can select Simplified Chinese. A separate mainland-China/iQue Sun target is therefore **not inferred** from the existence of Simplified Chinese localization.

## Primary sources for the current Phase 0 inventory

- The Pokémon Company, Japanese Pokémon Sun/Moon official site — release date, platform and product information: https://www.pokemon.co.jp/ex/sun_moon/
- Nintendo Japan support — Pokémon Sun/Moon update data Ver.1.2 page, including Ver.1.1 history: https://support.nintendo.com/jp/3ds/soft/bnda/update/index.html
- Nintendo UK — Pokémon Sun product page; states nine selectable languages in the game and records the European release: https://www.nintendo.com/en-gb/Games/Nintendo-3DS-games/Pokemon-Sun-1092368.html
- The Pokémon Company corporate release — documents Sun/Moon as supporting nine selectable languages: https://corporate.pokemon.co.jp/PostImages/850f9ea9cdecd73192ff941ced42d43bffcda492.pdf
- The Pokémon Company North America press site — North American launch on 2016-11-18: https://press.pokemon.com/en/releases/NEW-POKEMON-REVEALED-FOR-POKEMON-SUN-AND-POKEMON-MOON-84523
- Nintendo Europe / Nintendo Netherlands — European launch on 2016-11-23: https://www.nintendo.com/nl-nl/Nieuws/2016/november/Welkom-in-Alola-Pokemon-Sun-en-Pokemon-Moon-komen-vandaag-uit-in-Europa-exclusief-voor-de-Nintendo-3DS-1158904.html
- Pokémon Korea — official Korean game page, November 2016 release month and Korean Nintendo distribution: https://pokemonkorea.co.kr/game/view/5246?cate2=7&sword=
- Nintendo (Hong Kong) — official Hong Kong/Taiwan launch and language/system-target information: https://www.nintendo.com/hk/pressrelease/3ds_20160901_sun_moon_release.html
- Nintendo (Hong Kong), Simplified Chinese release material — JPN/Traditional-Chinese-system software and 9-language support: https://www.nintendo.com/hk/pressrelease/3ds_20160920_sun_moon_release_sc.html
- Nintendo (Hong Kong), Taiwan site — official 2016-11-18 Taiwan-market release confirmation: https://www.nintendo.com/tw/pressrelease/3ds_20161118_sun_moon_release.html
- Official Simplified-Chinese Sun/Moon site — product information and JPN/Traditional-Chinese-region hardware/software note: https://www.pokemon-sunmoon-cn.com/sc/

## Secondary/public technical and packaging evidence

- 3DSDB public catalog for base/update Title IDs, product families and update content-version leads: https://3dsdb.com/
- 3DSDB static regional catalog: https://hax0kartik.github.io/3dsdb/static.html
- 3DSDB Korean catalog source: https://github.com/hax0kartik/3dsdb/blob/master/jsons/list_KR.json
- GameFAQs Pokémon Sun release-data catalog for regional package-code leads: https://gamefaqs.gamespot.com/3ds/187276-pokemon-sun/data
- Bulbapedia Pokémon Sun/Moon release matrix for regional cross-checking: https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_Sun_and_Moon
- Bulbapedia mainland-China history, used to flag a conflict with the general release matrix: https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_in_mainland_China
- Contemporary Korean reporting citing Korean Nintendo for the exact Korean launch date: https://www.inven.co.kr/webzine/news/?news=164522
- Japanese physical-product cross-checks: GEO Online, Rakuten Books, Suruga-ya, and Yamada Webcom (see `research/SUN_IDENTIFIERS.md`).

These technical leads are recorded for investigation and must not be treated as equivalent to a project-verified retail/update build hash.

See the Phase 0 research records:

- `research/SUN_JPN_BASELINE.md`
- `research/SUN_REGION_MATRIX.md`
- `research/SUN_UPDATE_MATRIX.md`
- `research/SUN_IDENTIFIERS.md`

## Status vocabulary
- **Planned** — intended for investigation but not yet verified.
- **Verified** — identity and hashes confirmed.
- **Mapped** — executable/data layout documented.
- **In progress** — active source reconstruction.
- **Matched** — reconstruction verified against the target.
- **Reference only** — used for comparison but not a reconstruction target.

## Recording rules
1. Record exact revision/update information whenever known.
2. Prefer cryptographic hashes over filenames as identity evidence.
3. Do not commit retail game images or console keys.
4. Record regional or language differences instead of assuming two releases are identical.
5. Link version-specific findings to relevant documentation or verification issues.
