# The Extended African Comparative Wordlist (EACW)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23677135.svg)](https://doi.org/10.5281/zenodo.23677135)

*The Extended African Comparative Wordlist: A digital lexical organization system for field linguists.*

The EACW is a comparative wordlist and a system of lexical reference for field linguists: 2,556 items in nineteen semantic sections, 2,274 of which make up its default list. Every item has a reference that says something about it (C001f *mother*: C for kinship, 001 for *parent*, f for female), a default word class, a clarification where the gloss needs one, a taxon for animals and plants, a regional code, and its numbers in the SIL Comparative African Wordlist (CAWL) and the Swadesh list.

**This repository is the definitive EACW.** The list printed in the paper that describes it is one edition; the files here are maintained, corrected and extended in dated editions, and will carry the list's translations into languages of wider communication.

- **Current edition:** 2026-10-24
- **Licence:** Creative Commons Attribution 4.0 International ([CC BY 4.0](LICENSE)), © 2026 Joshua A. G. Smolders
- **DOI (all editions, always the newest):** [10.5281/zenodo.23677135](https://doi.org/10.5281/zenodo.23677135)
- **DOI of edition 2026-10-24:** [10.5281/zenodo.23677136](https://doi.org/10.5281/zenodo.23677136)

## Citing it

> Smolders, Joshua A. G. 2026. *The Extended African Comparative Wordlist (EACW)*, edition 2026-10-24 [dataset]. Zenodo. https://doi.org/10.5281/zenodo.23677136

Cite the edition you used: each edition has a DOI of its own. To refer to the EACW in general, use the DOI for all editions, [10.5281/zenodo.23677135](https://doi.org/10.5281/zenodo.23677135), which always points to the newest. The paper that explains the list:

> Smolders, Joshua A. G. 2026. The Extended African Comparative Wordlist: A digital lexical organization system for field linguists. Manuscript.

## The files

All files are UTF-8, tab-separated, with a header row.

### `eacw.tsv`: the list

One row per item, in the list's order.

| Column | Contents |
|---|---|
| `ref` | The EACW reference (A001, A002b, C001f, R3SGDPRX, Q005) |
| `gloss` | The English gloss, written to be safe in file names |
| `word_class` | The default word class (NOUN, VERB, ADJECTIVE, PRONOUN, QUANT, ADVERB, CONJ, DEM, INTERJ, INTERROG, NEG, PREP); a default only, to be changed where the language differs |
| `default` | `yes`: in the default (published) list; `no`: a hidden item, a recommended variant to add where the language calls for it |
| `sub` | The regional code: blank, everywhere; `A`, all of Africa; `E`, `W`, `N`, `S`, `C` (space-separated when several): only East Africa and the Horn, West, North Africa and the Sahara, Southern, Central Africa |
| `clarification` | The gloss's plain meaning, where it needs one |
| `taxon` | For animals and plants: genus and species, with the family in brackets (*Capra hircus (Bovidae)*) |

### `cawl.tsv`: the SIL Comparative African Wordlist

One row per CAWL item: `number` (0001–1700), `domain` (its section number), `word_class`, and **`eacw`**, the EACW items it corresponds to (space-separated). The `gloss` and `french` columns are empty: the CAWL states no licence, so its glosses are left out until SIL International gives permission. Only the CAWL's numbers and section numbers are here, for the correspondences.

### `swadesh.tsv`: the Swadesh list

The 207 items combining Swadesh's 100- and 200-word lists (Swadesh 1952, 1955): `number`, `gloss`, `word_class`, **`eacw`** (its EACW items) and `cawl` (its CAWL number, where there is one).

### How the correspondences work

- An underspecified CAWL or Swadesh item links to **every form it covers** (Swadesh *we* → R1PL, R1DU, R1PLIN, R1PLEX).
- An ambiguous CAWL item takes a reference on **each EACW item that clarifies it** (CAWL 0358 *nephew* → C022m, C025m).
- In the human terms (B and C), links follow the family: an ungendered item links to the generic and its female and male forms; a gendered pair also links to its generic; except where the generic and its gendered forms each have links of their own.
- An item never links to the parts of what it names, to other referents, or to another word class where the exact item exists.
- 1,694 of the CAWL's 1,700 items and all 207 Swadesh items have an EACW counterpart; 1,958 EACW items carry a CAWL or Swadesh number.

## The reference system in brief

- **A section letter and three digits** (A001), in the list's order: A Human body, B Human designations, C Kinship terms and ethnonyms, D Mammals, E Birds, F Fish, G Reptiles and amphibians, H Insects and other small things, I Spiritual, disease, ceremony, J Flora, food, drink, K Cultural artifacts, L Inanimate nature, M Speech, thought, N Space, direction, time, O Other, P Property concepts, Q Quantifiers, R Pronouns, V Verbs. S, T, U and W–Z are left free for songs, texts, utterances and categories of the researcher's own.
- **Q** is the number itself (Q005 *five*, Q1736); **R** takes a gloss code (R1SG, R1PLIN, R3SGDPRX, RLOCDADR).
- **Sub-letters:** a lone **b** (c, d…) marks related terms (A002 *skin* → A002b *wrinkle*); an **a, b, c** series marks the parts of a whole (A030a *upper cheek*, A030b *lower cheek*).
- **f and m are female and male**, and reserved for that in every section (B001f *woman*, B001m *man*).
- **Trees:** a hidden generic, **a** the tree, **b** the fruit (J051a *mango tree*, J051b *mango fruit*).
- **Private use areas:** ethnic groups are C + the ISO 639-3 code of the group's language (CORM *Oromo*); class pronouns RC + the class (RC3).
- **New items** go after the last item of their section with the next number; numbers are never reused.

## Versions of the list

A version is two choices: the **default items only** or the **hidden items too**, and **which region**.

| Region | Default items | With hidden items |
|---|---|---|
| Global (blank codes only) | 2,055 | 2,316 |
| Africa (every code) | 2,274 | 2,556 |
| East Africa and the Horn | 2,255 | 2,535 |
| West Africa | 2,204 | 2,482 |
| North Africa and the Sahara | 2,110 | 2,380 |
| Southern Africa | 2,209 | 2,486 |
| Central Africa | 2,203 | 2,480 |

A single region takes the blank codes, the A codes and that region's letter.

## Editions

Each release is an edition named by its date; [EDITIONS.md](EDITIONS.md) says what each one changed, so that a database built on an earlier edition can be brought up to date.

## Corrections and suggestions

Please open an [issue](../../issues) for a wrong gloss, a missing item, a doubtful correspondence or a regional code that should change. Corrections go into the next edition.

## References

- Dixon, R. M. W. 2010. *Basic linguistic theory*, vol. 1: *Methodology*. Oxford: Oxford University Press.
- Snider, Keith & James Roberts. 2006. *SIL Comparative African Wordlist (SILCAWL)* (SIL Electronic Working Papers 2006-005). Dallas: SIL International.
- Swadesh, Morris. 1952. Lexico-statistic dating of prehistoric ethnic contacts: With special reference to North American Indians and Eskimos. *Proceedings of the American Philosophical Society* 96(4). 452–463.
- Swadesh, Morris. 1955. Towards greater accuracy in lexicostatistic dating. *International Journal of American Linguistics* 21(2). 121–137. https://doi.org/10.1086/464321.
