# Weeks 11-12: Mini-Project - ETF Ranking Or Regime Classification

## Purpose

Complete a small, disciplined ETF modelling project. The goal is learning, not trading advice. The output should show that you can define a target, build timestamp-safe features, compare baselines and models, validate chronologically, and write a failure-mode analysis.

## Prerequisites

- Linear/logistic regression, regularisation, trees, ensembles, and time-series validation.
- Ability to create lagged monthly features.
- Familiarity with experiment notes and comparison tables.

## Maths/statistics stream - 4h/week

- Review ranking targets, binary labels, class balance, and noisy labels.
- Review volatility, drawdown, correlation, and Sharpe ratio.
- Think through why model metrics and allocation performance are not the same.
- Study parameter sensitivity and robustness checks.
- Define what result would be enough to continue research and what result would reject the idea.

## ML lab stream - 4h/week

- Define an ETF universe and monthly rebalance calendar.
- Build a target such as whether an ETF outperforms the universe median over the next 1-3 months.
- Build timestamp-safe features: 1m, 3m, 6m, and 12m return; volatility; drawdown; moving-average distance; correlation to broad market.
- Fit logistic regression, ridge/lasso where relevant, random forest, and gradient boosting.
- Compare against simple momentum ranking, equal weight, and always-risk-on or class-majority baseline.
- Validate with walk-forward or chronological validation.

## Coding tasks

- [ ] Create one mini-project notebook.
- [ ] Define ETF universe and date range.
- [ ] Build monthly returns and rebalance timestamps.
- [ ] Create 1m, 3m, 6m, and 12m return features.
- [ ] Create volatility, drawdown, moving-average distance, and broad-market correlation features.
- [ ] Create a next 1-3 month outperformance target.
- [ ] Check target shifting and feature availability.
- [ ] Fit logistic regression.
- [ ] Fit ridge or lasso where relevant.
- [ ] Fit random forest.
- [ ] Fit gradient boosting.
- [ ] Compare against simple momentum, equal-weight, and class-majority or always-risk-on baselines.
- [ ] Use chronological or walk-forward validation.
- [ ] Produce plots and a comparison table.
- [ ] Write a failure-mode analysis.

## Reading resources

- An Introduction to Statistical Learning: Revisit classification, regularisation, and tree-based methods as needed.
- scikit-learn documentation: Use metrics, pipelines, logistic regression, ridge/lasso, random forest, and gradient boosting.
- pandas documentation: Use rolling windows, grouped feature construction, `shift`, and date indexing.
- Advances in Financial Machine Learning: Use leakage, label, and validation warnings selectively; do not attempt advanced machinery unless the basic project is complete.

## Deliverables

- Notebook: ETF ranking or regime-classification mini-project.
- Short research note with hypothesis, target, data, features, validation, metrics, results, and failure modes.
- Plots: feature diagnostics, validation-window performance, confusion matrix or ranking performance, drawdown if allocation is simulated.
- Comparison table: baselines vs models.
- Failure-mode analysis.

## Acceptance criteria

- The project states clearly that it is for learning and is not trading advice.
- The target is defined before modelling.
- Every feature is timestamp-safe.
- At least three baselines are included: simple momentum ranking, equal-weight, and class-majority or always-risk-on.
- Logistic regression, random forest, and gradient boosting are compared on the same validation design.
- Walk-forward or chronological validation is used.
- Results include metrics, plots, and a written interpretation.
- The conclusion explains why the result is or is not worth extending.
- The failure-mode analysis covers leakage, overfitting, data quality, regime dependence, and portfolio assumptions.

## Reflection questions

- Did any model beat the dumb baselines convincingly?
- Which mattered more: feature design, model choice, or validation method?
- Did performance concentrate in one period?
- What would need to be true before this became a serious research direction?
- What should be simplified before adding complexity?

## Common traps

- Treating the mini-project as a trading system.
- Optimising the target, feature set, and model until the backtest looks good.
- Ignoring equal-weight and momentum baselines.
- Using overlapping labels without thinking about validation.
- Confusing classification accuracy with portfolio usefulness.
- Failing to write down negative results.

## Stretch tasks

- Add a simple top-N allocation simulation.
- Add transaction cost and turnover estimates.
- Compare 1-month vs 3-month targets.
- Add permutation importance or coefficient stability analysis.
