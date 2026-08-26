# Start here

**Right now: [Session 8 — 2026-08-27](weeks/2026-08-24/08-27.md).** One hour. Core is
*held over* from Session 7, not new: Taylor's theorem and the geometric series never
got attempted yesterday (real work happened, but time ran out at the repair block),
so today re-offers both with fresh instances rather than moving on to Induction. Plus
one review item (existential witnesses, overdue since 08-22), a second re-offer of the
plain-English quantifier-meaning question, and one repair item (a divergence-proof
construction — the same specific obstacle has now shown up twice).

Grading for yesterday: [`08-26-feedback.md`](weeks/2026-08-24/08-26-feedback.md).
**Good news:** setup discipline is retired — second clean cold instance, 7 days
apart. **Also real:** the divergence-proof stall is now a named, recurring thing
(evaluating a sign where an absolute value would do), not a one-off.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 7 done (Session 7 graded — partial;
Core carries into Session 8).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Where the three named bugs stand:**

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (08-21's √3, from memory, with the landing sentence) |
| **#3** — quantifier negation backwards | ✅ **closed** — atomic clean twice, compound predicates clean on all five items 08-25 (third pass, after failing 08-20 and 08-21) |
| **#2** — induction never uses the hypothesis | ⬜ untested since the calibration — now scheduled for **Monday 08-31** (slipped one session — calculus repair's Core hadn't been attempted yet) |

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), **setup discipline** (new, 08-26). None of it
returns as repair. Contrapositive *applied* to one's own proof is a separate, still-
open item — half right on its most recent attempt, waiting three sessions now for
the next open repair slot.

**New, still being watched — two patterns confirmed, not just noted once:**
being able to manipulate quantifiers correctly isn't the same skill as explaining
what they mean in plain English (wrong once, blank once — zero clean attempts
across two tries); and divergence proofs specifically stall on terms like
$(-1)^k$ — the instinct is to work out the sign instead of noticing $|(-1)^k|=1$
regardless of it (wrong twice, identical stopping point both times). Both get
another pass in Session 8.

## The hour

| | |
|---|---|
| 0–10 min | Review — 2 items today. |
| 10–18 min | Repair. **Capped at one item.** |
| 18–48 min | Core — the held-over Taylor/geometric-series material, new instances. |
| 48–60 min | Stretch (optional), then note where you got stuck. |

Reading isn't the session. Lesson files are handbooks to consult, not chapters to
read front to back — [`lessons/calculus-repair.md`](lessons/calculus-repair.md) is
already posted from Session 7; nothing new to read today.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

Those two boxes have been blank for three sessions running now (08-24 entirely,
08-25 partially, 08-26 again down to one free-text line). The one line you did add
on 08-26 — "did not have time today" — was genuinely useful; more of that, even two
words per box, is what turns a guess into a fact for the next session.

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
  Taylor is now being taught (Sessions 7–8); chain rule and integration by parts
  still need a session of their own before calculus repair is considered closed.
- **Session sizing.** Two sessions in a row (08-25 partially, 08-26 mostly) haven't
  finished — worth a direct look at the 08-28 review: is an hour actually enough
  for what's being planned, not just whether days get missed. Session 8 trims one
  sub-part as a first, small correction.
- **The review queue backlog is still working itself out.** One blank session
  (08-24) left five items overdue at once; the hard cap clears 1–2 a day. Setup
  discipline cleared 08-26. Friday (08-28) is the natural place to clear more.
