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

## Due 2026-08-20 (session 4)

| Item | Why it's here |
|---|---|
| **Contradiction technique ($\sqrt3$ irrational)** | First taught 08-19, tested cold in R1 — with emphasis on the landing sentence, which is exactly where 08-19's Core 2(b) stopped short |

*R2 in session 4 is a direct, targeted fix for a fresh 08-19 error (contrapositive proof
narrated as a contradiction) — it isn't on the interval schedule since it was only
just discovered, but it's cheap and specific enough to fix immediately rather than wait
for a formal queue slot.*

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 | 1 |
| Contrapositive vs. contradiction | §3–4 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Setup discipline | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Quantifier negation rule | §5 | — | — | 2026-08-21 (first taught 08-20) | — |
| Pigeonhole / finite injective ⟹ surjective | §8 | — | — | 2026-08-21 (first taught 08-20) | — |
| Σ: running total vs. *n*-th term | §6 | — | — | 2026-08-25 (first taught) | — |
| Induction hypothesis as the engine | §6 | — | — | 2026-08-25 (first taught) | — |

*Items marked "first taught" enter the 1-day interval on the date they're introduced.*

**Contrapositive vs. contradiction advanced 1d → 3d.** R1 on 08-19 was correct and
well-articulated (the "lighter tool, specific target" framing). Note the irony tracked
above: correct in the abstract on the same day the same distinction got blurred in
Core 2(a)'s execution — the review item measures the concept, not yet the applied
habit, so it advances on its own terms while R2 above targets the applied gap directly.

**Setup discipline advanced 1d → 3d.** Four independent clean uses on 08-19 (R2,
Core 1(a), Core 2(a), Core 2(b)) — no circularity anywhere.

**Existential witnesses in $\mathbb{Z}$ advanced 1d → 3d.** Clean in both places a
witness was needed on 08-19 (Core 2(a)'s $k \in \mathbb{Z}$, Core 2(b)'s
$c \in \mathbb{Z}$).

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Completing a proof after setup** (A1) — bug #1. **Relapsed 2026-08-19.** The
  2026-08-18 clean retrieval still counts as one data point, but 08-19's Core 2(b)
  ($\sqrt3$ irrational) derived every fact needed and then never wrote the closing
  contradiction sentence — a longer, multi-step proof than the one bug #1 looked fixed
  on. Working theory: landing holds on short proofs and drops on longer chains. Retest
  is 2026-08-20's R1 (reconstruct $\sqrt3$ irrational from memory, land it explicitly).
- **Quantifier negation: flip quantifiers, not domain restrictions** (A3) — bug #3.
  Not yet re-tested; first drill is 2026-08-20's Core 1.
- **Injective / surjective, finite-case mechanism (pigeonhole).** New 2026-08-19 —
  Core 1(b)/(c) restated the claim without deriving it; the mechanism is in lesson §8
  but wasn't pointed to. *Constructing an example and proving both halves is no longer
  on this list* — 08-19 Core 1(a) did that cleanly (mechanics correct, notation
  needed a fix). Retest is 2026-08-20 Core 2.
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
