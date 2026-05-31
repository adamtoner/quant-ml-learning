# Weeks 05-06: Regularisation And Overfitting

## Purpose

Learn why flexible models can fit noise, how validation exposes that problem, and how ridge/lasso regularisation changes coefficients and out-of-sample behaviour.

## Prerequisites

- Linear regression, MSE, residuals, and chronological splits.
- Basic train/test evaluation.
- Familiarity with scikit-learn estimators.

## Maths/statistics stream - 4h/week

- Study bias/variance tradeoff.
- Review train/test/validation split roles.
- Derive the intuition for L2 and L1 penalties.
- Understand why feature scaling matters for regularised models.
- Connect polynomial features to model flexibility.

## ML lab stream - 4h/week

- Generate synthetic nonlinear data.
- Fit polynomial regression with increasing degree and visualise overfitting.
- Compare OLS, ridge, and lasso.
- Add feature scaling through scikit-learn pipelines.
- Apply regularised models to noisy financial features.
- Run parameter sensitivity checks over regularisation strength.

## Coding tasks

- [ ] Create one notebook for overfitting and regularisation.
- [ ] Generate synthetic nonlinear data with noise.
- [ ] Fit polynomial models of multiple degrees.
- [ ] Plot train error vs validation/test error.
- [ ] Compare OLS, ridge, and lasso.
- [ ] Use feature scaling before ridge and lasso.
- [ ] Apply lagged ETF features to OLS, ridge, and lasso.
- [ ] Run a sensitivity table over regularisation parameters.
- [ ] Record which coefficients are shrunk or zeroed.

## Reading resources

- An Introduction to Statistical Learning: Use resampling methods and linear model selection/regularisation chapters.
- scikit-learn documentation: Use `Ridge`, `Lasso`, `PolynomialFeatures`, `StandardScaler`, and `Pipeline`.
- Mathematics for Machine Learning: Use optimisation and vector calculus sections as needed for penalty intuition.

## Deliverables

- Notebook: visual overfitting demo and regularised model comparison.
- Plot: train vs validation/test error by complexity.
- Plot: coefficient paths or coefficient comparison.
- Short note: why the best in-sample model is suspect.
- Experiment write-up using the template.

## Acceptance criteria

- The synthetic example visibly demonstrates overfitting.
- Ridge and lasso are compared against OLS on the same split.
- Feature scaling is used correctly for regularised models.
- Parameter sensitivity is shown rather than hidden.
- Financial feature results are interpreted conservatively.
- The note distinguishes model fit from forecast reliability.

## Reflection questions

- Where did the bias/variance tradeoff show up in the plots?
- Did regularisation improve out-of-sample results or just make coefficients smaller?
- Which features looked unstable?
- How much did conclusions depend on the chosen train/test period?

## Common traps

- Scaling the full dataset before splitting.
- Selecting the best parameter on the test set.
- Treating lasso-selected features as objectively important.
- Ignoring coefficient instability.
- Using too many financial features too early.

## Commit Checklist

- [ ] Notebook runs top-to-bottom.
- [ ] Experiment note completed.
- [ ] Dumb baseline included.
- [ ] Leakage checks written.
- [ ] Reusable repeated code moved or marked for `src/`.
- [ ] Results interpreted conservatively.
- [ ] Git commit created.

## Stretch tasks

- Implement ridge regression closed-form solution.
- Add repeated chronological validation windows.
- Compare rolling z-score features with raw lagged features.
