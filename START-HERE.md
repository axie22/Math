# Start here

**Right now: [Session 6 retry — 2026-08-25](weeks/2026-08-24/08-25.md).** One hour.
Monday's session (08-24) came back entirely blank, so today repeats its content —
compound-predicate negation repair, then two new ideas: using a negation as a proof
obligation (proving a sequence diverges), and quantifier order — with all-new problem
instances rather than moving on to induction.

Grading for Friday: [`08-21-feedback.md`](weeks/2026-08-17/08-21-feedback.md).
Nothing to grade for Monday — the work file was blank.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 5 done (Session 6 in progress — 08-24
attempt had no evidence, retried 08-25).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Week 1 result:** two of the three named bugs are closed. Both remaining open items
below were retested on Friday: bug #1 (proof landing) closed clean, and pigeonhole's
general principle also closed clean, with the best synthesis proof in the repo so far.

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (Friday's √3, from memory, with the landing sentence) |
| **#3** — quantifier negation backwards | 🟡 half, **still half** — atomic negations clean; **compound predicates now 0 for 7** across three sessions (08-20, 08-21), Monday's third attempt untested (blank) |
| **#2** — induction never uses the hypothesis | ⬜ untested since the calibration — now scheduled for Thursday (08-27), slid one day by Monday's blank session |

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and, as of Friday, the general principle). None of it returns as repair.
Contrapositive *applied* to one's own proof is a separate, still-open item — half
right on its second attempt Friday.

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
  material Wednesday (now 08-26). Phase 3 (concentration) and Phase 4 (smoothness) both
  need it.
- **Decide the honest session rate.** Week 1 ran 5 of 5. Week 2 opened with a fully
  blank session (Monday 08-24) — the first since the restructure. Worth a direct look
  at the 08-28 review: was it circumstantial, or a real signal that the rate is
  softer than it looked.
- **The review queue is backing up.** One blank session (08-24) left four items
  overdue at once (atomic negation, bug #1's retention check, pigeonhole's retention
  check, plus the existing setup-discipline/witness-domain pair). The hard cap only
  clears one review item a day, so it'll take a few sessions to work through — not a
  crisis, but worth naming so it doesn't look like new backlog when it's really one
  missed day.
