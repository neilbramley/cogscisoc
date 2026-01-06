# Changelog

## 2026

### v2.2026.1

- LaTeX
  - Replace `\twopagesummarysubmission` document command with `twopagesummary` package option
  - Mark `\cogscifinalcopy` document command for future deprecation in favor of `final` package option
  - Make expl3 option handling more versatile and robust
  - Refactor `cogsci.sty` to include template-essential typesetting packages originally in the `*.tex` files
  - Pass BibLaTeX style (`style=apa`) from `cogsci.sty`
  - Auto-load hyperref at end of preamble; add `hyperref`/`nohyperref` package options
  - Disable microtype protrusion via `\PassOptionsToPackage` to prevent characters exceeding margins if the microtype package is used
  - Use `@pdfthesis{}` rather than `@thesis{type={...}}`
- Typst
  - Bump [cogsci-typst-template](https://github.com/daeh/cogsci-typst-template) to v0.1.3
- Word
  - Remove anonymized full paper template in favor of single (deanonymized) template
  - Add manual spacing to titlebox

### v2.2026.0

- Update instructions for the 2026 Conference

  - Change titlebox author/affiliation format (authors listed together with superscript numbers linking to grouped affiliations; only corresponding author includes email; postal addresses removed)

  - Add AI use disclosure requirements to Acknowledgments section

  - Add 150-word limit for abstracts

  - Update guidelines for in-text citations and reference list formatting to reflect APA 7th edition

    - Use "et al." for 3+ authors (no first-citation special formatting); include DOIs/URLs; CogSci page numbers exemption removed

  - Use periodical form for CogSci Proceedings references:

    **Correct form** (periodical model, serial type, ISSN format, APA7)

    > August, B. C., Benally, C. D., & Cadena, D. E. (2007). Example conference paper title. *Proceedings of the Annual Meeting of the Cognitive Science Society*, *29*, 100–105. <https://escholarship.org/uc/item/k0e1y2>

    Outmoded form (monograph model, book type, ISBN format, APA6/APA7)

    > August, B. C., Benally, C. D., & Cadena, D. E. (2007). Example conference paper title. *Proceedings of the 29th Annual Conference of the Cognitive Science Society* (pp. 100–105). Hillsdale, NJ: Lawrence Erlbaum Associates.

    Outmoded form (anthology model, edited volume type, ISBN format, APA6)

    > August, B. C., Benally, C. D., & Cadena, D. E. (2007). Example conference paper title. In *Proceedings of the 29th Annual Conference of the Cognitive Science Society* (pp. 100–105). Hillsdale, NJ: Lawrence Erlbaum Associates.

- Modernize LaTeX template

  - Substantial refactor of `cogsci.sty` to improve consistency with explicit formatting directives
  - Update LaTeX 2.09 commands to LaTeX2e commands
  - Add expl3 key–value option processing (with `l3keys2e` fallback for LaTeX distributions prior to June 2022)
  - Add `authblk` package option for structured author/affiliation formatting
  - Make titlebox height dynamic (minimum 1.75 inches, expands to fit content)
  - Replace obsolete `pslatex` with `newtxtext` and `newtxmath` (TeX Gyre Termes)
  - Add `cmap`, `fontenc`, `babel`, `csquotes`, and `hyperref`
  - Switch from `apacite` (APA 6th edition) to BibLaTeX with `biblatex-apa` (APA 7th edition) and Biber backend (bb3034f); remove bundled `apacite.sty` and `apacite.bst` (ffde557)
    - Update `.bib` files based on BibLaTeX best practices: use specific entry types (e.g., `@phdthesis{}` rather than `@thesis{type=phdthesis}`); use `date` instead of `year`, `journaltitle` instead of `journal`; remove `address` fields (APA7 omits publisher location); add `doi` and `url` fields

- Add Typst template

  - Clone full paper template from [cogsci-typst-template](https://github.com/daeh/cogsci-typst-template) (96f02c7)
  - Add 2-page short summary template (bb3034f)
  - Bundle TeX Gyre Termes fonts for local compilation (bb3034f)
  - Bump `cogsci-conference` to v0.1.2

- Use pseudodata for paper authors and citations in templates

- Reorganize file structure (ffde557)

  - Flatten directory layout, rename files, purge superfluous and outdated Microsoft Word templates

<details>
<summary>Additional <code>cogsci.sty</code> changes</summary>

- Fix bottom margin by setting `\maxdepth` to account for descenders (avoids ink overflow into margins)
- Fix top margin positioning by setting `\topskip` to 0.01pt (avoids LaTeX output routine bug with 0pt)
- Redesign abstract environment with explicit 1/8" margins; conditionally omit "Abstract" heading for two-page summaries
- Recalculate section heading spacing to account for font size transitions
- Standardize paragraph indent to 1/8" (was 10pt)
- Remove `\AtBeginDocument` baselineskip hack (now handled by `\@setfontsize` definitions)
- Add proper `\NeedsTeXFormat` and `\ProvidesPackage` declarations

</details>

## 2020

- CC-BY licensing required for proceedings contributions

## 2019

- Introduce double-blind reviewing for 6-page paper submissions
- Add author anonymity switch to templates
- Add author anonymity switch to `cogsci.sty`, borrowing from ACL style files (Roger Levy, rplevy@mit.edu, MIT, 12/31/2018)
- Add `float` package; change figure/table placement to `[H]` for conformity with Word template (Roger Levy, rplevy@mit.edu, MIT, 12/31/2018)

## 2015

- Update template and bibliography (David Noelle, dnoelle@ucmerced.edu, UC Merced, 11/19/2014)

## 2007

- Modify `cogsci.sty` (Niels Taatgen, taatgen@cmu.edu, CMU, 10/24/2006)

## 2006

- Update template, style file, and bibliography (Eli M. Silk, esilk@pitt.edu, University of Pittsburgh, 05/24/2005)

## 2005

- Template modifications (Ken Forbus, 01/23/2004)

## 2001

- Move customizations from sample `.tex` files to `cogsci.sty` (Mary Ellen Foster, M.E.Foster@ed.ac.uk, University of Edinburgh, 12/11/2000)

## 2000

- Template modifications (Trisha Yannuzzi, trisha@ircs.upenn.edu, UPenn, 12/28/1999)

## 1999

- Template modifications (Tina Eliassi-Rad, eliassi@cs.wisc.edu, University of Wisconsin, 01/31/1998)

## 1998

- Template modifications (Pat Langley, langley@cs.stanford.edu, Stanford, 01/26/1997)
- LaTeX 2.09 to LaTeX2e corrections (Ramin Charles Nakisa, 01/28/1997)

## 1997

- Template modifications (David Noelle, noelle@ucsd.edu, UCSD, 03/15/1996)

## 1996

- Template modifications (Johanna Moore, jmoore@cs.pitt.edu, University of Pittsburgh, 03/17/1995)

## 1995

- Original template created, based on earlier style files for IJCAI-89, AAAI-90, COGSCI-91 (Ashwin Ram, ashwin@cc.gatech.edu, Georgia Tech, 04/01/1994)
