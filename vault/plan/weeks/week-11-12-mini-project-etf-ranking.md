# Weeks 11-12: Mini-Project - ETF Above-Median Classification

## Purpose

Complete a small, disciplined ETF modelling project. The goal is learning, not trading advice. The core task is to classify next-month above-median ETF return for a small ETF universe, then compare a momentum baseline, logistic regression, and one ensemble model.

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
- Use a core universe of 8-12 ETFs.
- Build one core target: whether an ETF outperforms the universe median next month.
- Build timestamp-safe features: 1m, 3m, 6m, and 12m return; volatility; drawdown; moving-average distance; correlation to broad market.
- Fit logistic regression and one ensemble model: random forest or gradient boosting.
- Compare against a simple momentum baseline and class-majority baseline.
- Validate with walk-forward or chronological validation.

Core models:

- Momentum baseline.
- Logistic regression.
- Random forest or gradient boosting, not both.

## Coding tasks

- [ ] Create one mini-project notebook.
- [ ] Define a core universe of 8-12 ETFs and a date range.
- [ ] Build monthly returns and rebalance timestamps.
- [ ] Create 1m, 3m, 6m, and 12m return features.
- [ ] Create volatility, drawdown, moving-average distance, and broad-market correlation features.
- [ ] Create one target: next-month above-median ETF return.
- [ ] Check target shifting and feature availability.
- [ ] Implement a momentum baseline.
- [ ] Fit logistic regression.
- [ ] Fit one ensemble model: random forest or gradient boosting.
- [ ] Compare against momentum and class-majority baselines.
- [ ] Use chronological or walk-forward validation.
- [ ] Produce plots and a comparison table.
- [ ] Write a failure-mode analysis.

## Reading resources

- An Introduction to Statistical Learning: Revisit classification, regularisation, and tree-based methods as needed.
- scikit-learn documentation: Use metrics, pipelines, logistic regression, random forest, and gradient boosting.
- pandas documentation: Use rolling windows, grouped feature construction, `shift`, and date indexing.
- Advances in Financial Machine Learning: Use leakage, label, and validation warnings selectively; do not attempt advanced machinery unless the basic project is complete.

## Deliverables

- Notebook: ETF next-month above-median classification mini-project.
- Short research note with hypothesis, target, data, features, validation, metrics, results, and failure modes.
- Plots: feature diagnostics, validation-window performance, and confusion matrix or ranking performance.
- Comparison table: baselines vs models.
- Failure-mode analysis.

## Acceptance criteria

- The project states clearly that it is for learning and is not trading advice.
- The core universe contains 8-12 ETFs.
- The only core target is next-month above-median ETF return.
- Every feature is timestamp-safe.
- Momentum and class-majority baselines are included.
- Logistic regression and one ensemble model are compared on the same validation design.
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
- Ignoring the momentum and class-majority baselines.
- Using overlapping labels without thinking about validation.
- Confusing classification accuracy with portfolio usefulness.
- Failing to write down negative results.

## Commit Checklist

- [ ] Notebook runs top-to-bottom.
- [ ] Experiment note completed.
- [ ] Dumb baseline included.
- [ ] Leakage checks written.
- [ ] Reusable repeated code moved or marked for `src/`.
- [ ] Results interpreted conservatively.
- [ ] Git commit created.

## Stretch tasks

- Add the second ensemble model not used in the core comparison.
- Add a 3-month target.
- Add a simple top-N allocation simulation.
- Add transaction cost and turnover estimates.
- Add permutation importance.
- Add coefficient stability analysis.
