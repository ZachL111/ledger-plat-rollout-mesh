# Review Journal

The review surface for `ledger-plat-rollout-mesh` is deliberately narrow: one fixture, one scoring rule, and one local check.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its platform engineering focus without claiming live deployment or external usage.

## Cases

- `baseline`: `rollout width`, score 141, lane `ship`
- `stress`: `quota pressure`, score 245, lane `ship`
- `edge`: `route drift`, score 145, lane `ship`
- `recovery`: `secret scope`, score 208, lane `ship`
- `stale`: `rollout width`, score 127, lane `watch`

## Note

This file is intentionally plain so the fixture remains the source of truth.
