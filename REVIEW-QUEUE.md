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

## Resolved 2026-08-31 (Session 10) — results

*Real, substantial work — the strongest single session since 08-25. Full grading:
`weeks/2026-08-31/08-31-feedback.md`.*

| Item | Result |
|---|---|
| Bug #1 — landing ($\sqrt5$ irrational) | ✅ **correct, second clean cold retrieval.** Advances 3d → 7d, due 2026-09-07. |
| Quantifier negation — atomic case | ✅ **correct, third clean cold instance.** Advances 3d → 7d, due 2026-09-07. |
| Quantifier statements — plain-English meaning ($xy=1$) | 🔲 **blank, fourth non-clean exposure** — but for the first time, blank while everything else in the session (R1, R2, Core 1, Core 2) was completed carefully. A localized skip, not a time-budget problem. Session 11 (09-01) changes approach: worked scaffold example first. |
| Induction — sum formula ($1+3+\cdots+(2n-1)=n^2$) | ✅ **correct, clean.** $S(n)$ vs. term correctly distinguished, hypothesis visibly substituted. First real evidence bug #2 is fixed. |
| Induction — divisibility ($3\mid n^3-n$) | ✅ **correct**, one presentation note (writing an equality chain as if it were a chain of "3 divides" restatements — content correct, form flagged in feedback). |

## Due 2026-09-01 (Session 11)

| Item | Due since | Status today |
|---|---|---|
| Induction hypothesis as the engine (first-taught, 1d check) | 2026-08-31 | **Session 11 R1**, fresh instance ($2+4+\cdots+2n=n(n+1)$) — fast retention check, 1 day out. |
| Contrapositive vs. contradiction, applied | 08-22, re-offered 08-28 (blank) | **Session 11 R2**, fresh claim ($5n+3$ even $\Rightarrow n$ odd) — explicitly asks for the missing "why this settles the original claim" sentence. |
| Quantifier statements — plain-English meaning (repair) | 08-25 | **Session 11 Repair slot**, fifth exposure, fresh predicate ($x-y=1$), worked scaffold example included this time. |
| Existential witnesses in $\mathbb{Z}$ | 08-22, paused since 08-28 | **Not today** — resume condition met by Session 10's real evidence; slated for Session 12 (09-02) instead, to keep today's session inside the hard cap. |
| Pigeonhole — general principle (retirement check) | 08-24 | Carries forward — one blank exposure so far (08-28), eligible for a re-offer. |
| Quantifier negation — compound predicates (retention check) | 08-28 | Carries forward — not yet retested at its first 3-day check. |
| Negation-as-proof-obligation (definitional part) | 08-26 | Carries forward — folds into the next divergence-proof problem. |
| Divergence-proof execution (repair) | — | Carries forward — still one genuine wrong attempt on record; Session 11's one repair slot went to plain-English quantifiers again (escalated approach). |

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 | 1 |
| Setup discipline | §1 | 2026-08-26 | 7d | 2026-09-02 | 2 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | **paused — resume condition met 08-31, slated for Session 12 (09-02)** | 1 |
| Quantifier negation — atomic case | §5 | 2026-08-31 | 7d | **2026-09-07** | 3 |
| Quantifier negation — compound predicates | §5 | 2026-08-25 | 3d | 2026-08-28 (overdue, not yet retested) | 1 (retired) |
| Bug #1 — landing | §4 | 2026-08-31 | 7d | **2026-09-07** | 2 (retired) |
| Pigeonhole — general principle | §8 | 2026-08-21 | 3d | 2026-08-24 (overdue; one blank offering 08-28, eligible for re-offer) | 1 (retired) |
| Negation as a proof obligation — definition + structure | §5 | 2026-08-25 | 1d | 2026-08-26 (overdue, still open) | 1 (first taught) |
| Quantifier order — construct and prove true/false | §5 | 2026-08-26 | 3d | 2026-08-29 (overdue, not yet retested) | 2 |
| **Induction hypothesis as the engine** | §6 | 2026-08-31 | 1d (first taught) | **2026-09-01 (Session 11 R1)** | 1 |
| Σ: running total vs. *n*-th term | §6 | 2026-08-31 | — | folded into induction's evidence — no separate check needed, correct alongside Core 1 | — |
| Induction — counting / strong induction (new today) | §6 | — | — | first taught, Session 11 (09-01) | — |

**Bug #1 — landing, and Quantifier negation — atomic case, both advanced 3d → 7d
(2026-08-31).** Second and third clean cold retrievals respectively. Both due
2026-09-07.

**Induction hypothesis as the engine — entered the queue 2026-08-31 (first
taught), 1-day interval per the standing rule for first-taught concepts.** Due
2026-09-01 — Session 11's R1, deliberately an easy/fast instance since this is a
speed check on whether the mechanism survived overnight, not a new problem.

**Quantifier order — construct and prove true/false, advanced 1d → 3d
(2026-08-26).** Second clean cold instance. Due 2026-08-29, not yet retested —
carries forward.

**Existential witnesses in $\mathbb{Z}$ — paused 2026-08-28, resume condition met
2026-08-31.** Two consecutive blank exposures (08-27, 08-28) triggered the pause;
`STATE.md`'s own stated resume condition ("the first Monday–Thursday session that
produces real evidence for whatever's ahead of them in the queue") fired when
Session 10 landed clean. Not resumed in Session 11 purely to stay inside the hard
cap (two review items already committed) — **slated for Session 12 (09-02)**
instead, the same day it was originally due to have been checked, one week late.

**Quantifier statements — plain-English meaning — fifth exposure, approach changed
2026-09-01.** Wrong (08-25), blank ×4 (08-26, 08-27/08-28, 08-31). The 08-31 blank
came inside an otherwise fully-completed session — the clearest evidence yet that
this is a localized, specific difficulty rather than a time-budget problem.
Session 11's Repair slot adds a worked scaffold example (a different, structurally
analogous predicate, fully explained) directly above the fresh instance ($T(x,y)$:
"$x-y=1$"). If this comes back blank again under the new approach, `STATE.md` flags
it for a direct conversation rather than a sixth written attempt.

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Contrapositive narrated as contradiction, applied to own writing.** New
  2026-08-19, half right 08-21, blank 08-28 (Session 9). **Fresh instance in
  Session 11 (09-01) R2** — explicitly asks for the one sentence that's been
  missing every time (why the contrapositive settles the original claim).
- **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  08-25: blank. 08-26 (fresh instance): wrong, stopped at the identical step.
  08-27, 08-28: both offered a third instance, both sessions blank. Still just one
  genuine wrong attempt on record. Sessions 10 and 11 both used their one repair
  slot on the plain-English quantifier item instead — still waiting for an open
  slot.
- **Quantifier statements — plain-English meaning, not symbol transliteration.**
  See "Scheduled" above for the full history — this is the item getting a worked
  scaffold in Session 11 rather than a sixth cold re-ask.
- **Σ notation: sum of first *n* terms, not the *n*-th term** (A2). **Resolved
  2026-08-31** — Session 10 Core 1 correctly distinguished $S(n)$ from the $n$-th
  term unprompted. Removing from this list; folded into the induction evidence
  above.
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now.
- **Definition of linear independence** (B1) — deferred to Phase 1.

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
