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

## Due 2026-08-18 (session 2)

| Item | Why it's here |
|---|---|
| **Prove: $n^2$ even ⟹ $n$ even** | Calibration A1 — set up correctly, never finished |
| **Definitions: even, odd, $a \mid b$** | Prerequisite for everything in §1. Must be automatic |

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Contrapositive vs. contradiction | §3–4 | — | 1d | 2026-08-19 | 0 |
| Unfold-the-definition habit | §1 | — | 1d | 2026-08-19 | 0 |
| Injective / surjective definitions | §8 | — | 1d | 2026-08-19 | 0 |
| Quantifier negation rule | §5 | — | — | 2026-08-20 (first taught) | — |
| Σ: running total vs. *n*-th term | §6 | — | — | 2026-08-25 (first taught) | — |
| Induction hypothesis as the engine | §6 | — | — | 2026-08-25 (first taught) | — |

*Items marked "first taught" enter the 1-day interval on the date they're introduced.*

---

## Failed — reset to 1-day, high priority

*From the 2026-08-17 calibration. These re-surface until two clean cold retrievals at
≥7-day spacing.*

- **Completing a proof after setup** (A1) — bug #1
- **Quantifier negation: flip quantifiers, not domain restrictions** (A3) — bug #3
- **Induction: state and use the hypothesis** (A2) — bug #2
- **Σ notation: sum of first *n* terms, not the *n*-th term** (A2)
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now
- **Definition of linear independence** (B1) — deferred to Phase 1

The two linear-algebra items are deliberately *not* being drilled during Phase 0.
Memorizing definitions ahead of the phase that builds them produces recall without
understanding. Phase 1 starts from the axioms and they'll be earned there.

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

*(none)*
