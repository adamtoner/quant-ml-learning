# Learning And Research Principles

## Core Rules

- Start with simple baselines before complex models.
- Put statistics before clever ML.
- Never use lookahead information.
- Use chronological validation for time series.
- Write experiment notes for every model, feature set, and validation change.
- Assume overfitting until evidence says otherwise.
- Compare every result against dumb baselines.
- Treat live trading as secondary to learning.
- Do not optimise a strategy until the research process is sound.
- Use ETFs first because they are compliance-simpler, diversified, liquid enough for learning, and easier to model with monthly data.

## Research Discipline

- Define the hypothesis before touching the model.
- Define the target before building features.
- Freeze validation rules before interpreting results.
- Keep feature construction reproducible and timestamp-aware.
- Separate exploratory analysis from evaluation.
- Prefer robust, boring results over impressive single-run metrics.
- Track negative results; they are part of the research record.

## Model Discipline

- Fit a naive baseline first: mean prediction, class majority, equal weight, or simple momentum.
- Use linear models before tree ensembles unless the problem structure clearly demands nonlinearity.
- Add model complexity only when diagnostics justify it.
- Treat feature importance as a diagnostic, not as proof of causality.
- Use parameter sensitivity checks before trusting conclusions.

## Financial Research Discipline

- Monthly ETF modelling is the first serious project.
- Single stocks, options, crypto, commodities, and similar instruments are research-only until compliance clearance exists.
- Backtests are research tools, not evidence of tradability by themselves.
- Include transaction costs, turnover, missing data, survivorship, and rebalance timing before treating results seriously.
- Prefer process quality over strategy optimisation in the first 12 weeks.
