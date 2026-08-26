# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-26 (Session 7 graded — real work through the repair block,
then time ran out. Setup discipline retired; a specific, recurring divergence-proof
obstacle identified. Session 8 built for 08-27, Core held over from Session 7.)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 8 of ~15 (Session 7 complete and graded — review/repair reached, Core did not; Session 8 built for 2026-08-27) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 10 of 14 offered (Days 1, 2, 6 + calibration + Sessions 2–5 + Session 6 retry (08-25) + Session 7 (08-26, partial); Session 6's first offering on 08-24 remains zero-evidence) |

### Immediate next action

**[Session 8 — 2026-08-27](weeks/2026-08-24/08-27.md)** is built and waiting.
**Core is held over from Session 7, not new:** Taylor's theorem and the geometric
series got zero evidence yesterday (blank from time, not from difficulty), so today
re-offers both with fresh instances (cos $x$ in place of $e^x$; $r=-\tfrac13$ in
place of $r=\tfrac12$) rather than advancing to Induction. Induction I now starts
Monday 08-31, a one-session slip.

Two review items (existential witnesses, oldest-overdue; a second re-offer of the
plain-English quantifier-meaning question, still zero clean attempts across two
tries) and one repair item (a divergence-proof construction — same specific
stopping point as 08-25's, now confirmed twice: evaluating a sign instead of
noticing $|(-1)^k|=1$ regardless of it). Work into
[`weeks/2026-08-24/08-27-work.md`](weeks/2026-08-24/08-27-work.md).

Grading context: [`weeks/2026-08-24/08-26-feedback.md`](weeks/2026-08-24/08-26-feedback.md)
(Session 7).

**What changed today (2026-08-26):** real work again through R1/R2/1(a), then the
"did not have time today" note at the top of the work file turned out to be
literal — everything from 1(b) on, including both new-material blocks, is blank.
**Setup discipline retired** — second clean cold instance at 7-day spacing.
Quantifier-order true/false construction confirmed a second time. The divergence
proof (R2) came back wrong in a specific, informative way: stuck at the exact same
step as 08-25's identical exposure (about to case-split on a sign that an absolute
value would have handled directly) — two occurrences now, named as a real repair
track rather than one-off noise. The actual repair target (plain-English
explanation) and both new-material items remain untouched — no evidence, held,
re-offered tomorrow. Today's Core was trimmed by one sub-part (Core 2(c)) to bring
session length back toward what two consecutive sessions have shown is actually
achievable in an hour.

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
| Setup discipline (state the hypothesis, not the conclusion) | Session 3 (08-19): clean 4/4. Session 7 (08-26) R1: clean again, 7 days later | **closed 2026-08-26 — two clean cold retrievals at ≥7-day spacing. Retired to `REVIEW-QUEUE.md`'s 7-day interval** |
| Existential witness domain ($\mathbb{Z}$ vs $\mathbb{N}$) | Session 3: clean in both places needed | **competent — closing, needs one more clean instance. Overdue since 08-22, still carrying forward (hard cap gave 08-26's one review slot to setup discipline instead)** |
| Injective/surjective — construct an example, prove both halves | Session 3 Core 1(a) — correct mechanics, notation fix needed | **competent (mechanics)** |
| Pigeonhole — deriving a specific finite instance | Session 4 Core 2(a), 2(b) — full, landed derivation | **competent — real repair, first clean derivation** |
| Pigeonhole — general principle stated precisely, connected across sessions | Session 5 (08-21) Part 2d/3a/3b — correct condition, correct connection, full proof | **retired 2026-08-21 — see `REVIEW-QUEUE.md`, 3-day interval. Same missed-check status as bug #1 above** |
| Quantifier negation — atomic (single ∀/∃ over one plain predicate) | Session 4 — clean 3/3 (08-20). Session 6 retry R1 (08-25) — **clean again**, second independent cold instance across a real gap | **competent, confirmed — advances to the 3-day interval in `REVIEW-QUEUE.md`** |
| Quantifier negation — compound predicates (implication, De Morgan) | Failed 08-20 (Core 1c, 1e) and 08-21 (Part 2c). Session 6 retry (08-25) §1(a)–(e) — **all five correct**, including the restriction+connective trap in (d) that had specifically caused the 08-20 relapse | **retired 2026-08-25 — third pass, clean, real repair. Moved to `REVIEW-QUEUE.md` at the 3-day interval. Minor note, not a gap: (a)'s stated *rule name* didn't match the connective present even though the answer was correct — watch whether this recurs, but (c) named the correct rule for an identical shape, so this reads as a one-off labeling slip, not confusion** |
| Contrapositive vs. contradiction, conceptual distinction | Session 3 R1 — correct, well-articulated | **competent (concept)** |
| Contrapositive vs. contradiction, applied to own proof | Session 5 (08-21) Part 2b — half right: named the technique, didn't write why proving the contrapositive settles the original claim | **gap — two genuine attempts (08-19, 08-21), neither fully clean. Not retested 08-25 (hard cap gave the day's repair slot to compound-predicate negation, which then closed) — next open repair slot goes here** |
| Negation as a proof obligation — writing $\lnot(a_n\to L)$ and describing the three proof moves | Session 6 retry (08-25) §2(a),(b) — both correct on first exposure | **competent — new skill, enters `REVIEW-QUEUE.md` at the 1-day interval per Step 7 (first-taught concepts start short regardless of the first result)** |
| Negation as a proof obligation — actually executing the divergence proof | Session 6 retry (08-25) §2(c) blank. Session 7 (08-26) R2, fresh instance ($b_n=1+(-1)^n$) — wrong, stuck at $b_{N+1}=1+(-1)^{N+1}$, about to case-split on parity instead of using $|(-1)^{N+1}|=1$ | **real gap, now two data points at the identical stopping step. Session 8's (08-27) repair item, third instance** |
| Quantifier order — determine which of ∀∃/∃∀ holds, prove the true one | Session 6 retry (08-25) §3(a) true case — correct, clean construction ($y=-x$). Session 7 (08-26) 1(a), fresh predicate ($y=x^2$) — correct again | **competent, confirmed — second clean cold instance, advances to the 3-day interval in `REVIEW-QUEUE.md`** |
| Quantifier order — disprove the false one via negation + counterexample | Session 6 retry (08-25) §3(a) false case — right strategy (correct negation, valid witness $x=1-y$), but $(1-y)+y$ computed as $0$ instead of $1$ — an arithmetic slip, not a strategy error | **partial — logged with the existing arithmetic-slips line below, not a new repair track. Watch for recurrence** |
| Quantifier statements — plain-English meaning, not symbol transliteration | Session 6 retry (08-25) §3(b) — wrong, transliteration instead of explanation. Session 7 (08-26) 1(b) — blank, not reached (time) | **gap — one wrong, one blank, zero clean attempts across two exposures. Re-offered again Session 8 (08-27), fresh predicate, in the review block** |
| $\delta$–$\varepsilon$ role-swap in continuity, conceptual consequence | Session 6 retry (08-25) §3(c) — blank, no content | **no data — carries forward, not yet re-offered (lower priority than the plain-English gap above)** |
| Bug #2 — induction never uses the hypothesis | Calibration A2 — IH never written down or used | **gap — structural. Block starts Thursday 2026-08-27** |
| Induction: reading Σ notation | Calibration A2 — read closed form as the *n*-th term, not the sum | **misconception — untested since** |
| Rank | Calibration B1 — "number of non-empty values." Incorrect | **gap — significant, deferred to Phase 1** |
| Linear independence | Calibration B1 — circular definition | **gap — deferred to Phase 1** |
| Basis, null space, rank–nullity | Calibration B1/B2 — blank | **no data, presumed gap — deferred to Phase 1** |
| Diagonalizability criteria | Calibration B4 — blank | **no data — deferred to Phase 1** |
| Arithmetic under time pressure | Calibration A2 (2 slips), D1 (1 slip), Session 6 retry (08-25) §3(a) false case (dropped a constant term) | **minor, recurring — watch it, not a dedicated repair track** |
| Chain rule, integration by parts | Calibration Section C — entirely blank, not yet re-tested since 08-21's Taylor-only redo | **NO DATA — Taylor now being taught (Session 7); chain rule/integration by parts remain untested, revisit before closing calculus repair** |
| Taylor's theorem with remainder | Calibration — blank. 08-21 timed redo — blank again. Session 7 (08-26) — not reached (time) | **taught (lesson posted), zero attempt evidence yet — held, re-offered Session 8 (08-27) with a new function ($\cos x$)** |
| Geometric series | Never tested (not on the calibration). Session 7 (08-26) — not reached (time) | **taught alongside Taylor, zero attempt evidence yet — held, re-offered Session 8 (08-27) with $r=-\tfrac13$** |
| Gradient (conceptual) | Calibration D2a — right direction, imprecise; key properties absent | **partial** |
| Eigenvectors, spectral theorem, SVD, Lagrange | Not attempted since Days 4–6 preview | **not taught yet — re-teach in Phases 1–2** |
| Probability | MATH-UA 235, A- (Fall 2024) | weak evidence, **presumed strength** |
| Applied ML | CSCI-UA 473 A, DS-UA 301 A | **strength** |

**The headline:** two of the three named bugs from the calibration are now closed
(#1 landing a proof, #3 quantifier negation including its compound-predicate
descendant). The third (#2, induction) now starts Monday 08-31, slipped one session
because calculus repair's Core still hasn't been attempted. Two narrower patterns
are now confirmed rather than single data points: mechanical quantifier manipulation
is ahead of verbal explanation of what quantifiers mean (wrong once, blank once,
zero clean attempts), and evaluating a sign explicitly instead of taking an absolute
value stalls divergence proofs specifically at the moment a term like $(-1)^k$
needs bounding (wrong twice, identical stopping point both times).

---

## Rolling horizon — next 10 sessions

*Revised 2026-08-17 from calibration results, reordered around the three named bugs.
Updated 2026-08-26: Session 7 graded (partial — Core not reached); Session 8 built,
Induction I slipped to Monday 08-31.*

| # | Date | Topic | Lesson § | Type |
|---|---|---|---|---|
| 1 | Mon 08-17 | ~~Calibration diagnostic~~ | — | ✅ done |
| 2 | Tue 08-18 | ~~Unfolding definitions; A1 by contrapositive; A4~~ | §0, §1, §3 | ✅ done |
| 3 | Wed 08-19 | ~~Setup discipline repair; injective/surjective; contradiction — √3 irrational~~ | §1, §4 | ✅ done |
| 4 | Thu 08-20 | ~~Quantifier negation drill I + pigeonhole proof~~ | §5, §8 | ✅ done |
| 5 | Fri 08-21 | ~~Review day~~ — Section C timed redo + mixed retrieval + synthesis | — | ✅ done |
| 6 | Mon 08-24 → **retried Tue 08-25** | ~~Quantifier negation drill II — compound-predicate repair (third pass), plus two new ideas: divergence proof from a negation, quantifier order~~ | §5 | ✅ **done 08-25** — 08-24 was blank; the 08-25 retry landed the repair and produced real (if partial) new-material evidence |
| 7 | Wed 08-26 | ~~Calculus repair — Taylor's theorem with remainder, geometric series~~ | new (calc) | ✅ **done 08-26 — partial.** Setup discipline retired, divergence-proof gap confirmed twice. Core (Taylor, geometric series) never reached — zero evidence, held |
| 8 | Thu 08-27 | **Calculus repair, continued — Taylor ($\cos x$), geometric series ($r=-\tfrac13$), fresh instances.** Held from Session 7, not new content. Plus: existential-witness review, a second plain-English re-offer, and the divergence-proof repair item | new (calc) | **built, pending** |
| 9 | Fri 08-28 | **Review day** — mixed; whatever's actually landed by then across negation, pigeonhole retention, Taylor/geometric series, plain-English explanation, and the divergence-proof gap | — | review |
| 10 | Mon 08-31 | **Induction I** — the hypothesis *is* the engine (slipped from 08-27; runs once Session 8's calculus material has actually been attempted) | §6 | scheduled |

**Session 6 note, now closed out:** the compound-predicate negation repair that
opened 08-20 and relapsed 08-21 finally closed clean on 08-25's retry, all five
items including the restriction+connective trap. This is real repair, not a
recognized-shape effect — the trap item (d) was specifically designed to catch the
old relapse pattern and didn't.

**Session 7 note:** review and repair got real attempts (setup discipline retired,
quantifier-order confirmed, a specific divergence-proof obstacle identified); Core
did not get attempted at all. This is not the 08-24 pattern (zero evidence on
everything) — it's partial, and the response is the same principle applied
narrowly: hold only the pieces with no evidence (Core), keep the pieces with real
evidence (retirements, the new repair track) moving forward.

**Schedule status:** one new one-session slip. Induction I moves from Thu 08-27 to
Mon 08-31 because Session 7's Core (Taylor, geometric series) was never attempted —
starting Induction before calculus repair has had one real pass would mean holding
two new topics with zero evidence at once. Everything else in the horizon shifts
by the same one session; re-priced fully at the 08-28 review alongside the
throughput question already flagged there.

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
  2026-08-25: wrong, transliteration instead of explanation. 2026-08-26: blank, not
  reached (time). Two exposures, zero clean attempts. Re-offered again Session 8
  (08-27), fresh predicate, in the review block (repair slot went to the
  divergence-proof item instead).
- [ ] **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  2026-08-25 §2(c): blank. 2026-08-26 R2 (fresh instance): wrong, stuck at the
  identical step — about to case-split on parity instead of noting $|(-1)^k|=1$
  regardless of $k$'s parity. Two occurrences, same specific stopping point.
  Session 8's (08-27) repair item.
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of
  building from *n*. IH never written. Block now starts Monday 2026-08-31 (slipped
  one session — see Rolling horizon).
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

**Closed 2026-08-26 (retired to `REVIEW-QUEUE.md`'s 7-day interval):**
- **Setup discipline (state the hypothesis, not the conclusion).** Session 3
  (08-19): clean 4/4. Session 7 (08-26) R1: clean again, exactly 7 days later —
  meets the two-clean-retrievals-at-≥7-days bar this file's own header sets.

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

**Still closing (existential witness domain — one more clean instance retires it;
overdue since 2026-08-22):** carried forward again, pulled into Session 8's (08-27)
review slot.

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
| 2026-08-24 | 3 so far (08-24, 08-25, 08-26) | 2 (08-25 retry — full; 08-26 — partial, review/repair only, Core not reached) | ~67% so far, week in progress |

At a sustained 3–4/week, the ~36-week plan stretches toward 45–55 weeks. Week
2026-08-24 opened with one fully missed day, a strong full recovery, then a partial
day where the session itself ran long relative to available time — worth weighing
at the 08-28 review alongside the still-open question of whether sessions are sized
right for the time actually available, not just whether days get missed.

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

- **2026-08-26 (grading + build)** — Session 7's work file showed real work through
  the repair block, then stopped ("did not have time today," and the file bears
  that out — everything from 1(b) on is blank). Graded in
  `weeks/2026-08-24/08-26-feedback.md`. **Setup discipline retired** — second clean
  cold instance at 7-day spacing. Quantifier-order true/false construction confirmed
  a second time, advances to the 3-day review interval. The divergence-proof
  execution skill came back wrong in a specific, now-recurring way: stuck at
  evaluating $(-1)^{N+1}$'s sign instead of using $|(-1)^{N+1}|=1$ — identical
  stopping point to 08-25's exposure, two data points, named as a real repair track
  and given Session 8's one repair slot. The actual repair target (plain-English
  quantifier meaning) and both new-material blocks (Taylor, geometric series) were
  never reached — zero evidence, held, not graded as wrong. Solutions posted to
  `weeks/2026-08-24/08-26-solution.md`. Session 8
  (`weeks/2026-08-24/08-27.md`) built: Taylor and the geometric series re-offered
  with fresh instances (holding, not advancing), Core trimmed by one sub-part to
  match observed pacing. **Induction I slips from Thu 08-27 to Mon 08-31** — new
  material doesn't start on top of calculus repair's Core still having zero
  evidence.
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
