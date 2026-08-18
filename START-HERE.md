# Start here

**Right now: [Session 2 — 2026-08-18](weeks/2026-08-17/08-18.md).** One hour. Read §0,
§1, §3 of the [proof foundations lesson](lessons/proof-foundations.md) first (~10 min),
then work the problems into
[`08-18-work.md`](weeks/2026-08-17/08-18-work.md).

That's the answer. Everything below is context you can read later.

---

## What phase you're in and why

**Phase 0 — proof foundations.** ~5 weeks, ~25 sessions.

Not because proofs are the goal, but because the [calibration](diagnostics/2026-08-18-calibration-feedback.md)
showed they're the bottleneck. Convex optimization is a sequence of inequality proofs.
Statistical learning theory is a sequence of quantifier arguments. Rigorous linear
algebra is a sequence of "suppose $\sum c_i v_i = 0$" moves. Starting anywhere else
means arriving at those phases unable to read them.

Three specific bugs to fix, in this order:

| | Bug | Fixed by |
|---|---|---|
| 1 | You frame a proof and stop before executing | **Sessions 2–3** — unfolding definitions |
| 2 | Quantifier negation is exactly backwards | Sessions 4–6 — mechanical drilling |
| 3 | Induction never uses the hypothesis | Sessions 7–9 — the induction block |

Bug 1 first because the habit it installs — *replace the word with its definition and
compute* — is the move the other two also need.

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
