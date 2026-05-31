# 12-Month Roadmap

This roadmap keeps the first 12 weeks concrete and months 4-12 at a higher level. The sequence is designed to delay financial ML complexity until the validation and statistics habits are in place.

## Months 1-3: Foundations And First ETF Mini-Project

Goal: Reactivate maths/statistics, learn classical ML mechanics, and complete a small ETF ranking or regime-classification study.

Detailed 2-week plans:

- [Weeks 01-02: Linear regression](weeks/week-01-02-linear-regression.md)
- [Weeks 03-04: Classification and logistic regression](weeks/week-03-04-classification-logistic-regression.md)
- [Weeks 05-06: Regularisation and overfitting](weeks/week-05-06-regularisation-overfitting.md)
- [Weeks 07-08: Trees and ensembles](weeks/week-07-08-trees-ensembles.md)
- [Weeks 09-10: Time-series validation](weeks/week-09-10-time-series-validation.md)
- [Weeks 11-12: Mini-project, ETF ranking or regime classification](weeks/week-11-12-mini-project-etf-ranking.md)

Milestones:

- Implement linear regression from scratch and compare with scikit-learn.
- Build classification metrics from first principles.
- Demonstrate overfitting and regularisation on synthetic and financial-style data.
- Compare linear/logistic models with tree-based models.
- Show why random splits are invalid for time-series forecasting.
- Complete a mini-project with a notebook, plots, comparison table, and failure-mode analysis.

Deliverables:

- 6-8 notebooks.
- 6 short experiment notes.
- A reusable experiment-note habit.
- A first ETF ranking or regime-classification research note.

## Months 4-5: Financial Data And Backtesting

Goal: Build clean monthly ETF data workflows and simple backtesting infrastructure.

Focus:

- ETF universe definition and survivorship caveats.
- Monthly adjusted-price data handling.
- Return calculation, feature shifting, missing data, and rebalance calendars.
- Equal-weight, market-proxy, and simple momentum baselines.
- Transaction cost and turnover assumptions.

Deliverables:

- Data quality note.
- Baseline allocation notebook.
- Basic monthly backtest function.
- Performance report with CAGR, volatility, Sharpe ratio, drawdown, turnover, and benchmark comparison.

## Month 6: Portfolio Construction

Goal: Convert forecasts or rankings into portfolio weights without pretending prediction accuracy is enough.

Focus:

- Equal weight, top-N ranking, volatility scaling, and simple risk constraints.
- Rebalance frequency and turnover.
- Capacity and liquidity as research considerations.
- Position limits and sector/asset-class concentration.

Deliverables:

- Portfolio construction notebook.
- Comparison of allocation rules using the same signals.
- Note on how portfolio rules changed results relative to raw model metrics.

## Month 7: Time-Series Validation And Robustness

Goal: Make validation the centre of the research process.

Focus:

- Rolling and expanding windows.
- Walk-forward model selection.
- Model decay and regime sensitivity.
- Parameter sensitivity.
- Robustness to universe changes and start dates.

Deliverables:

- Walk-forward evaluation framework.
- Robustness report.
- Clear rejection criteria for weak strategies.

## Months 8-9: Financial ML

Goal: Apply financial ML ideas selectively after the basic process is reliable.

Focus:

- Label design for returns and rankings.
- Class imbalance and noisy labels.
- Feature importance stability.
- Purged or embargoed validation concepts where overlapping labels make them necessary.
- Avoiding backtest overfitting.

Deliverables:

- Financial ML pitfalls note.
- ETF model comparison using disciplined validation.
- Failure analysis of at least one model that looked good under weaker validation.

## Month 10: Research Process Hardening

Goal: Make experiments reproducible and easier to review.

Focus:

- Standard experiment configs.
- Dataset version notes.
- Model comparison tables.
- Plot conventions.
- Reusable feature and validation utilities.

Deliverables:

- Reusable project structure for experiments.
- Research report template.
- One reproduced experiment from raw data to final note.

## Months 11-12: Extension Topics

Goal: Broaden carefully after the ETF process is credible.

Possible directions:

- Macro features for ETF allocation.
- Regime classification.
- Bayesian thinking and uncertainty.
- Dimensionality reduction.
- Causal inference basics.
- Deep learning only if a specific data shape justifies it.
- Research-only studies of restricted instruments, with compliance constraints explicit.

Deliverables:

- One extension note.
- One controlled experiment adding a new feature family or modelling approach.
- Year-end review: what was learned, what failed, and what research process should be kept.
