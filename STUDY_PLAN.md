# Study plan - Statistical Modelling

12 study weeks, about 8 hours per week (3 h theory, 4 h homework in R, 1 h review).
First written exam: **16 February 2027**. Start: 2 November 2026.
Starting point: basic probability, good knowledge of R, algebra to be refreshed.

## Sources

| Tag | File | Role |
|-----|------|------|
| TN | `Slides/Teaching_notes_SM_Pennoni_2026.pdf` | Reference text for theory and statistics |
| APP | `Slides/Applications_SM_26_Pennoni.pdf` | Reference text for R (code and case studies) |
| W | `Slides/Basic_Introduction_Matrix_Algebra_Weisberg_200e6.pdf` | Matrix algebra needed for the course |
| SL | `Slides/Slides_SM_26_Pennoni.pdf` | Course summary, used as a map at the start of each block |

Page numbers below come from each file's table of contents.

## Calendar

| Period | Content |
|--------|---------|
| 2 Nov - 27 Dec | Weeks 1-8 |
| 28 Dec - 3 Jan | Break |
| 4 Jan - 9 Jan | Week 9 |
| 10 Jan - 24 Jan | Break (two weeks) |
| 25 Jan - 14 Feb | Weeks 10-12 (clustering, mock exams, real exam of May 2026 and final review) |
| 16 Feb | Written exam |

## Weekly routine

1. Read the theory (TN), skim SL for the big picture.
2. Redo the examples in R (APP).
3. Solve the homework alone, then compare with the solutions.
4. Answer the open theory question of the homework in writing.

Status legend: `[ ]` not started, `[~]` in progress, `[x]` done.

## Block 0 - Foundations

### [ ] Week 1 (2 Nov) - RStudio setup and matrix algebra
- APP p.5-29: R basics, programming, functions, graphics, libraries, R Markdown (chunks, `echo`, `eval`).
- W: A.6.1-A.6.7 (operations, transpose, inverse, orthogonality, rank), A.7 (random vectors), A.8 (least squares with matrices).
- R practice: `%*%`, `t()`, `solve()`, `crossprod()`, `eigen()`.
- Check: compile a test `.Rmd` to PDF; set R and RStudio to English.

Sessions (4 x about 2 h):

| Session | Day | Content |
|---------|-----|---------|
| [ ] 1 | Tue 3 Nov | Setup and R Markdown: R and RStudio in English, compile a test `.Rmd` to PDF (tinytex), skim APP p.5-29 and redo only the non-trivial examples. |
| [ ] 2 | Thu 5 Nov | Matrix algebra, part 1: W A.6.1-A.6.7 (operations, transpose, inverse, orthogonality, rank); a few hand calculations on 2x2 and 3x3 matrices. |
| [ ] 3 | Sat 7 Nov | Matrix algebra, part 2: W A.7 (random vectors) and A.8 (least squares with matrices). |
| [ ] 4 | Sun 8 Nov | R practice and review: redo sessions 2-3 in R (`%*%`, `t()`, `solve()`, `crossprod()`, `eigen()`), check key results by hand, write a short `.Rmd` summary (last 30 min = review). |

### [ ] Week 2 (9 Nov) - Probability refresher
- TN 1.2 (p.11) and 2.1-2.8 (p.16-32): basic definitions, Gaussian, Student-t, ECDF, QQ plot, expected value and variance, joint and conditional distributions, association, partial correlation.
- APP p.30-55: credit rating case study, exploratory analysis, generating random values, measures of association.
- Homework: week 1, exercises 1-3 (software installation and first steps).

## Block 1 - The course

### [ ] Week 3 (16 Nov) - Multivariate Gaussian, estimation, bootstrap
- TN 2.9 (p.33-38) and 3 (p.39-54): bivariate and multivariate Gaussian, SVD, estimators, likelihood and MLE, bootstrap, percentile intervals.
- APP p.56-84: bivariate Normal, variance-covariance matrix, likelihood example, nonparametric bootstrap, percentile method.
- Homework: week 1, exercises 4-10 and open questions.
- Note: write the bootstrap with a `for` loop, as the exam requires (not `boot()`).

### [ ] Week 4 (23 Nov) - Multiple linear regression
- TN 4.1-4.5 (p.55-66): model, matrix notation, least squares, residuals, ANOVA, R-squared.
- APP p.85-90: output of `lm`, goodness of fit.
- Exercise: compute the OLS estimate by hand as `solve(t(X) %*% X) %*% t(X) %*% y` and compare with `lm`.
- Homework: week 3 (exercises 11-13).

### [ ] Week 5 (30 Nov) - Inference for the linear model
- TN 5 (p.71-84): properties of the estimators, F-test, t-tests, confidence intervals, multicollinearity (VIF).
- APP p.105-110: full vs null model, t-test, confidence intervals.
- Homework: week 4 (exercises 14-16).

### [ ] Week 6 (7 Dec) - Variable selection, prediction, model building
- TN 6-8 (p.85-95): data-driven selection, prediction, bootstrap for prediction, strategies for model building, AIC and BIC.
- APP p.111-124: body fat example, prediction of the mean response.
- Homework: weeks 5-6, first part (exercises 17-19).

### [ ] Week 7 (14 Dec) - Diagnostics
- TN 4.6 (p.67-70): unusual and influential observations.
- APP p.91-104: fitted values, residuals, leverage, Cook's distance, removing one record.
- Homework: weeks 5-6, second part (exercises 20-22).

### [ ] Week 8 (21 Dec) - Categorical variables and extensions
- TN 9-10 (p.95-97).
- APP p.125-141: summary and plots by categorical variable, models with factors.
- Homework: week 7, first part (exercises 23-26).

### [ ] Week 9 (4 Jan) - Logistic regression
- TN 11-12 (p.98-106): Bernoulli, Binomial, logistic model, inference.
- APP p.142-162: `glm`, fitted values, model selection, adding explanatory variables; ROC, AUC, Brier score.
- Homework: week 7, remaining exercises (27-31).

### [ ] Week 10 (25 Jan) - Model-based clustering
- TN 13 (p.107-): finite mixtures, Gaussian mixtures, parsimonious covariance, EM.
- APP p.163-: `Mclust`, classification, model selection, bootstrap standard errors.
- Homework: week 8 (exercises 32-33).

## Block 2 - Exam preparation

### [ ] Week 11 (1 Feb) - Mock exams
- Facsimile 1, 2bis and 4: each in 1h30 with the provided `.Rmd`, compiled to PDF.
- Compare with the solutions and note every mistake.

### [ ] Week 12 (8 Feb) - Real exam, final review
- May 2026 exam under exam conditions, then check against the solutions.
- Read `Main_Mistakes_15_May_2026.pdf` and fix recurring errors.
- Use the remaining days for weak topics and written theory answers (AIC vs BIC, bootstrap, logistic regression, EM).

## Open points

- No slack: the two breaks leave exactly 12 study weeks. Any delay must be recovered inside the breaks (e.g. 28 Dec - 3 Jan) or by trimming week 12.
- Verify the exam registration deadline on Segreterie Online well in advance (late registration is not accepted).
- The mapping between homework weeks and chapters is inferred from the tables of contents and may shift by a few exercises.
