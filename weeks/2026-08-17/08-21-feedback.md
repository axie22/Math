# Feedback — Session 5 (2026-08-21, review day)

## Verdict

**Bug #1 is closed. Bug #2 is untested. Bug #3 is the only thing still actually broken —
and it's specifically the compound-predicate half of it.**

| Item | Result |
|---|---|
| C1 chain rule | ✅ correct |
| C2 Taylor | ⬜ blank (2nd time) — **retired from testing, moved to teaching** |
| C3 integration by parts | ✅ correct |
| 2a √3 from memory | ✅ **landed it.** Bug #1 closed |
| 2b contrapositive framing | 🟡 half |
| 2c(i) negate an implication | ❌ |
| 2c(ii) negate a conjunction | ❌ |
| 2d pigeonhole in words | ✅ |
| 3a pigeonhole proof | ✅ |
| 3b why finiteness | ✅ good |

---

## What's now closed

**2a — you landed it.** Third attempt, but this time the last sentence exists:
*"…we said that $\gcd(a,b)=1$ but this cannot be true since $3\mid b$ and $3\mid a$, so
we have reached a contradiction."* That's the sentence that was missing on Tuesday and
Thursday. **Bug #1 — stopping at the setup — is retired.** It will not be repaired
again; it moves to the review queue at a 3-day interval and that's it.

**3a and 3b are the best work in the repo so far.** 3a is a correct general proof, not a
recitation of Thursday's specific case. 3b explains *why* the counting argument needs
finiteness in your own words — "there is no concept of running out of room" is exactly
right, and you connected it to $f(n)=2n$ without being walked through it. That is the
first genuine synthesis you've produced.

**C1 and C3 are correct.** Chain rule and integration by parts are fine — your C1
middle line is written sloppily (it reads as if you multiplied an extra factor) but the
answer $\frac{e^{2x}}{1+e^{2x}}$ is right and the structure is right. C3 is clean.

**Pigeonhole, injective/surjective, unfolding, contrapositive/contradiction, divisibility
transitivity — all retired.** They will not appear again as repair items.

---

## What's still broken — and it's one rule

Every compound negation this week failed the same way. Five of them:

| Statement | You wrote | Correct |
|---|---|---|
| Thu (c) $\lnot\forall x(x>0 \implies x^2>0)$ | $\exists x(x \le 0 \implies x^2 \le 0)$ | $\exists x(x>0 \wedge x^2 \le 0)$ |
| Thu (d) unbounded | $\forall M \le 0, \dots$ | $\forall M > 0, \exists n, \|a_n\| > M$ |
| Thu (e) $\lnot\forall x(P \vee Q)$ | $\exists x(P \vee \lnot Q)$ | $\exists x(\lnot P \wedge \lnot Q)$ |
| Fri 2c(i) $\lnot\forall x(x<0 \implies x^2>0)$ | $\exists x(x<0 \implies x^2 \le 0)$ | $\exists x(x<0 \wedge x^2 \le 0)$ |
| Fri 2c(ii) $\lnot\exists n(\text{even} \wedge n>100)$ | $\forall n(\text{even} \vee n<100)$ | $\forall n(\text{odd} \vee n \le 100)$ |

Meanwhile every *atomic* negation was correct — Thursday (a), (b), (f) and Core 2(a) all
clean, and (f)'s witness $x=0.5$ was properly verified.

So the split is sharp: **quantifiers you now handle correctly. Connectives you don't.**

Three specific sub-errors, all fixable:

1. **The implication survives.** $\lnot(A \implies B)$ is $A \wedge \lnot B$ — the arrow
   *disappears* and becomes an "and." You kept the arrow in both (c) and 2c(i). This is
   the big one: an implication is not a statement you negate piecewise, it's a statement
   that becomes a conjunction.
2. **The antecedent gets negated too.** In (c) and 2c(i) you flipped $x>0$ to $x\le 0$.
   The antecedent is *asserted*, not negated — you're claiming a witness that satisfies
   the hypothesis and fails the conclusion.
3. **De Morgan half-applied.** In (e) you negated $Q$ but not $P$, and kept $\vee$
   instead of swapping to $\wedge$. In 2c(ii) you swapped the connective correctly but
   left "n is even" un-negated and turned $n > 100$ into $n < 100$ instead of $n \le 100$.

**One more:** Thursday's (d) is bug #3 in its original form — you negated the domain
restriction $M > 0$ into $M \le 0$. Everything else that week left restrictions alone,
so this is a relapse under load rather than a persistent misunderstanding, but it's the
reason Monday leads with a restriction-vs-connective drill.

**2b is half right.** "We used the contrapositive" ✅. But
"$3 \nmid n \implies 3 \nmid n^2$" is the contrapositive *statement*, not the ending. The
proof should have closed: *"…so $3 \nmid n^2$. This proves the contrapositive, and
therefore $3 \mid n^2 \implies 3 \mid n$."* The missing move is saying **why proving the
contrapositive settles the original claim.**

---

## C2 (Taylor) — changing approach

Blank in the calibration, blank again Friday. Per the new rule, an item that comes back
blank twice stops being a test question — **re-asking a third time produces no
information.** You're not failing to retrieve Taylor series; you never had it fluently
enough for retrieval to be the right frame.

So it stops being a review-block item and becomes a **taught** item: a dedicated calculus
repair session (Wednesday), covering Taylor with remainder properly, because Phase 3
(concentration inequalities) and Phase 4 (smoothness, second-order conditions) both lean
on it hard.

---

## One thing you can do that costs 20 seconds

**Every timing field and every "where I got stuck" box has been blank all week — all
four sessions.**

That's not a nag about diligence; it's the single biggest reason this week felt
repetitive. When Session 2's injective/surjective came back blank, there was no way to
tell whether you'd run out of time or been stuck — so it was re-issued Tuesday, and then
mined for follow-ups Wednesday, Thursday, *and* Friday. One line — "ran out of time" —
would have moved it to the top of Tuesday and closed it in one pass instead of four.

Two words in that box is worth more than a fifth correct proof.
