# Start here

**Right now: [Session 12 — 2026-09-02, Sup/inf + strong induction's second attempt](weeks/2026-08-31/09-02.md).**
Yesterday (09-01) was the strongest session in this repo's history — R1, R2, and
the Repair item all clean, including first-ever clean passes on the two
longest-open gaps here (contrapositive-applied, and plain-English quantifier
meaning after one wrong plus four blanks). Core 1 ($2^n$ subsets, the literal
Phase 0 exit-gate counting problem) was clean too. Only Core 2 (strong induction,
first real attempt) came back blank — re-offered fresh today, first thing in Core.

Today: one review item (existential witnesses, resuming after a two-session
pause), one repair item (divergence-proof execution, finally getting its own
slot after two sessions of the quantifier item taking priority), and Core: strong
induction's retry (binary representation, not primes) plus **the last major
untaught Phase 0 topic — supremum/infimum**, with a short new lesson section
(`lessons/proof-foundations.md` §9) and a first real $\varepsilon$-style proof.
The optional Stretch previews exit-gate item 5 directly.

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~15 sessions, 11 offered, 8 with real evidence
(three — 08-24, 08-27, 08-28 — came back entirely blank; the two most recent,
08-31 and 09-01, were the strongest of the phase).

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
repair. What's open now is narrower: strong induction specifically (one blank,
being re-offered), divergence-proof execution (waiting on today's repair slot),
and the paused calculus-repair block.

Also retired: unfolding definitions, contrapositive vs. contradiction (concept),
divisibility transitivity, injective/surjective, pigeonhole (both the specific-case
derivation and the general principle), setup discipline, **contrapositive applied
to one's own proof** (first clean instance 09-01, after three prior non-clean
attempts), and **plain-English quantifier meaning** (first clean instance 09-01,
after one wrong plus four blanks — the longest-open item in the repo, broken by a
worked-scaffold approach rather than a sixth cold re-ask). None of it returns as
repair.

Divergence proofs still stall on terms like $(-1)^k$ (wrong once, identical
stopping point, then several sessions where its repair slot went to the quantifier
item instead) — today's Repair slot is finally its turn.

## The hour

Today's normal Mon–Thu shape: review (1 item) → repair (1 item) → Core (2 new
problems) → optional stretch. See the session file for the exact breakdown.
`lessons/proof-foundations.md` §9 (new — supremum/infimum) is worth reading before
Core 2; it's four short paragraphs with one worked example.

## The one rule that matters

**Write into the `-work.md` file — including the timing and the "where I got stuck" box.**

The last two sessions (08-31, 09-01) both had real, careful work, and both still
left the timing/stuck boxes blank. It doesn't block anything, but it's the one
piece of information the next session can't infer — even two words turns a guess
into a fact.

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
  four and two blank exposures respectively. Existential witnesses had the same
  pause but resume today — see `CURRICULUM.md` §7's 2026-08-27 amendment for the
  open question on Taylor/geometric series specifically, still waiting on your
  judgment.
- **Chain rule, integration by parts** — blank on the calibration, never re-tested.
  Still waiting on calculus repair's Core to produce any evidence at all before this
  can even be scheduled.
- **Throughput.** Two sessions of data this week (08-31, 09-01), both full — better
  than either prior post-restructure week at this point, but still short of a full
  week's read. Revisit at the 09-04 Friday review.
- **Backlog of overdue retention checks** — setup discipline, pigeonhole general
  principle, compound-predicate negation, quantifier order — all due, none retested
  yet; the one-review-item-per-session hard cap means these queue up faster than
  they clear. Not urgent (all are past clean instances), but worth knowing the
  queue is backing up.
- **Phase 0 exit gate is getting close.** Sup/inf (today) was the last major
  untaught topic. Not imminent — expect it once sup/inf gets a second pass and the
  retention backlog above clears — but worth knowing it's on the visible horizon
  now, not a distant abstraction.
