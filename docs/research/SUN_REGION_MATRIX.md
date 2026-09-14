# Pokémon Sun — Initial Region and Distribution Matrix

## Scope

This document is the first public-source inventory of regional Pokémon Sun releases. It is intentionally conservative: official sources establish release facts where available, while packaging/product-code details from public catalogs remain technical leads until independently verified against target media or equivalent primary evidence.

The Japanese release remains the project baseline.

## Release matrix — first pass

| Region / distribution | Release date | Official-source status | Public product-code lead | Build/hash status | Notes |
| --- | --- | --- | --- | --- | --- |
| Japan (JPN) | 2016-11-18 | Official Japanese Pokémon site | Japanese physical `CTR-P-BNDJ`; eShop/title lead `CTR-N-BNDA` | Unknown | Baseline target. Physical JAN `4902370534009` agrees across multiple Japanese retailers/catalogs. |
| North America (NA) | 2016-11-18 | Official Pokémon Company North America press material | `CTR-BNDE-USA`; eShop family `BNDE` | Unknown | ESRB-region packaging lead from secondary catalog. |
| Australia (AU) | 2016-11-18 | Release date supported by multiple public references; primary Nintendo AU source still to be archived | `CTR-BNDP-AUS` | Unknown | Shares `BNDP` family lead with Europe but must not be assumed byte-identical. |
| Europe (EUR) | 2016-11-23 | Official Nintendo Europe pages | `CTR-BNDP-EUR`; eShop family `BNDP` | Unknown | European release explicitly five days after the 2016-11-18 baseline regions. |
| South Korea (KOR) | 2016-11-18 | Pokémon Korea official page confirms Nov. 2016 and Korean Nintendo as distributor; contemporary Korean-Nintendo-sourced reporting confirms the 18th | `CTR-BNDK-KOR` | Unknown | Exact package/build identity remains unverified. |
| Hong Kong market | 2016-11-18 | Nintendo (Hong Kong) official press release | `CTR-BNDW-CHT` lead for Traditional-Chinese-region distribution | Unknown | Official material explicitly describes both Traditional-Chinese-system and Japanese-system software offerings; both allow selection of all nine in-game languages. |
| Taiwan market | 2016-11-18 | Nintendo (Hong Kong) official Taiwan press material | `CTR-BNDW-CHT` lead for Traditional-Chinese-region distribution | Unknown | Official material states simultaneous Hong Kong/Taiwan launch and the same two system-targeted offerings. Do not assume HK/TW packages are identical without direct evidence. |
| Mainland China / CHN-specific software | No distinct CHN target identified | Official Simplified-Chinese Sun/Moon site discusses only Japanese-region and Traditional-Chinese-region 3DS software | None identified | Unknown | Simplified Chinese is an in-game language option. Current first-party evidence does **not** establish a separate mainland-China/iQue Sun build or package. |

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

The official Simplified-Chinese Sun/Moon site makes the same separation visible from the other direction: it tells users of Japanese-version and Traditional-Chinese-version Nintendo 3DS systems to purchase the corresponding regional software, and explains that either software can select Simplified Chinese at game start. It does not identify a third mainland-China/iQue software package.

This common game capability does **not** prove that every regional package, eShop listing, executable, RomFS, manual, rating wrapper, or external distribution record is byte-identical. Regional packaging language fields can also differ from the languages selectable after boot.

## Product-code leads

Current physical/distribution code evidence is deliberately recorded at different strengths:

| Lead | Reported region | Status |
| --- | --- | --- |
| `CTR-P-BNDJ` | Japan physical | Multiple independent Japanese retailer/catalog matches |
| `CTR-BNDE-USA` | North America | Secondary release-database lead; direct verification pending |
| `CTR-BNDP-AUS` | Australia | Secondary release-database lead; direct verification pending |
| `CTR-BNDP-EUR` | Europe | Secondary release-database lead; direct verification pending |
| `CTR-BNDK-KOR` | South Korea | Secondary release-database lead; direct verification pending |
| `CTR-BNDW-CHT` | Traditional-Chinese-region distribution | Secondary release-database lead; direct verification pending |

Public 3DS catalogs also repeatedly associate the application Title ID `0004000000164800` with Pokémon Sun and the update Title ID `0004000E00164800` with its update data. These are retained as technical targeting leads, not project-verified build identities.

## First-party release evidence captured in this batch

### Japan

The Japanese Pokémon Sun/Moon official site lists 2016-11-18 as the release date for Nintendo 3DS.

Source: https://www.pokemon.co.jp/ex/sun_moon/

Japanese retail/catalog sources independently agree on physical code `CTR-P-BNDJ` and JAN `4902370534009`; see `SUN_IDENTIFIERS.md`.

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
- Simplified-Chinese Hong Kong press release: https://www.nintendo.com/hk/pressrelease/3ds_20160920_sun_moon_release_sc.html
- Taiwan press release: https://www.nintendo.com/tw/pressrelease/3ds_20161118_sun_moon_release.html
- Earlier Taiwan product announcement: https://www.nintendo.com/tw/pressrelease/3ds_20160602_sun_moon_release.html

This is strong evidence that **hardware/distribution region and selected in-game language are separate axes** and must be modeled separately in the project.

### Simplified Chinese and mainland-China distinction

The official Simplified-Chinese Sun/Moon site lists a 2016-11-18 product release date, but its hardware note identifies only Japanese-region and Traditional-Chinese-region Nintendo 3DS systems/software and tells those users to purchase the corresponding software. It also says both versions can select Simplified Chinese.

Source: https://www.pokemon-sunmoon-cn.com/sc/

Therefore the project currently interprets the official evidence conservatively as **official Simplified-Chinese localization available through JPN/Traditional-Chinese-region software**, not proof of a distinct CHN/iQue retail target. A separate mainland-China build remains unestablished unless stronger evidence appears.

## Secondary cross-checks and conflicts

### GameFAQs release data

GameFAQs currently lists the region/product-code combinations recorded above, including Japanese, North American, Australian, European, Korean, and Traditional-Chinese Asian entries.

Source: https://gamefaqs.gamespot.com/3ds/187276-pokemon-sun/data

### Bulbapedia

The general Sun/Moon page currently lists mainland China as a 2016-11-18 release, while Bulbapedia's dedicated mainland-China history states that no Pokémon Nintendo 3DS games were released in mainland China and that compatible Taiwanese-region software could be used on Chinese-region iQue 3DS XL systems in some cases. Because this internal secondary-source conflict exists, the general release-table claim is not used as authoritative evidence for a CHN-specific Sun build.

Sources:

- General game page: https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_Sun_and_Moon
- Mainland-China history: https://bulbapedia.bulbagarden.net/wiki/Pok%C3%A9mon_in_mainland_China

### 3DSDB

The public catalog associates Pokémon Sun with Title ID `0004000000164800` and product-code family `CTR-BNDA` in cataloged entries.

Source: https://3dsdb.com/

## Important unresolved questions

- Are Japan, North America, Australia, Europe, Korea, Hong Kong and Taiwan separate executable/RomFS builds, region wrappers around shared content, or some combination?
- Which components are byte-identical across regions, and which differ only in metadata, manuals, ratings, or distribution packaging?
- Does one shared application Title ID cover all supported hardware regions while NCCH/exheader metadata or distribution wrappers differ?
- Does the reported `CTR-BNDW-CHT` identifier map specifically to the Traditional-Chinese-system software referenced by Nintendo (Hong Kong), and what identifier corresponds to the Japanese-system offering sold in Hong Kong/Taiwan?
- Are Hong Kong and Taiwan physical packages/serials identical or separately localized despite sharing distribution announcements?
- What archived first-party Korean Nintendo page records the exact 2016-11-18 Korean date and package identifiers?
- Is there any distinct CHN/iQue distribution artifact not mentioned by the current official Simplified-Chinese pages?
- What are the exact cartridge/eShop content versions and cryptographic hashes for every target?

## Verification policy

Public product-code, Title-ID, and release-database leads are not promoted to `Observed`, `Verified`, or `Matched` solely from catalog listings. They remain investigation targets until stronger evidence satisfies the repository's verification rules.
