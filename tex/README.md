# LaTeX scaffold for the Foundations and Trends monograph

This project is a clean, compileable monograph scaffold organized chapter-by-chapter.
It mirrors the accepted proposal structure for:

**Task Coordination for Multi-Agent Systems under Complex Temporal Tasks**  
**Authors:** Meng Guo, Zhongkui Li

## Build

Recommended:
```bash
latexmk -pdf main.tex
```

Fallback:
```bash
pdflatex main.tex
pdflatex main.tex
```

## Structure

- `main.tex` — master file
- `preamble/packages.tex` — package imports
- `preamble/macros.tex` — reusable commands
- `frontmatter/` — title page, abstract, preface
- `chapters/` — one file per chapter
- `backmatter/` — list of symbols and references placeholders
- `figures/`, `tables/` — asset folders
- `notes/` — scratch notes

## Notes

- The files currently contain outline-only placeholders (`TODO`).
- Each chapter is separated into its own `.tex` file.
- Section headings follow the accepted proposal so we can expand the manuscript incrementally.
- A neutral `book`-class scaffold is used so the project compiles cleanly while content is being drafted.
- `backmatter/references.bib` is included as a starter BibTeX database for later population.
