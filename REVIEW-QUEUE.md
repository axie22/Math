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

## Resolved 2026-08-27 (Session 8) — results

*Session 8's work file came back completely blank — no attempt on anything,
including R1/R2. Not graded as failed (blank ≠ wrong); every item below simply
carries forward unresolved, same as before 08-27, plus one day older.*

| Item | Result |
|---|---|
| Existential witnesses in $\mathbb{Z}$ | 🔲 **not attempted** — carries forward, now overdue since 08-22 (5 days), pulled into Session 9's Item 1 with a fresh instance. |
| Quantifier statements — plain-English meaning | 🔲 **not attempted** — third exposure still pending (wrong 08-25, blank 08-26, blank 08-27). Pulled into Session 9's Item 3, fresh predicate. |
| Divergence proof execution | 🔲 **not attempted** — third instance still pending (blank 08-25, wrong 08-26, blank 08-27). Pulled into Session 9's Item 4. |
| Taylor's theorem, geometric series (Core, held from Session 7) | 🔲 **not attempted, second consecutive blank.** Per the two-blank rule, dropped from active rotation — not re-offered Session 9 (or immediately after). See `STATE.md`. |

## Due 2026-08-28 (Session 9, Friday review)

*Same backlog as 08-27, one day older, plus the items that were already scheduled
to come due this week. Friday's hard-cap exemption ("mostly repair" allowed) is
what makes room for all of these in one session — five items total, all review,
no new material.*

| Item | Due since | Status today |
|---|---|---|
| Existential witnesses in $\mathbb{Z}$ | 08-22 | **Session 9 Item 1**, fresh instance ($n<-50$, divisible by 3). |
| Quantifier statements — plain-English meaning | 08-25 (repair) | **Session 9 Item 3**, fresh predicate ($x+y=0$) — third exposure. |
| Contrapositive vs. contradiction (concept, applied) | 08-22 | **Session 9 Item 2** — finally back in an open slot. |
| Bug #1 — landing (retirement-interval check) | 08-24 | Still carries forward — did not fit Session 9, next in line. |
| Pigeonhole — general principle (retirement-interval check) | 08-24 | **Session 9 Item 5**, folded into the synthesis problem. |
| Negation-as-proof-obligation (definitional part) | 08-26 | **Session 9 Item 4**, folded into the divergence-proof problem's setup. |
| Divergence-proof execution (repair, not a queue item) | — | **Session 9 Item 4**, third instance ($c_n=3+5(-1)^n$). |

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

**Negation as a proof obligation — definition + structure.** Due 08-26, not
retested 08-26 or 08-27. **Folded into Session 9's (08-28) Item 4**, as the
explicit setup step before the divergence-proof computation.

**Bug #1 — landing / Pigeonhole — general principle — split as of 08-28.** Both
retired 2026-08-21, both missed their first retirement-interval check (due
08-24), neither retested since. **Pigeonhole folded into Session 9's (08-28)
Item 5** (the pigeonhole+existential synthesis problem). **Bug #1 remains
unresolved** — the one backlog item that didn't fit today, now the oldest open
item in the whole queue (overdue since 08-24, five days). Next in line, most
likely Monday 08-31 or next Friday.

---

## Failed — reset to 1-day, high priority

*These re-surface until two clean cold retrievals at ≥7-day spacing.*

- **Contrapositive narrated as contradiction, applied to own writing.** New
  2026-08-19, half right 08-21 (technique named, closing reasoning missing). Two
  genuine attempts, neither clean. Not pulled 08-25, 08-26, or 08-27 (repair slot
  went elsewhere, then the session went unattempted) — **Session 9's (08-28)
  Item 2, finally in an open slot.**
- **Divergence proof execution — evaluating a sign instead of using $|\cdot|$.**
  08-25 §2(c): blank. 08-26 R2 (fresh instance, $b_n=1+(-1)^n$): wrong, stopped at
  the identical step — about to case-split on the parity of $N+1$ instead of noting
  $|(-1)^{N+1}|=1$ regardless. 08-27: blank, session not attempted, third instance
  never reached. Still one genuine wrong attempt on record. **Session 9's (08-28)
  Item 4**, third instance ($c_n=3+5(-1)^n$), same "do I need the sign, or does
  $|\cdot|$ already answer this?" question.
- **Quantifier statements — plain-English meaning, not symbol transliteration.**
  08-25: wrong (transliteration, not explanation). 08-26: blank (not reached — ran
  out of time before the repair block finished). 08-27: blank (session not
  attempted at all). Zero clean attempts across three exposures. **Session 9's
  (08-28) Item 3**, fresh predicate ($P(x,y)$: "$x+y=0$") — if this isn't clean
  this time, it graduates from re-offer to a named, dedicated repair item.
- **Induction: state and use the hypothesis** (A2) — bug #2. Not yet re-tested;
  block starts Monday 2026-08-31.
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
