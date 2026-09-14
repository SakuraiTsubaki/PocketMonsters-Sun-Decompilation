# Pokémon Sun — Regional Update Matrix

## Purpose

Track Pokémon Sun update releases by region/source without assuming that publication dates, update packages, or identifiers are globally identical.

The project has no retail/update binaries. All build hashes and update-title identifiers therefore remain unresolved until independently verified.

## Update evidence matrix

| Region/source | Ver.1.1 date shown | Ver.1.2 date shown | Evidence | Notes |
| --- | --- | --- | --- | --- |
| Japan | 2017-01-11 | 2017-05-17 | Nintendo Japan support | Official Japanese update history. |
| North America | 2017-01-10 | 2017-05-16 | Nintendo of America support | One calendar day earlier than Japan/HK; likely publication-time-zone presentation must be tested rather than treated as a distinct code revision. |
| Hong Kong / Taiwan distribution | 2017-01-11 | 2017-05-17 | Nintendo (Hong Kong) | Official Traditional-Chinese support pages; explicitly separate Sun and Moon update downloads. |
| South Korea | Ver.1.1 confirmed in distribution notice | TBD | Pokémon Korea | Pokémon Korea posted a Ver.1.1 distribution notice dated 2017-01-13, referring users to Korean Nintendo for details. Exact package publication time/date needs archival confirmation. |
| Europe | TBD | TBD | TBD | European first-party update page still to be captured. |
| Australia | TBD | TBD | TBD | Australian first-party update page still to be captured. |

## Fix-content comparison

The official Japanese, North American, and Hong Kong materials describe the same core fixes.

### Ver.1.1

- Memento / Parting Shot behavior corrected.
- Rocky Helmet battle win/loss judgment corrected.
- Certain Pokémon evolution move-learning issue corrected.
- Additional unspecified gameplay fixes.

### Ver.1.2

- Sky Drop interaction with a Pokémon using Spiky Shield corrected.
- Scatterbug Egg Move issue corrected.
- Additional unspecified gameplay fixes.

The matching public fix lists strongly suggest equivalent update intent across these regions, but **do not prove byte-identical update packages**.

## Important regional observation

Nintendo of America lists Ver.1.1 as 2017-01-10 and Ver.1.2 as 2017-05-16, while Nintendo Japan and Nintendo (Hong Kong) list 2017-01-11 and 2017-05-17 respectively.

This should currently be modeled as a **date/time-zone presentation difference candidate**, not as proof of separate revision numbers or separate code content. Exact CDN/package timestamps, content versions, update Title IDs, and hashes are still required.

## Sun/Moon update separation

Nintendo (Hong Kong) explicitly warns that Pokémon Sun and Pokémon Moon use different update data and directs users to select the separate Sun or Moon update entry in Nintendo eShop.

That confirms at minimum that the two paired games must retain distinct update-package identities in the project even when their public fix descriptions are shared.

## Primary sources

### Japan

Nintendo Japan Support — Pokémon Sun/Moon update data Ver.1.2 page including Ver.1.1 history:

https://support.nintendo.com/jp/3ds/soft/bnda/update/index.html

### North America

Nintendo Support — How to Update Pokémon Sun and Pokémon Moon:

https://en-americas-support.nintendo.com/app/answers/detail/a_id/25400/~/how-to-update-pok%C3%A9mon-sun-and-pok%C3%A9mon-moon

### Hong Kong / Taiwan distribution

Nintendo (Hong Kong) — Ver.1.1 notice:

https://www.nintendo.com/hk/pressrelease/3ds_20170111_sun_moon_update.html

Nintendo (Hong Kong) — Ver.1.2 notice:

https://www.nintendo.com/hk/pressrelease/3ds_20170517_sun_moon_update.html

### South Korea

Pokémon Korea — Ver.1.1 distribution notice:

https://pokemonkorea.co.kr/sun_moon/menu82?mode=view&number=1713

## Unresolved technical fields

- Sun update Title ID for each hardware/distribution region.
- Nintendo CDN content version for v1.1 and v1.2.
- Exact encrypted/decrypted package hashes.
- Whether regional update metadata differs while code/data content remains identical.
- Whether the Japanese-system and Traditional-Chinese-system offerings in Hong Kong/Taiwan use distinct update Title IDs.
- Korean Ver.1.2 first-party archival notice and exact Korean eShop metadata.
- European/Australian first-party update publication metadata.

## Verification state

All release/fix-history statements cited to first-party support pages are source-confirmed historical facts. Build/package identity remains **Unverified** under this repository's build-level verification vocabulary until direct reproducible identity evidence is available.
