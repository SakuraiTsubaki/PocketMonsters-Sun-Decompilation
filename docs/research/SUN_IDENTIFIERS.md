# Pokémon Sun — Product and Update Identifier Research

## Purpose

Track public identifiers for Pokémon Sun while keeping physical-package identifiers, Nintendo 3DS application metadata, eShop metadata, and update metadata separate.

No retail cartridge, installed title, or update package is held by this project. Values below therefore remain public-source research findings until the repository can satisfy its direct target-verification criteria.

## Japanese physical package

Multiple independent Japanese retail/catalog sources agree on the following standard Japanese physical release identifiers:

| Field | Value | Evidence state |
| --- | --- | --- |
| Title | `ポケットモンスター サン` | Public-source agreement |
| Platform | Nintendo 3DS | Public-source agreement |
| Release date | 2016-11-18 | Official + public-source agreement |
| Physical product code | `CTR-P-BNDJ` | Multiple independent Japanese retailer/catalog matches |
| JAN | `4902370534009` | Multiple independent Japanese retailer/catalog matches |
| Rating | CERO A | Multiple Japanese retailer/catalog matches |

Independent matches captured in this batch:

- GEO Online: `CTR-P-BNDJ`, JAN `4902370534009`
- Rakuten Books: `CTR-P-BNDJ`, JAN `4902370534009`
- Suruga-ya: `CTR-P-BNDJ`, JAN `4902370534009`
- Yamada Webcom: `CTR-P-BNDJ`, JAN `4902370534009`

These sources provide substantially stronger support for the physical package code than a single release database, but this remains external evidence rather than direct inspection of a project-held cartridge/package.

## Base application metadata leads

Public Nintendo 3DS catalogs and tooling repeatedly associate Pokémon Sun with:

| Field | Value | Evidence state |
| --- | --- | --- |
| Application Title ID | `0004000000164800` | Multiple public technical-source match |
| Nintendo eShop-style product code | `CTR-N-BNDA` | Public catalog match |
| Generic title/product family | `BNDA` | Public catalog match |

Important distinction:

- `CTR-P-BNDJ` is the Japanese physical-package/software product code reported by Japanese retailers.
- `CTR-N-BNDA` is an eShop/title metadata-style code appearing in public Nintendo 3DS catalogs.
- `CTR-BNDA` is a shorter family value reported by some ROM/release catalogs.

These strings must not be silently treated as interchangeable identifiers.

## Update metadata leads

Multiple public Nintendo 3DS catalogs independently associate the Pokémon Sun update title with:

| Field | Value | Evidence state |
| --- | --- | --- |
| Update Title ID | `0004000E00164800` | Multiple public technical-source match |
| Update product code | `CTR-U-BNDA` | Multiple public technical-source match |
| Final public update | Ver.1.2 | Official Nintendo history |
| Final catalog content version | `2112` | Multiple public catalog match |
| Catalog size | about 36.56 MiB / 292 blocks | Public catalog match; not a project hash identity |

The Title ID relationship is structurally consistent with Nintendo 3DS update titles using the `0004000E` title category while preserving the base title's low identifier (`00164800`). This structural observation is useful, but project records still rely on the independently listed update entries rather than deriving the ID by assumption alone.

## Region observations

Public catalog entries show the same base application Title ID `0004000000164800` and update Title ID `0004000E00164800` in multiple regional catalog datasets, including Korean and Traditional-Chinese-region listings.

This is evidence that the application/update Title IDs are shared across at least multiple cataloged regional distributions. It is **not** yet proof that every regional NCCH/RomFS/update content object is byte-identical.

Region-specific physical package codes remain separate investigation targets, e.g.:

- Japan: `CTR-P-BNDJ` strongly supported by multiple Japanese retailers.
- North America: `CTR-BNDE-USA` release-database lead.
- Europe: `CTR-BNDP-EUR` release-database lead.
- Australia: `CTR-BNDP-AUS` release-database lead.
- Korea: `CTR-BNDK-KOR` release-database lead.
- Traditional-Chinese distribution: `CTR-BNDW-CHT` release-database lead.

The exact label grammar (`CTR-P-*`, packaging suffixes, cartridge label codes, eShop `CTR-N-*`, update `CTR-U-*`) should continue to be recorded as separate fields rather than normalized into one ambiguous "product code" column.

## Sources

### Japanese physical package / JAN cross-checks

- GEO Online — https://ec.geo-online.co.jp/shop/g/g510304503/
- Rakuten Books — https://books.rakuten.co.jp/rb/14334460/
- Suruga-ya — https://www.suruga-ya.jp/kaitori/kaitori_detail/104001199
- Yamada Webcom — https://www.yamada-denkiweb.com/2814094015/

### Base/update technical metadata

- 3DSDB static catalog — https://hax0kartik.github.io/3dsdb/static.html
- 3DSDB Korean catalog source — https://github.com/hax0kartik/3dsdb/blob/master/jsons/list_KR.json
- 3DSDB web catalog — https://3dsdb.com/

### Official update history

- Nintendo Japan Support — https://support.nintendo.com/jp/3ds/soft/bnda/update/index.html

## Verification limits

Do not promote these identifier findings to repository `Observed`/`Matched` solely because multiple databases agree. Under this repository's verification policy, direct target-build observation or reproducible equivalent evidence is still required for build-level verification.

## Next identifier tasks

1. Locate first-party or preserved Nintendo/TPC evidence for the Japanese physical code and JAN where possible.
2. Determine the exact Nintendo eShop metadata fields corresponding to `CTR-N-BNDA` and the base application version.
3. Recover public metadata for Ver.1.1 as well as Ver.1.2, including Nintendo content-version number if available.
4. Determine whether update Title ID/product code are genuinely shared across all regional hardware distributions.
5. Separate physical package code, cartridge label code, eShop product code, application Title ID, update Title ID, and content version in all future manifests.
