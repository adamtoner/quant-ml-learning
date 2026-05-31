# Quant Learning Project

This repository is a local learning workspace for rebuilding quantitative research and machine learning skills with a controlled, research-first process. The first applied project is a monthly systematic ETF modelling and allocation study, using ETFs as the investable universe because they are simpler for compliance and data handling.

Live trading is secondary. The immediate goal is to become better at research design, statistical reasoning, validation, implementation, and written experiment review.

## Learning Goal

Build the skill base needed for serious quant research:

- Reactivate linear algebra, calculus, probability, statistics, and optimisation.
- Learn classical machine learning deeply enough to implement, debug, and critique models.
- Develop financial research habits before optimising strategies.
- Use simple baselines before complex models.
- Write short notes for every experiment so results are inspectable and repeatable.

The weekly time split is roughly:

- 4 hours/week maths and statistics.
- 4 hours/week machine learning and applied ML lab.

## Repository Structure

```text
.
├── README.md
├── data/                 # Local datasets, not planned in this pass
├── notebooks/            # Future notebooks and exploratory work
├── resources/            # Local source material, papers, or notes
├── src/                  # Future reusable code
└── vault/
    └── plan/
        ├── roadmap.md
        ├── principles.md
        ├── repo-workflow.md
        ├── resources.md
        ├── glossary.md
        ├── experiment-note-template.md
        └── weeks/
            ├── week-01-02-linear-regression.md
            ├── week-03-04-classification-logistic-regression.md
            ├── week-05-06-regularisation-overfitting.md
            ├── week-07-08-trees-ensembles.md
            ├── week-09-10-time-series-validation.md
            └── week-11-12-mini-project-etf-ranking.md
```

## How To Use The Plan

Start with `vault/plan/principles.md`, then read `vault/plan/roadmap.md` and `vault/plan/repo-workflow.md`. Work through the files in `vault/plan/weeks/` in order. Each 2-week block has strict acceptance criteria; do not move on until the deliverables are written and the common traps have been checked.

Use `vault/plan/experiment-note-template.md` for every notebook, model comparison, or backtest-like experiment. Keep notes short, factual, and specific.

Notebooks are for experiments, explanation, and plots. They should not become the only source of project logic. Repeated data cleaning, feature construction, validation, metric, or plotting code should be extracted into `src/` once it appears in more than one notebook.

## Weekly Workflow

Each week:

1. Spend about 4 hours on maths/statistics reading, derivation, and hand calculation.
2. Spend about 4 hours implementing and comparing models in Python.
3. Produce at least one durable artifact: a notebook, plot, short research note, reusable function, or experiment write-up.
4. Compare against a dumb baseline before interpreting model performance.
5. Record leakage risks, validation method, failure modes, and next action.

## Streams

The maths/statistics stream supplies the language for understanding models: vector spaces, loss functions, gradients, probability, inference, bias/variance, and validation.

The ML lab stream turns that theory into working code: scratch NumPy implementations where useful, scikit-learn comparisons, diagnostics, plots, and reproducible experiments.

The quant project is the applied testbed. It should not outrun the foundations. Monthly ETF modelling is useful because it forces chronological validation, target definition, feature hygiene, portfolio thinking, and comparison against simple allocation baselines.

## First 12-Week Milestone

By the end of week 12, this repository should contain:

- A set of notebooks covering linear regression, logistic regression, regularisation, tree models, and time-series validation.
- Scratch implementations where they teach the mechanics, especially linear regression and optionally logistic regression.
- Short notes for each experiment using the standard template.
- Plots for residuals, overfitting, validation comparison, feature importance, drawdown, and model performance.
- A mini-project that ranks ETFs or classifies regimes using chronological or walk-forward validation.
- A comparison table with dumb baselines, linear/logistic models, and tree/ensemble models.
- A written failure-mode analysis explaining why the first models should not be treated as trading-ready.
