# Start here

**Right now: [Session 18 — 2026-09-10, Thursday](weeks/2026-09-07/09-10.md).**
Session 17 (09-09) came back **entirely blank too** — the **sixth consecutive**
entirely-blank session (after 09-02, 09-03, 09-04, 09-07, 09-08), now spanning
three full calendar weeks with only two productive sessions (08-31, 09-01) in
that whole span. Nothing from this run is graded as wrong — it's held, not
advanced. **A direct notification was also sent outside this repo today** —
`CURRICULUM.md` §7 (2026-09-09 entry) and `STATE.md` explain why, and it's
worth reading either of them before today's session if you haven't already
seen the notification.

Today: one review item (pigeonhole general-principle retirement check, a fresh
hash-table-collision application — pulled from the old backlog since every
newer retention check is now paused). No repair item — every repair-track item
is now paused, seven of them, after plain-English-quantifier meaning joined the
list yesterday. Core is **one** problem today, not two — a fresh sup instance
($\sup\{2-\frac1n\}=2$) rather than the 2b/2c pair carried forward for the last
three sessions, which had gone three sessions unopened without ever being
touched. This is a deliberate, reversible experiment in how much is being
asked, not a permanent change.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 17 offered, 8 with real evidence
(nine — 08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07, 09-08, 09-09 — came
back entirely blank; the two strongest of the phase, 08-31 and 09-01, were
immediately followed by six blank sessions across the three weeks since).

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
evidence across six exposures and four framings), divergence-proof execution
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

Nine sessions now (08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07, 09-08,
09-09) have come back with nothing written in at all, six of them in a row
across the last three weeks. If today only gets partway, even a half-filled box
beats a blank one — "ran out of time" and "no idea what to do after the setup"
send tomorrow's session in completely different directions, and a totally blank
file gives the next run nothing to work with except "hold." `CURRICULUM.md`
§7's 2026-09-09 entry is written directly for you, not just as a log — worth
five minutes even if today's problems have to wait.

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

- **The blank-session pattern is now the steady state, not an anomaly.** Six
  consecutive entirely-blank sessions (09-02, 09-03, 09-04, 09-07, 09-08,
  09-09) span three full calendar weeks. `CURRICULUM.md` §7's 2026-09-09 entry
  says this run has stopped writing escalating paragraphs about it and instead
  sent you a direct notification outside the repo — the decision (continue,
  pause, or change the delivery mechanism) still needs to come from you, not
  from another blank file tomorrow.
- **Calculus repair itself, paused.** Taylor's theorem and the geometric series have
  four and two blank exposures respectively, no date assigned — see `CURRICULUM.md`
  §7's 2026-08-27 amendment, still waiting on your judgment.
- **Chain rule, integration by parts** — blank on the calibration, never re-tested.
  Still waiting on calculus repair's Core to produce any evidence at all before this
  can even be scheduled.
- **Throughput.** Trailing six sessions: 0 of 6 with real evidence. Four full
  weeks since restructure: 100%, 40%, 40%, and the current week opening 0 of 3.
  The 5-sessions/week pricing in `CURRICULUM.md` §6 no longer looks like the
  sustained rate — see the throughput table in `STATE.md`.
- **Backlog of overdue retention checks** — setup discipline, pigeonhole general
  principle, compound-predicate negation, quantifier order, induction-counting —
  all still due, none retested since 08-28; the hard cap means these queue up
  faster than they clear.
- **Phase 0 exit gate — content complete, evidence isn't.** All five gate topics
  have now been taught at least once (sup/inf, taught 09-02, was the last), but
  sup/inf has zero real attempts across six exposures and both strong induction
  and existential witnesses are paused — the gate itself isn't imminent until
  those produce real evidence.
