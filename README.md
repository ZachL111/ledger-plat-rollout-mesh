# ledger-plat-rollout-mesh

`ledger-plat-rollout-mesh` explores platform engineering with a small Java codebase and local fixtures. The technical goal is to package a Java local lab for rollout analysis with node-edge fixtures, cycle and reachability reports, and documented operating limits.

## Reason For The Project

The point is to make a small domain rule concrete enough that a reader can change it and immediately see what broke.

## Ledger Plat Rollout Mesh Review Notes

Start with `quota pressure` and `rollout width`. Those cases create the widest score spread in this repo, so they are the best quick check when the model changes.

## What It Does

- `fixtures/domain_review.csv` adds cases for rollout width and quota pressure.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/ledger-plat-rollout-walkthrough.md` walks through the case spread.
- The Java code includes a review path for `quota pressure` and `rollout width`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## How It Is Put Together

The fixture data drives the tests. The code stays thin, while `metadata/domain-review.json` and `config/review-profile.json` explain what each case is meant to protect.

The Java addition stays small enough to inspect in one sitting.

## Run It

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Check It

That command is also the regression path. It verifies the domain cases and catches mismatches between the CSV, metadata, and code.

## Boundaries

This remains a local project with deterministic fixtures. It does not depend on credentials, hosted services, or live data. Future work should add richer malformed inputs before widening the public API.
