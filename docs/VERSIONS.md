# Version Coverage

Use this document as the authoritative inventory of game versions targeted by this decompilation project.

## Baseline policy

The project uses the Japanese release as the investigation baseline. Other regions, languages, revisions, and updates are compared against that baseline as they are independently identified. Because no retail ROM/game image is available to this project, externally documented release/update facts may be recorded before exact build hashes are available; such rows remain **Planned** until target identity and hashes are independently verified.

| Status | Region | Language | Revision / update | Platform / build | Hashes | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Planned | JPN | Multi-language; 9 selectable languages documented for Sun/Moon | Retail base / v1.0 | Nintendo 3DS; exact build identity TBD | TBD | Japanese baseline. Official release date: 2016-11-18. Exact cartridge/download build hashes remain unverified. |
| Planned | JPN | Multi-language | Update Ver.1.1 | Nintendo 3DS update; 2017-01-11 | TBD | Update existence/date and fixes documented by Nintendo Japan; exact update-title/build hash TBD. |
| Planned | JPN | Multi-language | Update Ver.1.2 | Nintendo 3DS update; 2017-05-17 | TBD | Update existence/date and fixes documented by Nintendo Japan; exact update-title/build hash TBD. |
| Planned | North America | Multi-language capability; package-language presentation TBD | Retail base / v1.0 | Nintendo 3DS; exact build identity TBD | TBD | Official Pokémon Company North America launch date: 2016-11-18. Public product-code lead: `CTR-BNDE-USA`. |
| Planned | Australia | Multi-language capability; package-language presentation TBD | Retail base / v1.0 | Nintendo 3DS; exact build identity TBD | TBD | 2016-11-18 release supported by public cross-checks; primary Nintendo AU archival source still required. Public lead: `CTR-BNDP-AUS`. |
| Planned | Europe | Multi-language capability; package-language presentation varies by listing | Retail base / v1.0 | Nintendo 3DS European distribution; exact build identity TBD | TBD | Official Nintendo Europe release date: 2016-11-23. Public lead: `CTR-BNDP-EUR`. |
| Planned | South Korea | Korean plus common nine-language game capability under investigation | Retail base / v1.0 | Nintendo 3DS; exact build identity TBD | TBD | Contemporary reporting gives 2016-11-18; first-party archival confirmation still required. Public lead: `CTR-BNDK-KOR`. |
| Planned | Hong Kong / Taiwan distribution lead | Traditional Chinese plus common nine-language game capability under investigation | Retail base / v1.0 | Nintendo 3DS; distribution identity TBD | TBD | Public lead: `CTR-BNDW-CHT`; Hong Kong and Taiwan must remain separately traceable until first-party evidence resolves distribution details. |
| Planned | Mainland China | Simplified Chinese language capability is documented, but retail/distribution target is unresolved | TBD | TBD | TBD | Do not infer a distinct mainland-China retail build solely from language support. |

## Current public identifiers under investigation

These identifiers are useful leads but are not yet promoted to verified target identity because this project has no matching retail image/build for direct hash verification.

| Identifier | Value | Evidence state | Notes |
| --- | --- | --- | --- |
| Application Title ID | `0004000000164800` | External public-source match | Repeated in public 3DS catalogs/tools for Pokémon Sun. Direct target verification pending. |
| Product-code family | `CTR-BNDA` | External public-source match | Public catalog entry; exact regional packaging/product-code variants are tracked separately and remain unverified. |

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

Region packaging and per-distribution language presentation must still be investigated separately; region and language are not assumed to be equivalent.

## Primary sources for the current Phase 0 inventory

- The Pokémon Company, Japanese Pokémon Sun/Moon official site — release date, platform and product information: https://www.pokemon.co.jp/ex/sun_moon/
- Nintendo Japan support — Pokémon Sun/Moon update data Ver.1.2 page, including Ver.1.1 history: https://support.nintendo.com/jp/3ds/soft/bnda/update/index.html
- Nintendo UK — Pokémon Sun product page; states nine selectable languages in the game and records the European release: https://www.nintendo.com/en-gb/Games/Nintendo-3DS-games/Pokemon-Sun-1092368.html
- The Pokémon Company corporate release — documents Sun/Moon as supporting nine selectable languages: https://corporate.pokemon.co.jp/PostImages/850f9ea9cdecd73192ff941ced42d43bffcda492.pdf
- The Pokémon Company North America press site — North American launch on 2016-11-18: https://press.pokemon.com/en/releases/NEW-POKEMON-REVEALED-FOR-POKEMON-SUN-AND-POKEMON-MOON-84523
- Nintendo Europe / Nintendo Netherlands — European launch on 2016-11-23: https://www.nintendo.com/nl-nl/Nieuws/2016/november/Welkom-in-Alola-Pokemon-Sun-en-Pokemon-Moon-komen-vandaag-uit-in-Europa-exclusief-voor-de-Nintendo-3DS-1158904.html

## Secondary/public technical leads

- 3DSDB public catalog entry for Pokémon Sun (`0004000000164800`, `CTR-BNDA`): https://3dsdb.com/
- GameFAQs Pokémon Sun release-data catalog for regional product-code leads: https://gamefaqs.gamespot.com/3ds/187276-pokemon-sun/data
- Bulbapedia Pokémon Sun/Moon release matrix for regional cross-checking: https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_Sun_and_Moon

These technical leads are recorded for investigation and must not be treated as equivalent to a project-verified retail build hash.

See `research/SUN_JPN_BASELINE.md` and `research/SUN_REGION_MATRIX.md` for evidence notes and unresolved questions.

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
