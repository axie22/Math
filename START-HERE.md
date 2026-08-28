# Start here

**Right now: [Session 10 — 2026-08-31, Induction I](weeks/2026-08-31/08-31.md).** New
material — the first real test of bug #2 (induction with no engine), open since the
2026-08-17 calibration. Friday's session (08-28) came back completely blank, the
**second blank session in a row** (08-27, then 08-28) — not graded as wrong, held,
noted, not nagged about, but worth knowing it's now happened back-to-back rather than
with a recovery day in between. Today: two review items (Bug #1's retirement check,
$\sqrt5$ irrational, a week overdue — and a quick atomic-negation retest), one repair
item (plain-English quantifier meaning, now a named dedicated slot after three
non-clean tries), and two Core induction proofs — a sum formula and a divisibility
claim, deliberately different shapes so "use the hypothesis" doesn't just mean "the
sum trick."

**Taylor's theorem, the geometric series, and now existential witnesses are all
paused.** All three have two consecutive blank exposures in their tested slot — not
wrong, never reached. Per the standing rule that pauses rather than re-offers a third
time back to back. See `STATE.md` and `CURRICULUM.md` §7 — there's a new amendment
there worth your judgment: three of the last six offered sessions have now come back
entirely blank, and it's started shaping which skills get real evidence at all.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 9 offered, 6 with real evidence (three
— 08-24, 08-27, 08-28 — came back entirely blank).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Where the three named bugs stand:**

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (08-21's √3, from memory, with the landing sentence) |
| **#3** — quantifier negation backwards | ✅ **closed** — atomic clean twice, compound predicates clean on all five items 08-25 (third pass, after failing 08-20 and 08-21) |
| **#2** — induction never uses the hypothesis | 🟡 **first real test today, Monday 08-31** |

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), setup discipline. None of it returns as
repair. Contrapositive *applied* to one's own proof is a separate, still-open item —
half right on its most recent attempt, offered again 08-28 but the session was
blank; still waiting for a clean pass.

**Plain-English quantifier meaning has moved from "pattern" to "named repair
item."** Wrong once (08-25), blank twice (08-26, 08-28) — three exposures, zero
clean attempts. Today's Repair slot is its fourth try, fresh predicate. Divergence
proofs still stall on terms like $(-1)^k$ (wrong once, identical stopping point,
then two blank sessions where its third instance never got reached) — still
waiting on an open repair slot, not today's.

## The hour

Today's normal Mon–Thu shape: review (2 items) → repair (1 item) → Core (2 new
Induction I problems) → optional stretch. See the session file for the exact
breakdown. `lessons/proof-foundations.md` §6 is worth a look before Core if the
mechanism isn't already clear — first time that section's actually been needed.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

08-27 *and* 08-28 both came back with literally nothing filled in, not even the
timing box — two in a row now. If the session isn't happening on a given day,
that's completely fine — but if you do sit down with it, even two words in the
timing/stuck boxes turns a guess into a fact for the next session.

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

- **Three of the last six offered sessions came back entirely blank** (08-24,
  08-27, 08-28), the last two consecutively — new amendment in `CURRICULUM.md` §7
  naming this directly, since it's now pausing skills (Taylor, geometric series,
  existential witnesses) purely because their retest kept landing inside a blank
  session, not because they were attempted and found hard.
- **Chain rule, integration by parts** — blank on the calibration, never re-tested.
  Still waiting on calculus repair's Core to produce any evidence at all before this
  can even be scheduled.
- **Calculus repair itself.** Taylor's theorem has been offered four times total and
  never once been attempted. See `CURRICULUM.md` §7's 08-27 amendment for the open
  question (placement in the session vs. something about the material itself) that's
  waiting on your judgment.
- **Throughput.** Two full weeks of data now say something closer to 3–4
  sessions/week than the planned 5 — flagged plainly in `STATE.md`'s weekly review
  rather than deferred again.
- **Bug #1's retirement check** (√ irrational, general form) was the oldest item in
  the review queue, overdue since 08-24 — it's today's R1, finally delivered a
  week late.
