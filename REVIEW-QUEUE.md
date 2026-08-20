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

## Due 2026-08-21 (session 5, review day)

| Item | Why it's here |
|---|---|
| **Bug #1 landing ($\sqrt3$ irrational)** | Carried over — 08-20's R1 retest was not attempted (blank). Zero new evidence two days running. Retest is 08-21 Part 2a. |
| **Contrapositive vs. contradiction, applied** | Carried over — 08-20's R2 retest was not attempted (blank). Retest is 08-21 Part 2b. |
| **Quantifier negation — compound predicates** | 08-20 Core 1 split cleanly: atomic ∀/∃-over-one-predicate negation clean (a, b, f), but negating an implication (c) and a disjunction (e) both failed — the connective-specific rule (implication→conjunction, De Morgan swap) wasn't applied despite being printed in the problem file. Retest is 08-21 Part 2c. |
| **Pigeonhole — general principle in words** | 08-20 Core 2(a)/(b) derived the specific case cleanly (real repair of 08-19's gap), but Core 2(c) — state the general principle, connect to 08-19 — was circular/incomplete ("finite" alone, not the actual $|A|>|B|$ condition; no connection made). Retest is 08-21 Part 2d, then generalized as a full proof in Part 3. |

*Quantifier negation's **atomic** case (single ∀/∃ over a plain predicate, no
implication or and/or inside) is now holding — see Scheduled below, split out as its
own line rather than bundled with the compound case, since they're behaving
differently.*

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 | 1 |
| Contrapositive vs. contradiction | §3–4 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Setup discipline | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Quantifier negation — atomic case | §5 | 2026-08-20 | 1d | 2026-08-21 | 1 |
| Σ: running total vs. *n*-th term | §6 | — | — | 2026-08-25 (first taught) | — |
| Induction hypothesis as the engine | §6 | — | — | 2026-08-25 (first taught) | — |

*Items marked "first taught" enter the 1-day interval on the date they're introduced.*

**Quantifier negation — atomic case, new line, 1-day interval.** 08-20 Core 1(a), (b),
(f) were all clean: quantifier flipped, domain restriction untouched, predicate
negated, and (f) carried a witness proof through correctly too. Kept at a short
interval for now since it's only one data point — advances properly once it's held
across a real gap, not just the day it was taught.

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

- **Completing a proof after setup** (A1) — bug #1. **Relapsed 2026-08-19, then not
  attempted at all 2026-08-20.** The 2026-08-18 clean retrieval still counts as one
  data point, but 08-19's Core 2(b) ($\sqrt3$ irrational) derived every fact needed
  and never wrote the closing contradiction sentence, and 08-20's R1 retest was left
  blank — zero new evidence, two days running. Retest is 2026-08-21 Part 2a.
- **Contrapositive narrated as contradiction, applied to own writing.** New
  2026-08-19 — Core 2(a) used the contrapositive correctly per instructions but
  closed with contradiction language against a nonexistent "given." 08-20's R2, a
  direct targeted fix, was left blank — not attempted. Retest is 2026-08-21 Part 2b.
- **Quantifier negation — compound predicates (implication, De Morgan)** (A3) —
  narrower descendant of bug #3. First drilled 2026-08-20: negating an implication
  (Core 1c) and a disjunction (Core 1e) both failed, in each case because the
  connective-specific transformation wasn't applied — the implication was left as an
  implication with both sides' inequalities flipped, and "or" wasn't swapped to
  "and." The **atomic** case (plain ∀/∃ over one predicate) is holding — see
  Scheduled — so this line now tracks specifically the compound-predicate piece, not
  quantifier negation as a whole. Retest is 2026-08-21 Part 2c.
- **Pigeonhole — general principle stated precisely, connected across sessions.**
  Narrowed 2026-08-20 — Core 2(a)/(b) now derive the specific case cleanly (real
  repair of the 08-19 gap below), but Core 2(c) gave "both sets are finite" instead
  of the actual condition ($|A|>|B|$) and didn't connect to 08-19's equal-size case.
  *Deriving a specific pigeonhole instance is no longer on this list* — 08-20 Core
  2(a)/(b) did that cleanly. Retest is 2026-08-21 Part 2d, generalized to a full proof
  in Part 3.
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
