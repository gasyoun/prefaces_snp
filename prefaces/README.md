# SNP — Front matter (prefaces)

OCR + translation of the **front matter** of the Cologne dictionary **SNP** — G. J. Meulenbeld, *Sanskrit names of plants and their botanical equivalents* (Appendix Four to *The Mādhavanidāna and its Chief Commentary*, Leiden: E. J. Brill, 1974), together with R. P. Das's *Additions* (in *Das Wissen von der Lebensspanne der Bäume = Surapāla's Vṛkṣāyurveda*, Stuttgart: Franz Steiner, 1988).

- **Dictionary:** SNP (Meulenbeld plants)
- **Author of the source work:** Gerrit Jan Meulenbeld; additions by Rahul Peter Das / Meulenbeld
- **CDSL editors of the digital edition:** Jim Funderburk, Thomas Malten, Peter M. Scharf
- **Years:** 1974 (Part 1), 1988 (Part 2, additions); digital edition 2014
- **Source language:** **English** (with Sanskrit plant names in IAST, Latin botanical binomials, and a few French/German bibliographic titles left verbatim)
- **Cologne source (online index):** [snppref.html](https://sanskrit-lexicon.uni-koeln.de/scans/csldev/csldoc/build/dictionaries/prefaces/snppref.html)
- **Scans:** 7 pages, from `_images/snp_001…004.jpg` (Part 1: title, contents, introduction) and `_images/snp-ad_01…03.jpg` (Part 2: preface to additions / additional abbreviations).

Because the source language is English, there is **no `.en.md`** layer — the base `snprefNN.md` files *are* the English edition. A Russian translation (`.ru.md`) is provided for every page.

## File conventions

| Suffix | Meaning |
|---|---|
| `snprefNN.md` | Faithful OCR of page NN, source language (English) |
| `snprefNN.ru.md` | Russian translation of page NN |
| `snppref_all.en.md` | All pages, English, single file (+ TOC) |
| `snppref_all.ru.md` | All pages, Russian, single file (+ TOC) |
| `build_combined.py` | Reproducible generator of the `*_all.*` files (`DICT=snp python build_combined.py`) |
| `scans/` | Source page images downloaded from the Cologne csldoc server |

## Consolidated editions

| Language | File |
|---|---|
| English (source) | [snppref_all.en.md](snppref_all.en.md) |
| Russian | [snppref_all.ru.md](snppref_all.ru.md) |

Build with: `DICT=snp python build_combined.py`

## Contents

| NN | Section | Vol. | Source scan | English | Russian |
|---|---|---|---|---|---|
| 01 | Mādhavanidāna Title Page | 1 | [snp_001.jpg](scans/snp_001.jpg) | [snppref01.md](snppref01.md) | [snppref01.ru.md](snppref01.ru.md) |
| 02 | Partial contents (p. VI) | 1 | [snp_002.jpg](scans/snp_002.jpg) | [snppref02.md](snppref02.md) | [snppref02.ru.md](snppref02.ru.md) |
| 03 | Appendix 4 Introduction, 1 (p. 520) | 1 | [snp_003.jpg](scans/snp_003.jpg) | [snppref03.md](snppref03.md) | [snppref03.ru.md](snppref03.ru.md) |
| 04 | Introduction, 2 (p. 521) | 1 | [snp_004.jpg](scans/snp_004.jpg) | [snppref04.md](snppref04.md) | [snppref04.ru.md](snppref04.ru.md) |
| 05 | Preface to additions, 1 (p. 425) | 2 | [snp-ad_01.jpg](scans/snp-ad_01.jpg) | [snppref05.md](snppref05.md) | [snppref05.ru.md](snppref05.ru.md) |
| 06 | Preface to additions, 2 (p. 426) | 2 | [snp-ad_02.jpg](scans/snp-ad_02.jpg) | [snppref06.md](snppref06.md) | [snppref06.ru.md](snppref06.ru.md) |
| 07 | Preface to additions, 3 (p. 427) | 2 | [snp-ad_03.jpg](scans/snp-ad_03.jpg) | [snppref07.md](snppref07.md) | [snppref07.ru.md](snppref07.ru.md) |

## Notes

- **Source language is English** — confirmed from [`csl-orig/v02/snp/snpheader.xml`](https://github.com/sanskrit-lexicon/csl-orig/blob/master/v02/snp/snpheader.xml) (`titleStmt` `xml:lang="en-Latn"`, `langUsage` = English + Sanskrit) and from the scans themselves.
- **Two source works / two page-number ranges.** Vol. 1 pages (520-521) are from Meulenbeld 1974; vol. 2 pages (425-427) are from Das 1988. The contents page is paginated VI.
- **Sanskrit** stays verbatim in IAST (ā ī ū ṛ ñ ṭ ḍ ṇ ś ṣ ḥ ṃ …); **Latin botanical binomials** (COMMIPHORA, BALSAMODENDRUM, CARPOPOGON PRURIENS, etc.) kept as printed; **bibliographic titles** (German *Das Wissen von der Lebensspanne der Bäume*; French *La Hārītasaṃhitā … nomenclature âyurvédique*) left in their original language/script.
- The **title page** carries a printer's device (*TUTA SUB AEGIDE PALLAS · EJB ·*) and a library stamp (*Indologisches Seminar der Universität Bonn*); both are recorded as bracketed notes.
- **Digitizer stamps** (running header / Cologne footer) were omitted, per the OCR convention. The "[Br]" source-citation header on the additions page (a cataloguing line, not original text) is preserved as a small `<sub>` note because it documents the 1988 source.
- Pages 03-04 reproduce, after the Introduction, the first two glossary entries (*akṣa*, *agaru*) as printed on the scan — they are the opening of the dictionary body, captured here for completeness.

## ⚠️ Home-repo decision needed

**SNP has no dedicated GitHub repository under `sanskrit-lexicon`.** This `prefaces_snp/` working directory holds all output but has **not been committed or pushed anywhere**. A maintainer decision is needed on where these files should live — e.g. a new `sanskrit-lexicon/SNP` repo, a `prefaces/` folder inside `csl-orig/v02/snp/`, or another host. Until then, treat this directory as the canonical (uncommitted) deliverable.

<details>
<summary><strong>OCR run notes (2026-06-22)</strong> — cost, timing, and technical lessons</summary>

Produced by the `/cologne-preface-ocr` skill (synchronous, single-thread; **no subagents** per the per-dict prompt and `.preface_retry_rules.md`). Process retrospective, not part of the deliverable.

**Cost.** All OCR done on the main thread (no subagents). 7 scans × ~4 native-resolution crop reads each ≈ 28 image reads, plus 14 page writes (7 source + 7 RU), 2 consolidated files, README, and the source-file identity check. Estimated main-thread total ≈ **0.4–0.5 M tokens**.

**Time.** Wall-clock ≈ 15-20 min, gated by the one-at-a-time foreground scan downloads (2 s sleep between, rate-limit-sensitive Cologne server) and the sequential crop→read loop.

**Technical lessons (reusable):**
1. The toctree's embedded image is **`.jpg`, not `.png`** for SNP — the skill's `grep '_images/[^"]+\.png'` returned nothing; widen to `\.(jpg|png)`.
2. Scans are pre-downsampled to **1892 × 2834** (≈1.4 MB JPEGs). Width is already ≤1900, so a full-width horizontal band reads fine; only the 2834 px height needs splitting (4 overlapping bands per page).
3. **Two publications in one front matter**: vol. 1 = Meulenbeld 1974 (pp. 520-521), vol. 2 = Das 1988 additions (pp. 425-427). Page numbers are *not* monotonic across the set — trust the section labels, not the numbers.
4. Source language = **English**, so no `.en.md` layer; `build_combined.py` was adapted to emit `snppref_all.en.md` from the base `.md` files.
5. **No GitHub repo** for SNP — output parked in `GitHub/prefaces_snp/`, uncommitted, pending a home-repo decision (see above).

</details>
