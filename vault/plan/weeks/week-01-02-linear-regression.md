# Weeks 01-02: Linear Regression

## Purpose

Learn linear regression as geometry, optimisation, and a practical forecasting baseline. This block should make vectors, matrices, least squares, MSE, gradients, residuals, and chronological splits feel operational.

## Prerequisites

- Basic Python, NumPy arrays, pandas DataFrames.
- Comfort with functions, derivatives, and matrix notation.
- Basic understanding of returns and monthly price data.

## Maths/statistics stream - 4h/week

- Review vectors, matrices, transposes, dot products, norms, and matrix multiplication.
- Derive simple linear regression as least squares.
- Derive MSE and its gradient for linear regression.
- Understand residuals, fitted values, and why residual plots matter.
- Work through why chronological splits are required for ETF-style prediction.

## ML lab stream - 4h/week

- Implement linear regression from scratch in NumPy using the normal equation.
- Implement gradient descent for MSE on a small synthetic dataset.
- Compare both scratch versions with `sklearn.linear_model.LinearRegression`.
- Produce residual plots and predicted-vs-actual plots.
- Build a basic ETF-style regression exercise using lagged returns to predict next-month returns.
- Use a chronological split, not a random split.

## Coding tasks

- [ ] Create one notebook for scratch linear regression.
- [ ] Generate synthetic linear data with noise.
- [ ] Implement prediction as `X @ beta`.
- [ ] Implement MSE.
- [ ] Solve least squares with NumPy linear algebra.
- [ ] Implement gradient descent and plot loss over iterations.
- [ ] Compare coefficients and predictions with scikit-learn.
- [ ] Build an ETF-style monthly regression dataset with lagged features.
- [ ] Use a chronological train/test split.
- [ ] Plot residuals over time and residuals vs fitted values.

## Reading resources

- Mathematics for Machine Learning: Use the linear algebra sections on vectors, matrices, inner products, projections, and least squares.
- An Introduction to Statistical Learning: Use the linear regression chapter for interpretation, residuals, and model assessment.
- NumPy documentation: Use `ndarray`, broadcasting, and `numpy.linalg`.
- scikit-learn documentation: Use `LinearRegression` and regression metrics.

## Deliverables

- Notebook: scratch and scikit-learn linear regression comparison.
- Short note: what least squares is optimising.
- Plot: residuals vs fitted values.
- Plot: loss curve for gradient descent.
- Experiment write-up using `vault/plan/experiment-note-template.md`.

## Acceptance criteria

- You can explain dot product, matrix multiplication, MSE, gradient, and residual without hand-waving.
- Scratch normal-equation predictions match scikit-learn to numerical tolerance on the same data.
- Gradient descent reduces MSE on synthetic data.
- The ETF exercise uses only past features to predict a future target.
- The evaluation split is chronological.
- The note explicitly names at least three ways the ETF regression can fail.

## Reflection questions

- What does least squares minimise, geometrically and statistically?
- What does a residual plot show that a single metric hides?
- Did the ETF regression beat a mean-return baseline?
- What would have leaked if the split or features were built carelessly?

## Common traps

- Including the target month in the feature calculation.
- Treating high in-sample R2 as evidence of forecasting power.
- Forgetting an intercept term in the scratch implementation.
- Comparing models on different train/test splits.
- Reading residual plots as proof of tradability.

## Stretch tasks

- Add ridge regression manually after completing plain OLS.
- Standardise features and inspect how coefficients change.
- Compare daily-derived monthly features with pure monthly features.
