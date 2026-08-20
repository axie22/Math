# Start here

**Right now: [Session 5 — 2026-08-21](weeks/2026-08-17/08-21.md).** Friday review
day — no new material, closed book throughout. Part 1 is the timed Section C redo
(chain rule / Taylor / integration by parts) that's been outstanding since the
2026-08-18 calibration; Part 2 is mixed retrieval; Part 3 is a synthesis problem.
Work into [`08-21-work.md`](weeks/2026-08-17/08-21-work.md).

Yesterday's quantifier-negation drill split cleanly: plain ∀/∃ negation is solid, but
negating an implication or an "or" statement both failed — the connective-specific
rule wasn't applied even though it was printed right there in the problem. Pigeonhole
showed real progress — the specific $\{1,\dots,6\}\to\{1,\dots,5\}$ case got properly
derived and landed this time — but stating the *general* principle in words was weak.
And two review-block retests (landing the $\sqrt3$ proof, fixing the
contrapositive/contradiction framing) went unattempted two sessions running — today's
review day leads with both of those. Full grading of session 4:
[`08-20-feedback.md`](weeks/2026-08-17/08-20-feedback.md).

## What phase you're in and why

**Phase 0 — proof foundations.** ~5 weeks, ~25 sessions.

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves. Starting anywhere else
means arriving at those phases unable to read them.

Three named bugs, attacked in this order:

| Order | Bug | Sessions | Lesson § |
|---|---|---|---|
| 1st | **#1** — you frame a proof and stop before executing | 2–3 | §1 |
| 2nd | **#3** — quantifier negation is exactly backwards | 4, 6 | §5 |
| 3rd | **#2** — induction never uses the hypothesis | 7–9 | §6 |

(The bug *numbers* are from the calibration feedback, where they're ordered by which
question they showed up on. They're attacked in a different order: bug #1 first because
the habit it installs — *replace the word with its definition and compute* — is the
move the other two also need.)

## The hour

| | |
|---|---|
| 0–10 min | Review block. Closed book, from memory. |
| 10–45 min | Core problems. |
| 45–60 min | Stretch (optional), then note where you got stuck. |

Reading isn't the session. The lesson file is a handbook to consult, not a chapter to
read front to back — it's organized so each session points at two or three sections.

## The one rule that matters

**Write into the `-work.md` file.** It's the only thing that tells the system what you
actually know. Blank means difficulty holds; partial counts; wrong is the most
informative thing in the repo. Six days of problems produced zero data before the
calibration, and that's the whole reason the first three weeks went sideways.

Solutions post the next day, never the same day. Sitting stuck is the mechanism.

## Where everything lives

| File | What it's for |
|---|---|
| [`CURRICULUM.md`](CURRICULUM.md) | The 6-phase plan and its exit gates. Changes monthly, by you |
| [`STATE.md`](STATE.md) | Where you are, what you've proven you know, next 10 sessions |
| [`REVIEW-QUEUE.md`](REVIEW-QUEUE.md) | Spaced repetition — what resurfaces when |
| [`RUN-PROMPT.md`](RUN-PROMPT.md) | The prompt the daily scheduled task runs |
| [`lessons/`](lessons/README.md) | Reference. Only `proof-foundations.md` is current |
| `weeks/<monday>/` | `MM-DD.md` problems · `-work.md` yours · `-solution.md` next day · `-feedback.md` grading |
| [`diagnostics/`](diagnostics/2026-08-18-calibration-feedback.md) | Calibration and phase-gate assessments |

## Still outstanding

- **Section C, timed (10 min) — now Part 1 of today's session.** It was left blank at
  the calibration; it's the one hole left in the evidence table and decides whether
  calculus repair needs its own sessions or can stay interleaved.
- **Decide the honest session rate.** The plan is priced at 5/week; you've been running
  ~3, though this week (2026-08-17) is on pace for 5/5 pending today. If 3 is real, the
  plan should be re-priced rather than quietly slipping against a number that was never
  going to happen — worth a real look once a few weeks of post-restructure data exist.
