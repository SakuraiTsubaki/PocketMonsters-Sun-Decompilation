# Pokémon Sun — Initial Region and Distribution Matrix

## Scope

This document is the first public-source inventory of regional Pokémon Sun releases. It is intentionally conservative: official sources establish release facts where available, while packaging/product-code details from public catalogs remain technical leads until independently verified against target media or equivalent primary evidence.

The Japanese release remains the project baseline.

## Release matrix — first pass

| Region / distribution | Release date | Official-source status | Public product-code lead | Build/hash status | Notes |
| --- | --- | --- | --- | --- | --- |
| Japan (JPN) | 2016-11-18 | Official Japanese Pokémon site | `CTR-BNDJ-JPN` retail; `BNDA` eShop | Unknown | Baseline target. Retail/eShop distinction requires deeper identifier mapping. |
| North America (NA) | 2016-11-18 | Official Pokémon Company North America press material | `CTR-BNDE-USA`; `BNDE` eShop | Unknown | ESRB-region packaging lead from secondary catalog. |
| Australia (AU) | 2016-11-18 | Release date supported by multiple public references; primary Nintendo AU source still to be archived | `CTR-BNDP-AUS` | Unknown | Shares `BNDP` family lead with Europe but must not be assumed byte-identical. |
| Europe (EUR) | 2016-11-23 | Official Nintendo Europe pages | `CTR-BNDP-EUR`; `BNDP` eShop | Unknown | European release explicitly five days after the 2016-11-18 baseline regions. |
| South Korea (KOR) | 2016-11-18 | Secondary contemporary reporting cites Korean Nintendo; primary archived source still required | `CTR-BNDK-KOR` | Unknown | Korean packaging and distribution require first-party archival confirmation. |
| Asia / Traditional Chinese distribution (CHT lead) | 2016-11-18 lead | Public catalogs/encyclopedic sources; first-party HK/TW source still required | `CTR-BNDW-CHT` | Unknown | Do not collapse Hong Kong and Taiwan until distribution/packaging evidence is resolved. |
| Mainland China | TBD | Conflicting/insufficient first-party evidence in this batch | TBD | Unknown | Keep separate from Hong Kong/Taiwan. No retail-region assumption is made here. |

## Language capability vs. region

Sun/Moon support nine selectable in-game languages according to official Nintendo/The Pokémon Company material:

- Japanese
- English
- French
- German
- Italian
- Spanish
- Korean
- Traditional Chinese
- Simplified Chinese

This common game capability does **not** prove that every regional package, eShop listing, manual, rating wrapper, or external distribution record is identical. Regional packaging language fields can also differ from the languages selectable after boot.

## Product-code leads

Secondary release catalogs currently report the following retail product-code patterns for Pokémon Sun:

| Lead | Reported region | Status |
| --- | --- | --- |
| `CTR-BNDJ-JPN` | Japan | Secondary lead; direct verification pending |
| `CTR-BNDE-USA` | North America | Secondary lead; direct verification pending |
| `CTR-BNDP-AUS` | Australia | Secondary lead; direct verification pending |
| `CTR-BNDP-EUR` | Europe | Secondary lead; direct verification pending |
| `CTR-BNDK-KOR` | South Korea | Secondary lead; direct verification pending |
| `CTR-BNDW-CHT` | Traditional-Chinese Asia distribution | Secondary lead; direct verification pending |

A public 3DS catalog also associates the application Title ID `0004000000164800` with Pokémon Sun across multiple cataloged dumps. This is retained as a targeting lead, not a project-verified hash identity.

## First-party release evidence captured in this batch

### Japan

The Japanese Pokémon Sun/Moon official site lists 2016-11-18 as the release date for Nintendo 3DS.

Source: https://www.pokemon.co.jp/ex/sun_moon/

### North America

The Pokémon Company North America press site stated that Pokémon Sun/Moon would launch in North America on 2016-11-18.

Source: https://press.pokemon.com/en/releases/NEW-POKEMON-REVEALED-FOR-POKEMON-SUN-AND-POKEMON-MOON-84523

### Europe

Nintendo Europe/Nintendo Netherlands records the European launch on 2016-11-23 and the product page also records the European Nintendo 3DS release date.

Sources:

- https://www.nintendo.com/en-gb/Games/Nintendo-3DS-games/Pokemon-Sun-1092368.html
- https://www.nintendo.com/nl-nl/Nieuws/2016/november/Welkom-in-Alola-Pokemon-Sun-en-Pokemon-Moon-komen-vandaag-uit-in-Europa-exclusief-voor-de-Nintendo-3DS-1158904.html

## Secondary cross-checks

### GameFAQs release data

GameFAQs currently lists the region/product-code combinations recorded above, including Japanese, North American, Australian, European, Korean, and Traditional-Chinese Asian entries.

Source: https://gamefaqs.gamespot.com/3ds/187276-pokemon-sun/data

### Bulbapedia

Bulbapedia lists 2016-11-18 for Japan, North America, Australia, South Korea, Hong Kong and Taiwan, and 2016-11-23 for Europe. It also states that all copies support the nine selectable languages.

Source: https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_Sun_and_Moon

### 3DSDB

The public catalog associates Pokémon Sun with Title ID `0004000000164800` and product-code family `CTR-BNDA` in cataloged entries.

Source: https://3dsdb.com/

## Important unresolved questions

- Are Japan, North America, Australia, Europe, Korea, Hong Kong and Taiwan separate executable/RomFS builds, region wrappers around shared content, or some combination?
- Which components are byte-identical across regions, and which differ only in metadata, manuals, ratings, or distribution packaging?
- What exact title/update IDs apply to each region and update revision?
- Does the reported `CTR-BNDW-CHT` entry cover Hong Kong, Taiwan, or multiple Asian distribution channels?
- What first-party archival evidence exists for Korean, Hong Kong and Taiwan release metadata?
- Is there a distinct mainland-China retail/distribution target for the 3DS release, or only Simplified Chinese as an in-game language option within other distributions?
- What are the exact cartridge/eShop content versions and cryptographic hashes for every target?

## Verification policy

None of the public product-code leads above are promoted to `Observed`, `Verified`, or `Matched` solely from catalog listings. They remain investigation targets until stronger evidence satisfies the repository's verification rules.
