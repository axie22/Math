# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-25 (session 5 grading backfilled — was never written back;
session 6 (08-24) found blank, held; session 6 retry built for 08-25)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 6 of ~15 (still in progress — 08-24 attempt had no evidence, retried 08-25) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 8 of 12 offered (Days 1, 2, 6 + calibration + Sessions 2–5; Session 6 offered 08-24 with zero evidence, offered again 08-25) |

### Immediate next action

**[Session 6 retry — 2026-08-25](weeks/2026-08-24/08-25.md)** is built and waiting.
Session 6 was assigned 2026-08-24 (compound-predicate negation repair, third pass,
plus two new ideas: proving divergence from a negation, and quantifier order) and
came back with an entirely blank work file — no timing, no attempts. Per the
no-evidence rule this is a hold, not a failure: today repeats the same content with
fresh problem instances rather than advancing to Induction I. Work into
[`weeks/2026-08-24/08-25-work.md`](weeks/2026-08-24/08-25-work.md).

Grading context: [`weeks/2026-08-17/08-21-feedback.md`](weeks/2026-08-17/08-21-feedback.md)
(Session 5, the last session with any evidence at all).

**Housekeeping note (2026-08-25):** Session 5's grading (08-21-feedback.md) existed
but was never written back into this file, `REVIEW-QUEUE.md`, or `progress.md` — a
gap in whatever built Session 6 originally. Backfilled today: evidence log below,
review queue retirements, and the 08-21 progress row all now reflect Session 5's
actual results. `weeks/2026-08-17/08-21-solution.md`, which 08-24.md promised but
never posted, was also backfilled.

---

## Evidence log

*Observed work in this repo is strong evidence; transcript grades are weak evidence
(old, and about a different kind of task). Updated 2026-08-25 from Session 5's
grading (backfilled) — Session 6 (08-24) produced no evidence to add.*

| Skill | Evidence | Verdict |
|---|---|---|
| Negating an implication (P⟹Q to P ∧ ¬Q) | Calibration A1 — done correctly. Session 4 Core 1(c) — failed fresh (implication left as an implication, both sides' inequalities flipped instead of A∧¬B); Core 2(a) — correct, but on a memorized disprove-injective shape, not clearly a fresh application | **gap — narrower than it looked. The calibration success may have been the same "recognized shape" effect; needs a genuinely novel implication to confirm either way** |
| Partial derivatives | Calibration D1 — both partials correct, 8 days after Day 1 | **competent** |
| Unfolding a definition and computing | Session 2 Core 1 — substitution mechanics correct in all 3 problems (a, b, c) | **competent** |
| Completing a proof after setting it up | Calibration A1: stopped at setup. Session 2 R1: carried to a landing (under-specified). Session 3 Core 2(b): every fact derived, closing contradiction sentence never written — relapse on a longer, multi-step proof. Session 4 R1: not attempted. Session 5 (08-21) Part 2a: **landed it** — closing contradiction sentence present and correct, third attempt | **retired — bug #1 closed 2026-08-21. Moved to `REVIEW-QUEUE.md` at a 3-day interval; will not be repaired again. First retention check due 08-24, not yet run (08-24 was blank)** |
| Setup discipline (state the hypothesis, not the conclusion) | Session 2 Core 1(a), 1(b) — setup assumed the thing being proved. Session 3: clean 4/4 (R2, Core 1(a), Core 2(a), Core 2(b)) | **competent — closing, needs one more clean instance at ≥7-day spacing (due 2026-08-22)** |
| Existential witness domain ($\mathbb{Z}$ vs $\mathbb{N}$) | Session 2: $\mathbb{N}$ used throughout. Session 3: clean in both places a witness was needed (Core 2(a), 2(b)) | **competent — closing, needs one more clean instance at ≥7-day spacing (due 2026-08-22)** |
| Injective/surjective — construct an example, prove both halves | Calibration A4, Session 2 Core 2 — blank twice. Session 3 Core 1(a) — correct mechanics (injectivity and non-surjectivity both proved), notation for stating the function itself needed a fix | **competent (mechanics)** |
| Pigeonhole — deriving a specific finite instance | Session 3 Core 1(b), 1(c) — restated the claim without deriving it. Session 4 Core 2(a), 2(b) — correct negation of injective, and a full, landed derivation that no injective $\{1,\dots,6\}\to\{1,\dots,5\}$ exists | **competent — real repair, first clean derivation** |
| Pigeonhole — general principle stated precisely, connected across sessions | Session 4 Core 2(c) — gave "both finite" instead of $\lvert A\rvert>\lvert B\rvert$; didn't connect to Session 3's equal-size case. Session 5 (08-21) Part 2d — **correct**, gave the actual $|A|>|B|$ condition and connected it to Session 3's equal-size case; Part 3a/3b then generalized it to a full correct proof plus original-language explanation of why finiteness is required — best work in the repo so far | **retired — closed 2026-08-21, real repair after one gap. Moved to `REVIEW-QUEUE.md` at a 3-day interval. First retention check due 08-24, not yet run (08-24 was blank)** |
| Quantifier negation — atomic (single ∀/∃ over one plain predicate) | Session 4 Core 1(a), (b), (f) — clean 3/3, including a witness proof in (f). Not retested 08-21 (that session's negation content was compound-only) | **competent — still only one clean session of data; 08-21's review day skipped retesting it, so the "second clean instance" check moves to 08-25's R1** |
| Quantifier negation — compound predicates (implication, De Morgan) | Session 4 Core 1(c) — implication negated incorrectly (inverse, not negation). Core 1(e) — disjunction negated incorrectly (De Morgan swap missing, one side left unnegated). Core 1(d) — quantifier flip correct, but the old bug #3 domain-restriction error resurfaced on this one item. Session 5 (08-21) Part 2c(i), 2c(ii) — **failed again**, same two sub-errors: arrow survived instead of becoming "and," De Morgan applied to only one side | **gap, now failed twice with real attempts (08-20, 08-21). Session 6 (08-24) meant to be the third pass but came back blank — no new evidence. Repeated as today's (08-25) one repair item, hard-cap rule, with fresh instances** |
| Contrapositive vs. contradiction, conceptual distinction | Session 3 R1 — correct, well-articulated | **competent (concept)** |
| Contrapositive vs. contradiction, applied to own proof | Session 3 Core 2(a) — used the contrapositive correctly per the problem's instructions, but narrated the ending as a contradiction against a nonexistent "given." Session 4 R2 (direct retest): not attempted. Session 5 (08-21) Part 2b — **half right**: named the technique (contrapositive) correctly, but still didn't write the sentence explaining why proving the contrapositive settles the original claim | **gap — two genuine attempts now (08-19, 08-21), neither fully clean. Not pulled 08-25 (hard cap gave the repair slot to compound-predicate negation); waits for the next open repair slot** |
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
| 5 | Fri 08-21 | ~~Review day~~ — Section C timed redo + mixed retrieval + pigeonhole/infinite-set synthesis | — | ✅ done (bug #1 and pigeonhole general principle both closed; compound negation and contrapositive-applied still open; Taylor blank twice, moved to teaching) |
| 6 | ~~Mon 08-24~~ **→ retried Tue 08-25** | **Quantifier negation drill II** — compound predicates repair (third pass), *plus* two new ideas: proving divergence from a negation, quantifier order | §5 | 08-24 offered, zero evidence (blank). Retried 08-25 with fresh instances, same content — **built, pending** |
| 7 | Wed 08-26 | **Calculus repair — Taylor's theorem with remainder.** Moved here from "review-block item" to "taught" per the 08-21 grading: blank on the calibration and blank again 08-21, so it stops being a retrieval question and becomes material that's actually taught | new (calc) | scheduled |
| 8 | Thu 08-27 | **Induction I** — the hypothesis *is* the engine | §6 | new (slid from Tue 08-25, one day later than originally planned, because of the 08-24 hold) |
| 9 | Fri 08-28 | **Review day** — mixed; whatever's actually landed by then across negation, pigeonhole retention, and Taylor | — | review |
| 10 | Mon 08-31 | **Induction II** — sum recurrences, factoring the IH out | §6 | new (slid from Wed 08-26) |

**Session 6 note (2026-08-20, still current):** the original plan for session 6 was
straight to nested, ε-δ-shaped negation. Session 4 found the actual remaining gap is
narrower and different — negating implications and disjunctions specifically, not the
∀/∃ flip or nesting itself. Session 6 opens with compound-predicate negation before
adding nesting, not after. **Update 2026-08-25:** this plan never got tested on 08-24
(blank work file), so it's unchanged and repeated today with new problem instances
rather than progressing to nesting.

**Schedule slip note (2026-08-25):** one hold day (08-24) pushes everything after it
back by one calendar day. Friday review days stay fixed to Friday regardless — the
slip shows up in how much new material has actually landed by then, not in moving the
review day itself.

Sessions 11–25 (sets/functions, counterexamples, sup/inf, ε-arguments, remaining
calculus repair, Phase 0 gate) get scheduled at the 08-28 review, once real
throughput is known.

---

## Open weaknesses

*Review days bias toward this list. Remove only after two clean cold retrievals at
≥7-day spacing.*

- [ ] **Quantifier negation, compound predicates (implication, De Morgan).** Bug #3's narrower descendant. Failed 2026-08-20 (Core 1c, 1e) **and again 2026-08-21** (Part 2c(i), 2c(ii)) — same two sub-errors both times. Session 6 (08-24) was meant to be the third pass but produced zero evidence (blank). Today's (08-25) repair item, fresh instances, now also mixing in a domain-restriction to guard against 08-20 (d)'s relapse.
- [ ] **Contrapositive vs. contradiction, applied.** Session 3 Core 2(a) narrated the ending as a contradiction against a nonexistent "given." Session 4 R2: not attempted. Session 5 (08-21) Part 2b: **half right** — named the technique but still didn't write why proving the contrapositive settles the original claim. Two genuine attempts, neither clean. Waiting for an open repair slot (hard cap gave 08-25's slot to compound-predicate negation).
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of building from *n*. IH never written. Not yet re-tested — block now starts 2026-08-27 (slid one day from the 08-24 hold).
- [ ] Rank / linear independence / basis / null space — definitions absent
- [ ] Σ notation: closed form vs. *n*-th term
- [ ] Arithmetic slips when moving terms across an equals sign / FOIL under time pressure, or transcribing a binomial expansion (Session 2 Core 1(b): $4xy \to 4xy^2$; Session 3 Core 2(a): "$12k\,3$" for $12k+4$ — didn't affect the final result either time, but worth slowing down on)
- [ ] Gradient stated precisely (vector of partials, steepest ascent, ⊥ level curves)

**Closed 2026-08-21, retired to `REVIEW-QUEUE.md`'s 3-day interval (not open weaknesses
anymore):**
- **Bug #1 — landing the proof.** Session 5 (08-21) Part 2a landed the closing
  contradiction sentence cleanly, third genuine attempt. One clean demonstration
  retires it per the current rules.
- **Pigeonhole — general principle stated precisely + connected across sessions.**
  Session 5 (08-21) Part 2d/3a/3b: correct condition, correct connection, full general
  proof, and original-language explanation of the finiteness requirement — the
  strongest work in the repo so far.

**Closed earlier (setup discipline, existential witness domain in $\mathbb{Z}$,
inherited from Session 3):** four clean, independent instances each — see evidence
log. Retention checks due 2026-08-22, not yet run — carried forward into whichever
session next has an open review slot.

**Off this list since Session 4:** deriving a specific pigeonhole instance (Core
2(a)/(b), a real repair of Session 3's gap) and quantifier negation over a single
atomic predicate (Core 1(a), (b), (f) clean) — both moved to the review queue.

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
| 2026-08-17 | 5 (Mon–Fri) | 5 (Day 6, calibration, Sessions 2–5, all with real evidence) | 100% |
| 2026-08-24 | 1 so far (Mon 08-24, offered) | 0 (blank — first fully-missed session since the restructure) | 0% so far, week in progress |

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

- **2026-08-25** — Housekeeping + Session 6 retry. Discovered Session 5's grading
  (`08-21-feedback.md`) was never written back into this file, `REVIEW-QUEUE.md`, or
  `progress.md`, and its promised solution file (`08-21-solution.md`) was never
  posted — all backfilled today. Session 6 (`weeks/2026-08-24/08-24-work.md`, assigned
  2026-08-24) came back entirely blank: no timing, no attempts on any of R1, the
  compound-negation repair, or either new idea. Per the no-evidence rule this is a
  hold, not a failure — built a retry (`weeks/2026-08-24/08-25.md`) with the same
  content (compound-predicate negation repair, third pass; divergence-from-negation;
  quantifier order) but entirely fresh problem instances, plus one review item
  (atomic negation, overdue since 08-21). Solutions for the unattempted 08-24
  problems posted anyway (`08-24-solution.md`), same one-day lag. Rolling horizon
  slides by one day for everything after 08-24; Friday review days stay fixed.
  Flagging for the 08-28 weekly review: this is the first fully-missed session since
  the restructure, worth a direct check-in rather than silently treating it as noise.
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
