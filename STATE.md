# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-18 (session 2 graded, session 3 built)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 2 of ~25 (complete) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 5 of 8 offered (Days 1, 2, 6 + calibration + Session 2) |

### Immediate next action

**[Session 3 — 2026-08-19](weeks/2026-08-17/08-19.md)** is built and waiting:
injective/surjective (non-optional — third attempt after two blanks), the
$3\mid n^2 \implies 3\mid n$ lemma, and $\sqrt3$ irrational by contradiction. Read §4 of
[`lessons/proof-foundations.md`](lessons/proof-foundations.md) if you haven't already
(~3 min), then work into
[`weeks/2026-08-17/08-19-work.md`](weeks/2026-08-17/08-19-work.md).

Grading context: [`weeks/2026-08-17/08-18-feedback.md`](weeks/2026-08-17/08-18-feedback.md).

Also outstanding: **Section C redone, timed** (10 min) — still not done, carried over
from 2026-08-17. It is the last hole in the evidence table and it decides whether
calculus repair needs its own sessions.

---

## Evidence log

*Observed work in this repo is strong evidence; transcript grades are weak evidence
(old, and about a different kind of task). Updated 2026-08-18 from Session 2.*

| Skill | Evidence | Verdict |
|---|---|---|
| Negating an implication (P⟹Q to P ∧ ¬Q) | Calibration A1 — done correctly | **competent** |
| Partial derivatives | Calibration D1 — both partials correct, 8 days after Day 1 | **competent** |
| Unfolding a definition and computing | Session 2 Core 1 — substitution mechanics correct in all 3 problems (a, b, c) | **competent** |
| Completing a proof after setting it up | Calibration A1: stopped at setup. Session 2 R1: carried through to a landing, though landing was under-specified (claim stated, witness not named) | **improving — bug #1, 1 of 2 clean retrievals** |
| Setup discipline (state the hypothesis, not the conclusion) | Session 2 Core 1(a), 1(b) — setup assumed the thing being proved. Core 1(c) — done correctly | **gap — new, split out from bug #1** |
| Existential witness domain ($\mathbb{Z}$ vs $\mathbb{N}$) | Session 2 R1, R2, Core 1 — $\mathbb{N}$ used throughout where $\mathbb{Z}$ was needed | **gap — new, mechanical** |
| Induction: using the hypothesis | Calibration A2 — IH never written down or used | **gap — bug #2, structural** |
| Induction: reading Σ notation | Calibration A2 — read closed form as the *n*-th term, not the sum | **misconception** |
| Quantifier negation | Calibration A3 — negated domain restrictions, kept quantifiers. Backwards, 4×, consistently | **gap — bug #3, highest ROI** |
| Injection / surjection | Calibration A4 — blank. Session 2 Core 2 — blank again | **no data, 2× skipped — Session 3 Core 1, non-optional** |
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

*Shifted one day earlier: calibration was completed Mon 2026-08-17, not the 18th.*

| # | Date | Topic | Lesson § | Type |
|---|---|---|---|---|
| 1 | Mon 08-17 | ~~Calibration diagnostic~~ | — | ✅ done |
| 2 | Tue 08-18 | ~~Unfolding definitions; A1 by contrapositive; A4~~ | §0, §1, §3 | ✅ done (Core 2/A4 still blank) |
| 3 | **Wed 08-19** | **Setup discipline repair; injective/surjective (non-optional); contradiction — √3 irrational** | §1, §4 | ⬅ **built** |
| 4 | Thu 08-20 | **Quantifier negation drill I** — ~20 statements, mechanical | §5 | drill |
| 5 | Fri 08-21 | **Review day** — retrieval + Section C redone, timed | — | review |
| 6 | Mon 08-24 | **Quantifier negation drill II** — nested, ε-δ shaped | §5 | drill |
| 7 | Tue 08-25 | **Induction I** — the hypothesis *is* the engine | §6 | new |
| 8 | Wed 08-26 | **Induction II** — sum recurrences, factoring the IH out | §6 | new |
| 9 | Thu 08-27 | **Induction III** — strong induction, well-ordering | §6 | new |
| 10 | Fri 08-28 | **Review day** — mixed; induction + negation retrieval | — | review |

Sessions 11–25 (sets/functions, counterexamples, sup/inf, ε-arguments, calculus repair,
Phase 0 gate) get scheduled at the 08-28 review, once real throughput is known.

---

## Open weaknesses

*Review days bias toward this list. Remove only after two clean cold retrievals at
≥7-day spacing.*

- [ ] **Bug #1 — stopping at the setup.** Improving: Session 2 carried every attempted proof to a landing. One clean retrieval logged (08-18 R1); needs one more independent clean instance before closing.
- [ ] **New — setup discipline.** Setup states the conclusion instead of only the hypothesis (Session 2 Core 1a, 1b). Split out from bug #1 because the failure is different: it's not stopping early, it's smuggling the answer into the assumptions.
- [ ] **New — existential witness domain.** $\exists k \in \mathbb{N}$ used where $\mathbb{Z}$ was required, consistently, Session 2. Mechanical, should close fast.
- [ ] **Injective/surjective — construct an example, prove both halves.** Calibration A4 and Session 2 Core 2 both blank. Zero data after two attempts. Session 3 Core 1, non-optional.
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of building from *n*. IH never written. Not yet re-tested.
- [ ] **Bug #3 — negation flips the wrong things.** Domain restrictions negated, quantifiers left alone. Exactly backwards. Not yet re-tested.
- [ ] Rank / linear independence / basis / null space — definitions absent
- [ ] Σ notation: closed form vs. *n*-th term
- [ ] Arithmetic slips when moving terms across an equals sign / FOIL under time pressure (Session 2 Core 1(b): $4xy \to 4xy^2$)
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
| 2026-08-17 | 3 so far | 3 (Day 6, calibration, Session 2) | 100% |

At a sustained 3/week, the ~36-week plan becomes ~60. **Open question for review:** were
the misses circumstantial, or is 3/week the honest steady state? Re-pricing the plan
around a rate you actually hit beats slipping quietly against one you don't.

---

## Changelog

- **2026-08-18** — Session 2 graded, Session 3 built. Bug #1 (stopping at setup)
  showed real improvement — every attempted proof was carried to a landing. Two new
  mechanical issues surfaced and are now tracked separately: setup discipline
  (assuming the conclusion) and existential-witness domain ($\mathbb{Z}$ vs
  $\mathbb{N}$). Injective/surjective still has zero data after two assignments —
  promoted to non-optional Core 1 in Session 3. Full grading in
  `weeks/2026-08-17/08-18-feedback.md`.
- **2026-08-17** — Session 2 built. Phase 0 lesson written
  (`lessons/proof-foundations.md`). `START-HERE.md` added as the repo entry point;
  `lessons/README.md` marks the multivariable and linear-algebra lessons as preview.
- **2026-08-17** — Calibration graded. Evidence log populated with real data for the
  first time. Horizon reordered around the three named bugs. Amendments proposed to
  `CURRICULUM.md` §7 (Phase 0: 3→5 weeks).
- **2026-08-17** — Restructured. Added `CURRICULUM.md`, this file, `REVIEW-QUEUE.md`,
  `RUN-PROMPT.md`. Retargeted from "ML/AI + aerospace" to "ML research depth + proof
  maturity." Inserted Phase 0 (proofs) ahead of everything. Days 1–6 reclassified as a
  preview of Phase 2 material, not as completed coverage.
- **2026-08-10** — Started daily practice.
