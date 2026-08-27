# Start here

**Right now: [Session 9 — 2026-08-28, Friday review](weeks/2026-08-24/08-28.md).** One
hour, no new material. Yesterday's session (08-27) came back completely blank — not
graded as wrong, just held, and it's noted, not nagged about. Today pulls five items
from the backlog that's been accumulating since 08-22: existential witness (fresh
instance), contrapositive-vs-contradiction *applied* (finally back in an open slot
after three sessions waiting), plain-English quantifier meaning (third try, fresh
predicate — a clean pass here retires it, another miss makes it a named repair item),
a third divergence-proof instance with the "state the three moves first" check folded
in, and a synthesis problem connecting pigeonhole to a formal $\exists$ statement.

**Taylor's theorem and the geometric series are not in today's session, and won't be
for a bit.** Two Core offerings in a row (08-26, 08-27) got zero attempts — not wrong,
never reached. Per the standing rule, two blanks means the problem is likely
time/engagement, not difficulty, so they're paused rather than offered a third time
back to back. See `STATE.md` and `CURRICULUM.md` §7 for the reasoning and an open
question worth your judgment: whether calculus repair needs a different placement in
the session, not just another attempt.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 8 offered, 6 with real evidence (two —
08-24 and 08-27 — came back entirely blank).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Where the three named bugs stand:**

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (08-21's √3, from memory, with the landing sentence) |
| **#3** — quantifier negation backwards | ✅ **closed** — atomic clean twice, compound predicates clean on all five items 08-25 (third pass, after failing 08-20 and 08-21) |
| **#2** — induction never uses the hypothesis | ⬜ untested since the calibration — scheduled for **Monday 08-31** |

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), setup discipline. None of it returns as
repair. Contrapositive *applied* to one's own proof is a separate, still-open item —
half right on its most recent attempt, waiting since 08-19 for an open slot; today's
the day.

**Two patterns confirmed, not just noted once:** being able to manipulate quantifiers
correctly isn't the same skill as explaining what they mean in plain English (wrong
once, blank twice — zero clean attempts across three tries now); and divergence
proofs specifically stall on terms like $(-1)^k$ — the instinct is to work out the
sign instead of noticing $|(-1)^k|=1$ regardless of it (wrong twice, identical
stopping point both times). Both get a fresh attempt today.

## The hour

Today's Friday shape (no new material, five retrieval items, ~10-12 min each) — see
the session file for the exact breakdown. Normal Mon–Thu shape is review → repair →
core → optional stretch; that resumes Monday with Induction I.

Reading isn't the session. Lesson files are handbooks to consult, not chapters to
read front to back — nothing new to read today.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

08-27 came back with literally nothing filled in, not even the timing box. If the
session isn't happening on a given day, that's completely fine — but if you do sit
down with it, even two words in the timing/stuck boxes turns a guess into a fact for
the next session.

Solutions post the next day, never the same day. Sitting stuck is the mechanism.

## Where everything lives

| File | What it's for |
|---|---|
| [`CURRICULUM.md`](CURRICULUM.md) | The 6-phase plan and its exit gates. Changes at weekly/monthly review |
| [`STATE.md`](STATE.md) | Where you are, what you've proven you know, next 10 sessions |
| [`REVIEW-QUEUE.md`](REVIEW-QUEUE.md) | Spaced repetition — what resurfaces when |
| [`RUN-PROMPT.md`](RUN-PROMPT.md) | The prompt the daily scheduled task runs |
| [`lessons/`](lessons/README.md) | Reference. `proof-foundations.md` and `calculus-repair.md` are current |
| `weeks/<monday>/` | `MM-DD.md` problems · `-work.md` yours · `-solution.md` next day · `-feedback.md` grading |
| [`diagnostics/`](diagnostics/2026-08-18-calibration-feedback.md) | Calibration and phase-gate assessments |

## Still outstanding

- **Chain rule, integration by parts** — blank on the calibration, never re-tested.
  Still waiting on calculus repair's Core to produce any evidence at all before this
  can even be scheduled.
- **Calculus repair itself.** Taylor's theorem has been offered four times total and
  never once been attempted. That's no longer read as pacing — see `CURRICULUM.md`
  §7's 08-27 amendment for the open question (placement in the session vs. something
  about the material itself) that's waiting on your judgment.
- **Throughput.** Two full weeks of data now say something closer to 3–4
  sessions/week than the planned 5 — flagged plainly in this week's `STATE.md`
  review rather than deferred again.
- **Bug #1's retirement check** (√ irrational, general form) is the oldest item in
  the review queue, overdue since 08-24. Didn't fit today; next in line.
