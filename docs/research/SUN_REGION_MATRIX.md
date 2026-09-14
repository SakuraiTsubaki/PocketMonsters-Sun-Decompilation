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
| South Korea (KOR) | 2016-11-18 | Pokémon Korea official page confirms Nov. 2016 and Korean Nintendo as distributor; contemporary Korean-Nintendo-sourced reporting confirms the 18th | `CTR-BNDK-KOR` | Unknown | Exact package/build identity remains unverified. |
| Hong Kong market | 2016-11-18 | Nintendo (Hong Kong) official press release | `CTR-BNDW-CHT` lead for Traditional-Chinese distribution | Unknown | Official material explicitly describes both Traditional-Chinese-system and Japanese-system software offerings; both allow selection of all nine in-game languages. |
| Taiwan market | 2016-11-18 | Nintendo (Hong Kong) official Taiwan press material | `CTR-BNDW-CHT` lead for Traditional-Chinese distribution | Unknown | Official material states simultaneous Hong Kong/Taiwan launch and the same two system-targeted offerings. Do not assume HK/TW packages are identical without direct evidence. |
| Mainland China | TBD | Insufficient first-party evidence in this batch for a distinct retail/distribution target | TBD | Unknown | Simplified Chinese is an in-game language option, but this alone does not establish a mainland-China retail build. |

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

Nintendo (Hong Kong) is especially useful here: its 2016 Sun/Moon press releases explicitly state that both the software intended for Traditional-Chinese-region systems and the software intended for Japanese-region systems allow selection of the same nine game languages.

This common game capability does **not** prove that every regional package, eShop listing, executable, RomFS, manual, rating wrapper, or external distribution record is byte-identical. Regional packaging language fields can also differ from the languages selectable after boot.

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

### South Korea

Pokémon Korea's official game page confirms the Korean release month as November 2016, Nintendo 3DS-family compatibility, Korean Nintendo as the release/distribution company, and a suggested price of 49,000 KRW per version.

Source: https://pokemonkorea.co.kr/game/view/5246?cate2=7&sword=

Contemporary Korean reporting citing Korean Nintendo gives the exact release date as 2016-11-18. This date remains tagged as contemporary secondary evidence until an archived Korean Nintendo first-party page is captured.

Cross-check: https://www.inven.co.kr/webzine/news/?news=164522

### Hong Kong and Taiwan

Nintendo (Hong Kong) officially announced a simultaneous 2016-11-18 launch in both Hong Kong and Taiwan markets. Its press material visibly distinguishes software for Traditional-Chinese-region systems from software for Japanese-region systems, while explicitly stating that either software offering can select all nine in-game languages.

Sources:

- Hong Kong press release: https://www.nintendo.com/hk/pressrelease/3ds_20160901_sun_moon_release.html
- Taiwan press release: https://www.nintendo.com/tw/pressrelease/3ds_20161118_sun_moon_release.html
- Earlier Taiwan product announcement: https://www.nintendo.com/tw/pressrelease/3ds_20160602_sun_moon_release.html

This is strong evidence that **hardware/distribution region and selected in-game language are separate axes** and must be modeled separately in the project.

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
- Does the reported `CTR-BNDW-CHT` identifier map specifically to the Traditional-Chinese-system software referenced by Nintendo (Hong Kong), and what identifier corresponds to the Japanese-system offering sold in Hong Kong/Taiwan?
- Are Hong Kong and Taiwan physical packages/serials identical or separately localized despite sharing distribution announcements?
- What archived first-party Korean Nintendo page records the exact 2016-11-18 Korean date and package identifiers?
- Is there a distinct mainland-China retail/distribution target for the 3DS release, or only Simplified Chinese as an in-game language option within other distributions?
- What are the exact cartridge/eShop content versions and cryptographic hashes for every target?

## Verification policy

None of the public product-code leads above are promoted to `Observed`, `Verified`, or `Matched` solely from catalog listings. They remain investigation targets until stronger evidence satisfies the repository's verification rules.
