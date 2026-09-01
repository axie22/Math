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

## Resolved 2026-09-01 (Session 11) — results

*The strongest session in the repo so far — four of six items attempted, all four
clean. Full grading: `weeks/2026-08-31/09-01-feedback.md`.*

| Item | Result |
|---|---|
| Induction hypothesis as the engine (1d retention check) | ✅ **correct, second clean demonstration** (one day after 08-31's first). Advances 1d → 3d, due 2026-09-04. Not yet the ≥7d-spacing bar for full closure — watch the 3d check. |
| Contrapositive vs. contradiction, applied | ✅ **correct, first fully clean instance** — includes the "logically equivalent, same truth value" sentence that was missing every prior time (08-19, 08-21, 08-28). **Retired**, pushed to the 3d interval, due 2026-09-04. |
| Quantifier statements — plain-English meaning ($x-y=1$, worked scaffold) | ✅ **correct — closes the longest-open item in the repo.** First clean pass after 1 wrong + 4 blanks. **Retired**, pushed to the 3d interval, due 2026-09-04. |
| Induction — counting ($2^n$ subsets) | ✅ **correct, clean** — literal Phase 0 exit-gate item 2. First-taught 1d check due 2026-09-02 — not retested today (hard cap allowed one review slot, used on existential witnesses); carries forward. |
| Induction — strong induction (product of primes) | 🔲 **blank** — first attempt at this specific mechanism, everything else in the session was full. Re-offered fresh (binary representation) in Session 12 (09-02), early in the Core block. |

## Due 2026-09-02 (Session 12)

| Item | Due since | Status today |
|---|---|---|
| Existential witnesses in $\mathbb{Z}$ | 08-22, paused since 08-28, resume condition met 08-31 | **Session 12 R1**, fresh instance ($n<-200$, $n\equiv1\bmod6$) — first offering since the pause. |
| Divergence-proof execution (repair) | — | **Session 12 Repair slot**, finally open after two sessions of the quantifier item taking priority. Fresh instance ($d_n=5-2(-1)^n$), definitional part (write the negation, name the three moves) folded in. |
| Induction — counting ($2^n$ subsets), 1d retention check | 2026-09-02 | **Not today** — hard cap allowed one review item, used on existential witnesses. Carries forward. |
| Strong induction (as a mechanism) | first taught 08-31, first attempted 09-02 | **Session 12 Core 1**, fresh instance (binary representation, not primes) — first real attempt. |
| Sup/inf — $\varepsilon$-characterization | new today | **Session 12 Core 2** ($\sup\{n/(n+1)\}=1$) and Stretch ($\sup(A+B)=\sup A+\sup B$, optional). First-taught, entering the queue at the 1d interval once graded. |
| Pigeonhole — general principle (retirement check) | 08-24 | Carries forward — one blank exposure so far (08-28), eligible for a re-offer. |
| Quantifier negation — compound predicates (retention check) | 08-28 | Carries forward — not yet retested at its first 3-day check. |
| Quantifier order — construct and prove true/false | 08-29 | Carries forward — not yet retested. |

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 (overdue, long-stale — no urgent signal, low priority re-offer) | 1 |
| Setup discipline | §1 | 2026-08-26 | 7d | 2026-09-02 (due today, not selected — hard cap; carries forward) | 2 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | **Session 12 R1 (09-02)** | 1 |
| Quantifier negation — atomic case | §5 | 2026-08-31 | 7d | **2026-09-07** | 3 |
| Quantifier negation — compound predicates | §5 | 2026-08-25 | 3d | 2026-08-28 (overdue, not yet retested) | 1 (retired) |
| Bug #1 — landing | §4 | 2026-08-31 | 7d | **2026-09-07** | 2 (retired) |
| Pigeonhole — general principle | §8 | 2026-08-21 | 3d | 2026-08-24 (overdue; one blank offering 08-28, eligible for re-offer) | 1 (retired) |
| Negation as a proof obligation — definition + structure | §5 | 2026-08-25 | 1d | **Session 12 Repair slot (09-02)**, folded into the divergence-proof problem | 1 (first taught) |
| Quantifier order — construct and prove true/false | §5 | 2026-08-26 | 3d | 2026-08-29 (overdue, not yet retested) | 2 |
| **Induction hypothesis as the engine** | §6 | 2026-09-01 | 3d | **2026-09-04** | 2 (retired) |
| Σ: running total vs. *n*-th term | §6 | 2026-08-31 | — | folded into induction's evidence — no separate check needed, correct alongside Core 1 | — |
| **Contrapositive vs. contradiction, applied** | §4 | 2026-09-01 | 3d (first retired) | **2026-09-04** | 1 (retired) |
| **Quantifier statements — plain-English meaning** | §5 | 2026-09-01 | 3d (first retired) | **2026-09-04** | 1 (retired) |
| Induction — counting ($2^n$ subsets) | §6 | 2026-09-01 | 1d (first taught) | 2026-09-02 (due today, not selected — hard cap; carries forward) | 1 |
| Strong induction (mechanism) | §6 | first taught 08-31 | — | first real attempt, **Session 12 Core 1 (09-02)** | — |
| Sup/inf — $\varepsilon$-characterization | §9 (new) | — | — | first taught, **Session 12 Core 2 + Stretch (09-02)** | — |

**Induction hypothesis as the engine, contrapositive-applied, and plain-English
quantifiers — all resolved 2026-09-01.** The first advanced on its own interval
(1d→3d, second clean demonstration); the other two are first-time retirements
(one clean pass each), entering the queue fresh at the 3d interval per the standing
rule for a newly-retired item. All three due 2026-09-04 (Friday).

**Quantifier order — construct and prove true/select false, advanced 1d → 3d
(2026-08-26).** Second clean cold instance. Due 2026-08-29, not yet retested —
carries forward.

**Existential witnesses in $\mathbb{Z}$ — paused 2026-08-28, resume condition met
2026-08-31, resuming 2026-09-02.** Two consecutive blank exposures (08-27, 08-28)
triggered the pause; the resume condition (a real-evidence session ahead of it in
the queue) fired 08-31 and was confirmed again 09-01. First offering since the
pause is Session 12's R1 — a fresh instance, not 08-27's or 08-28's.

**Setup discipline and Induction — counting are both due today (2026-09-02) but
not retested** — the hard cap allows one review item per session, and existential
witnesses had the stronger claim (explicitly slated, longer-paused). Both carry
forward; whichever opens up first on a future session should take priority over a
brand-new review pull.

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  08-25: blank. 08-26 (fresh instance): wrong, stopped at the identical step.
  08-27, 08-28: both offered a third instance, both sessions blank. Sessions 10 and
  11 both used their one repair slot on the plain-English quantifier item instead.
  **Finally has its own slot: Session 12 Repair (09-02)**, fresh instance
  ($d_n=5-2(-1)^n$), with the overdue definitional part folded in.
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now.
- **Definition of linear independence** (B1) — deferred to Phase 1.

**Resolved 2026-09-01, removed from this list:**
- **Contrapositive narrated as contradiction, applied to own writing.** First fully
  clean instance — see "Scheduled" above for the retirement.
- **Quantifier statements — plain-English meaning, not symbol transliteration.**
  First fully clean instance after 1 wrong + 4 blanks — see "Scheduled" above.
- **Σ notation: sum of first *n* terms, not the *n*-th term** (A2). **Resolved
  2026-08-31** — Session 10 Core 1 correctly distinguished $S(n)$ from the $n$-th
  term unprompted.

**Not in this list — tracked separately, not as active repair:**
- The arithmetic slip in 08-25's §3(a) false case (dropped a constant term) is
  logged in `STATE.md`'s recurring arithmetic-slips line, alongside two earlier
  instances. No new instance in Session 10.
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
