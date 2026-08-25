# Start here

**Right now: [Session 7 — 2026-08-26](weeks/2026-08-24/08-26.md).** One hour. First
genuinely new material since Session 5: Taylor's theorem with remainder and the
geometric series (both moved from "tested" to "taught" after coming back blank
twice). Plus one review item (setup discipline), one re-offered problem (a
divergence-proof construction that came back blank yesterday), and one repair item
(explaining quantifier statements in plain English, not just manipulating them).

Grading for yesterday: [`08-25-feedback.md`](weeks/2026-08-24/08-25-feedback.md).
**Good news:** compound-predicate negation — the thing that failed 08-20 and
08-21 — closed clean on all five items. It's retired.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 6 done (Session 6's two attempts
both now complete and graded).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Where the three named bugs stand:**

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (08-21's √3, from memory, with the landing sentence) |
| **#3** — quantifier negation backwards | ✅ **closed** — atomic clean twice, compound predicates clean on all five items 08-25 (third pass, after failing 08-20 and 08-21) |
| **#2** — induction never uses the hypothesis | ⬜ untested since the calibration — scheduled for Thursday (08-27) |

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle). None of it returns as repair. Contrapositive
*applied* to one's own proof is a separate, still-open item — half right on its most
recent attempt, waiting for the next open repair slot.

**New, still being watched:** two brand-new topics (negation as a proof obligation;
quantifier order) split the same way most new topics have — the mechanical/setup
half landed clean, the execution half didn't. One new finding worth naming: being
able to manipulate quantifiers correctly isn't the same skill as explaining what
they mean in plain English, and the second one came back as a symbol
transliteration rather than substance. One data point so far.

## The hour

| | |
|---|---|
| 0–10 min | Review + repair. **Capped at one item each.** |
| 10–45 min | New material — two ideas, not one. |
| 45–60 min | Stretch (optional), then note where you got stuck. |

Reading isn't the session. Lesson files are handbooks to consult, not chapters to
read front to back — including the new one,
[`lessons/calculus-repair.md`](lessons/calculus-repair.md).

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

Those two boxes have been blank for two sessions running now (08-24 entirely, 08-25
partially). A question skipped for time is indistinguishable from a question you
couldn't do without them — "ran out of time" or "no idea what to do after the
setup" are two words that would save the next session from guessing.

Solutions post the next day, never the same day. Sitting stuck is the mechanism.

## Where everything lives

| File | What it's for |
|---|---|
| [`CURRICULUM.md`](CURRICULUM.md) | The 6-phase plan and its exit gates. Changes at weekly/monthly review |
| [`STATE.md`](STATE.md) | Where you are, what you've proven you know, next 10 sessions |
| [`REVIEW-QUEUE.md`](REVIEW-QUEUE.md) | Spaced repetition — what resurfaces when |
| [`RUN-PROMPT.md`](RUN-PROMPT.md) | The prompt the daily scheduled task runs |
| [`lessons/`](lessons/README.md) | Reference. `proof-foundations.md` and the new `calculus-repair.md` are current |
| `weeks/<monday>/` | `MM-DD.md` problems · `-work.md` yours · `-solution.md` next day · `-feedback.md` grading |
| [`diagnostics/`](diagnostics/2026-08-18-calibration-feedback.md) | Calibration and phase-gate assessments |

## Still outstanding

- **Chain rule, integration by parts** — blank on the calibration, never re-tested
  (08-21's redo only covered Taylor). Taylor itself starts getting taught today;
  chain rule and integration by parts still need a session of their own before
  calculus repair is considered closed.
- **Decide the honest session rate.** Week 2 opened with one blank session (08-24)
  then a strong recovery (08-25). Worth a direct look at the 08-28 review with two
  full weeks of post-restructure data.
- **The review queue is still working through last week's backlog.** One blank
  session left five items overdue at once; the hard cap clears one a day, so it's
  taking a few sessions — not a crisis, just worth naming so it doesn't read as new
  backlog when it's really one missed day working itself out.
