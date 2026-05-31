# Weeks 03-04: Classification And Logistic Regression

## Purpose

Learn classification as probability modelling and decision-making under noisy labels. Use logistic regression to classify whether next-month ETF return is positive or above the universe median, then compare against dumb baselines.

## Prerequisites

- Week 01-02 linear regression concepts.
- Basic probability notation.
- Comfort with NumPy vectorisation and scikit-learn fit/predict APIs.

## Maths/statistics stream - 4h/week

- Review probability, conditional probability, odds, and log-odds.
- Study the sigmoid/logistic function and its shape.
- Understand binary cross-entropy as a loss for probability predictions.
- Work through confusion matrix, accuracy, precision, recall, false positives, and false negatives.
- Learn ROC/AUC basics and when AUC can mislead.

## ML lab stream - 4h/week

- Fit logistic regression with scikit-learn on synthetic data.
- Implement sigmoid and binary cross-entropy manually.
- If feasible, implement logistic regression gradient descent conceptually or from scratch.
- Build monthly ETF labels: next-month return positive, or next-month return above universe median.
- Compare logistic regression against class-majority, always-positive, and simple momentum baselines.
- Evaluate using chronological splits.

## Coding tasks

- [ ] Create one notebook for classification and logistic regression.
- [ ] Implement sigmoid.
- [ ] Implement binary cross-entropy.
- [ ] Compute a confusion matrix manually for a small example.
- [ ] Fit scikit-learn logistic regression on synthetic data.
- [ ] Build ETF positive-return or above-median labels using shifted future returns.
- [ ] Compare accuracy, precision, recall, and ROC/AUC.
- [ ] Compare against class-majority and simple momentum baselines.
- [ ] Record class balance by train and test period.

## Reading resources

- An Introduction to Statistical Learning: Use the classification and logistic regression chapter.
- Mathematics for Machine Learning: Use probability sections needed for odds, conditional probability, and likelihood intuition.
- scikit-learn documentation: Use `LogisticRegression`, classification metrics, confusion matrix, ROC/AUC.
- pandas documentation: Use `shift`, grouping, and date indexing for label construction.

## Deliverables

- Notebook: logistic regression and classification metrics.
- Short note: target definition and class balance.
- Plot: ROC curve or threshold metric comparison.
- Table: logistic regression vs dumb baselines.
- Experiment write-up using the template.

## Acceptance criteria

- Labels are created with future returns shifted correctly.
- No feature uses information from the target period.
- You can explain odds, log-odds, sigmoid, and binary cross-entropy.
- The notebook reports class balance and confusion matrices.
- Logistic regression is compared to at least two dumb baselines.
- The conclusion does not rely on accuracy alone.

## Reflection questions

- Which error is worse in this task: false positives or false negatives?
- Did threshold choice matter more than model choice?
- Was the above-median target more useful than positive/negative return?
- Did the model beat the class-majority baseline out of sample?

## Common traps

- Optimising for accuracy when classes are imbalanced.
- Forgetting that predicted probabilities need a decision threshold.
- Using random splits on time-series data.
- Treating AUC as sufficient evidence of usefulness.
- Creating labels before checking timestamp alignment.

## Commit Checklist

- [ ] Notebook runs top-to-bottom.
- [ ] Experiment note completed.
- [ ] Dumb baseline included.
- [ ] Leakage checks written.
- [ ] Reusable repeated code moved or marked for `src/`.
- [ ] Results interpreted conservatively.
- [ ] Git commit created.

## Stretch tasks

- Implement logistic regression gradient descent from scratch.
- Plot precision and recall as the threshold changes.
- Compare positive-return and above-median labels side by side.
