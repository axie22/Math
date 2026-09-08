# Start here

**Right now: [Session 17 — 2026-09-09, Wednesday](weeks/2026-09-07/09-09.md).**
Session 16 (09-08) came back **entirely blank too** — the **fifth consecutive**
entirely-blank session (after 09-02, 09-03, 09-04, 09-07), now spanning two full
calendar weeks and crossing both a weekend and a week-boundary with no change in
outcome either time. Nothing from this run is graded as wrong — it's held, not
advanced. This is flagged as directly and plainly as this file can manage in
`CURRICULUM.md` §7 (2026-09-08 entry) and `STATE.md` — genuinely worth reading
before today's session, not after.

Today: one review item (plain-English-quantifier-meaning retention check, with
a worked scaffold ahead of the fresh instance — the same move that produced this
skill's first-ever clean instance on 09-01). No repair item — every repair-track
item is now paused (six of them, after contrapositive-applied joined the list
yesterday). Core carries the same two sup/inf problems forward unchanged for a
third session running (2b: an infimum proof; 2c: sup's $\varepsilon$-part
applied generally) — not because the material is being avoided, but because
across three sessions in a row these two specific problems have never actually
been opened, so there is nothing yet to gain from writing a different pair.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 16 offered, 8 with real evidence
(eight — 08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07, 09-08 — came back
entirely blank; the two strongest of the phase, 08-31 and 09-01, were
immediately followed by five blank sessions across the two weeks since).

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
evidence across five exposures and four framings), divergence-proof execution
(paused, one wrong attempt plus six blanks), bug #2's retention check (paused),
contrapositive-applied's retention check (paused as of today), and the paused
calculus-repair block.

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), setup discipline, **contrapositive applied
to one's own proof** (first clean instance 09-01), and **plain-English quantifier
meaning** (first clean instance 09-01, after one wrong plus four blanks — broken
by a worked-scaffold approach rather than a sixth cold re-ask). Both of those last
two hit their first retention check on 09-04 and came back blank;
contrapositive-applied's re-offer (09-08) was also blank and is now paused, while
plain-English quantifiers' re-offer (today, 09-09) reuses the scaffold that
worked the first time.

## The hour

Normal Mon–Thu shape: review (~10 min, spaced-retrieval items due today) → repair
(~nothing right now — see above) → Core (~35–40 min, today's topic) → optional
stretch (~10–15 min). Fridays are different — no new material, a wider
mixed-retrieval set instead, plus one synthesis problem tying two different-era
topics together. See the day's session file for the exact breakdown.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

Eight sessions now (08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07, 09-08) have
come back with nothing written in at all, five of them in a row across the last
two weeks. If today only gets partway, even a half-filled box beats a blank
one — "ran out of time" and "no idea what to do after the setup" send tomorrow's
session in completely different directions, and a totally blank file gives the
next run nothing to work with except "hold." `CURRICULUM.md` §7's 2026-09-08
entry is written directly for you, not just as a log — worth five minutes even
if today's problems have to wait.

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

- **The blank-session pattern is now the steady state, not an anomaly.** Five
  consecutive entirely-blank sessions (09-02, 09-03, 09-04, 09-07, 09-08) span
  two full calendar weeks, crossing a weekend and a week-boundary with zero
  change either time. `CURRICULUM.md` §7's 2026-09-08 entry says directly that
  this run no longer expects writing another version of this flag to change the
  outcome, and that the decision — continue, pause, or change the delivery
  mechanism — needs to come from you rather than from another blank file
  tomorrow.
- **Calculus repair itself, paused.** Taylor's theorem and the geometric series have
  four and two blank exposures respectively, no date assigned — see `CURRICULUM.md`
  §7's 2026-08-27 amendment, still waiting on your judgment.
- **Chain rule, integration by parts** — blank on the calibration, never re-tested.
  Still waiting on calculus repair's Core to produce any evidence at all before this
  can even be scheduled.
- **Throughput.** Trailing five sessions: 0 of 5 with real evidence. Four full
  weeks since restructure: 100%, 40%, 40%, and the current week opening 0 of 2.
  The 5-sessions/week pricing in `CURRICULUM.md` §6 no longer looks like the
  sustained rate — see the throughput table in `STATE.md`.
- **Backlog of overdue retention checks** — setup discipline, pigeonhole general
  principle, compound-predicate negation, quantifier order, induction-counting —
  all still due, none retested since 08-28; the hard cap means these queue up
  faster than they clear.
- **Phase 0 exit gate — content complete, evidence isn't.** All five gate topics
  have now been taught at least once (sup/inf, taught 09-02, was the last), but
  sup/inf has zero real attempts across five exposures and both strong induction
  and existential witnesses are paused — the gate itself isn't imminent until
  those produce real evidence.
