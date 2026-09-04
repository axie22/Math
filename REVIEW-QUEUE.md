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

## Resolved 2026-09-04 (Session 14) — results

*Entirely blank session — the sixth in the repo's history (after 08-24, 08-27,
08-28, 09-02, 09-03), and the first time three have landed back-to-back (09-02,
09-03, 09-04). This one immediately follows the two strongest sessions in the
repo (08-31, 09-01). Nothing graded as wrong; everything held. No feedback file —
nothing to grade.*

| Item | Result |
|---|---|
| Divergence-proof execution (repair, moved to the front of the session) | 🔲 **blank** — second consecutive blank exposure (09-03, 09-04). **Per the two-blank rule, paused.** See "Paused / off active rotation" below. |
| Bug #2 retention check ($\sum k^3$) | 🔲 **blank** — first retention check since retirement (09-01), first blank. Re-offered once, Session 15 (09-07) R1, fresh instance ($\sum k^2$). |
| Contrapositive-applied retention check ($n^3+5$) | 🔲 **blank** — first retention check since retirement (09-01), first blank. Re-offered once, Session 16 (09-08). |
| Plain-English quantifier retention check ($P(x,y):x^2=y$) | 🔲 **blank** — first retention check since retirement (09-01), first blank. Re-offered once, Session 17 (09-09), reusing the scaffold-first approach that worked before. |
| Synthesis — uniqueness of the supremum | 🔲 **blank** — third blank exposure for sup/inf material, third distinct framing (compute a sup, compute an inf + second sup, prove uniqueness), three consecutive sessions. Not re-offered as a fourth cold problem; Session 15's Core changes the representation entirely (worked scaffold + parallel instance). |

## Resolved 2026-09-03 (Session 13) — results

*Entirely blank session — the fifth in the repo's history (after 08-24, 08-27,
08-28, 09-02), and the second time two have landed back-to-back (09-02, 09-03) —
the first pair was 08-27/08-28. This one immediately follows the two strongest
sessions in the repo (08-31, 09-01), same as 09-02 did. Nothing graded as wrong;
everything held. No feedback file — nothing to grade.*

| Item | Result |
|---|---|
| Existential witness, second offering since the 08-28 pause | 🔲 **blank** — second consecutive blank in the resumed cycle. **Per the two-blank rule, paused again** — logged as untested in `STATE.md`. |
| Divergence-proof execution (repair) | 🔲 **blank** — fourth blank exposure since the one wrong attempt (08-26). |
| Sup/inf — infimum (Core 1) and second supremum instance (Core 2) | 🔲 **blank** — second blank exposure for this material. |

## Due 2026-09-07 (Session 15 — Monday, first session of a new week)

*Not a Friday, so back to the normal weekday cap: at most one review item, at most
one repair item. No repair item is offered — divergence-proof execution just
paused (see below). That freed slot is not repurposed for a second review item;
the one-review-item cap is kept as stated in `RUN-PROMPT.md`, and the other two
due retention checks are spread across the next two weekday sessions instead of
crowded into one.*

| Item | Due since | Status today |
|---|---|---|
| Bug #2 — induction hypothesis as engine, retention check | 2026-09-04 (first check blank) | **Session 15 R1**, fresh instance ($\sum k^2$), re-offered once per the standing blank rule. |
| Sup/inf | first taught 09-02, zero attempt evidence across three framings on three consecutive sessions | **Session 15 Core**, changing representation: worked scaffold (a fully solved sup proof, both parts of the definition shown) followed by a structurally parallel instance for Alex to complete, plus a second problem connecting the $\varepsilon$-part of sup's definition to quantifier/Archimedean reasoning already retired. |
| Contrapositive-applied, retention check | 2026-09-04 (first check blank) | Carries forward to **Session 16 (09-08)** — one review item per weekday, R1's slot is bug #2 today. |
| Plain-English quantifier meaning, retention check | 2026-09-04 (first check blank) | Carries forward to **Session 17 (09-09)** — same reasoning; reuses the scaffold-first approach that broke this gap open on 09-01. |
| Setup discipline (retention check) | 2026-09-02 | Not selected — carries forward. |
| Pigeonhole — general principle (retirement check) | 08-24 | Carries forward — oldest open item in the queue, one blank exposure so far (08-28). |
| Quantifier negation — compound predicates (retention check) | 08-28 | Carries forward — not yet retested at its first 3-day check. |
| Quantifier order — construct and prove true/false | 08-29 | Carries forward — not yet retested. |
| Induction — counting ($2^n$ subsets), 1d retention check | 2026-09-02 | Carries forward — not yet retested. |

**Divergence-proof execution removed from the "Due" rotation** as of 09-04's second
consecutive blank exposure (09-03, 09-04) — see "Paused / off active rotation"
below. Existential witnesses, strong induction, and Taylor/geometric series remain
off rotation, unchanged.

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
| Negation as a proof obligation — definition + structure | §5 | 2026-08-25 | 1d | folded into the divergence-proof problem repeatedly, still not retested (item paused 09-04) | 1 (first taught) |
| Quantifier order — construct and prove true/false | §5 | 2026-08-26 | 3d | 2026-08-29 (overdue, not yet retested) | 2 |
| **Induction hypothesis as the engine** | §6 | 2026-09-01 | 3d (first retired) | first retention check (09-04) blank — **re-offered Session 15 (09-07)** | 1 (retired) |
| Σ: running total vs. *n*-th term | §6 | 2026-08-31 | — | folded into induction's evidence — no separate check needed | — |
| **Contrapositive vs. contradiction, applied** | §4 | 2026-09-01 | 3d (first retired) | first retention check (09-04) blank — **re-offered Session 16 (09-08)** | 1 (retired) |
| **Quantifier statements — plain-English meaning** | §5 | 2026-09-01 | 3d (first retired) | first retention check (09-04) blank — **re-offered Session 17 (09-09)** | 1 (retired) |
| Induction — counting ($2^n$ subsets) | §6 | 2026-09-01 | 1d (first taught) | 2026-09-02 (due, not selected — hard cap; carries forward) | 1 |
| Sup/inf — two-part definition | §9 | taught 09-02; attempts offered 09-02, 09-03, 09-04, all blank, three different framings | — | **Session 15 (09-07)** — representation changed (worked scaffold + parallel instance), per the three-consecutive-session rule | — |

**Existential witnesses — paused, unchanged since 09-03.** Both offerings since
the 08-28 resume (09-02, 09-03) landed inside entirely blank sessions — off
active rotation, resumes only once a real-evidence session opens a slot ahead of
it.

**Quantifier order — construct and prove true/select false, advanced 1d → 3d
(2026-08-26).** Second clean cold instance. Due 2026-08-29, not yet retested —
carries forward.

---

## Paused / off active rotation

*Items with two consecutive blank exposures — logged as untested per the standing
two-blank rule, not as demonstrated gaps, except where noted. Resume once a
real-evidence session opens a slot ahead of them.*

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
- **Divergence-proof execution — newly paused 2026-09-04.** One genuine wrong
  attempt (08-26), then six blank exposures since (08-27, 08-28, 09-02, 09-03,
  09-04), the last two of which (09-03, 09-04) are the consecutive pair that
  triggers the standing rule. Note: this item had already exceeded two blank
  exposures well before today without being paused — earlier sessions kept
  re-offering it as "the least-tested item" rather than applying the rule at its
  first qualifying point. That inconsistency is flagged in `CURRICULUM.md` §7
  rather than silently resolved; the rule is being applied from here forward.

Five items now share this status — up from four on 09-03, three on 09-02, two on
08-28. The mechanism doing the pausing is working exactly as specified; what it's
being fed is the open question (see `CURRICULUM.md` §7).

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  **Moved to "Paused / off active rotation" above as of 2026-09-04** — see that
  section for the full history. Still exactly one genuine attempt on record
  (08-26, wrong), now over a month old.
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now.
- **Definition of linear independence** (B1) — deferred to Phase 1.

**Resolved 2026-09-01, removed from this list:**
- **Contrapositive narrated as contradiction, applied to own writing.** First fully
  clean instance — see "Scheduled" above for the retirement. First retention check
  (09-04) came back blank — this is a re-offer situation, not a re-failure; see the
  "Due 2026-09-07" table above.
- **Quantifier statements — plain-English meaning, not symbol transliteration.**
  First fully clean instance after 1 wrong + 4 blanks — see "Scheduled" above.
  First retention check (09-04) came back blank — re-offer, not re-failure; see
  above.
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
