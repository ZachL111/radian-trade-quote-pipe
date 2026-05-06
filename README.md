# radian-trade-quote-pipe

`radian-trade-quote-pipe` is a Zig project in trading systems. Its focus is to design a Zig verification harness for quote systems, covering format conversion, round-trip fixtures, and failure-oriented tests.

## Problem It Tries To Make Smaller

This is intentionally local and self-contained so it can be inspected without credentials, services, or seeded history.

## Radian Trade Quote Pipe Review Notes

The first comparison I would make is `spread pressure` against `fill risk` because it shows where the rule is most opinionated.

## Working Pieces

- `fixtures/domain_review.csv` adds cases for spread pressure and fill risk.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/radian-trade-quote-walkthrough.md` walks through the case spread.
- The Zig code includes a review path for `spread pressure` and `fill risk`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Design Notes

The fixture data drives the tests. The code stays thin, while `metadata/domain-review.json` and `config/review-profile.json` explain what each case is meant to protect.

The added Zig path is deliberately direct, with fixtures doing most of the explaining.

## Example Run

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Tests

The verifier is intentionally local. It should fail if the fixture score math, lane assignment, or language-specific test drifts.

## Known Limits

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
