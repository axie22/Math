# Review Queue — spaced retrieval

> The daily run pulls items due today into the session's opening review block, and
> pushes new items when a topic is first learned.

## How it works

Every concept learned enters the queue and resurfaces at expanding intervals:

**1 day → 3 days → 7 days → 21 days → 60 days → retired**

On a **successful** cold retrieval, the item advances one interval. On a **failed**
one, it drops back to the 1-day interval *and* the topic gets added to
`STATE.md` → Open weaknesses. Retired items may still appear on review days.

The old system's only retrieval was a warm-up recycled from *literally yesterday* — a
one-day interval, once, with no second exposure. Everything from Aug 10 was gone by
Aug 14. This queue is the fix, and it is the single change most likely to make the
hour compound.

**Cold means cold.** Attempt from memory with the lesson file closed. A recognized
concept is not a retrieved one, and the difference is the entire mechanism.

---

## Due today or overdue

*(nothing — queue starts after the calibration diagnostic)*

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| _(empty)_ | | | | | |

---

## Backlog — Days 1–6 material, un-queued

These were taught before the queue existed and no retrieval data exists for any of
them. They are **not** being dropped into the queue as "known." Phase 2 re-teaches this
material properly; until then, review days may sample from this list to keep it warm,
treating any success as provisional.

- Partial derivatives and the gradient (Day 1, 2026-08-10)
- Directional derivatives, steepest ascent/descent (Day 2, 2026-08-11)
- Critical points, Hessian, second-derivative test (Day 3, 2026-08-12)
- Lagrange multipliers, constrained optimization (Day 4, 2026-08-13)
- Eigenvalues/eigenvectors via characteristic polynomial (Day 5, 2026-08-16)
- PCA as eigendecomposition of a covariance matrix (Day 5, 2026-08-16)
- Diagonalization, A = PDP⁻¹, matrix powers (Day 6, 2026-08-17)
- Spectral theorem statement (Day 6, 2026-08-17)
- SVD via eigendecomposition of AᵀA (Day 6, 2026-08-17)

---

## Retired

*(none)*
