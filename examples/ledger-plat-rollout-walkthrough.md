# Ledger Plat Rollout Mesh Walkthrough

I use this file as a small checklist before changing the Java implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | rollout width | 141 | ship |
| stress | quota pressure | 245 | ship |
| edge | route drift | 145 | ship |
| recovery | secret scope | 208 | ship |
| stale | rollout width | 127 | watch |

Start with `stress` and `stale`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

The next useful expansion would be a malformed fixture around quota pressure and secret scope.
