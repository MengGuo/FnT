# Revised monograph LaTeX source

Master file: `root.tex`.

Compile with `latexmk -pdf root.tex`, or run `pdflatex root.tex`, `bibtex root`, and `pdflatex root.tex` twice. Required packages include `dsfont`, `siunitx`, and `algorithm2e`.

Substantive revision text is blue through `\rev{...}` and the `revision` environment in `preamble/macros.tex`. The bibliography hook in `backmatter/references.tex` marks corrected and replacement entries. The active database contains verified records; unchanged records requiring author review are preserved separately in `backmatter/references_author_review.bib` and are not loaded. See the package-level reference audit and author questions. Nonprinting author-question comments identify unresolved passages.

See `../README_REVISION.md` for scope and `../AUTHOR_QUESTIONS.md` for pending decisions.
