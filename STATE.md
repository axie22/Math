# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-17 (calibration graded)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 1 of ~25 (calibration complete) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 4 of 7 offered (Days 1, 2, 6 + calibration) |

### Immediate next action

Session 2 (**2026-08-19**): redo **A1** with the mechanism explained, then **A4**, then
begin quantifier negation. See
[`diagnostics/2026-08-18-calibration-feedback.md`](diagnostics/2026-08-18-calibration-feedback.md).

Also outstanding: **Section C redone, timed** (10 min). It is the last hole in the
evidence table and it decides whether calculus repair needs its own sessions.

---

## Evidence log

*Observed work in this repo is strong evidence; transcript grades are weak evidence
(old, and about a different kind of task). Updated 2026-08-17 from the calibration.*

| Skill | Evidence | Verdict |
|---|---|---|
| Negating an implication (P⟹Q to P ∧ ¬Q) | Calibration A1 — done correctly | **competent** |
| Partial derivatives | Calibration D1 — both partials correct, 8 days after Day 1 | **competent** |
| Completing a proof after setting it up | Calibration A1 — stopped at the setup | **gap — bug #1** |
| Induction: using the hypothesis | Calibration A2 — IH never written down or used | **gap — bug #2, structural** |
| Induction: reading Σ notation | Calibration A2 — read closed form as the *n*-th term, not the sum | **misconception** |
| Quantifier negation | Calibration A3 — negated domain restrictions, kept quantifiers. Backwards, 4×, consistently | **gap — bug #3, highest ROI** |
| Injection / surjection | Calibration A4 — blank | **no data** |
| Rank | Calibration B1 — "number of non-empty values." Incorrect | **gap — significant** |
| Linear independence | Calibration B1 — circular definition | **gap** |
| Basis, null space, rank–nullity | Calibration B1/B2 — blank | **no data, presumed gap** |
| Diagonalizability criteria | Calibration B4 — blank | **no data** |
| Arithmetic under time pressure | A2 (2 slips), D1 (1 slip) | **minor, watch it** |
| Chain rule, Taylor, integration | Calibration C — entirely blank | **NO DATA — resolve before Phase 0 week 2** |
| Gradient (conceptual) | Calibration D2a — right direction, imprecise; key properties absent | **partial** |
| Eigenvectors, spectral theorem, SVD, Lagrange | Days 4–6 not attempted; D2b/c, D3, D4 blank | **not taught yet — re-teach in Phases 1–2** |
| Probability | MATH-UA 235, A- (Fall 2024) | weak evidence, **presumed strength** |
| Applied ML | CSCI-UA 473 A, DS-UA 301 A | **strength** |

**The headline:** Section A failed in three *specific, mechanical* ways rather than
diffusely. Named bugs have named fixes. Section B is worse than the transcript
predicted and Phase 1 must not be compressed.

---

## Rolling horizon — next 10 sessions

*Revised 2026-08-17 from calibration results. Reordered to hit the three named bugs
first, hardest-hitting first.*

| # | Date | Topic | Type |
|---|---|---|---|
| 1 | 2026-08-18 | ~~Calibration diagnostic~~ | ✅ done |
| 2 | 2026-08-19 | Redo A1 with the mechanism; A4; unfolding definitions | repair |
| 3 | 2026-08-20 | **Quantifier negation drill I** — ~20 statements, mechanical | drill |
| 4 | 2026-08-21 | **Review day** — A1/A3 retrieval + Section C, timed | review |
| 5 | 2026-08-24 | **Quantifier negation drill II** — nested, ε-δ shaped | drill |
| 6 | 2026-08-25 | Direct proof & contrapositive; when each is the lighter tool | new |
| 7 | 2026-08-26 | **Induction I** — what the hypothesis is and why it's the engine | new |
| 8 | 2026-08-27 | **Induction II** — telescoping sums, factoring the IH out | new |
| 9 | 2026-08-28 | **Review day** — mixed; induction + negation retrieval | review |
| 10 | 2026-08-31 | **Induction III** — strong induction, well-ordering | new |

Sessions 11–25 (contradiction, sets/functions, sup/inf, ε-arguments, calculus repair,
Phase 0 gate) get scheduled at the 2026-08-28 review, once real throughput is known.

---

## Open weaknesses

*Review days bias toward this list. Remove only after two clean cold retrievals at
≥7-day spacing.*

- [ ] **Bug #1 — stopping at the setup.** Frame the proof, then don't execute. Missing habit: unfold the definition and compute.
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of building from *n*. IH never written.
- [ ] **Bug #3 — negation flips the wrong things.** Domain restrictions negated, quantifiers left alone. Exactly backwards.
- [ ] Rank / linear independence / basis / null space — definitions absent
- [ ] Σ notation: closed form vs. *n*-th term
- [ ] Arithmetic slips when moving terms across an equals sign
- [ ] Gradient stated precisely (vector of partials, steepest ascent, ⊥ level curves)

---

## Gate results

| Phase | Date attempted | Score | Result |
|---|---|---|---|
| Calibration (not a gate) | 2026-08-17 | A ~20% · B ~5% · C no data · D n/a | Baseline recorded |

---

## Throughput

*Watch this. The plan is priced at 5 sessions/week; the plan is only real if that's real.*

| Week | Offered | Completed | Rate |
|---|---|---|---|
| 2026-08-10 | 5 | 2 (Days 1, 2) | 40% |
| 2026-08-17 | 2 so far | 2 (Day 6, calibration) | 100% |

At a sustained 3/week, the ~36-week plan becomes ~60. **Open question for review:** were
the misses circumstantial, or is 3/week the honest steady state? Re-pricing the plan
around a rate you actually hit beats slipping quietly against one you don't.

---

## Changelog

- **2026-08-17** — Calibration graded. Evidence log populated with real data for the
  first time. Horizon reordered around the three named bugs. Amendments proposed to
  `CURRICULUM.md` §7 (Phase 0: 3→5 weeks).
- **2026-08-17** — Restructured. Added `CURRICULUM.md`, this file, `REVIEW-QUEUE.md`,
  `RUN-PROMPT.md`. Retargeted from "ML/AI + aerospace" to "ML research depth + proof
  maturity." Inserted Phase 0 (proofs) ahead of everything. Days 1–6 reclassified as a
  preview of Phase 2 material, not as completed coverage.
- **2026-08-10** — Started daily practice.
