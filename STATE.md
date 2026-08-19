# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-19 (session 3 graded, session 4 built)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 3 of ~25 (complete) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 6 of 9 offered (Days 1, 2, 6 + calibration + Sessions 2–3) |

### Immediate next action

**[Session 4 — 2026-08-20](weeks/2026-08-17/08-20.md)** is built and waiting:
quantifier negation (bug #3, first real drill), plus a pigeonhole proof (no injective
$\{1,\dots,6\}\to\{1,\dots,5\}$) that directly repairs yesterday's Core 1(b)/(c) gap.
Read §5 (new) and skim §8 (finite case) of
[`lessons/proof-foundations.md`](lessons/proof-foundations.md), then work into
[`weeks/2026-08-17/08-20-work.md`](weeks/2026-08-17/08-20-work.md).

Grading context: [`weeks/2026-08-17/08-19-feedback.md`](weeks/2026-08-17/08-19-feedback.md).

Also outstanding: **Section C redone, timed** (10 min) — still not done, carried over
from 2026-08-17, and now the plan for Friday 2026-08-21's review day. It is the last
hole in the evidence table and it decides whether calculus repair needs its own
sessions.

---

## Evidence log

*Observed work in this repo is strong evidence; transcript grades are weak evidence
(old, and about a different kind of task). Updated 2026-08-19 from Session 3.*

| Skill | Evidence | Verdict |
|---|---|---|
| Negating an implication (P⟹Q to P ∧ ¬Q) | Calibration A1 — done correctly | **competent** |
| Partial derivatives | Calibration D1 — both partials correct, 8 days after Day 1 | **competent** |
| Unfolding a definition and computing | Session 2 Core 1 — substitution mechanics correct in all 3 problems (a, b, c) | **competent** |
| Completing a proof after setting it up | Calibration A1: stopped at setup. Session 2 R1: carried to a landing (under-specified). Session 3 Core 2(b): every fact derived, closing contradiction sentence never written — relapse on a longer, multi-step proof | **gap — bug #1, relapsed on longer proofs. Retest 2026-08-20** |
| Setup discipline (state the hypothesis, not the conclusion) | Session 2 Core 1(a), 1(b) — setup assumed the thing being proved. Session 3: clean 4/4 (R2, Core 1(a), Core 2(a), Core 2(b)) | **competent — closing, needs one more clean instance at ≥7-day spacing (due 2026-08-22)** |
| Existential witness domain ($\mathbb{Z}$ vs $\mathbb{N}$) | Session 2: $\mathbb{N}$ used throughout. Session 3: clean in both places a witness was needed (Core 2(a), 2(b)) | **competent — closing, needs one more clean instance at ≥7-day spacing (due 2026-08-22)** |
| Injective/surjective — construct an example, prove both halves | Calibration A4, Session 2 Core 2 — blank twice. Session 3 Core 1(a) — correct mechanics (injectivity and non-surjectivity both proved), notation for stating the function itself needed a fix | **competent (mechanics)** |
| Pigeonhole — finite injective ⟹ surjective | Session 3 Core 1(b), 1(c) — restated the claim without deriving it; mechanism exists in lesson §8 but wasn't read | **gap — new. Retest 2026-08-20 Core 2** |
| Contrapositive vs. contradiction, conceptual distinction | Session 3 R1 — correct, well-articulated | **competent (concept)** |
| Contrapositive vs. contradiction, applied to own proof | Session 3 Core 2(a) — used the contrapositive correctly per the problem's instructions, but narrated the ending as a contradiction against a nonexistent "given" | **gap — new, concept/application split** |
| Induction: using the hypothesis | Calibration A2 — IH never written down or used | **gap — bug #2, structural** |
| Induction: reading Σ notation | Calibration A2 — read closed form as the *n*-th term, not the sum | **misconception** |
| Quantifier negation | Calibration A3 — negated domain restrictions, kept quantifiers. Backwards, 4×, consistently | **gap — bug #3, highest ROI. First drill 2026-08-20** |
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
| 3 | Wed 08-19 | ~~Setup discipline repair; injective/surjective (non-optional); contradiction — √3 irrational~~ | §1, §4 | ✅ done (setup + witness domain clean; pigeonhole + landing gaps found) |
| 4 | **Thu 08-20** | **Quantifier negation drill I** (~10 statements) + pigeonhole proof (repairs session 3 Core 1b/c) | §5, §8 | ⬅ **built** |
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

- [ ] **Bug #1 — landing the proof.** Session 2: every attempted proof reached a landing (one clean instance, 08-18 R1). Session 3 Core 2(b): relapsed on a longer, multi-step proof — every fact derived, closing contradiction sentence never written. Retest 2026-08-20 R1.
- [ ] **New — pigeonhole / finite injective ⟹ surjective.** Session 3 Core 1(b), 1(c) restated the claim without deriving it. Mechanism is in lesson §8, wasn't pointed to. Retest 2026-08-20 Core 2.
- [ ] **New — contrapositive vs. contradiction, applied.** Session 3 Core 2(a) used the contrapositive correctly per instructions but narrated the ending as a contradiction against a nonexistent "given." Concept (R1, same day) was correct in the abstract; the gap is applying it while writing. Quick fix queued 2026-08-20 R2.
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of building from *n*. IH never written. Not yet re-tested.
- [ ] **Bug #3 — negation flips the wrong things.** Domain restrictions negated, quantifiers left alone. Exactly backwards. First drill 2026-08-20 Core 1.
- [ ] Rank / linear independence / basis / null space — definitions absent
- [ ] Σ notation: closed form vs. *n*-th term
- [ ] Arithmetic slips when moving terms across an equals sign / FOIL under time pressure, or transcribing a binomial expansion (Session 2 Core 1(b): $4xy \to 4xy^2$; Session 3 Core 2(a): "$12k\,3$" for $12k+4$ — didn't affect the final result either time, but worth slowing down on)
- [ ] Gradient stated precisely (vector of partials, steepest ascent, ⊥ level curves)

**Closed this session (setup discipline, existential witness domain in $\mathbb{Z}$):**
four clean, independent instances each across Session 3 — see evidence log. Not
removed from tracking yet (need one more clean instance at ≥7-day spacing per the
retirement rule), but no longer active open weaknesses; only in `REVIEW-QUEUE.md`'s
scheduled table now. Constructing an injective-not-surjective example and proving both
halves is also off this list — Session 3 Core 1(a) did it cleanly.

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
| 2026-08-17 | 4 so far | 4 (Day 6, calibration, Sessions 2–3) | 100% |

At a sustained 3/week, the ~36-week plan becomes ~60. **Open question for review:** were
the misses circumstantial, or is 3/week the honest steady state? Re-pricing the plan
around a rate you actually hit beats slipping quietly against one you don't.

---

## Changelog

- **2026-08-19** — Session 3 graded, Session 4 built. Setup discipline and
  existential-witness domain ($\mathbb{Z}$ vs $\mathbb{N}$) both closed clean 4/4
  across today's problems — real, independent evidence, not one repeated example.
  Injective/surjective got its first real data (Core 1(a)): mechanics correct,
  notation needed a fix. Two new issues found: Core 1(b)/(c) restated the pigeonhole
  claim without deriving it (mechanism exists in lesson §8, wasn't pointed to), and
  Core 2(b) ($\sqrt3$ irrational) derived every fact and never wrote the closing
  contradiction sentence — bug #1 relapsing on a longer proof than the one it looked
  fixed on yesterday. Also: Core 2(a) applied the contrapositive correctly but
  narrated it with contradiction language — a concept/application split, since R1 the
  same day got the distinction right in the abstract. Session 4 advances to the next
  new topic (quantifier negation, bug #3) since nothing today was a method-level
  failure of what was actually being taught, while folding both open repairs into the
  review block and a pigeonhole Core problem. Full grading in
  `weeks/2026-08-17/08-19-feedback.md`.
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
