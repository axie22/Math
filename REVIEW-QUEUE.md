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

## Resolved 2026-08-26 (Session 7) — results

*Real work again, but time ran out at the repair block — see `08-26-feedback.md`.*

| Item | Result |
|---|---|
| Setup discipline | ✅ **correct, second clean cold instance at 7-day spacing (08-19 → 08-26). Retired**, see Scheduled below. |
| Quantifier order — determine true/false | ✅ **correct, second clean cold instance** (via 1(a), framed as a quick confirmation, not a full proof re-ask). Advances 1d → 3d. |
| Divergence proof execution ($\varepsilon$-$N$, oscillating term) | ❌ **wrong — same specific obstacle as 08-25's §2(c)**: got to $b_{N+1}=1+(-1)^{N+1}$ and stopped short of using $|(-1)^{N+1}|=1$ instead of resolving the sign. Second occurrence of the identical stopping point. Becomes 08-27's repair item, fresh instance. |
| Quantifier statements — plain-English meaning | 🔲 **not reached (blank)** — the actual repair item, never got to it. Not a second wrong (that would reset harder); still one wrong (08-25) + now one blank. Re-offered once more 08-27, fresh predicate. |
| Taylor's theorem, geometric series (new material) | 🔲 **not reached (blank)** — zero evidence either way. Held, re-offered 08-27 with fresh instances. |

## Due 2026-08-27 (Session 8)

*Six items are now overdue at once — five carried from the 08-24 blank day
(traceable to that one miss), plus one more that just came due. Hard cap allows
2–3 review-block slots; the rest wait for Friday's review day, which is built to
absorb exactly this kind of backlog.*

| Item | Due since | Status today |
|---|---|---|
| Existential witnesses in $\mathbb{Z}$ | 08-22 | **Pulled into Session 8's R1**, fresh instance. |
| Quantifier statements — plain-English meaning | 08-25 (repair) | **Pulled into Session 8's R2** (re-offer, not a queue item — see Failed list). |
| Contrapositive vs. contradiction (concept) | 08-22 | Carries forward — next open slot, likely Friday. |
| Bug #1 — landing (retirement-interval check) | 08-24 | Carries forward — still the oldest unresolved retirement check. |
| Pigeonhole — general principle (retirement-interval check) | 08-24 | Carries forward — same status as Bug #1. |
| Negation-as-proof-obligation (definitional part) | 08-26 | Carries forward — not yet retested since first taught 08-25. |

Divergence-proof execution is **not** in this table — it's the active repair item
(see Failed list), not a spaced-review item; same for the plain-English gap.

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 | 1 |
| Contrapositive vs. contradiction | §3–4 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Setup discipline | §1 | 2026-08-26 | 7d | 2026-09-02 | 2 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Quantifier negation — atomic case | §5 | 2026-08-25 | 3d | 2026-08-28 | 2 |
| Quantifier negation — compound predicates | §5 | 2026-08-25 | 3d | 2026-08-28 | 1 (retired) |
| Bug #1 — landing ($\sqrt3$ irrational) | §4 | 2026-08-21 | 3d | 2026-08-24 (missed, still open) | 1 (retired) |
| Pigeonhole — general principle | §8 | 2026-08-21 | 3d | 2026-08-24 (missed, still open) | 1 (retired) |
| Negation as a proof obligation — definition + structure | §5 | 2026-08-25 | 1d | 2026-08-26 (missed, still open) | 1 (first taught) |
| Quantifier order — construct and prove true/false | §5 | 2026-08-26 | 3d | 2026-08-29 | 2 |
| Σ: running total vs. *n*-th term | §6 | — | — | first taught, TBD (Induction block, now Mon 08-31) | — |
| Induction hypothesis as the engine | §6 | — | — | first taught, TBD (Induction block, now Mon 08-31) | — |

**Setup discipline, advanced 3d → 7d, retired (2026-08-26).** Second clean cold
instance (first: Session 3, 08-19) at exactly 7 days' spacing — meets this file's
own bar for closing an item out. This is the retention check going forward, not
active teaching.

**Quantifier order — construct and prove true/false, advanced 1d → 3d
(2026-08-26).** Second clean cold instance: 08-25 built $y=-x$ from scratch with a
full proof; 08-26's 1(a) was a lighter true/false confirmation on a new predicate
($y=x^2$), explicitly framed as "you did this correctly yesterday, just confirm" —
still a real cold retrieval, still counts.

**Negation as a proof obligation — definition + structure, unchanged, now missed.**
Due 08-26, not retested (08-26's R2 tested the *execution* half, a related but
distinct skill — see Failed list). Carries forward to the next open slot.

**Bug #1 — landing / Pigeonhole — general principle — unchanged, now the oldest
items in the queue.** Both retired 2026-08-21, both missed their first
retirement-interval check (due 08-24, the blank day), neither retested since.
Should be next in line once a slot opens — likely Friday 08-28.

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Contrapositive narrated as contradiction, applied to own writing.** New
  2026-08-19, half right 08-21 (technique named, closing reasoning missing). Two
  genuine attempts, neither clean. Not pulled 08-25 or 08-26 (repair slot went
  elsewhere both times) — **next open repair slot goes here**, most likely Friday.
- **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  08-25 §2(c): blank. 08-26 R2 (fresh instance, $b_n=1+(-1)^n$): wrong, stopped at
  the identical step — about to case-split on the parity of $N+1$ instead of noting
  $|(-1)^{N+1}|=1$ regardless. Same obstacle twice now, on two different instances.
  **This is 08-27's repair item**, a third instance built specifically to force the
  "do I need the sign, or does $|\cdot|$ already answer this?" question.
- **Quantifier statements — plain-English meaning, not symbol transliteration.**
  08-25: wrong (transliteration, not explanation). 08-26: blank (not reached — ran
  out of time before the repair block finished). Zero clean attempts across two
  exposures. **Re-offered again 08-27**, fresh predicate ($T(x,y)$: "$x<y$"),
  placed early (review block, not repair — keeping the hard cap's one repair slot
  free for the divergence-proof item above).
- **Induction: state and use the hypothesis** (A2) — bug #2. Not yet re-tested;
  block now starts Monday 2026-08-31 (slipped one session from Thu 08-27 — Session
  7/8's calculus-repair material wasn't reached until 08-27, so induction can't
  start until it has been).
- **Σ notation: sum of first *n* terms, not the *n*-th term** (A2). Not yet re-tested.
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now.
- **Definition of linear independence** (B1) — deferred to Phase 1.

**Not in this list — tracked separately, not as active repair:**
- The arithmetic slip in 08-25's §3(a) false case (dropped a constant term) is
  logged in `STATE.md`'s recurring arithmetic-slips line, alongside two earlier
  instances. Three data points now; worth a dedicated callout if a fourth appears,
  but not yet its own repair track.
- The δ–ε role-swap question (08-25 §3c, blank) is a first-exposure blank, not a
  failure — handled per the no-evidence rule (re-offer once, when a slot opens),
  not the Failed-list mechanism.

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
