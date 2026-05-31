# Weeks 07-08: Trees And Ensembles

## Purpose

Learn decision trees, random forests, and gradient boosting as flexible nonlinear models, while treating their financial use with scepticism. The goal is model comparison and diagnostic skill, not model worship.

## Prerequisites

- Classification and regression metrics.
- Regularisation and overfitting concepts.
- Basic scikit-learn pipelines and chronological splits.

## Maths/statistics stream - 4h/week

- Understand recursive partitioning.
- Study impurity measures at a high level: Gini, entropy, and variance reduction.
- Learn bagging and why random forests reduce variance.
- Learn boosting intuition: sequentially correcting errors.
- Review why high flexibility is dangerous on noisy financial labels.

## ML lab stream - 4h/week

- Fit decision trees on synthetic data and visualise overfitting with depth.
- Fit random forests and gradient boosting with scikit-learn.
- Compare linear/logistic models against tree models on the same ETF-style task.
- Inspect feature importance and test its stability across periods.
- Keep XGBoost/LightGBM out of the core workflow; list them only as stretch.

## Coding tasks

- [ ] Create one notebook for tree and ensemble comparisons.
- [ ] Fit shallow and deep decision trees on synthetic data.
- [ ] Plot performance as tree depth changes.
- [ ] Fit random forest and gradient boosting models with scikit-learn.
- [ ] Compare against linear or logistic regression on the same ETF target.
- [ ] Plot feature importance.
- [ ] Refit on different chronological windows and compare feature importance stability.
- [ ] Record where tree models overfit relative to simpler models.

## Reading resources

- An Introduction to Statistical Learning: Use the tree-based methods chapter.
- scikit-learn documentation: Use decision trees, random forests, gradient boosting, and feature importance examples.
- ISL model assessment material: Revisit validation and overfitting sections before interpreting tree results.

## Deliverables

- Notebook: tree and ensemble model comparison.
- Plot: depth or complexity vs out-of-sample performance.
- Plot/table: feature importance across at least two windows.
- Short note: why tree models can overfit financial data.
- Experiment write-up using the template.

## Acceptance criteria

- Decision tree depth sensitivity is demonstrated.
- Random forest and gradient boosting are compared to a simple linear/logistic model.
- All ETF comparisons use the same target, features, and chronological split.
- Feature importance stability is checked.
- The conclusion includes at least three reasons tree performance may not generalise.

## Reflection questions

- Did nonlinear models improve out-of-sample performance after baselines?
- Were feature importances stable across time?
- Did tree depth or ensemble complexity matter more than expected?
- What evidence would be needed before trusting a tree model in a financial setting?

## Common traps

- Treating feature importance as causal explanation.
- Letting tree depth grow until in-sample metrics look good.
- Comparing models on different feature sets without saying so.
- Adding XGBoost/LightGBM before understanding scikit-learn models.
- Ignoring period-specific model instability.

## Stretch tasks

- Try XGBoost or LightGBM only after the scikit-learn comparisons are complete.
- Add permutation importance.
- Compare classification and regression formulations of the same ETF problem.
