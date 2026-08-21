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

## Resolved 2026-08-21 (session 5, review day) — results

| Item | Result |
|---|---|
| Bug #1 landing ($\sqrt3$ irrational) | ✅ **landed it, third attempt.** Retired — see Scheduled, 3-day interval. |
| Contrapositive vs. contradiction, applied | 🟡 half — named the technique but didn't write why proving the contrapositive settles the original claim. Still open, tracked in Failed. |
| Quantifier negation — compound predicates | ❌ failed again, both items (implication, De Morgan) — second failure in a row. Still open, tracked in Failed. |
| Pigeonhole — general principle in words | ✅ correct, and the Part 3 synthesis proof was the best work in the repo so far. Retired — see Scheduled, 3-day interval. |

## Due 2026-08-25 (session 6 retry — Monday 08-24 came back blank)

*Monday's session had zero evidence, so nothing here advanced and nothing new
resolved between 08-21 and today. Only one review slot exists per the hard cap, so
today pulls the single most-overdue item and the rest carry forward again — this is
what a review queue backing up actually looks like, traceable to one blank session
rather than four separate problems.*

| Item | Due since | Status today |
|---|---|---|
| Quantifier negation — atomic case | 08-21 (missed — 08-21's review day only covered the compound case) | **Pulled into today's R1**, fresh instance. |
| Contrapositive vs. contradiction (concept) | 08-22 | Carries forward. |
| Setup discipline | 08-22 | Carries forward. |
| Existential witnesses in $\mathbb{Z}$ | 08-22 | Carries forward. |
| Bug #1 — landing (retirement-interval check) | 08-24 | Carries forward — first check since retirement, still needed. |
| Pigeonhole — general principle (retirement-interval check) | 08-24 | Carries forward — first check since retirement, still needed. |

Compound-predicate negation and contrapositive-applied are **not** in this table —
they're active repairs (see Failed, below), not spaced-review items. The hard cap
gives compound-predicate negation the one repair slot today: it's failed twice with
real attempts (08-20, 08-21) and is the higher-leverage item, since it blocks the
Phase 0 exit gate's "implication at the bottom of the quantifier stack" requirement
directly.

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 | 1 |
| Contrapositive vs. contradiction | §3–4 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Setup discipline | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Quantifier negation — atomic case | §5 | 2026-08-20 | 1d | 2026-08-21 (retested 08-25) | 1 |
| Bug #1 — landing ($\sqrt3$ irrational) | §4 | 2026-08-21 | 3d | 2026-08-24 | 1 (retired) |
| Pigeonhole — general principle | §8 | 2026-08-21 | 3d | 2026-08-24 | 1 (retired) |
| Σ: running total vs. *n*-th term | §6 | — | — | first taught, TBD (Induction block slides one day, now Thu 08-27) | — |
| Induction hypothesis as the engine | §6 | — | — | first taught, TBD (Induction block slides one day, now Thu 08-27) | — |

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

**Bug #1 — landing, new line, retired at 3-day interval (2026-08-21).** 08-21 Part 2a
finally included the missing sentence — "...since $3\mid b$ and $3\mid a$, so we have
reached a contradiction" — closing a gap that relapsed on 08-19 and went untested on
08-20. One clean demonstration retires it from active repair per the current rules;
this line is the retention check going forward. First retirement-interval check due
2026-08-24, not yet attempted (08-24 was blank).

**Pigeonhole — general principle, new line, retired at 3-day interval (2026-08-21).**
08-21 Part 2d stated the actual condition ($|A|>|B|$, not just "both finite") and
connected it correctly to 08-19's equal-size case; Part 3a/3b then generalized it to a
full proof and explained the finiteness requirement in original language — the
strongest work in the repo so far. Retired from active repair. First
retirement-interval check due 2026-08-24, not yet attempted (08-24 was blank).

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Contrapositive narrated as contradiction, applied to own writing.** New
  2026-08-19 — Core 2(a) used the contrapositive correctly per instructions but
  closed with contradiction language against a nonexistent "given." 08-20's R2 was
  left blank. **08-21 Part 2b: half right** — named the technique (contrapositive)
  correctly but still didn't write the sentence explaining *why proving the
  contrapositive settles the original claim*. Two genuine attempts (08-19, 08-21),
  neither fully clean — stays open. Not pulled today (hard cap gives the one repair
  slot to compound-predicate negation); next retest whenever a repair slot opens.
- **Quantifier negation — compound predicates (implication, De Morgan)** (A3) —
  narrower descendant of bug #3. Failed 2026-08-20 (Core 1c, 1e) **and again
  2026-08-21** (Part 2c(i), 2c(ii)) — same two sub-errors both times: the arrow
  surviving instead of becoming "and," and De Morgan applied to only one side. Two
  genuine failures in a row now — this is today's repair item (2026-08-25), with new
  problem instances and a domain-restriction-plus-connective item added since 08-20's
  (d) showed the restriction rule can relapse under load even once the connective
  rule looks separately solid.
- **Induction: state and use the hypothesis** (A2) — bug #2. Not yet re-tested; block
  was scheduled to start 2026-08-25, now slides to 2026-08-27 (Thursday) since
  08-24/08-25 are both compound-negation-repair sessions (08-24 blank, retried
  08-25).
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
