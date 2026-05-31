# Curated Resources

Use these as primary references. Do not expand the list until the first 12 weeks are complete unless a specific gap appears.

## Maths For ML

### Mathematics for Machine Learning

- What it is for: Linear algebra, calculus, probability, and optimisation foundations for ML.
- When to use it: Weeks 1-6, then as a reference.
- Prioritise: Linear algebra chapters for vectors, matrices, projections, and least squares; vector calculus sections for gradients; probability sections before classification.

### The Matrix Cookbook

- What it is for: Quick reference for matrix identities and derivatives.
- When to use it: When deriving least squares, ridge regression, gradients, or covariance expressions.
- Prioritise: Matrix differentiation and quadratic forms.

## Classical ML

### An Introduction to Statistical Learning

- What it is for: The main reading-first ML text for linear models, classification, resampling, regularisation, trees, and ensembles.
- When to use it: Weeks 1-8.
- Prioritise: Linear regression, classification, resampling methods, linear model selection and regularisation, tree-based methods.

### scikit-learn User Guide

- What it is for: Practical model APIs, preprocessing, metrics, model selection, and diagnostics.
- When to use it: Every ML lab block after implementing the core idea.
- Prioritise: Linear models, preprocessing, metrics, model evaluation, decision trees, random forests, gradient boosting, pipelines.

### Dive into Deep Learning

- What it is for: Optional bridge from classical ML to neural network thinking.
- When to use it: Only after the first 12 weeks, or as a light reference for gradient descent and optimisation intuition.
- Prioritise: Linear regression, softmax/logistic classification concepts, optimisation basics.

## Statistics

### OpenIntro Statistics or equivalent undergraduate statistics reference

- What it is for: Probability distributions, estimation, confidence intervals, hypothesis testing, and regression diagnostics.
- When to use it: Weeks 1-6 and whenever interpreting noisy model results.
- Prioritise: Probability, sampling, regression inference, residuals, bias, variance.

### ISL resampling and model assessment chapters

- What it is for: Train/test splits, cross-validation, bias/variance, and model comparison.
- When to use it: Weeks 5-10.
- Prioritise: Resampling methods, validation-set approach, cross-validation, model flexibility.

## Financial ML / Backtesting

### Advances in Financial Machine Learning

- What it is for: Financial ML pitfalls: leakage, labels, sampling, validation, and overfitting.
- When to use it: After basic ML foundations; use selectively in weeks 9-12.
- Prioritise: Financial data structures, labelling, sample weights, cross-validation, backtest overfitting. Treat as advanced and do not copy techniques mechanically.

### Systematic Trading and backtesting references

- What it is for: Practical thinking about signals, portfolios, costs, turnover, and robust backtesting.
- When to use it: Months 4-6 when moving from model metrics to allocation research.
- Prioritise: Rebalance timing, transaction costs, position sizing, drawdown, and performance attribution.

## Python Tools

### NumPy documentation

- What it is for: Arrays, vectorisation, broadcasting, linear algebra, and scratch implementations.
- When to use it: Weeks 1-6.
- Prioritise: `ndarray`, broadcasting, `numpy.linalg`, random number generation.

### pandas documentation

- What it is for: Time-indexed tabular data, rolling features, joins, missing data, and resampling.
- When to use it: Weeks 1-12, especially ETF feature engineering.
- Prioritise: indexing, groupby, rolling windows, resample, shift, merge/asof-style alignment, missing values.

### scikit-learn documentation

- What it is for: Fit/predict API, preprocessing, metrics, pipelines, and model comparison.
- When to use it: Weeks 1-12.
- Prioritise: `LinearRegression`, `Ridge`, `Lasso`, `LogisticRegression`, `DecisionTreeClassifier`, `RandomForestClassifier`, `GradientBoostingClassifier`, metrics, train/test utilities, pipelines.
