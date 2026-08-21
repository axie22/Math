# Start here

**Right now: [Session 6 — 2026-08-24](weeks/2026-08-24/08-24.md).** One hour. Two new
ideas today, not one — using a negation as a proof obligation (proving a sequence
diverges) and quantifier order. One repair section first: negating compound predicates,
the only thing from last week still broken.

Grading for Friday: [`08-21-feedback.md`](weeks/2026-08-17/08-21-feedback.md).

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 5 done.

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Week 1 result:** two of the three named bugs are closed.

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (Friday's √3, from memory, with the landing sentence) |
| **#3** — quantifier negation backwards | 🟡 half. Atomic negations clean; **compound predicates 0 for 5** |
| **#2** — induction never uses the hypothesis | ⬜ untested since the calibration — comes up later this week |

Also retired: unfolding definitions, contrapositive vs. contradiction, divisibility
transitivity, injective/surjective, pigeonhole. None of it returns as repair.

## The hour

| | |
|---|---|
| 0–10 min | Review + repair. **Capped at one item each** as of this week. |
| 10–45 min | New material — two ideas, not one. |
| 45–60 min | Stretch (optional), then note where you got stuck. |

Reading isn't the session. The lesson file is a handbook to consult, not a chapter to
read front to back.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

Those two boxes were blank all of week 1, and that is the direct cause of the
redundancy: a question skipped for time is indistinguishable from a question you
couldn't do, so Session 2's injective/surjective got re-issued Tuesday and mined for
follow-ups Wednesday, Thursday and Friday. Two words — "ran out of time" — would have
closed it in one pass.

Solutions post the next day, never the same day. Sitting stuck is the mechanism.

## Where everything lives

| File | What it's for |
|---|---|
| [`CURRICULUM.md`](CURRICULUM.md) | The 6-phase plan and its exit gates. Changes at weekly/monthly review |
| [`STATE.md`](STATE.md) | Where you are, what you've proven you know, next 10 sessions |
| [`REVIEW-QUEUE.md`](REVIEW-QUEUE.md) | Spaced repetition — what resurfaces when |
| [`RUN-PROMPT.md`](RUN-PROMPT.md) | The prompt the daily scheduled task runs |
| [`lessons/`](lessons/README.md) | Reference. Only `proof-foundations.md` is current |
| `weeks/<monday>/` | `MM-DD.md` problems · `-work.md` yours · `-solution.md` next day · `-feedback.md` grading |
| [`diagnostics/`](diagnostics/2026-08-18-calibration-feedback.md) | Calibration and phase-gate assessments |

## Still outstanding

- **Taylor series** — blank twice, so it stops being a test question and becomes taught
  material Wednesday. Phase 3 (concentration) and Phase 4 (smoothness) both need it.
- **Decide the honest session rate.** Week 1 ran 4 of 5, which is fine. If it settles
  nearer 3/week the ~34-week plan should be re-priced at ~55 rather than slipping
  quietly.
