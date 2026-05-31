# Weeks 09-10: Time-Series Validation

## Purpose

Make validation design the centre of the research process. Learn why random train/test splits are wrong for time series and how chronological, rolling, expanding, and walk-forward validation change conclusions.

## Prerequisites

- Basic regression/classification workflows.
- Feature shifting and target construction.
- Understanding of leakage and overfitting.

## Maths/statistics stream - 4h/week

- Review stationarity intuition and model decay at a practical level.
- Study chronological splits, rolling windows, expanding windows, and walk-forward validation.
- Understand leakage from target shifting errors, overlapping labels, and full-sample preprocessing.
- Learn why overlapping labels can make observations less independent.
- Think through how validation answers a specific deployment question.

## ML lab stream - 4h/week

- Build a random split and chronological split on the same ETF-style dataset.
- Compare results and diagnose why they differ.
- Implement rolling-window and expanding-window evaluation.
- Implement a simple walk-forward validation loop.
- Check target shifting and feature timestamps explicitly.
- Record model decay across validation windows.

## Coding tasks

- [ ] Create one notebook for time-series validation.
- [ ] Build one ETF-style dataset with explicit feature and target timestamps.
- [ ] Evaluate a model with random split.
- [ ] Evaluate the same model with chronological split.
- [ ] Implement rolling-window validation.
- [ ] Implement expanding-window validation.
- [ ] Implement a simple walk-forward loop.
- [ ] Plot performance by validation window.
- [ ] Document leakage risks and target shifting rules.
- [ ] Check whether overlapping labels exist.

## Reading resources

- scikit-learn documentation: Use model evaluation material, but adapt it carefully for time series.
- pandas documentation: Use `shift`, rolling windows, date indexes, and resampling.
- Advances in Financial Machine Learning: Use the sections on financial labels and cross-validation selectively, focusing on leakage and overlapping-label concepts.

## Deliverables

- Notebook: random vs chronological vs walk-forward comparison.
- Plot: metric by validation window.
- Short note: why random split was invalid or misleading.
- Reusable pseudocode or function outline for walk-forward validation.
- Experiment write-up using the template.

## Acceptance criteria

- The same dataset and model are evaluated under random and chronological splits.
- The notebook shows how conclusions change under proper validation.
- Rolling and expanding windows are both implemented or clearly sketched.
- Feature and target timestamp alignment is documented.
- Leakage checks are written explicitly.
- The final note states which validation method should be used for the week 11-12 mini-project.

## Reflection questions

- How much did random split performance differ from chronological performance?
- Which validation design best matches monthly ETF allocation?
- Did the model decay over time?
- Which leakage risks are still unresolved?

## Common traps

- Using random cross-validation because it is convenient.
- Scaling or imputing before splitting by time.
- Forgetting that rolling features must be computed from past data only.
- Ignoring overlapping labels in multi-month targets.
- Selecting models based on the final test period.

## Commit Checklist

- [ ] Notebook runs top-to-bottom.
- [ ] Experiment note completed.
- [ ] Dumb baseline included.
- [ ] Leakage checks written.
- [ ] Reusable repeated code moved or marked for `src/`.
- [ ] Results interpreted conservatively.
- [ ] Git commit created.

## Stretch tasks

- Add an embargo gap between train and test periods for overlapping labels.
- Compare 1-month and 3-month targets.
- Track performance by market regime or broad-market drawdown period.
