# Start here

**Right now: [Session 19 — 2026-09-11, Friday review](weeks/2026-09-07/09-11.md).**
Session 18 (09-10) came back **entirely blank too** — the **seventh
consecutive** entirely-blank session, and the first time **every session
offered this week** (09-07 through 09-10) came back blank. Nothing from this
run is graded as wrong — it's held, not advanced. A short new
`CURRICULUM.md` §7 entry (2026-09-10) records the fully-blank week as new
information; it does not repeat the case for a cadence decision that's
already been made five times since 08-28, including a direct notification
sent outside the repo on 09-09.

Today (Friday, no new material by schedule either way): four backlog items
pulled at once — setup discipline, compound-predicate negation, quantifier
order, induction-counting — none of them paused, all 9–14 days overdue. No
repair item — every repair-track item remains paused, seven of them. One
synthesis problem tries a fourth lever on sup/inf: leading with the already-
retired §5 negation skill into the §9 sup definition, rather than a seventh
cold computation.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 18 offered, 8 with real evidence
(ten — 08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07, 09-08, 09-09, 09-10 —
came back entirely blank; the two strongest of the phase, 08-31 and 09-01,
were immediately followed by seven blank sessions, including a fully blank
calendar week).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Where the three named bugs stand:**

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (08-21's √3; reconfirmed cleanly 08-31) |
| **#3** — quantifier negation backwards | ✅ **closed** — atomic clean three times (most recently 08-31), compound predicates clean on all five items 08-25 |
| **#2** — induction never uses the hypothesis | ✅ **closed** — clean on two Core problems 08-31, clean again on a fresh instance 09-01. Retention check blank twice (09-04, 09-07) — now **paused**, logged as untested |

All three named bugs from the calibration still have real, repeated evidence of
repair — none of that is in question. What's open now: strong induction and
existential witnesses (both paused, two blank exposures each), sup/inf (zero real
evidence across seven exposures and five framings), divergence-proof execution
(paused, one wrong attempt plus six blanks), and every retention check that has
ever been offered on a Phase 0 closure (bug #2, contrapositive-applied,
plain-English quantifiers — all three paused), plus the paused calculus-repair
block.

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), setup discipline, **contrapositive applied
to one's own proof** (first clean instance 09-01), and **plain-English quantifier
meaning** (first clean instance 09-01, after one wrong plus four blanks — broken
by a worked-scaffold approach rather than a sixth cold re-ask). All three of the
newest closures (bug #2, contrapositive-applied, plain-English quantifiers) had
their first retention check come back blank on 09-04, and every one of the
re-offers since has also come back blank — all three retention checks are now
paused.

## The hour

Normal Mon–Thu shape: review (~10 min, spaced-retrieval items due today) → repair
(~nothing right now — see above) → Core (~35–40 min, today's topic) → optional
stretch (~10–15 min). Fridays are different — no new material, a wider
mixed-retrieval set instead, plus one synthesis problem tying two different-era
topics together. See the day's session file for the exact breakdown.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

Ten sessions now (08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07, 09-08, 09-09,
09-10) have come back with nothing written in at all, seven of them in a row,
and this last week is the first where all four sessions offered came back
blank. If today only gets partway, even a half-filled box beats a blank one —
"ran out of time" and "no idea what to do after the setup" send tomorrow's
session in completely different directions, and a totally blank file gives the
next run nothing to work with except "hold."

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

- **The blank-session pattern has now claimed an entire calendar week.** Seven
  consecutive entirely-blank sessions (09-02 through 09-10) include, for the
  first time, a week (09-07's) where all four offered sessions came back
  blank. `CURRICULUM.md` §7's 2026-09-10 entry records this plainly rather
  than re-arguing a case already made five times since 08-28 — the decision
  (continue, pause, or change the delivery mechanism) is still Alex's, not
  something another blank file can resolve.
- **Calculus repair itself, paused.** Taylor's theorem and the geometric series have
  four and two blank exposures respectively, no date assigned — see `CURRICULUM.md`
  §7's 2026-08-27 amendment, still waiting on your judgment.
- **Chain rule, integration by parts** — blank on the calibration, never re-tested.
  Still waiting on calculus repair's Core to produce any evidence at all before this
  can even be scheduled.
- **Throughput.** Trailing seven sessions: 0 of 7 with real evidence. Five full/partial
  weeks since restructure: 100%, 40%, 40%, 0% (this last week). The 5-sessions/week
  pricing in `CURRICULUM.md` §6 no longer looks like the sustained rate — see the
  throughput table in `STATE.md`.
- **Backlog of overdue retention checks** — setup discipline, pigeonhole general
  principle, compound-predicate negation, quantifier order, induction-counting —
  four of these filled Session 19's review block in one shot; pigeonhole carries
  forward, still not cleanly retested since 08-21.
- **Phase 0 exit gate — content complete, evidence isn't.** All five gate topics
  have now been taught at least once (sup/inf, taught 09-02, was the last), but
  sup/inf has zero real attempts across seven exposures and both strong induction
  and existential witnesses are paused — the gate itself isn't imminent until
  those produce real evidence.
