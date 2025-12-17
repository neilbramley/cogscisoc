# Cognitive Science Society Annual Conference Materials

**Submission templates for the Annual Meeting of the Cognitive Science Society.**

Templates are available in three formats, described in the **[LaTeX](#LaTeX)**, **[Typst](#Typst)**, and **[Microsoft Word](#Microsoft-Word)** sections below. The directory corresponding to each format contains templates for *6-page full papers* and *2-page short summaries*, along with examples of the compiled PDFs.

## Important Notes

### Double-Blind Reviewing

Beginning in 2019, 6-page full paper submissions are reviewed double-blind, so submissions must be anonymized. **The policy for double-blind reviews is strictly enforced.** Ensure your submissions are anonymized before submission.

### Page Limits

In the *initial submission*, full papers can be no longer than six pages plus an unlimited number of pages for references. In the *final submission*, full papers (including the title and authors) can be no longer than six pages plus an unlimited number of pages for acknowledgments and references.

The text of the paper should be formatted in two columns with an overall width of 7 inches and length of 9.25 inches, with 0.25 inches between the columns. Leave two line spaces between the last author affiliation and the text of the paper; the text of the paper (starting with the abstract) should begin no less than 2.75 inches below the top of the page. The left margin should be 0.75 inches and the top margin should be 1 inch.

### CC-BY Licensing

An online proceedings will be published by the Cognitive Science Society. At the time of final (camera-ready) submission, authors will be required to agree to release their proceedings contribution under a CC-BY license. This means that authors allow free reuse of their work provided the original authors are attributed.

## LaTeX

Files in the [`latex/`](latex/) directory include:

- [`cogsci_full_paper_template.tex`](latex/cogsci_full_paper_template.tex) — 6-page full paper template ([anonymized PDF](latex/cogsci_full_paper_template_anonymized.pdf), [deanonymized PDF](latex/cogsci_full_paper_template_deanonymized.pdf))
- [`cogsci_2page_short_summary_template.tex`](latex/cogsci_2page_short_summary_template.tex) — 2-page short summary template ([PDF](latex/cogsci_2page_short_summary_template.pdf))
- [`cogsci.sty`](latex/cogsci.sty) — style file
- [`cogsci_bibliography_template.bib`](latex/cogsci_bibliography_template.bib) — example BibLaTeX bibliography

**Anonymization:** The full paper template anonymizes authors by default. Use `\cogscifinalcopy` to deanonymize the final camera-ready version.

### Overleaf Web App

For convenience, this template is also available on [Overleaf](https://www.overleaf.com/latex/templates/cognitive-science-society-conference-cogsci-template/ysczfkpyjpqw).

## Typst

Files in the [`typst/`](typst/) directory include:

- [`cogsci_full_paper_template.typ`](typst/cogsci_full_paper_template.typ) — 6-page full paper template ([anonymized PDF](typst/cogsci_full_paper_template_anonymized.pdf), [deanonymized PDF](typst/cogsci_full_paper_template_deanonymized.pdf))
- [`cogsci_2page_short_summary_template.typ`](typst/cogsci_2page_short_summary_template.typ) — 2-page short summary template ([PDF](typst/cogsci_2page_short_summary_template.pdf))
- [`cogsci_bibliography_template.bib`](typst/cogsci_bibliography_template.bib) — example BibLaTeX bibliography

These templates use the official style from the Typst Universe: [`cogsci-conference`](https://typst.app/universe/package/cogsci-conference).

Templates require the fonts [TeX Gyre Termes](https://www.gust.org.pl/projects/e-foundry/tex-gyre) and [TeX Gyre Termes Math](https://www.gust.org.pl/projects/e-foundry/tg-math/index_html), which are distributed under the [GUST Font License (GFL)](https://tug.org/fonts/licenses/GUST-FONT-LICENSE.txt). The Typst web app includes these fonts automatically. For local usage, this repository includes OTF files in [`typst/fonts/`](typst/fonts/). You can install the fonts system-wide or pass the `fonts` directory path to the compiler (see below).

**Anonymization:** The full paper template is initialized to anonymize authors. Set `anonymize: false` to deanonymize the final camera-ready version.

### Typst Web App

The [`cogsci-conference`](https://typst.app/universe/package/cogsci-conference) template is available in the [Typst web app](https://typst.app/). To use it, click "Start from template" on the dashboard and search for `cogsci-conference`. If you don't see the dashboard when you visit <https://typst.app/>, you need to create and/or log in to an account.

### Local Usage

If you're using Typst locally, you might find the [Tinymist Typst VS Code Extension](https://marketplace.visualstudio.com/items?itemName=myriad-dreamin.tinymist) (the [Tinymist](https://myriad-dreamin.github.io/tinymist/) extension for [Visual Studio Code](https://code.visualstudio.com/)) convenient.

To compile the PDF, use the Typst CLI or the Tinymist extension.

<details>
<summary>Typst PDF Compilation</summary>

With the Typst CLI:

```shell
typst compile --font-path fonts --pdf-standard a-3u cogsci_full_paper_template.typ
```

If the required fonts are installed system-wide, you can omit `--font-path`. Otherwise, use `--font-path <path-to-fonts-dir>` to specify a directory containing the OTF files. With the [Tinymist Typst VS Code Extension](https://marketplace.visualstudio.com/items?itemName=myriad-dreamin.tinymist), specify the font directory with the `tinymist.fontPaths` setting (see the Tinymist [documentation](https://myriad-dreamin.github.io/tinymist/config/vscode.html) for details).

Specifying a [PDF standard](https://typst.app/docs/reference/pdf/#pdf-standards) like `--pdf-standard a-3u` is optional but ensures that the PDF text is searchable.

</details>

## Microsoft Word

Files in the [`word/`](word/) directory include:

- [`cogsci_full_paper_template_anonymized.dotx`](word/cogsci_full_paper_template_anonymized.dotx) — 6-page full paper template, anonymized ([PDF](word/cogsci_full_paper_template_anonymized.pdf))
- [`cogsci_full_paper_template_deanonymized.dotx`](word/cogsci_full_paper_template_deanonymized.dotx) — 6-page full paper template, deanonymized ([PDF](word/cogsci_full_paper_template_deanonymized.pdf))
- [`cogsci_2page_short_summary_template.dotx`](word/cogsci_2page_short_summary_template.dotx) — 2-page short summary template ([PDF](word/cogsci_2page_short_summary_template.pdf))

The template files are in `.dotx` format (not `.docx`). When you open, edit, and save a template, Word will prompt you to save the edited version as a `.docx` file.

**Anonymization:** Use the anonymized template for the initial submission; use the deanonymized template for the final camera-ready version.
