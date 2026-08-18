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

## Due 2026-08-19 (session 3)

| Item | Why it's here |
|---|---|
| **Contrapositive vs. contradiction — when/why** | Queued 08-17, tested cold in R1 |
| **Setup line: sum of two evens is even** | New item, see "Failed" below — tests the setup-discipline bug directly |

*Injective/surjective is due today too, but it's being tested as a full Core problem
(session 3, Core 1) rather than a review-block recall, since it's never actually been
attempted — there's nothing to "retrieve" yet. See the Failed section.*

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 | 1 |
| Contrapositive vs. contradiction | §3–4 | — | 1d | 2026-08-19 | 0 |
| Quantifier negation rule | §5 | — | — | 2026-08-20 (first taught) | — |
| Σ: running total vs. *n*-th term | §6 | — | — | 2026-08-25 (first taught) | — |
| Induction hypothesis as the engine | §6 | — | — | 2026-08-25 (first taught) | — |
| Contradiction technique ($\sqrt3$ irrational) | §4 | — | — | 2026-08-20 (first taught) | — |

*Items marked "first taught" enter the 1-day interval on the date they're introduced.*

**Unfold-the-definition habit advanced 1d → 3d.** The actual substitution mechanics
(replace the word with its definition, compute) were correct in all three of
08-18's Core 1 problems — the failures there were in Setup and Land, not in the unfold
step itself. Splitting "unfolding" from "setup discipline" as separate tracked skills
starting today; see below.

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Setup discipline: state the hypothesis, never the conclusion.** New 2026-08-18 —
  Session 2 Core 1(a) and 1(b) both began by assuming the thing being proved (e.g.
  "assume $a+b$ is even" when only $a,b$ being even is given). Tested via R2 today.
- **Existential witnesses: $k \in \mathbb{Z}$, not $\mathbb{N}$.** New 2026-08-18 —
  every unfold in session 2 used $\mathbb{N}$. Doesn't break the specific proofs
  attempted so far but silently excludes negative integers as a general habit.
- **Injective / surjective — construct an example and prove both halves.** Calibration
  A4, then session 2 Core 2 — blank both times, zero data. Session 3, Core 1,
  non-optional.
- **Completing a proof after setup** (A1) — bug #1. **One clean retrieval on
  2026-08-18** (R1: contrapositive redo, carried through to a landing, though the
  landing itself was under-specified — see feedback). One more clean, independent
  instance closes this.
- **Quantifier negation: flip quantifiers, not domain restrictions** (A3) — bug #3.
  Not yet re-tested; first drill scheduled 2026-08-20.
- **Induction: state and use the hypothesis** (A2) — bug #2. Not yet re-tested; block
  scheduled starting 2026-08-25.
- **Σ notation: sum of first *n* terms, not the *n*-th term** (A2). Not yet re-tested.
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now.
- **Definition of linear independence** (B1) — deferred to Phase 1.

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
