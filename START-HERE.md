# Start here

**Right now: [Session 13 — 2026-09-03, Sup/inf's first real attempt](weeks/2026-08-31/09-03.md).**
Yesterday (09-02) came back **entirely blank** — no timing, no attempts on
anything, including the review block. That's the third time this has happened in
the repo (after 08-24, 08-27, 08-28), and it followed directly after the two
strongest sessions here (08-31, 09-01). Nothing from yesterday is graded as
wrong — it's held, not advanced.

Today: sup/inf (introduced 09-02 via a new lesson section) still has zero real
attempt evidence, so today gives it its actual first try — one infimum instance
(new) and a second supremum instance with different algebra — rather than adding
more untested new material on top. One review item (existential witness, second
offering since its own pause), one repair item (divergence-proof execution, still
waiting on its first real attempt since one wrong attempt on 08-26). **Strong
induction is paused** — two blank exposures on two different representations
(09-01, 09-02) — not offered today.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 12 offered, 8 with real evidence
(four — 08-24, 08-27, 08-28, 09-02 — came back entirely blank; the two strongest
of the phase, 08-31 and 09-01, were immediately followed by another blank one).

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves.

**Where the three named bugs stand:**

| Bug | Status |
|---|---|
| **#1** — frame a proof and stop before executing | ✅ **closed** (08-21's √3; reconfirmed cleanly 08-31) |
| **#3** — quantifier negation backwards | ✅ **closed** — atomic clean three times (most recently 08-31), compound predicates clean on all five items 08-25 |
| **#2** — induction never uses the hypothesis | ✅ **closed** — clean on two Core problems 08-31, clean again on a fresh instance 09-01 (two clean demonstrations, 1-day spacing) |

All three named bugs from the calibration now have real, repeated evidence of
repair. What's open now: strong induction specifically (two blank exposures,
paused — same structural caveat as Taylor/geometric series below), sup/inf (new,
zero real evidence yet, today's actual first try), divergence-proof execution
(still waiting on its first real attempt since one wrong attempt on 08-26), and
the paused calculus-repair block.

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), setup discipline, **contrapositive applied
to one's own proof** (first clean instance 09-01, after three prior non-clean
attempts), and **plain-English quantifier meaning** (first clean instance 09-01,
after one wrong plus four blanks — the longest-open item in the repo, broken by a
worked-scaffold approach rather than a sixth cold re-ask). None of it returns as
repair.

## The hour

Today's normal Mon–Thu shape: review (1 item) → repair (1 item) → Core (2
problems) → optional stretch. See the session file for the exact breakdown.
`lessons/proof-foundations.md` §9 (supremum/infimum) is worth a quick re-read
before Core — it's four short paragraphs with one worked example.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

Four sessions now (08-24, 08-27, 08-28, 09-02) have come back with nothing written
in at all, most recently right after the two strongest sessions in the repo's
history. If today only gets partway, even a half-filled box beats a blank one —
"ran out of time" and "no idea what to do after the setup" send tomorrow's session
in completely different directions, and a totally blank file gives the next run
nothing to work with except "hold."

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
- **Throughput.** This week (08-31 through 09-02): two full sessions then one
  entirely blank. Revisit at the 09-04 Friday review.
- **Backlog of overdue retention checks** — setup discipline, pigeonhole general
  principle, compound-predicate negation, quantifier order, induction-counting —
  all due, none retested yet; the one-review-item-per-session hard cap means these
  queue up faster than they clear. Not urgent (all are past clean instances), but
  worth knowing the queue is backing up.
- **Phase 0 exit gate — content complete, evidence isn't.** All five gate topics
  have now been taught at least once (sup/inf, taught 09-02, was the last), but
  sup/inf has zero real attempts and strong induction is paused on two blanks — the
  gate itself isn't imminent until those produce real evidence.
- **Whether entirely-blank sessions correlate with anything.** Four now (08-24,
  08-27, 08-28, 09-02), the last landing immediately after the two strongest
  sessions in the repo. Worth your read on whether something about timing or
  cadence is behind it — `CURRICULUM.md` §7 has the standing, unresolved note.
