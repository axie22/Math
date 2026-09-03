# Review Queue — spaced retrieval

> The daily run pulls items due today into the session's opening review block, and
> pushes new items when a topic is first learned.

## How it works

Every concept learned enters the queue and resurfaces at expanding intervals:

**1 day → 3 days → 7 days → 21 days → 60 days → retired**

On a **successful** cold retrieval, the item advances one interval. On a **failed**
one, it drops back to the 1-day interval *and* the topic gets added to
`STATE.md` → Open weaknesses. Retired items may still appear on review days.

**Cold means cold.** Attempt from memory with the lesson file closed. A recognized
concept is not a retrieved one, and the difference is the entire mechanism.

---

## Resolved 2026-09-03 (Session 13) — results

*Entirely blank session — the fifth in the repo's history (after 08-24, 08-27,
08-28, 09-02), and the second time two have landed back-to-back (09-02, 09-03) —
the first pair was 08-27/08-28. This one immediately follows the two strongest
sessions in the repo (08-31, 09-01), same as 09-02 did. Nothing graded as wrong;
everything held. No feedback file — nothing to grade.*

| Item | Result |
|---|---|
| Existential witness, second offering since the 08-28 pause | 🔲 **blank** — second consecutive blank in the resumed cycle (09-02, 09-03). **Per the two-blank rule, paused again** — not offered Session 14, logged as untested in `STATE.md`. |
| Divergence-proof execution (repair) | 🔲 **blank** — fourth blank exposure since the one wrong attempt (08-26). No new data either way; re-offered again, Session 14 Repair, moved to the front of the session this time. |
| Sup/inf — infimum (Core 1) and second supremum instance (Core 2) | 🔲 **blank** — second blank exposure for this material (first was 09-02 Core 2). Zero real attempts across two exposures. Not re-offered as a third identical Core problem; Session 14's synthesis approaches sup from a different angle (uniqueness) instead. |

## Resolved 2026-09-02 (Session 12) — results

*Entirely blank session — third in the repo's history (after 08-24, 08-27,
08-28), and the first since two full, strong sessions (10, 11). Nothing graded as
wrong; everything held. No feedback file — nothing to grade.*

| Item | Result |
|---|---|
| Existential witness, resuming after the 08-28 pause | 🔲 **blank** — first offering since the pause, whole session blank. One blank in this new cycle; re-offered once more, Session 13 (09-03) R1, before it would pause again. |
| Divergence-proof execution (repair) | 🔲 **blank** — first dedicated repair slot since 08-26, still no attempt. No new data either way; re-offered again, Session 13 (09-03) Repair. |
| Strong induction — binary representation (Core 1) | 🔲 **blank** — second blank exposure on the mechanism (first was 09-01, product of primes). **Per the two-blank rule, paused** — logged as untested in `STATE.md`, not offered in Session 13. |
| Sup/inf — $\varepsilon$-characterization (Core 2, first exposure) | 🔲 **blank** — first exposure of new material, whole session blank. One blank exposure is within tolerance for material taught the same day; re-offered as Session 13's actual first real attempt (infimum, new, plus a second supremum instance). |

## Due 2026-09-04 (Session 14 — Friday review)

*Friday: no new material, so this is a mixed retrieval set, not a single "due
today" list — see `weeks/2026-08-31/09-04.md` for the full session.*

| Item | Due since | Status today |
|---|---|---|
| Induction hypothesis as engine (bug #2) | 2026-09-04, 3d interval | **Session 14 R1**, fresh instance ($\sum k^3$). First retention check since the two clean closures (08-31, 09-01). |
| Contrapositive vs. contradiction, applied | 2026-09-04, 3d interval (first retired) | **Session 14 R2**, fresh predicate ($n^3+5$ even $\Rightarrow n$ odd). First retention check since the first-ever clean instance (09-01). |
| Quantifier statements — plain-English meaning | 2026-09-04, 3d interval (first retired) | **Session 14 R3**, fresh predicate ($x^2=y$). First retention check since the first-ever clean instance (09-01), the longest-open gap in the repo before that. |
| Divergence-proof execution (repair) | — | **Session 14 Repair**, fresh instance ($f_n=-2+3(-1)^n$), moved to the front of the session (testing `CURRICULUM.md` §7's position hypothesis). |
| Sup/inf — uniqueness (different angle from computing a value) | first taught 09-02, zero attempt evidence on either angle | **Session 14 Synthesis** — combines contradiction (§4) with the $\varepsilon$-part of sup's definition (§9). |
| Setup discipline (retention check) | 2026-09-02 | Not selected — carries forward. |
| Pigeonhole — general principle (retirement check) | 08-24 | Carries forward — oldest open item in the queue, one blank exposure so far (08-28). |
| Quantifier negation — compound predicates (retention check) | 08-28 | Carries forward — not yet retested at its first 3-day check. |
| Quantifier order — construct and prove true/false | 08-29 | Carries forward — not yet retested. |
| Induction — counting ($2^n$ subsets), 1d retention check | 2026-09-02 | Carries forward — not yet retested. |

**Existential witnesses removed from the "Due" rotation** as of 09-03's second
blank exposure in the resumed cycle — see "Paused / off active rotation" below.
**Strong induction** remains off rotation from 09-02, unchanged.

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 (overdue, long-stale — no urgent signal, low priority re-offer) | 1 |
| Setup discipline | §1 | 2026-08-26 | 7d | 2026-09-02 (due, not selected — hard cap; carries forward) | 2 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | **Paused 2026-09-03** — two consecutive blank offerings since the 08-28 resume (09-02, 09-03) | 1 |
| Quantifier negation — atomic case | §5 | 2026-08-31 | 7d | **2026-09-07** | 3 |
| Quantifier negation — compound predicates | §5 | 2026-08-25 | 3d | 2026-08-28 (overdue, not yet retested) | 1 (retired) |
| Bug #1 — landing | §4 | 2026-08-31 | 7d | **2026-09-07** | 2 (retired) |
| Pigeonhole — general principle | §8 | 2026-08-21 | 3d | 2026-08-24 (overdue; one blank offering 08-28, eligible for re-offer) | 1 (retired) |
| Negation as a proof obligation — definition + structure | §5 | 2026-08-25 | 1d | **Session 14 Repair slot (09-04)**, folded into the divergence-proof problem again | 1 (first taught) |
| Quantifier order — construct and prove true/false | §5 | 2026-08-26 | 3d | 2026-08-29 (overdue, not yet retested) | 2 |
| **Induction hypothesis as the engine** | §6 | 2026-09-01 | 3d | **2026-09-04** | 2 (retired) |
| Σ: running total vs. *n*-th term | §6 | 2026-08-31 | — | folded into induction's evidence — no separate check needed | — |
| **Contrapositive vs. contradiction, applied** | §4 | 2026-09-01 | 3d (first retired) | **2026-09-04** | 1 (retired) |
| **Quantifier statements — plain-English meaning** | §5 | 2026-09-01 | 3d (first retired) | **2026-09-04** | 1 (retired) |
| Induction — counting ($2^n$ subsets) | §6 | 2026-09-01 | 1d (first taught) | 2026-09-02 (due, not selected — hard cap; carries forward) | 1 |
| Sup/inf — $\varepsilon$-characterization | §9 | taught 09-02; Core attempts offered 09-02, 09-03, both blank | — | **Session 14 Synthesis (09-04)** — uniqueness of sup via contradiction, a different angle from computing a value | — |

**Existential witnesses — paused again as of 09-03.** Both offerings since the
08-28 resume (09-02, 09-03) landed inside entirely blank sessions — two
consecutive blanks per the standing rule, so it's off active rotation again,
same status as strong induction and Taylor/geometric series. Resumes only once
a real-evidence session opens a slot ahead of it.

**Quantifier order — construct and prove true/select false, advanced 1d → 3d
(2026-08-26).** Second clean cold instance. Due 2026-08-29, not yet retested —
carries forward.

---

## Paused / off active rotation

*Items with two blank exposures where neither blank came from a session with any
other real engagement — logged as untested per the standing two-blank rule, not
as demonstrated gaps. Resume once a real-evidence session opens a slot ahead of
them.*

- **Strong induction (mechanism).** First taught 09-01. Blank on both
  representations offered so far: Core 2 (09-01, product of primes) and Core 1
  (09-02, binary representation) — both inside sessions with zero other
  engagement. Paused as of 09-02's second blank exposure.
- **Existential witnesses in $\mathbb{Z}$.** Paused once already (08-28), resumed
  09-02, then blank again on both offerings since (09-02, 09-03). Paused a
  second time as of 09-03's second blank exposure in the new cycle.
- **Taylor's theorem, geometric series.** Paused since 08-27 (two consecutive
  blank Core exposures, 08-26/08-27). No date assigned, pending Alex's judgment —
  see `CURRICULUM.md` §7.

Four items now share this status — up from two on 08-28, three on 09-02. The
mechanism doing the pausing is working exactly as specified; what it's being
fed is the open question (see `CURRICULUM.md` §7).

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  08-25: blank. 08-26 (fresh instance): wrong, stopped at the identical step.
  08-27, 08-28, 09-02, 09-03: four more blank offerings, none from a session with
  any other real engagement either — still exactly one genuine attempt on record,
  now over a month old. **Re-offered again, Session 14 Repair**, fresh instance
  ($f_n=-2+3(-1)^n$), moved to the front of the session for the first time —
  testing whether its usual position (last, after review) is part of why it never
  gets reached.
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now.
- **Definition of linear independence** (B1) — deferred to Phase 1.

**Resolved 2026-09-01, removed from this list:**
- **Contrapositive narrated as contradiction, applied to own writing.** First fully
  clean instance — see "Scheduled" above for the retirement.
- **Quantifier statements — plain-English meaning, not symbol transliteration.**
  First fully clean instance after 1 wrong + 4 blanks — see "Scheduled" above.
- **Σ notation: sum of first *n* terms, not the *n*-th term** (A2). Resolved
  2026-08-31 — Session 10 Core 1 correctly distinguished $S(n)$ from the $n$-th
  term unprompted.

**Not in this list — tracked separately, not as active repair:**
- The arithmetic slip in 08-25's §3(a) false case (dropped a constant term) is
  logged in `STATE.md`'s recurring arithmetic-slips line, alongside two earlier
  instances. No new instance since.
- The δ–ε role-swap question (08-25 §3c, blank) is a first-exposure blank, low
  priority, not yet re-offered.

---

## Backlog — Days 1–6 material, un-queued

Taught before the queue existed. **Days 3, 4, and 5 (08-12, 08-13, 08-16) were never
attempted**, so most of this was never learned in the first place. Phase 2 re-teaches
it properly; nothing here is treated as known.

| Topic | Day | Attempted? |
|---|---|---|
| Partial derivatives and the gradient | 1 (08-10) | ✅ — and retained (calibration D1) |
| Directional derivatives, steepest ascent | 2 (08-11) | ✅ |
| Critical points, Hessian, 2nd-derivative test | 3 (08-12) | ❌ |
| Lagrange multipliers | 4 (08-13) | ❌ |
| Eigenvalues/eigenvectors, PCA | 5 (08-16) | ❌ |
| Diagonalization, spectral theorem, SVD | 6 (08-17) | ✅ (without Day 5's foundation) |

---

## Retired

*(none — retired items stay listed under Scheduled with their interval, per the
convention already in use above)*
