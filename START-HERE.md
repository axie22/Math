# Start here

**Right now: [Session 14 — 2026-09-04, Friday review: backlog + synthesis](weeks/2026-08-31/09-04.md).**
Yesterday (09-03) came back **entirely blank too** — the fifth time this has
happened in the repo (after 08-24, 08-27, 08-28, 09-02), and the **second time
two have landed back-to-back**, both immediately after the two strongest
sessions here (08-31, 09-01). Nothing from this week's blanks is graded as
wrong — it's held, not advanced. This is now a strong enough pattern that it's
flagged directly for you in `CURRICULUM.md` §7 and `STATE.md`'s weekly review —
worth a real look at whether something about timing or delivery is in the way,
independent of the material itself.

Today is Friday — no new material. One repair item moved to the *front* of the
session for the first time (divergence-proof execution, testing whether its
usual last-in-session position is why it's been offered five times and
attempted once), three retention checks on Phase 0's newest closures (bug #2,
contrapositive-applied, plain-English quantifiers — all due today), and one
synthesis problem proving the supremum is unique (combining proof by
contradiction with sup's $\varepsilon$-definition). **Existential witnesses is
now paused too** (two consecutive blanks in its resumed cycle) — joining strong
induction and Taylor's theorem/the geometric series, all off active rotation for
the same reason.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 13 offered, 8 with real evidence
(five — 08-24, 08-27, 08-28, 09-02, 09-03 — came back entirely blank; the two
strongest of the phase, 08-31 and 09-01, were immediately followed by two blank
sessions in a row, not just one).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Where the three named bugs stand:**

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (08-21's √3; reconfirmed cleanly 08-31) |
| **#3** — quantifier negation backwards | ✅ **closed** — atomic clean three times (most recently 08-31), compound predicates clean on all five items 08-25 |
| **#2** — induction never uses the hypothesis | ✅ **closed** — clean on two Core problems 08-31, clean again on a fresh instance 09-01 (two clean demonstrations, 1-day spacing). Retention check due today (09-04), never yet retested |

All three named bugs from the calibration now have real, repeated evidence of
repair. What's open now: strong induction and existential witnesses (both
paused, two blank exposures each), sup/inf (zero real evidence across two
exposures on either computational angle), divergence-proof execution (four
blank exposures since one wrong attempt on 08-26), and the paused
calculus-repair block.

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), setup discipline, **contrapositive applied
to one's own proof** (first clean instance 09-01, after three prior non-clean
attempts), and **plain-English quantifier meaning** (first clean instance 09-01,
after one wrong plus four blanks — the longest-open item in the repo, broken by a
worked-scaffold approach rather than a sixth cold re-ask). Both of those last two
get their first retention check today (09-04). None of it returns as repair.

## The hour

Fridays are different from the normal Mon–Thu shape (review → repair → Core →
stretch): no new material, a wider mixed-retrieval set instead, plus one
synthesis problem tying two different-era topics together. See the session file
for today's exact breakdown.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

Five sessions now (08-24, 08-27, 08-28, 09-02, 09-03) have come back with nothing
written in at all, and the last two happened back-to-back, right after the two
strongest sessions in the repo's history. If today only gets partway, even a
half-filled box beats a blank one — "ran out of time" and "no idea what to do
after the setup" send tomorrow's session in completely different directions, and
a totally blank file gives the next run nothing to work with except "hold."
Worth reading `CURRICULUM.md` §7's newest entry (2026-09-03) directly — it's
written for you, not just as a log.

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

- **Calculus repair itself, paused.** Taylor's theorem and the geometric series have
  four and two blank exposures respectively, no date assigned — see `CURRICULUM.md`
  §7's 2026-08-27 amendment, still waiting on your judgment.
- **Chain rule, integration by parts** — blank on the calibration, never re-tested.
  Still waiting on calculus repair's Core to produce any evidence at all before this
  can even be scheduled.
- **Throughput — worth a direct look now, not just a note.** This week
  (08-31–09-04) lands at 2 of 5 sessions with real evidence regardless of what
  today produces, tying the worst week on record. Four weeks in: 100%, 40%,
  ~40-50% twice. The 5-sessions/week pricing in `CURRICULUM.md` §6 no longer
  looks like the sustained rate — see the 09-04 weekly review in `STATE.md`.
- **Backlog of overdue retention checks** — setup discipline, pigeonhole general
  principle, compound-predicate negation, quantifier order, induction-counting —
  all still due, none retested since 08-28; the hard cap means these queue up
  faster than they clear. Not urgent (all are past clean instances), but the
  queue is now backing up more than at any prior check.
- **Phase 0 exit gate — content complete, evidence isn't.** All five gate topics
  have now been taught at least once (sup/inf, taught 09-02, was the last), but
  sup/inf has zero real attempts on either angle and both strong induction and
  existential witnesses are paused — the gate itself isn't imminent until those
  produce real evidence.
- **The two-strong-then-two-blank pattern has now happened twice, identically.**
  08-27/08-28 followed 08-25/08-26; 09-02/09-03 followed 08-31/09-01. Both times,
  the repo's strongest sessions were immediately followed by a pair of entirely
  blank ones. `CURRICULUM.md` §7's 2026-09-03 entry names this plainly and asks
  directly whether something about timing, reminders, or how the day's session
  reaches you is behind it — worth reading and acting on rather than waiting for
  a sixth instance.
