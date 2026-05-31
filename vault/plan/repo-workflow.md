# Repository Workflow

This repository should separate exploration, reusable implementation, and research notes. Do not let notebooks become the only source of logic.

## Roles

- `notebooks/`: experiments, explanation, plots, and exploratory analysis.
- `src/`: reusable code that is shared across notebooks or experiments.
- `vault/` or `notes/`: experiment write-ups, research notes, decisions, and failure-mode analysis.
- `vault/plan/`: planning documents, templates, and weekly learning blocks.

## Notebook Rules

- A notebook may contain temporary exploration and explanatory code.
- A notebook should run top-to-bottom before a block is considered complete.
- Repeated logic should not stay duplicated across notebooks.
- If the same data cleaning, feature construction, validation, metric, or plotting logic appears more than once, extract it into `src/` or mark it explicitly for extraction.
- Notebook conclusions must link back to an experiment note or include enough detail to recreate the result.

## Source Code Rules

- Put reusable functions in `src/` once they are used by more than one experiment.
- Keep `src/` focused on stable utilities: data loading, feature construction, validation splits, metrics, plotting helpers, and model comparison helpers.
- Avoid moving unstable exploratory code into `src/` too early.
- Add tests when reusable code becomes important enough that a silent error would invalidate multiple experiments.

## Notes Rules

- Every completed experiment should have a written note using `vault/plan/experiment-note-template.md`.
- Notes should record hypothesis, data, target, features, validation method, baseline, results, failure modes, and next action.
- Negative results should be written down. They prevent repeated mistakes.

## Commit Rules

- Every completed 2-week block should produce a git commit.
- Commit only after the notebook runs top-to-bottom, the experiment note is complete, and leakage checks are written.
- A useful commit message should name the block and the main artifact, for example: `week 01-02 linear regression baseline`.
- Do not commit generated clutter, broken notebooks, or exploratory dead ends unless they are intentionally preserved as research evidence.
