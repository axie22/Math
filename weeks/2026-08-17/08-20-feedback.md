# Feedback — Session 4 (2026-08-20)

Work graded: [`08-20-work.md`](08-20-work.md). Problems: [`08-20.md`](08-20.md).

## Headline

**The review block wasn't attempted — both R1 and R2 are blank.** Those were the
retests for two things flagged open yesterday: bug #1 relapsing on a longer proof
(√3), and the contrapositive/contradiction framing slip. Neither got new evidence
today. That's not a failure in the way a wrong answer is a failure — it's just zero
data, two days running now on both items. They carry to tomorrow.

**Core 1 (quantifier negation, brand new today) split cleanly in two.** Every problem
that was a single quantifier over one plain predicate — (a), (b), (f) — came out
correct. Every problem that required negating a *compound* predicate — an implication
in (c), a disjunction in (e) — came out wrong, and wrong in the same shape both times:
the connective-specific rule (implication → conjunction; De Morgan's swap) didn't get
applied, even though it's printed verbatim in the "Rule" box at the top of the problem
file. (d) added a third, smaller thing: the quantifier flipped correctly this time
(∃ → ∀, real progress from the calibration, where quantifiers never flipped at all),
but the domain restriction $M>0$ still got touched, becoming $M \le 0$ instead of
staying put — the original bug #3 pattern, just now showing up in 1 of 6 instead of
4 of 4.

**Core 2 (pigeonhole) is genuine progress.** (a) and (b) actually *derive* the
argument this time, instead of restating the claim the way yesterday's Core 1(b)/(c)
did. (c), which asked for the general principle in words plus a connection back to
yesterday, didn't land.

---

## Item-by-item

### R1 — reconstruct √3 irrational, land it explicitly

**Blank.** This was today's retest for bug #1 after yesterday's Core 2(b) derived
every fact and stopped one sentence short of the landing. No attempt means no new
evidence either way — it's not "still broken," it's "still unknown," and that
distinction matters for what happens next. Retest is tomorrow's review block.

### R2 — which technique did yesterday's Core 2(a) use, and how should it have ended?

**Blank.** Same treatment — this was the direct, targeted fix for yesterday's
contrapositive-narrated-as-contradiction slip. Still open, still untested. Retest
tomorrow.

### Core 1 — negate these

**(a)** $\forall n\in\mathbb{Z}, n^2\ge0 \to \exists n\in\mathbb{Z}, n^2<0$.
**Correct.** Quantifier flipped, domain restriction untouched, predicate negated —
textbook execution.

**(b)** $\exists x\in\mathbb{R}, x^2=2 \to \forall x\in\mathbb{R}, x^2\ne2$.
**Correct** (written as "$\forall x \in mathbb{R}$" — missing backslash before
`mathbb`, purely a typo, not a math error; worth a glance before submitting since it's
easy to miss when scanning your own work).

**(c)** $\forall x\in\mathbb{R}, (x>0 \implies x^2>0)$.
**Incorrect.** You wrote $\exists x\in\mathbb{R}, (x\le0 \implies x^2\le0)$ — the
quantifier flipped correctly, but the implication itself was left as an implication
and both sides just got their inequality flipped. That produces something closer to
the *inverse* of the original (¬A ⟹ ¬B), which isn't what negation means here.

The rule, stated right above this problem in the file: $\lnot(A\implies B) \equiv A \wedge \lnot B$. $A$ (the antecedent, $x>0$) is **not** negated — it becomes a conjunct exactly as written. Only $B$ (the consequent, $x^2>0$) gets negated.

**Correct answer:** $\exists x\in\mathbb{R}, \big(x>0 \wedge x^2\le0\big)$.

**(d)** Bounded: $\exists M>0, \forall n\in\mathbb{N}, |a_n|\le M$.
**Incorrect, but closer than it looks.** You wrote
$\forall M\le0, \exists n\in\mathbb{N}, |a_n|>M$ — the quantifier swap ($\exists\to \forall$, $\forall\to\exists$) is exactly right, and the final inequality flip ($\le\to>$) is exactly right. The one broken piece: $M>0$ is a domain restriction, not
part of what's being asserted, so it should stay $M>0$ — you wrote $M\le0$. This is
the original bug #3 move, but notice it only touched one restriction out of several
across today's six problems, not all of them the way the calibration did.

**Correct answer:** $\forall M>0, \exists n\in\mathbb{N}, |a_n|>M$.

**(e)** $\forall x\in S, (P(x)\vee Q(x))$.
**Incorrect.** You wrote $\exists x\in \mathbb{S}, (P(x)\vee\lnot Q(x))$ — the
quantifier flipped, but neither De Morgan move happened: $P(x)$ should have become
$\lnot P(x)$ (it didn't), and $\vee$ should have swapped to $\wedge$ (it didn't).
Right now the negation of "$P$ or $Q$" reads as "$P$ or not-$Q$," which isn't the
opposite of the original statement at all — "not (raining or snowing)" means "not
raining **and** not snowing," not "raining or not snowing."

**Correct answer:** $\exists x\in S, \big(\lnot P(x) \wedge \lnot Q(x)\big)$.

**(f)** Negate $\forall x\in\mathbb{R}, x^2\ge x$, then prove it.
**Correct, all the way through.** Negation: $\exists x\in\mathbb{R}, x^2<x$. Witness
$x=0.5$: $0.5^2=0.25<0.5$. ✓. This is a real little proof — witness plus verification
— not just a mechanical flip, and it's clean.

**Pattern worth naming:** the failures aren't random across the six. Every atomic
statement (one quantifier, one plain predicate) is correct. Every statement built from
a connective — implication in (c), "or" in (e) — is wrong, and wrong because the
connective-specific transformation didn't happen. That's a narrower, more precise
finding than "quantifier negation is a gap": the mechanical ∀/∃ flip is solid now,
and what's missing is specifically the second half of the rule, the part that
restructures what's *inside* the quantifier.

### Core 2 — pigeonhole

**(a)** Negation of "$f$ injective" ($f(a)=f(b)\implies a=b$).
**Correct.** "$\exists a,b$ where $a\ne b$ and $f(a)=f(b)$" is exactly
$\exists a,b, \big(f(a)=f(b)\wedge a\ne b\big)$ — the right shape.

Worth noticing: this is also a negation of an implication, the same move that failed
in Core 1(c). One likely reason it worked here — "how to disprove injective" is
written out directly in lesson §1 and §8 as a standing recipe ("exhibit $a\ne b$ with
$f(a)=f(b)$"), so this may be a recalled shape rather than the general rule freshly
applied. Worth testing on an implication you *haven't* seen a stock disproof-recipe
for, to see whether the rule itself has actually transferred.

**(b)** No injective $f:\{1,\dots,6\}\to\{1,\dots,5\}$ exists.
**Correct, and a real repair of yesterday's gap.** Setup states exactly the
assumption being contradicted. The argument itself — 6 elements forced into 5 outputs
means some output repeats, i.e. $\exists a\ne b, f(a)=f(b)$, contradicting
injectivity — is the actual pigeonhole mechanism, derived rather than asserted. And
it lands: the contradiction is named explicitly in the last sentence. That's worth
flagging against the bug #1 concern from yesterday — this proof, while shorter than
the √3 one, did carry all the way to an explicit landing.

**(c)** General principle + connection to yesterday.
**Weak.** "It works since the domain and codomain both have finite size" isn't the
principle — finiteness alone doesn't force a collision (an injection
$\{1,2\}\to\{1,2,3\}$ exists just fine, both sets finite). The actual condition is
**size**: $|A|>|B|$, both finite. And the question asked for a specific connection
to yesterday's Core 1(b) (same-size finite sets), which didn't get made.

**The general principle:** if $A, B$ are finite and $|A|>|B|$, no injective function
$A\to B$ exists — more inputs than possible distinct outputs forces two inputs to
share one.

**The connection:** yesterday's case was $|A|=|B|$ exactly — the boundary case, where
an injective map is forced to be surjective too because there's no room left over
once every input has a distinct output. Today's case is $|A|>|B|$ — strictly too many
inputs, where injective is impossible outright. Same finite-counting argument, applied
on either side of the equality.

---

## What this changes

- **Bug #1 (landing) and contrapositive-applied: still open, no new data two days
  running.** Not closing them, not escalating them either — genuinely unknown until
  they're actually attempted. If review-block time keeps getting displaced by Core,
  that's worth noticing out loud: the review block is 10 minutes for a reason, and it
  going first matters more than it looks like it does.
- **Quantifier negation, split into two tracked items going forward.** Atomic
  ∀/∃-over-one-predicate negation: clean 3/3 today (a, b, f) — this piece is holding.
  Compound-predicate negation (implications, De Morgan on and/or): 0/2 on fresh
  application (c, e), 1/1 on a memorized shape (Core 2a) — this piece is the real
  remaining gap, and it's narrower and more specific than the calibration's finding.
  The domain-restriction sub-bug also isn't fully retired — it resurfaced once (d).
- **Pigeonhole: mechanism now demonstrated cleanly** (Core 2a, 2b) — real repair of
  yesterday's restate-without-deriving gap. **General principle + cross-session
  connection still missing** (2c) — that's what's weak now, not the derivation itself.
- **REVIEW-QUEUE.md and STATE.md updated accordingly** — see those files for the
  specific interval changes.

**Tomorrow (2026-08-21) is the scheduled Friday review day regardless of today's
result** — no new material either way. It's built to prioritize exactly the four open
items above: the two blank review-block retests, compound-predicate negation, and the
pigeonhole general principle — plus the timed Section C redo that's been outstanding
since the calibration.
