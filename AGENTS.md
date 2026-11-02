# AGENTS.md

This file provides guidance to AI coding agents working in this repository.

## Context

Personal study repository for the Statistical Modelling course (MSc Data Science,
University of Milano-Bicocca). The language is **R** (RStudio, R Markdown). There is
no Python code and no virtual environment.

## Excluded Paths

The following hold exam material, homework, solutions and datasets. They are
git-ignored and must stay that way:

- `Exam/`, `Exercises/`
- any `*.Rdata`, `*.RData`, `*.rda`, `*.rds`, `*.zip` file

Rules:

- Never commit, stage, or paste the content of these files (exam texts,
  homework, solutions, datasets) into tracked files, commit messages, or PR descriptions.
- Reading them locally to help the user study is allowed; never modify or delete them.
- Before any commit, check `git status` to confirm none of these paths is staged.
- The repository is public: do not add personal data (student ID, surname-tagged
  exam submissions) to tracked files.

## Layout

- `Slides/` and `Rmarkdown/` are tracked; `Exam/` and `Exercises/` are local only.

## R Markdown Conventions

- Split code into multiple chunks, each followed by the results and a comment.
- Call `set.seed()` before any random procedure (bootstrap, simulation, EM start).
- When the task asks for an explicit algorithm (e.g. non-parametric bootstrap with
  `B` replications), write it by hand with a `for` loop; do not use `boot()` or
  `bootstrap()`.
- Paired data: resample rows of the data frame, never the columns independently.
- Use `nrow(df)` for the sample size of a data frame, not `length(df)`.
- Interpret results on the observed values (no conditional or vague wording) and
  tie them to the applied context. Do not claim normality or symmetry from
  mean/median closeness alone.
- AIC and BIC: lower is better only when comparing models fitted on the same data.
- Keep the `.Rmd` compilable to PDF at every step.

## Code Style

- Tidy, readable R; `snake_case` for object and function names.
- Comments in English; no emoji in code, comments, or output messages.
- Prefer base R where the course teaches it; add packages only if used in the course
  or listed in the README.

## Commits

Commit messages follow **Conventional Commits**: `type(scope): description`, for
example `docs(readme): update setup instructions`.
