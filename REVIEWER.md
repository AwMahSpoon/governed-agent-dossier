# Independent Reviewer Protocol

**Version:** 1.0
**Effective:** November 6, 2026
**Authority:** Reviewer scores only. Reviewer does not modify, extend, or unpin any sealed entry.

## Purpose

This protocol exists so that an outside party can verify the honesty of this system's forecasts without relying on the system's own claims about itself.

## What You Will Receive

- The sealed forecast ledger (append-only, timestamps visible)
- The frozen scoring formula
- The coin-flip baseline
- The alpha desk ledger (GATE vs BUY_EVERY_OPEN vs WAIT_EVERY_OPEN, after-cost)
- The OMNIS-Omega evaluation kit hash and commit reference

## Your Job

1. **Score only sealed entries whose deadlines have passed.** Do not score open entries. Do not estimate.
2. **Apply the frozen formula without modification:** 1 if directionally right within the stated confidence band, 0 otherwise. No partial credit. No rounding up.
3. **Compare against the coin-flip baseline** for the same set of scored entries. Report the comparison.
4. **Flag any entry whose criteria appear to have changed after sealing.** Check timestamps. If the text changed, the entry is void for scoring purposes.
5. **Do not accept explanations as substitutes for outcomes.** A rationale for why a forecast missed is not a point.
6. **Blank is not a pass.** An entry with no recorded outcome is unscored, not correct.
7. **A producer may not self-verify.** If you are the author of any forecast in this ledger, you are disqualified from scoring it.

## What You Must Not Do

- Do not rewrite, restate, or "improve" any sealed entry.
- Do not add new entries.
- Do not change the scoring formula.
- Do not recommend unpinning, overriding, or bypassing any governance pin.
- Do not infer intent from outcomes.

## Output Format

Return a plain table: entry ID, forecast text, deadline, recorded outcome, score (0 or 1), baseline score, and any flags. Nothing else.

## Integrity Note

This protocol is itself versioned. If you are asked to review under a different version, decline and cite this one.