# Start here

**Right now: [Session 4 — 2026-08-20](weeks/2026-08-17/08-20.md).** One hour. Read §5
of the [proof foundations lesson](lessons/proof-foundations.md) (quantifiers and
negation — new today) and skim §8 (the finite case), then work the problems into
[`08-20-work.md`](weeks/2026-08-17/08-20-work.md).

Setup discipline and $\mathbb{Z}$-witnesses both went clean 4/4 yesterday — good, keep
doing that, but they're not fully retired yet. Two things carried over from
yesterday's grading instead: the review block asks you to land the $\sqrt3$ proof's
final sentence explicitly (you derived everything and stopped one line short), and
Core 2 reuses lesson §8's pigeonhole argument, which yesterday's Core 1(b)/(c) was
missing. Full grading of session 3:
[`08-19-feedback.md`](weeks/2026-08-17/08-19-feedback.md).

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

- **Redo calibration Section C, timed (10 min).** It was left blank so the chain rule /
  Taylor / integration picture is the one hole in the evidence table. It decides
  whether calculus repair needs its own sessions or can stay interleaved.
- **Decide the honest session rate.** The plan is priced at 5/week; you've been running
  ~3. If 3 is real, the plan should be re-priced at ~60 weeks rather than quietly
  slipping against a number that was never going to happen.
