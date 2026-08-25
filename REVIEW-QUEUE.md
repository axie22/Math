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

## Resolved 2026-08-25 (Session 6 retry) — results

*First real work since Session 5 (08-21) — Monday 08-24 came back blank.*

| Item | Result |
|---|---|
| Quantifier negation — atomic case | ✅ **correct, second clean cold instance.** Advances 1d → 3d. |
| Quantifier negation — compound predicates | ✅ **all five items correct**, including the restriction+connective trap. Third pass — **retired**, see Scheduled below. |
| Negation as a proof obligation — writing $\lnot(a_n\to L)$ + the three-move structure | ✅ correct, first exposure. New line, enters at 1-day interval. |
| Negation as a proof obligation — executing the construction | 🔲 blank both times attempted (§2c, §2d). No data yet — re-offered once, compact, 2026-08-26. |
| Quantifier order — determine true/false, prove the true one | ✅ correct, first exposure. New line, enters at 1-day interval. |
| Quantifier order — disprove the false one cleanly | 🟡 right strategy, arithmetic slip. Tracked with `STATE.md`'s arithmetic-slips line, not a separate repair track. |
| Quantifier statements — plain-English meaning (not transliteration) | ❌ **new gap.** Symbol restatement given instead of substantive explanation. Becomes 2026-08-26's repair item. |
| $\delta$–$\varepsilon$ role-swap, conceptual consequence | 🔲 blank, no content. Carries forward, lower priority than the plain-English gap. |

## Due 2026-08-26 (Session 7)

*Five items have been overdue since 08-22/08-24, all traceable to the one blank
session on 08-24. Hard cap allows one review slot — today it goes to setup
discipline, the oldest-waiting item closest to permanent retirement.*

| Item | Due since | Status today |
|---|---|---|
| Setup discipline | 08-22 | **Pulled into Session 7's R1**, fresh instance. |
| Existential witnesses in $\mathbb{Z}$ | 08-22 | Carries forward. |
| Contrapositive vs. contradiction (concept) | 08-22 | Carries forward. |
| Bug #1 — landing (retirement-interval check) | 08-24 | Carries forward — first check since retirement, still needed. |
| Pigeonhole — general principle (retirement-interval check) | 08-24 | Carries forward — first check since retirement, still needed. |
| Negation-as-proof-obligation (definitional part) | 08-26 (first taught 08-25) | Not pulled — brand new, lower priority than the four above; will surface once a slot opens. |
| Quantifier order (true/false construction) | 08-26 (first taught 08-25) | Not pulled — same reasoning as above. |

Compound-predicate negation is **not** in this table anymore — it retired 08-25 (see
Scheduled, 3-day interval, due 08-28). The plain-English gap and the divergence-proof
re-offer are **not** spaced-review items — they're the active repair item and the
one-time re-offer for Session 7 (see `STATE.md`), not drawn from this queue.

---

## Scheduled

| Item | Topic | Last seen | Interval | Due | Streak |
|---|---|---|---|---|---|
| Unfold-the-definition habit | §1 | 2026-08-18 | 3d | 2026-08-21 | 1 |
| Contrapositive vs. contradiction | §3–4 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Setup discipline | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Existential witnesses in $\mathbb{Z}$ | §1 | 2026-08-19 | 3d | 2026-08-22 | 1 |
| Quantifier negation — atomic case | §5 | 2026-08-25 | 3d | 2026-08-28 | 2 |
| Quantifier negation — compound predicates | §5 | 2026-08-25 | 3d | 2026-08-28 | 1 (retired) |
| Bug #1 — landing ($\sqrt3$ irrational) | §4 | 2026-08-21 | 3d | 2026-08-24 (missed, still open) | 1 (retired) |
| Pigeonhole — general principle | §8 | 2026-08-21 | 3d | 2026-08-24 (missed, still open) | 1 (retired) |
| Negation as a proof obligation — definition + structure | §5 | 2026-08-25 | 1d | 2026-08-26 | 1 (first taught) |
| Quantifier order — construct and prove true/false | §5 | 2026-08-25 | 1d | 2026-08-26 | 1 (first taught) |
| Σ: running total vs. *n*-th term | §6 | — | — | first taught, TBD (Induction block, Thu 08-27) | — |
| Induction hypothesis as the engine | §6 | — | — | first taught, TBD (Induction block, Thu 08-27) | — |

**Quantifier negation — atomic case, advanced 1d → 3d (2026-08-25).** Second clean
cold instance (first was Session 4's 3/3 on 08-20; this one crossed a real 5-day
gap). Streak now 2.

**Quantifier negation — compound predicates, new line, retired at 3-day interval
(2026-08-25).** Failed 08-20 and 08-21 with the identical two sub-errors both times
(arrow surviving instead of becoming "and"; De Morgan applied to only one side).
Session 6 retry (08-25) §1(a)–(e): all five correct, including the
restriction+connective trap in (d) that specifically caused the 08-20 relapse.
Third pass, clean — real repair, not a recognized-shape effect. One clean
demonstration retires it per the current rules; this line is the retention check
going forward.

**Negation as a proof obligation — definition + structure, new line, 1-day interval
(2026-08-25).** §2(a), 2(b) both correct on first exposure: the negated definition
and the three-move breakdown (choose ε, accept arbitrary N, construct n). Kept
short since it's only one data point — this is the *setup* half of the skill; the
*execution* half (§2c/2d) is still blank and tracked separately below, not in this
queue.

**Quantifier order — construct and prove true/false, new line, 1-day interval
(2026-08-25).** §3(a) true case clean ($\forall x\exists y$, $y=-x$); false case
right strategy with an arithmetic slip in the final line. Kept at a short interval;
the slip is tracked in `STATE.md`'s arithmetic-slips line, not here.

**Setup discipline / Existential witnesses / Contrapositive (concept) — unchanged.**
Still overdue since 08-22, still one clean instance short of retirement. Setup
discipline pulled into Session 7 (08-26); the other two carry forward again.

**Bug #1 — landing / Pigeonhole — general principle — unchanged.** Both retired
2026-08-21, both had their first retirement-interval check due 08-24, both missed
(08-24 was blank). Neither has been re-tested since — still the oldest unresolved
item in this queue, carried forward again pending an open slot.

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Contrapositive narrated as contradiction, applied to own writing.** New
  2026-08-19 — used the contrapositive correctly per instructions but closed with
  contradiction language against a nonexistent "given." **08-21 Part 2b:** half
  right — named the technique but still didn't write the sentence explaining *why*
  proving the contrapositive settles the original claim. Two genuine attempts
  (08-19, 08-21), neither fully clean. Not pulled 08-25 (repair slot went to
  compound-predicate negation, which then closed) — **next open repair slot goes
  here.**
- **Quantifier statements — plain-English meaning, not symbol transliteration.**
  New 2026-08-25. §3(b) asked what $\forall x\exists y\,P(x,y)$ and $\exists
  y\forall x\,P(x,y)$ *assert* about the reals; the answer given was a
  transliteration of the quantifier symbols into English words ("for all x there
  exists a y"), not an explanation of the mathematical content (additive
  inverses). One data point — **this is Session 7's (08-26) repair item**, a fresh
  predicate, isolating the explanation skill from the (already-demonstrated)
  construction skill.
- **Induction: state and use the hypothesis** (A2) — bug #2. Not yet re-tested;
  block starts Thursday 2026-08-27.
- **Σ notation: sum of first *n* terms, not the *n*-th term** (A2). Not yet re-tested.
- **Definition of rank** (B1) — deferred to Phase 1, not drilled now.
- **Definition of linear independence** (B1) — deferred to Phase 1.

**Not in this list — tracked separately, not as active repair:**
- The arithmetic slip in 08-25's §3(a) false case (dropped a constant term) is
  logged in `STATE.md`'s recurring arithmetic-slips line, alongside two earlier
  instances. Three data points now; worth a dedicated callout if a fourth appears,
  but not yet its own repair track.
- The divergence-proof *construction* (08-25 §2c/2d, blank) and the δ–ε role-swap
  question (08-25 §3c, blank) are first-exposure blanks, not failures — handled per
  the no-evidence rule (re-offer once), not the Failed-list mechanism.

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
