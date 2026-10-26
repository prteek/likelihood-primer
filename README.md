# likelihood-primer

A short primer on likelihood: the binomial likelihood and log-likelihood, Fisher information and its link to the
uncertainty of an estimate, and maximising the likelihood with Newton–Raphson, with a worked example in R.

```
index.qmd          the primer (R, knitr)
_quarto.yml        PDF format; renders to _output/likelihood-primer.pdf
references.bib     references
_freeze/           frozen results of the R code (tracked)
renv.lock          R package versions (renv)
_wide-tables.lua   fits wide tables to the page in the PDF
likelihood.jpg     thumbnail
```

## Render

```bash
Rscript -e 'renv::restore()'                       # once: install the R packages in renv.lock
QUARTO_R=/opt/homebrew/bin/Rscript quarto render   # -> _output/likelihood-primer.pdf
```

Rendering reuses the frozen results in `_freeze/` until a code chunk changes.
