# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-25 (Session 6 graded — real work arrived; compound-predicate
negation repair closed. Session 7 built for 08-26.)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 7 of ~15 (Session 6 complete and graded; Session 7 built for 2026-08-26) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 9 of 13 offered (Days 1, 2, 6 + calibration + Sessions 2–5 + Session 6 retry (08-25); Session 6's first offering on 08-24 remains zero-evidence) |

### Immediate next action

**[Session 7 — 2026-08-26](weeks/2026-08-24/08-26.md)** is built and waiting: the
first genuinely new material since Session 5, moving off compound-predicate negation
now that it's closed. Two new ideas, both calculus (Taylor's theorem with the
Lagrange remainder, geometric series) — the two items that came back blank on both
the calibration and the 08-21 timed redo, so per the rolling horizon they've
graduated from "tested" to "taught." A short new lesson is posted at
[`lessons/calculus-repair.md`](lessons/calculus-repair.md).

One review item (setup discipline, oldest-overdue), one re-offer of yesterday's
blank divergence-proof construction (fresh instance, per the no-evidence rule), and
one repair item (plain-English explanation of quantifier statements — new gap found
today, see below). Work into
[`weeks/2026-08-24/08-26-work.md`](weeks/2026-08-24/08-26-work.md).

Grading context: [`weeks/2026-08-24/08-25-feedback.md`](weeks/2026-08-24/08-25-feedback.md)
(Session 6 retry, the first real work since Session 5).

**What changed today (2026-08-25):** the 08-24/08-25 work file, blank yesterday, came
back with real, substantial work overnight. Graded below. Headline: **compound-
predicate negation — the item that failed 08-20 and 08-21 — is now clean on all five
items.** Closed, retired from active repair. Two new gaps surfaced in today's brand-
new material (quantifier order): an arithmetic slip in an otherwise-correct
counterexample construction, and a more interesting one — the ability to manipulate
quantifiers correctly is not the same skill as explaining what they mean in plain
English, and the latter came back as symbol transliteration rather than substance.
That becomes tomorrow's repair item. Two problems (the actual divergence-proof
construction, and the δ–ε role-swap question) came back blank on their first
exposure — normal for genuinely new material, re-offered per the no-evidence rule.

---

## Evidence log

*Observed work in this repo is strong evidence; transcript grades are weak evidence
(old, and about a different kind of task). Updated 2026-08-25 from Session 6 retry's
real grading.*

| Skill | Evidence | Verdict |
|---|---|---|
| Negating an implication (P⟹Q to P ∧ ¬Q) | Calibration A1 — done correctly. Session 4 Core 1(c) — failed fresh; Core 2(a) — correct but on a memorized shape. Session 6 retry (08-25) §1(a),(c),(d) — **correct three more times**, including the four-move restriction+connective trap in (d) | **closed — see compound-predicate negation below, same underlying skill** |
| Partial derivatives | Calibration D1 — both partials correct, 8 days after Day 1 | **competent** |
| Unfolding a definition and computing | Session 2 Core 1 — substitution mechanics correct in all 3 problems (a, b, c) | **competent** |
| Completing a proof after setting it up | Session 5 (08-21) Part 2a — landed it, third attempt | **retired 2026-08-21 — see `REVIEW-QUEUE.md`, 3-day interval. First retention check due 08-24, missed (blank session); next check whenever a review slot opens** |
| Setup discipline (state the hypothesis, not the conclusion) | Session 3: clean 4/4 | **competent — closing, needs one more clean instance at ≥7-day spacing. Overdue since 08-22; pulled into Session 7's (08-26) review slot** |
| Existential witness domain ($\mathbb{Z}$ vs $\mathbb{N}$) | Session 3: clean in both places needed | **competent — closing, needs one more clean instance. Overdue since 08-22, still carrying forward (hard cap gave 08-26's one review slot to setup discipline instead)** |
| Injective/surjective — construct an example, prove both halves | Session 3 Core 1(a) — correct mechanics, notation fix needed | **competent (mechanics)** |
| Pigeonhole — deriving a specific finite instance | Session 4 Core 2(a), 2(b) — full, landed derivation | **competent — real repair, first clean derivation** |
| Pigeonhole — general principle stated precisely, connected across sessions | Session 5 (08-21) Part 2d/3a/3b — correct condition, correct connection, full proof | **retired 2026-08-21 — see `REVIEW-QUEUE.md`, 3-day interval. Same missed-check status as bug #1 above** |
| Quantifier negation — atomic (single ∀/∃ over one plain predicate) | Session 4 — clean 3/3 (08-20). Session 6 retry R1 (08-25) — **clean again**, second independent cold instance across a real gap | **competent, confirmed — advances to the 3-day interval in `REVIEW-QUEUE.md`** |
| Quantifier negation — compound predicates (implication, De Morgan) | Failed 08-20 (Core 1c, 1e) and 08-21 (Part 2c). Session 6 retry (08-25) §1(a)–(e) — **all five correct**, including the restriction+connective trap in (d) that had specifically caused the 08-20 relapse | **retired 2026-08-25 — third pass, clean, real repair. Moved to `REVIEW-QUEUE.md` at the 3-day interval. Minor note, not a gap: (a)'s stated *rule name* didn't match the connective present even though the answer was correct — watch whether this recurs, but (c) named the correct rule for an identical shape, so this reads as a one-off labeling slip, not confusion** |
| Contrapositive vs. contradiction, conceptual distinction | Session 3 R1 — correct, well-articulated | **competent (concept)** |
| Contrapositive vs. contradiction, applied to own proof | Session 5 (08-21) Part 2b — half right: named the technique, didn't write why proving the contrapositive settles the original claim | **gap — two genuine attempts (08-19, 08-21), neither fully clean. Not retested 08-25 (hard cap gave the day's repair slot to compound-predicate negation, which then closed) — next open repair slot goes here** |
| Negation as a proof obligation — writing $\lnot(a_n\to L)$ and describing the three proof moves | Session 6 retry (08-25) §2(a),(b) — both correct on first exposure | **competent — new skill, enters `REVIEW-QUEUE.md` at the 1-day interval per Step 7 (first-taught concepts start short regardless of the first result)** |
| Negation as a proof obligation — actually executing the divergence proof | Session 6 retry (08-25) §2(c) blank ("not sure"), §2(d) blank | **no data yet — first exposure to *doing* the construction, not just describing it. Re-offered once, compact single instance, in Session 7 (08-26)** |
| Quantifier order — determine which of ∀∃/∃∀ holds, prove the true one | Session 6 retry (08-25) §3(a) true case — correct, clean construction ($y=-x$) | **competent — new skill, first clean instance** |
| Quantifier order — disprove the false one via negation + counterexample | Session 6 retry (08-25) §3(a) false case — right strategy (correct negation, valid witness $x=1-y$), but $(1-y)+y$ computed as $0$ instead of $1$ — an arithmetic slip, not a strategy error | **partial — logged with the existing arithmetic-slips line below, not a new repair track. Watch for recurrence** |
| Quantifier statements — plain-English meaning, not symbol transliteration | Session 6 retry (08-25) §3(b) — answered "for all x there exists a y" instead of stating what the statement asserts about the reals (additive inverses) | **new gap — first exposure, one data point. Becomes Session 7's (08-26) repair item** |
| $\delta$–$\varepsilon$ role-swap in continuity, conceptual consequence | Session 6 retry (08-25) §3(c) — blank, no content | **no data — carries forward, not yet re-offered (lower priority than the plain-English gap above)** |
| Bug #2 — induction never uses the hypothesis | Calibration A2 — IH never written down or used | **gap — structural. Block starts Thursday 2026-08-27** |
| Induction: reading Σ notation | Calibration A2 — read closed form as the *n*-th term, not the sum | **misconception — untested since** |
| Rank | Calibration B1 — "number of non-empty values." Incorrect | **gap — significant, deferred to Phase 1** |
| Linear independence | Calibration B1 — circular definition | **gap — deferred to Phase 1** |
| Basis, null space, rank–nullity | Calibration B1/B2 — blank | **no data, presumed gap — deferred to Phase 1** |
| Diagonalizability criteria | Calibration B4 — blank | **no data — deferred to Phase 1** |
| Arithmetic under time pressure | Calibration A2 (2 slips), D1 (1 slip), Session 6 retry (08-25) §3(a) false case (dropped a constant term) | **minor, recurring — watch it, not a dedicated repair track** |
| Chain rule, integration by parts | Calibration Section C — entirely blank, not yet re-tested since 08-21's Taylor-only redo | **NO DATA — Taylor now being taught (Session 7); chain rule/integration by parts remain untested, revisit before closing calculus repair** |
| Taylor's theorem with remainder | Calibration — blank. 08-21 timed redo — blank again | **moved from tested to taught — Session 7 (08-26) is the first real lesson** |
| Geometric series | Never tested (not on the calibration) | **taught alongside Taylor in Session 7 (08-26), per the calc-repair list in `CURRICULUM.md` §5** |
| Gradient (conceptual) | Calibration D2a — right direction, imprecise; key properties absent | **partial** |
| Eigenvectors, spectral theorem, SVD, Lagrange | Not attempted since Days 4–6 preview | **not taught yet — re-teach in Phases 1–2** |
| Probability | MATH-UA 235, A- (Fall 2024) | weak evidence, **presumed strength** |
| Applied ML | CSCI-UA 473 A, DS-UA 301 A | **strength** |

**The headline:** two of the three named bugs from the calibration are now closed
(#1 landing a proof, #3 quantifier negation including its compound-predicate
descendant). The third (#2, induction) starts Thursday. A new, narrower pattern is
emerging in today's data: mechanical quantifier manipulation is ahead of verbal
explanation of what quantifiers mean — worth watching whether this recurs before
treating it as a real, separate weakness rather than one data point.

---

## Rolling horizon — next 10 sessions

*Revised 2026-08-17 from calibration results, reordered around the three named bugs.
Updated 2026-08-25: Session 6 (both attempts) complete and graded; Session 7 built.*

| # | Date | Topic | Lesson § | Type |
|---|---|---|---|---|
| 1 | Mon 08-17 | ~~Calibration diagnostic~~ | — | ✅ done |
| 2 | Tue 08-18 | ~~Unfolding definitions; A1 by contrapositive; A4~~ | §0, §1, §3 | ✅ done |
| 3 | Wed 08-19 | ~~Setup discipline repair; injective/surjective; contradiction — √3 irrational~~ | §1, §4 | ✅ done |
| 4 | Thu 08-20 | ~~Quantifier negation drill I + pigeonhole proof~~ | §5, §8 | ✅ done |
| 5 | Fri 08-21 | ~~Review day~~ — Section C timed redo + mixed retrieval + synthesis | — | ✅ done |
| 6 | Mon 08-24 → **retried Tue 08-25** | ~~Quantifier negation drill II — compound-predicate repair (third pass), plus two new ideas: divergence proof from a negation, quantifier order~~ | §5 | ✅ **done 08-25** — 08-24 was blank; the 08-25 retry landed the repair and produced real (if partial) new-material evidence |
| 7 | Wed 08-26 | **Calculus repair — Taylor's theorem with remainder, geometric series.** Two new ideas, both moved from tested to taught since both came back blank twice. Plus: setup-discipline review, a re-offered divergence-proof construction, and the plain-English repair item | new (calc) | **built, pending** |
| 8 | Thu 08-27 | **Induction I** — the hypothesis *is* the engine | §6 | scheduled |
| 9 | Fri 08-28 | **Review day** — mixed; whatever's actually landed by then across negation, pigeonhole retention, Taylor, and the new plain-English-explanation item | — | review |
| 10 | Mon 08-31 | **Induction II** — sum recurrences, factoring the IH out | §6 | scheduled |

**Session 6 note, now closed out:** the compound-predicate negation repair that
opened 08-20 and relapsed 08-21 finally closed clean on 08-25's retry, all five
items including the restriction+connective trap. This is real repair, not a
recognized-shape effect — the trap item (d) was specifically designed to catch the
old relapse pattern and didn't.

**Schedule status:** no further slip. One hold day (08-24) still pushes everything
after it back by one calendar day relative to the original plan, but that slip is
now fully absorbed — Session 7 runs on 08-26 as the (already one-day-slid) schedule
intended.

Sessions 11–25 (sets/functions, counterexamples, sup/inf, ε-arguments, remaining
calculus repair, Phase 0 gate) get scheduled at the 08-28 review, once real
throughput is known.

---

## Open weaknesses

*Review days bias toward this list. Remove only after two clean cold retrievals at
≥7-day spacing.*

- [ ] **Contrapositive vs. contradiction, applied.** Session 3 Core 2(a) narrated the
  ending as a contradiction against a nonexistent "given." Session 5 (08-21) Part 2b:
  half right — named the technique but still didn't write why proving the
  contrapositive settles the original claim. Two genuine attempts, neither clean.
  Not retested 08-25 (repair slot went to compound-predicate negation, which then
  closed) — next open repair slot goes here.
- [ ] **Quantifier statements — plain-English meaning, not symbol transliteration.**
  New 2026-08-25. §3(b) answered "for all x there exists a y" instead of stating
  what the statement asserts about the mathematical objects (additive inverses).
  One data point — today's repair item (Session 7, 08-26), fresh predicate.
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of
  building from *n*. IH never written. Block starts Thursday 2026-08-27.
- [ ] Rank / linear independence / basis / null space — definitions absent, deferred
  to Phase 1.
- [ ] Σ notation: closed form vs. *n*-th term — untested since the calibration.
- [ ] Arithmetic slips when moving terms across an equals sign, FOIL under time
  pressure, or dropping a constant term mid-simplification (Session 2 Core 1(b);
  Session 3 Core 2(a); Session 6 retry (08-25) §3(a) false case — $(1-y)+y$
  computed as $0$ instead of $1$). Three instances now across three weeks — still
  minor individually, worth a direct one-line callout if a fourth shows up.
- [ ] Gradient stated precisely (vector of partials, steepest ascent, ⊥ level curves).
- [ ] Chain rule, integration by parts — blank on the calibration, never re-tested
  since (08-21's redo covered Taylor only). Revisit before Phase 0's calculus repair
  is considered closed.

**Closed 2026-08-25 (real repair, retired to `REVIEW-QUEUE.md`'s 3-day interval —
not open weaknesses anymore):**
- **Quantifier negation, compound predicates (implication, De Morgan).** Failed
  08-20 and 08-21, identical two sub-errors both times. Session 6 retry (08-25):
  all five items correct, including the restriction+connective trap that had
  specifically caused the earlier relapse. Third pass, clean.

**Closed 2026-08-21 (retired earlier, unchanged):**
- **Bug #1 — landing the proof.** Session 5 (08-21) Part 2a.
- **Pigeonhole — general principle stated precisely + connected across sessions.**
  Session 5 (08-21) Part 2d/3a/3b.

**Closed earlier (setup discipline, existential witness domain — both "closing," one
more clean instance retires them; both overdue since 2026-08-22):** carried forward,
setup discipline pulled into Session 7's (08-26) one review slot.

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
| 2026-08-24 | 2 so far (08-24, 08-25) | 1 (08-25 retry — real, substantial work) | 50% so far, week in progress |

At a sustained 3–4/week, the ~36-week plan stretches toward 45–55 weeks. Week
2026-08-24 opened with one fully missed day and then a strong recovery — worth
weighing at the 08-28 review alongside the still-open question of whether the
earlier misses were circumstantial.

---

## Weekly review — 2026-08-21 (Friday)

*Per `CURRICULUM.md` §8: written when building the Friday session, not after grading
it — Session 5 (08-21) is what triggers this. Unchanged since 08-21; the next weekly
review is due 2026-08-28.*

**On plan?** Yes, mechanically — still Phase 0, session 5 of ~25 at the time, on the
sequence `CURRICULUM.md` and the rolling horizon lay out. Session 4 was the first
session where the *specific* skill being taught came back with a precise,
diagnosable split rather than either a clean pass or diffuse noise — the second time
in a row a "new topic" session produced a narrow, named finding (pigeonhole was the
first, Session 3→4).

**Amendments in `CURRICULUM.md` §7 to accept?** Not this week — deferring to Alex's
judgment per the file's own rule. Two items in §7 remain genuinely open: Section C
(calculus) sizing, now partially resolved (Taylor is being taught rather than
retested as of Session 7); and the throughput re-pricing question (3–4/week vs.
5/week), still open and worth a direct look at 08-28 with two full weeks of
post-restructure data instead of one.

**Is the review queue backing up?** Yes, mechanically, from the 08-24 blank session
— five items were simultaneously overdue as of 08-25 (atomic negation, two
retirement checks, setup discipline, existential witnesses). The hard cap clears one
a day; 08-25 cleared atomic negation via R1, 08-26 clears setup discipline. This is
a direct, traceable consequence of one missed day, not the queue mechanism itself
breaking.

---

## Changelog

- **2026-08-25 (grading + build)** — Session 6 retry's work file, blank the day
  before, came back with real, substantial work. Graded in
  `weeks/2026-08-24/08-25-feedback.md`. **Compound-predicate negation, failed 08-20
  and 08-21, closed clean on all five items** — retired to the 3-day review
  interval. Atomic quantifier negation confirmed competent on a second clean cold
  instance. In the new material (negation-as-proof-obligation, quantifier order):
  the definitional/setup parts landed clean, but the actual divergence-proof
  construction came back blank (first exposure, re-offered), a quantifier-order
  counterexample had a correct strategy undone by an arithmetic slip (logged, not a
  new repair track), and a genuinely new gap surfaced — answering "what does this
  quantifier statement assert" with a symbol transliteration rather than the
  statement's actual mathematical content. That becomes Session 7's repair item.
  Solutions posted to `weeks/2026-08-24/08-25-solution.md`. Session 7
  (`weeks/2026-08-24/08-26.md`) built: Taylor's theorem with remainder and the
  geometric series, both moved from tested to taught per the standing rule (two
  blanks on the calibration and the 08-21 redo); new lesson at
  `lessons/calculus-repair.md`. One review item (setup discipline, oldest overdue),
  one re-offered divergence-proof construction, one repair item (plain-English
  explanation). Induction still starts Thursday 08-27, unchanged.
- **2026-08-25 (housekeeping, earlier same day)** — Discovered Session 5's grading
  (`08-21-feedback.md`) had never been written back into this file, `REVIEW-QUEUE.md`,
  or `progress.md`, and its promised solution file was never posted — all backfilled.
  Session 6 (`weeks/2026-08-24/08-24-work.md`, assigned 2026-08-24) had come back
  entirely blank — built a retry (`weeks/2026-08-24/08-25.md`) with the same content
  but entirely fresh problem instances. That retry is what produced the real grading
  above, later the same day.
- **2026-08-20** — Session 4 graded, Session 5 (Friday review) built. Quantifier
  negation split cleanly: atomic clean 3/3, compound-predicate negation failed both
  times despite the rule being printed directly in the problem file. Pigeonhole
  showed real repair on the specific-case derivation but not yet the general
  principle. Full grading in `weeks/2026-08-17/08-20-feedback.md`.
- **2026-08-19** — Session 3 graded, Session 4 built. Setup discipline and
  existential-witness domain both closed clean 4/4. Injective/surjective got its
  first real data. Bug #1 relapsed on a longer proof than the one it looked fixed
  on. Full grading in `weeks/2026-08-17/08-19-feedback.md`.
- **2026-08-18** — Session 2 graded, Session 3 built. Bug #1 showed real
  improvement. Setup discipline and existential-witness domain identified as new
  mechanical issues. Full grading in `weeks/2026-08-17/08-18-feedback.md`.
- **2026-08-17** — Session 2 built. Phase 0 lesson written
  (`lessons/proof-foundations.md`). `START-HERE.md` added as the repo entry point.
- **2026-08-17** — Calibration graded. Evidence log populated with real data for the
  first time. Horizon reordered around the three named bugs. Amendments proposed to
  `CURRICULUM.md` §7 (Phase 0: 3→5 weeks).
- **2026-08-17** — Restructured. Added `CURRICULUM.md`, this file, `REVIEW-QUEUE.md`,
  `RUN-PROMPT.md`. Retargeted from "ML/AI + aerospace" to "ML research depth + proof
  maturity." Inserted Phase 0 (proofs) ahead of everything.
- **2026-08-10** — Started daily practice.
