# FDS02Q040 - Statistical Modelling

Personal study repository for the **Statistical Modelling** course
(Master's Degree in Data Science, University of Milano-Bicocca, A.Y. 2025-2026,
Prof. Fulvia Pennoni). Everything is done in **R** with **RStudio** and
**R Markdown**.

## Course topics

- Random variables, multivariate Gaussian distribution, non-parametric bootstrap
- Multiple linear regression: OLS, MLE, inference, diagnostics, prediction
- Model selection and strategies for model building (AIC, BIC)
- Categorical explanatory variables and extensions of the linear model
- Logistic regression for binary data (ROC, AUC, Brier score)
- Model-based clustering: finite Gaussian mixtures and the EM algorithm

## Repository layout

| Folder | Content | Tracked by git |
|--------|---------|----------------|
| `Slides/` | Lecture slides, teaching notes, applications | yes |
| `Exercises/` | Homework text, solutions and datasets | no (local only) |
| `Exam/` | Past exams, mock exams, exam rules | no (local only) |
| `Rmarkdown/` | R Markdown reference guides | yes |

Exam material, homework, solutions and datasets are excluded through
`.gitignore`. To work on a new machine, copy them locally from
the course e-learning page.

## Setup

1. Install the latest R from CRAN and RStudio.
2. Install the packages used in the course:

```r
install.packages(c(
  "knitr", "rmarkdown", "tinytex",
  "skimr", "ggplot2", "dplyr", "GGally", "corrplot", "gridExtra",
  "faraway", "car", "carData", "HH", "scatterplot3d",
  "mvtnorm", "ggm", "e1071", "boot", "bootstrap",
  "mclust", "LMest", "ROCit"
))
```

PDF output requires a LaTeX distribution; `tinytex::install_tinytex()` is
enough.

No Python environment is needed: this repository contains no Python code.

## Working conventions

- Keep each `.Rmd` next to the `.RData` file it loads (extracted locally from the
  exercises archive).
- Compile to PDF frequently to catch syntax errors early.
