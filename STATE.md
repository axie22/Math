# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-20 (session 4 graded, session 5 built)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 4 of ~25 (complete) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 7 of 10 offered (Days 1, 2, 6 + calibration + Sessions 2–4) |

### Immediate next action

**[Session 5 — 2026-08-21](weeks/2026-08-17/08-21.md)** is built and waiting: the
scheduled Friday review day. No new material — Section C (calculus mechanics),
outstanding since the 2026-08-18 calibration, gets its timed redo; the rest is mixed
retrieval weighted at the four things still open after Session 4 (two review-block
items that went unattempted, compound-predicate quantifier negation, and the
pigeonhole general principle), plus a synthesis problem generalizing pigeonhole and
connecting it to the infinite-set counterexample from 08-19. Work into
[`weeks/2026-08-17/08-21-work.md`](weeks/2026-08-17/08-21-work.md), closed book.

Grading context: [`weeks/2026-08-17/08-20-feedback.md`](weeks/2026-08-17/08-20-feedback.md).

**Section C redone, timed — resolved by Session 5's build**, not yet by an actual
attempt. It's Part 1 of tomorrow's session; still no data until it's done.

---

## Evidence log

*Observed work in this repo is strong evidence; transcript grades are weak evidence
(old, and about a different kind of task). Updated 2026-08-20 from Session 4.*

| Skill | Evidence | Verdict |
|---|---|---|
| Negating an implication (P⟹Q to P ∧ ¬Q) | Calibration A1 — done correctly. Session 4 Core 1(c) — failed fresh (implication left as an implication, both sides' inequalities flipped instead of A∧¬B); Core 2(a) — correct, but on a memorized disprove-injective shape, not clearly a fresh application | **gap — narrower than it looked. The calibration success may have been the same "recognized shape" effect; needs a genuinely novel implication to confirm either way** |
| Partial derivatives | Calibration D1 — both partials correct, 8 days after Day 1 | **competent** |
| Unfolding a definition and computing | Session 2 Core 1 — substitution mechanics correct in all 3 problems (a, b, c) | **competent** |
| Completing a proof after setting it up | Calibration A1: stopped at setup. Session 2 R1: carried to a landing (under-specified). Session 3 Core 2(b): every fact derived, closing contradiction sentence never written — relapse on a longer, multi-step proof. Session 4 R1: not attempted | **gap — bug #1, relapsed on longer proofs, then untested two days running. Retest 2026-08-21 Part 2a** |
| Setup discipline (state the hypothesis, not the conclusion) | Session 2 Core 1(a), 1(b) — setup assumed the thing being proved. Session 3: clean 4/4 (R2, Core 1(a), Core 2(a), Core 2(b)) | **competent — closing, needs one more clean instance at ≥7-day spacing (due 2026-08-22)** |
| Existential witness domain ($\mathbb{Z}$ vs $\mathbb{N}$) | Session 2: $\mathbb{N}$ used throughout. Session 3: clean in both places a witness was needed (Core 2(a), 2(b)) | **competent — closing, needs one more clean instance at ≥7-day spacing (due 2026-08-22)** |
| Injective/surjective — construct an example, prove both halves | Calibration A4, Session 2 Core 2 — blank twice. Session 3 Core 1(a) — correct mechanics (injectivity and non-surjectivity both proved), notation for stating the function itself needed a fix | **competent (mechanics)** |
| Pigeonhole — deriving a specific finite instance | Session 3 Core 1(b), 1(c) — restated the claim without deriving it. Session 4 Core 2(a), 2(b) — correct negation of injective, and a full, landed derivation that no injective $\{1,\dots,6\}\to\{1,\dots,5\}$ exists | **competent — real repair, first clean derivation** |
| Pigeonhole — general principle stated precisely, connected across sessions | Session 4 Core 2(c) — gave "both finite" instead of $\lvert A\rvert>\lvert B\rvert$; didn't connect to Session 3's equal-size case | **gap — new, narrower than the mechanism gap it replaces. Retest 2026-08-21 Part 2d/3** |
| Quantifier negation — atomic (single ∀/∃ over one plain predicate) | Session 4 Core 1(a), (b), (f) — clean 3/3, including a witness proof in (f) | **competent — one day of data, watch for a second clean instance before calling it closed** |
| Quantifier negation — compound predicates (implication, De Morgan) | Session 4 Core 1(c) — implication negated incorrectly (inverse, not negation). Core 1(e) — disjunction negated incorrectly (De Morgan swap missing, one side left unnegated). Core 1(d) — quantifier flip correct, but the old bug #3 domain-restriction error resurfaced on this one item | **gap — bug #3's descendant, now specific: the connective-level rule, not the ∀/∃ flip itself. Retest 2026-08-21 Part 2c** |
| Contrapositive vs. contradiction, conceptual distinction | Session 3 R1 — correct, well-articulated | **competent (concept)** |
| Contrapositive vs. contradiction, applied to own proof | Session 3 Core 2(a) — used the contrapositive correctly per the problem's instructions, but narrated the ending as a contradiction against a nonexistent "given." Session 4 R2 (direct retest): not attempted | **gap — new, concept/application split, untested two days running. Retest 2026-08-21 Part 2b** |
| Induction: using the hypothesis | Calibration A2 — IH never written down or used | **gap — bug #2, structural** |
| Induction: reading Σ notation | Calibration A2 — read closed form as the *n*-th term, not the sum | **misconception** |
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
| 4 | ~~Thu 08-20~~ | ~~Quantifier negation drill I (6 statements) + pigeonhole proof~~ | §5, §8 | ✅ done (atomic negation clean; compound predicates and pigeonhole's general principle both gaps) |
| 5 | **Fri 08-21** | **Review day** — Section C timed redo + mixed retrieval + pigeonhole/infinite-set synthesis | — | ⬅ **built** |
| 6 | Mon 08-24 | **Quantifier negation drill II** — compound predicates first (implication/De Morgan repair from Session 4), *then* nested, ε-δ-shaped statements | §5 | drill |
| 7 | Tue 08-25 | **Induction I** — the hypothesis *is* the engine | §6 | new |
| 8 | Wed 08-26 | **Induction II** — sum recurrences, factoring the IH out | §6 | new |
| 9 | Thu 08-27 | **Induction III** — strong induction, well-ordering | §6 | new |
| 10 | Fri 08-28 | **Review day** — mixed; induction + negation retrieval | — | review |

**Session 6 note (2026-08-20):** the original plan for session 6 was straight to
nested, ε-δ-shaped negation. Session 4 found the actual remaining gap is narrower and
different — negating implications and disjunctions specifically, not the ∀/∃ flip or
nesting itself. The ε-N convergence example in lesson §5 is entirely atomic predicates
chained together (no implication or and/or inside), so drilling nesting alone would not
exercise the compound-predicate rule. Session 6 should open with 2–3 compound-predicate
negations before adding nesting, not after.

Sessions 11–25 (sets/functions, counterexamples, sup/inf, ε-arguments, calculus repair,
Phase 0 gate) get scheduled at the 08-28 review, once real throughput is known.

---

## Open weaknesses

*Review days bias toward this list. Remove only after two clean cold retrievals at
≥7-day spacing.*

- [ ] **Bug #1 — landing the proof.** Session 2: every attempted proof reached a landing (one clean instance, 08-18 R1). Session 3 Core 2(b): relapsed on a longer, multi-step proof — every fact derived, closing contradiction sentence never written. Session 4 R1: not attempted — still untested. Retest 2026-08-21 Part 2a.
- [ ] **New — contrapositive vs. contradiction, applied.** Session 3 Core 2(a) used the contrapositive correctly per instructions but narrated the ending as a contradiction against a nonexistent "given." Concept (R1, same day) was correct in the abstract; the gap is applying it while writing. Session 4 R2 (direct fix): not attempted. Retest 2026-08-21 Part 2b.
- [ ] **Quantifier negation, compound predicates (implication, De Morgan).** Bug #3's narrower descendant. Session 4 Core 1(c) negated an implication as its inverse instead of $A\wedge\lnot B$; Core 1(e) negated a disjunction without applying De Morgan. The plain ∀/∃-over-one-predicate case is now solid (Core 1a, 1b, 1f) — this item tracks specifically the connective-level rule. Retest 2026-08-21 Part 2c.
- [ ] **Pigeonhole, general principle stated precisely + connected across sessions.** Narrowed from last session's version. Session 4 Core 2(a)/(b) now derive a specific instance cleanly — that part is closed (see below). Core 2(c) gave "both finite" instead of $|A|>|B|$ and made no connection to Session 3's equal-size case. Retest 2026-08-21 Part 2d, generalized in Part 3.
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of building from *n*. IH never written. Not yet re-tested.
- [ ] Rank / linear independence / basis / null space — definitions absent
- [ ] Σ notation: closed form vs. *n*-th term
- [ ] Arithmetic slips when moving terms across an equals sign / FOIL under time pressure, or transcribing a binomial expansion (Session 2 Core 1(b): $4xy \to 4xy^2$; Session 3 Core 2(a): "$12k\,3$" for $12k+4$ — didn't affect the final result either time, but worth slowing down on)
- [ ] Gradient stated precisely (vector of partials, steepest ascent, ⊥ level curves)

**Closed this session (setup discipline, existential witness domain in $\mathbb{Z}$,
inherited from Session 3):** four clean, independent instances each — see evidence
log. Not removed from tracking yet (need one more clean instance at ≥7-day spacing per
the retirement rule), but no longer active open weaknesses; only in
`REVIEW-QUEUE.md`'s scheduled table now.

**Newly off this list (Session 4):** deriving a specific pigeonhole instance
(distinct from stating the general principle, which stays open above) — Core 2(a) and
2(b) both landed cleanly, a real repair of Session 3's gap. Quantifier negation over a
single atomic predicate is also off this list — Core 1(a), (b), (f) were clean; what
remains open is narrower (compound predicates, tracked above).

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
| 2026-08-17 | 5 (Mon–Fri) | 5 (Day 6, calibration, Sessions 2–4; Session 5 built, pending completion) | 100% so far |

At a sustained 3/week, the ~36-week plan becomes ~60. Week of 2026-08-17 is the first
full 5-for-5 week if Friday's session gets done — worth confirming at the actual
weekly review below rather than celebrating early. **Open question for review:** were
the earlier misses circumstantial, or is 3/week the honest steady state? Re-pricing the
plan around a rate you actually hit beats slipping quietly against one you don't.

---

## Weekly review — 2026-08-21 (Friday)

*Per `CURRICULUM.md` §8: written when building the Friday session, not after grading
it — Session 5 (08-21) is what triggers this.*

**On plan?** Yes, mechanically — still Phase 0, session 5 of ~25, on the sequence
`CURRICULUM.md` and the rolling horizon lay out. Underneath that, real signal:
Session 4 is the first session where the *specific* skill being taught (quantifier
negation) came back with a precise, diagnosable split (atomic solid, compound not)
rather than either a clean pass or a diffuse mess. That's the pattern this whole
restructure was betting on producing, and it's the second time in a row a "new topic"
session has produced a narrow, named finding instead of noise (pigeonhole was the
first, Session 3→4).

**Amendments in `CURRICULUM.md` §7 to accept?** Not this week — still deferring to
Alex's judgment per the file's own rule ("reviewed weekly... does not act on these
unilaterally"). Two items in §7 remain genuinely open and unresolved by this week's
data:
- Phase 0: 3→5 weeks, induction block, negation drill — still pending, no reason to
  change the recommendation.
- Section C (calculus) — still no data as of this writing; Session 5 Part 1 resolves
  this tomorrow. **Recommend revisiting this specific §7 item next week once Section C
  actually has a result**, since it's the one amendment blocked on a fact rather than
  a judgment call.
- Throughput re-pricing (3/week vs. 5/week) — this week is on pace for 5/5 pending
  Friday's completion. One good week isn't enough to resolve the question either way;
  flagging it as **worth a real look at the next 08-28 review**, once two or three
  weeks of post-restructure data exist instead of one.

**Is the review queue backing up?** Somewhat, in one specific place: two items (bug #1
landing, contrapositive-applied) have now gone two sessions without being attempted at
all — not failed, just skipped, apparently because Core work is displacing the review
block rather than following it. That's not the queue mechanism breaking; it's the
review block not happening. Worth watching whether Session 5, which is *entirely*
review, produces attempts on these — if they're still blank after a session with
nothing else competing for time, that's a different and more concerning finding than
"ran out of clock."

---

## Changelog

- **2026-08-20** — Session 4 graded, Session 5 (Friday review) built. Both review-block
  retests (bug #1 landing, contrapositive-applied) were left blank — no new evidence,
  carried to tomorrow. Quantifier negation, drilled for the first time, split cleanly:
  atomic ∀/∃-over-one-predicate negation clean 3/3 (a, b, f), compound-predicate
  negation (implication in c, disjunction/De Morgan in e) failed both times despite the
  rule being printed directly in the problem file; (d) also showed one resurfacing of
  the original domain-restriction bug. Pigeonhole showed real repair — Core 2(a)/(b)
  derived the specific $\{1,\dots,6\}\to\{1,\dots,5\}$ case cleanly and landed the
  contradiction, closing last session's "restated without deriving" gap — but Core
  2(c), asking for the general principle in words plus a connection to Session 3, was
  circular and made no connection. Session 5 is the regularly-scheduled Friday review
  day regardless of today's result: Section C (calculus, no data since the calibration)
  gets its timed redo, mixed retrieval targets the four open items above, and a
  synthesis problem generalizes pigeonhole to arbitrary finite sizes and connects it to
  the infinite-set counterexample from 08-19. Session 6's plan adjusted to open with
  compound-predicate negation before nesting, per the rolling-horizon note above. Full
  grading in `weeks/2026-08-17/08-20-feedback.md`.
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
