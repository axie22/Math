# State — where we actually are

> Read by the daily run at the start of every session. Written back at the end.
> `CURRICULUM.md` says where we're going; this file says where we are and what the
> next two weeks look like.

**Last updated:** 2026-08-27 (Session 8 graded — `08-27-work.md` came back completely
blank, no timestamps, nothing attempted. Held, not advanced, not treated as wrong.
Taylor's theorem and the geometric series now have two consecutive blank exposures
(08-26, 08-27) and are dropped from active rotation per the standing two-blank rule,
not offered a third time back-to-back. Session 9 — Friday review — built for 08-28,
pulling the accumulated review/repair backlog into the mixed-retrieval slot Friday
exists for.)

---

## Current position

| | |
|---|---|
| **Phase** | 0 — Proof foundations & calculus repair |
| **Session** | 9 of ~15 (Session 8 complete and graded — entirely blank, zero evidence; Session 9, Friday review, built for 2026-08-28) |
| **Started** | 2026-08-17 |
| **Phase gate** | not yet attempted |
| **Days completed overall** | 10 of 15 offered (Days 1, 2, 6 + calibration + Sessions 2–5 + Session 6 retry (08-25) + Session 7 (08-26, partial); Session 6's first offering (08-24) and Session 8 (08-27) remain zero-evidence) |

### Immediate next action

**[Session 9 — 2026-08-28, Friday review](weeks/2026-08-24/08-28.md)** is built and
waiting. No new material — per curriculum, Fridays are retrieval-only. Five items,
all pulled from the backlog that's been accumulating since 08-22: existential
witness (retirement check, fresh instance), contrapositive-vs-contradiction applied
(the actual "why does this establish the claim" gap, not just the technique — open
since 08-19), plain-English quantifier meaning (third exposure, fresh predicate —
if this comes back anything but clean it becomes a dedicated repair item, not a
fourth re-offer), a third divergence-proof instance with the negation-as-obligation
definitional check folded in, and a synthesis problem connecting pigeonhole to
formal existential statements (which doubles as pigeonhole's retirement check).
Bug #1's retirement check is the one backlog item that didn't fit — next in line.
Work into [`weeks/2026-08-24/08-28-work.md`](weeks/2026-08-24/08-28-work.md).

**Taylor's theorem and the geometric series are paused, not in today's session.**
Two consecutive blank exposures now (08-26: not reached, time; 08-27: session not
attempted at all) — per the standing two-blank rule this is a time/engagement
signal, not a knowledge gap, so they're dropped from active rotation rather than
offered a third time immediately. They come back in a normal Monday–Thursday
session once Induction I is under way, not automatically next — see Evidence log
below and the proposed amendment in `CURRICULUM.md` §7.

**What changed today (2026-08-27):** `08-27-work.md` came back completely blank —
no timestamps, no partial attempts anywhere, not even the review block. This is not
"ran out of time partway through" (that was 08-26's pattern); this is the session
not having been opened. Graded per the standing rule for an empty work file:
assume nothing mastered, default to hold, note it without nagging, move on. No
feedback file was written (nothing to grade). Session 9 (Friday review) absorbs the
overdue review/repair backlog that Session 8 was supposed to touch, since none of
it is new material and Friday is built exactly for this.

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
| Taylor's theorem with remainder | Calibration — blank. 08-21 timed redo — blank again. Session 7 (08-26) — not reached (time). Session 8 (08-27) — not reached (session not attempted) | **untested, four blank exposures now. Two consecutive blanks in the Core slot specifically (08-26, 08-27) — per the standing rule, dropped from active rotation rather than re-offered a third time immediately. Not a knowledge verdict; genuinely no attempt evidence exists either way. Flagged in `CURRICULUM.md` §7 as a possible sizing/sequencing problem, not just a pacing one** |
| Geometric series | Never tested (not on the calibration). Session 7 (08-26) — not reached (time). Session 8 (08-27) — not reached (session not attempted) | **untested, two blank exposures, both in the Core slot. Dropped from active rotation alongside Taylor per the same rule — same status, same reasoning** |
| Gradient (conceptual) | Calibration D2a — right direction, imprecise; key properties absent | **partial** |
| Eigenvectors, spectral theorem, SVD, Lagrange | Not attempted since Days 4–6 preview | **not taught yet — re-teach in Phases 1–2** |
| Probability | MATH-UA 235, A- (Fall 2024) | weak evidence, **presumed strength** |
| Applied ML | CSCI-UA 473 A, DS-UA 301 A | **strength** |

**The headline:** two of the three named bugs from the calibration are now closed
(#1 landing a proof, #3 quantifier negation including its compound-predicate
descendant). The third (#2, induction) still starts Monday 08-31. Two narrower
patterns are now confirmed rather than single data points: mechanical quantifier
manipulation is ahead of verbal explanation of what quantifiers mean (wrong once,
blank twice, zero clean attempts across three exposures), and evaluating a sign
explicitly instead of taking an absolute value stalls divergence proofs specifically
at the moment a term like $(-1)^k$ needs bounding (wrong twice, identical stopping
point both times, third instance built for 08-28). A third pattern is now visible at
the session level rather than the skill level: two of the last five offered
sessions (08-24, 08-27) came back entirely blank rather than partially done — this
looks less like specific material being hard and more like a scheduling/engagement
question worth naming directly rather than working around silently (see
`CURRICULUM.md` §7 and the throughput table below).

---

## Rolling horizon — next 10 sessions

*Revised 2026-08-17 from calibration results, reordered around the three named bugs.
Updated 2026-08-27: Session 8 graded (entirely blank); Session 9 (Friday review)
built for 08-28, pulling forward the review/repair backlog. Taylor and geometric
series paused (two consecutive blanks), not rescheduled to a specific date yet —
see the note below the table.*

| # | Date | Topic | Lesson § | Type |
|---|---|---|---|---|
| 1 | Mon 08-17 | ~~Calibration diagnostic~~ | — | ✅ done |
| 2 | Tue 08-18 | ~~Unfolding definitions; A1 by contrapositive; A4~~ | §0, §1, §3 | ✅ done |
| 3 | Wed 08-19 | ~~Setup discipline repair; injective/surjective; contradiction — √3 irrational~~ | §1, §4 | ✅ done |
| 4 | Thu 08-20 | ~~Quantifier negation drill I + pigeonhole proof~~ | §5, §8 | ✅ done |
| 5 | Fri 08-21 | ~~Review day~~ — Section C timed redo + mixed retrieval + synthesis | — | ✅ done |
| 6 | Mon 08-24 → **retried Tue 08-25** | ~~Quantifier negation drill II — compound-predicate repair (third pass), plus two new ideas: divergence proof from a negation, quantifier order~~ | §5 | ✅ **done 08-25** — 08-24 was blank; the 08-25 retry landed the repair and produced real (if partial) new-material evidence |
| 7 | Wed 08-26 | ~~Calculus repair — Taylor's theorem with remainder, geometric series~~ | new (calc) | ✅ **done 08-26 — partial.** Setup discipline retired, divergence-proof gap confirmed twice. Core (Taylor, geometric series) never reached — zero evidence, held |
| 8 | Thu 08-27 | ~~Calculus repair, continued — Taylor ($\cos x$), geometric series ($r=-\tfrac13$)~~ | new (calc) | ❌ **entirely blank — no attempt.** Zero evidence on everything, including review/repair. Not retried with a same-day-style redo (unlike 08-24→08-25) because 08-28 is Friday regardless; its content folds into Session 9 instead |
| 9 | Fri 08-28 | **Review day (built).** Existential witness, contrapositive-vs-contradiction applied, plain-English quantifiers (3rd try), divergence proof (3rd instance) + negation-as-obligation definitional check, pigeonhole+existential synthesis | — | **built, pending** |
| 10 | Mon 08-31 | **Induction I** — the hypothesis *is* the engine | §6 | scheduled, unchanged |

**Taylor's theorem / geometric series — not on this table with a date.** Two
consecutive blanks in the Core slot (08-26, 08-27) means they're paused per the
standing rule rather than assigned a fixed next date. They resume in the first
Monday–Thursday session after Induction I has had at least one real attempt,
unless the 09-04 monthly-ish review decides the calculus-repair approach itself
needs to change first (see `CURRICULUM.md` §7 amendment below).

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

**Session 8 note:** entirely blank — the second such session in five offered
(08-24 was the first). Graded per the no-work rule: hold, don't advance, note
without nagging. Because none of Session 8's content was new (it was itself a
held-over repeat of Session 7's Core plus review/repair items), nothing here
needed re-teaching — it simply moves into Friday's review, which draws from
exactly this kind of backlog by design.

**Schedule status:** Induction I stays at Mon 08-31, unchanged from the 08-26
plan — it doesn't need calculus repair's Core to have succeeded first, only to not
be actively contending for the same session, and pausing Taylor/geometric series
(rather than attempting them a third time immediately) clears that. Calculus
repair itself doesn't get a new date yet; it resumes once Induction I has had a
real pass, or sooner if the 08-28 review decides the material needs a different
approach rather than just another attempt. Full re-pricing, including whether
5 sessions/week is still the right planning assumption after two blank sessions
in one week, happens at the 08-28 weekly review below.

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
  Not retested 08-25 or 08-27 (08-27 was a full blank) — **Session 9's (08-28) Item
  2, finally back in an open slot.**
- [ ] **Quantifier statements — plain-English meaning, not symbol transliteration.**
  2026-08-25: wrong, transliteration instead of explanation. 2026-08-26: blank, not
  reached (time). 2026-08-27: blank, session not attempted at all. Three exposures,
  zero clean attempts. **Session 9's (08-28) Item 3, fresh predicate** — if this
  comes back anything but clean, it stops being a re-offer and becomes a named
  repair item with the hard cap's dedicated slot, not a fourth casual re-ask.
- [ ] **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  2026-08-25 §2(c): blank. 2026-08-26 R2 (fresh instance): wrong, stuck at the
  identical step — about to case-split on parity instead of noting $|(-1)^k|=1$
  regardless of $k$'s parity. 2026-08-27: blank (session not attempted, third
  instance never reached). Still only one genuine wrong attempt on record.
  **Session 9's (08-28) Item 4, third instance**, now paired with the
  negation-as-obligation definitional check that's also been overdue since 08-26.
- [ ] **Bug #2 — induction without an engine.** Verifying at *n+1* instead of
  building from *n*. IH never written. Block starts Monday 2026-08-31.
- [ ] **Taylor's theorem / geometric series — paused after two consecutive blank
  Core exposures (08-26, 08-27).** Not a demonstrated gap (zero attempt evidence
  either way) but flagged because it's now four total blank exposures for Taylor
  across the whole curriculum (calibration, 08-21 redo, 08-26, 08-27). Not
  re-offered until Induction I has had a real pass; see the proposed amendment in
  `CURRICULUM.md` §7.
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
overdue since 2026-08-22):** carried forward again — 08-27's offer went unattempted,
**pulled into Session 9's (08-28) Item 1** with a fresh instance.

**Pigeonhole — general principle, retirement-interval check (overdue since 08-24):**
folded into Session 9's (08-28) Item 5 as a synthesis problem rather than a bare
retest, since it connects naturally to today's existential-statement rigor.

**Bug #1 — landing, retirement-interval check (overdue since 08-24):** still the
one backlog item that didn't fit Session 9 — next in line, most likely Monday or
next Friday.

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
| 2026-08-24 | 4 so far (08-24, 08-25, 08-26, 08-27) | 2 (08-25 retry — full; 08-26 — partial, review/repair only, Core not reached) | 50% so far, 08-28 still to come |

At a sustained 3–4/week, the ~36-week plan stretches toward 45–55 weeks. Week
2026-08-24 has now produced two entirely blank sessions out of four offered
(08-24, 08-27) alongside one full completion (08-25) and one partial (08-26) — the
worst week yet by completion rate, even though every session that *did* get real
attempts produced real evidence and real progress. This is no longer a single
missed-day artifact; it's two data points in one week. Addressed directly in the
08-28 weekly review below rather than deferred again.

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

## Weekly review — 2026-08-28 (Friday)

*Per `CURRICULUM.md` §8: written when building the Friday session, not after
grading it — Session 9 (08-28) is what triggers this.*

**On plan?** Mechanically yes — still Phase 0, session 9 of ~15, on the sequence
`CURRICULUM.md` lays out. But the honest read of this week is worse than "on plan."
Week 2026-08-24 offered four sessions before today and produced two entirely blank
ones (08-24, 08-27) against one full completion (08-25) and one partial (08-26).
That's the lowest completion rate of any week so far, and unlike 08-24 (which read
as a single missed day with a clean recovery the next day), 08-27's blank has no
comparably clean explanation — it isn't paired with a same-day-style retry the way
08-24 was, because the calendar put a Friday next rather than another weekday.
Nothing here changes the phase or the gate; it changes how much confidence to put
in the ~15-session estimate for finishing Phase 0.

**Amendments in `CURRICULUM.md` §7 to accept?** Not this week — deferring to Alex's
judgment per the file's own rule, as always. A new amendment is appended below
rather than acted on: calculus repair's Core (Taylor, geometric series) has now
produced zero attempt evidence across four total exposures (calibration, the 08-21
redo, and both of its Core offerings on 08-26 and 08-27), which is different from
"blank because a session ran long" — it's blank on *every* occasion it's been
offered, including a session where nothing else was attempted either. Worth
Alex's judgment on whether the material, its placement in the session, or
something about calculus repair specifically needs to change, rather than
continuing to re-offer it and treating each blank as independent. The
throughput re-pricing question (3–4/week vs. 5/week), flagged as open since
08-21, is now sharper: two full weeks of post-restructure data say 3/5 and 2/4 —
consistent with 3–4/week being the real number, not 5. Not changing the plan
unilaterally; naming it plainly so the re-pricing decision isn't deferred a third
time.

**Is the review queue backing up?** Yes, further. As of today, six items have been
simultaneously overdue at some point this week (existential witnesses, Bug #1,
pigeonhole, negation-as-obligation, plus the plain-English and divergence-proof
repair items that don't formally live in the queue but function the same way).
Today's session clears four of them at once (existential witness, plain-English,
divergence-proof + its definitional check, pigeonhole via the synthesis problem);
Bug #1 remains the one item still waiting, now overdue since 08-24 — four days,
soon five. If Bug #1 is still waiting after Monday's session, that becomes worth a
direct callout rather than continued silent carry-forward.

---

## Changelog

- **2026-08-27 (grading + build)** — Session 8's work file (`08-27-work.md`) came
  back completely blank — no timestamps, no attempts anywhere, not even the review
  block. Graded per the no-work rule: assume nothing mastered, hold, don't
  advance, note without nagging. No feedback file written (nothing to grade).
  Solutions posted to `weeks/2026-08-24/08-27-solution.md` per the standing
  one-day lag, regardless of whether the problems were attempted. **Taylor's
  theorem and the geometric series now have two consecutive blank Core exposures
  (08-26, 08-27)** — per the standing two-blank rule, dropped from active
  rotation rather than offered a third time immediately; flagged in
  `CURRICULUM.md` §7. Session 9 (`weeks/2026-08-24/08-28.md`), Friday review,
  built: no new material, five items pulled from the accumulated backlog
  (existential witness, contrapositive-vs-contradiction applied, plain-English
  quantifiers third try, divergence proof third instance with the
  negation-as-obligation check folded in, and a pigeonhole+existential synthesis
  problem). Bug #1's retirement check is the one backlog item still waiting.
  Weekly review written (see above): this week's completion rate is the lowest
  yet (2 of 4 sessions before today), and the throughput and calculus-repair
  amendments are both sharpened rather than deferred again.
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
