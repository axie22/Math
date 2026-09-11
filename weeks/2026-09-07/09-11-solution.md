# Solutions — 2026-09-11 (Session 19, Friday review)

*Posted 2026-09-11, one-day lag, per the standing rule — regardless of whether
`09-11-work.md` has anything in it.*

---

## 1(a). Setup discipline — divisibility by 6

**Claim.** If $m$ and $n$ are both divisible by 6, then $m+n$ is divisible by 6.

**Setup only, as asked:**

> Let $m,n\in\mathbb{Z}$ with $6\mid m$ and $6\mid n$.

That's it — hypothesis named, nothing else. **The trap this drills:** writing
"want to show $6\mid(m+n)$" as part of Setup. The goal belongs in Land, not
Setup — Setup's whole job is naming what you're given, not previewing what
you're going for. Folding the conclusion in early is exactly the move that
produces proofs which *assume* the thing they're supposed to derive.

*For completeness, the rest of the proof:* unfold — $m=6a$, $n=6b$ for some
$a,b\in\mathbb{Z}$. Work — $m+n=6a+6b=6(a+b)$. Land — since $a+b\in\mathbb{Z}$,
this shows $6\mid(m+n)$. ∎

---

## 1(b). Quantifier negation — compound predicate

**Statement:**
$$\forall x\in\mathbb{R},\ \big(x>0 \implies \exists y\in\mathbb{R}\ (y^2=x \text{ and } y>0)\big)$$

**Technique:** §5's algorithm — walk left to right, flip every quantifier,
leave every domain restriction alone, negate the implication last using
$\lnot(P\implies Q)\equiv P\wedge\lnot Q$.

$$\forall x\in\mathbb{R} \;\rightsquigarrow\; \exists x\in\mathbb{R}$$

Inside, negate the implication: $\lnot\big(x>0\implies\exists y(\dots)\big)$
becomes $x>0 \wedge \lnot\exists y\in\mathbb{R}(y^2=x\text{ and }y>0)$, and the
inner $\exists$ becomes $\forall y\in\mathbb{R},\ \lnot(y^2=x\text{ and }y>0)$,
which by De Morgan is $y^2\ne x \text{ or } y\le 0$.

**In symbols:**
$$\exists x\in\mathbb{R}\ \Big(x>0\ \wedge\ \forall y\in\mathbb{R}\,(y^2\ne x\ \text{or}\ y\le 0)\Big)$$

**In plain English:** there's some positive real number that has no positive
real square root.

**The step most people get wrong here:** treating $x>0$ as a quantifier that
flips (into $x\le 0$ or similar), when it's actually the domain-restriction of
the outer $\forall x$ shorthand — $\forall x\in\mathbb{R}\,(x>0\implies\dots)$
is not the same syntactic shape as $\forall\varepsilon>0$, and the whole
implication (not just the restriction) has to be negated as one unit via
$P\wedge\lnot Q$, not term-by-term.

---

## 1(c). Quantifier order — $xy=1$

$P(x,y):\ xy=1$ over $x,y\in\mathbb{R}\setminus\{0\}$.

**True:** $\forall x\,\exists y\,P(x,y)$. **False:** $\exists y\,\forall x\,P(x,y)$.

**Proof of the true one.** Let $x\in\mathbb{R}\setminus\{0\}$ be arbitrary.
Choose $y=\dfrac1x$ — well-defined and nonzero since $x\ne0$. Then
$xy=x\cdot\frac1x=1$, so $P(x,y)$ holds. Since $x$ was arbitrary,
$\forall x\,\exists y\,P(x,y)$. ∎ (The witness $y=1/x$ depends on $x$ — that
dependence is exactly what the next part shows can't be removed.)

**Why the other is false, one sentence:** if a single $y$ worked for every
$x$, it would have to satisfy both $1\cdot y=1$ and $2\cdot y=1$
simultaneously, forcing $y=1$ and $y=\tfrac12$ at once — impossible, so no
such $y$ exists.

**The technique to name:** $\forall\exists$ lets the witness *depend on* the
universally-quantified variable; $\exists\forall$ demands one witness that
survives contact with *every* choice of the other variable. Disproving the
$\exists\forall$ form is a counterexample to a $\forall$ statement (§7) nested
one level in: fix any candidate $y$, then exhibit one $x$ that breaks it.

---

## 1(d). Induction — $2^n$ subsets

**Claim.** A set of size $n$ has exactly $2^n$ subsets.

**Base case** ($n=0$): the empty set has exactly one subset — itself, $\varnothing$
— and $2^0=1$. ✓ **This is the base case most people skip**, jumping to $n=1$
and getting $2^1=2$ (right answer, wrong reason — it hides that $n=0$ is
where the formula actually starts being non-obvious).

**Inductive step.** Assume a set of size $n$ has $2^n$ subsets (induction
hypothesis). Let $S$ be a set of size $n+1$. Fix any element $x\in S$ and let
$S'=S\setminus\{x\}$, so $|S'|=n$.

**Use the hypothesis:** every subset of $S$ falls into exactly one of two
disjoint kinds — those that don't contain $x$, and those that do.

- Subsets not containing $x$ are exactly the subsets of $S'$: by the
  hypothesis, there are $2^n$ of them.
- Subsets containing $x$ are exactly $\{x\}\cup T$ for $T$ a subset of $S'$ —
  a bijection with the subsets of $S'$, so there are also $2^n$ of them.

These two kinds are disjoint and cover every subset of $S$, so
$$|\mathcal P(S)| = 2^n + 2^n = 2\cdot 2^n = 2^{n+1},$$
which is the claim at $n+1$. ∎

**The move that makes this a genuinely different instance from Session 11's**
(09-01): that version built the count directly as a case-split recursion;
this one names the bijection $T\mapsto\{x\}\cup T$ explicitly, which is the
same idea Phase 1 will reuse when counting bases of subspaces.

---

## 2. Synthesis — negation meets supremum

Recall part 2 of $s=\sup A$: $\forall\varepsilon>0\,\exists a\in A\,(a>s-\varepsilon)$.

**(a) Negation**, via §5's algorithm — the domain restriction $\varepsilon>0$
is untouched, only the quantifiers flip and the final inequality negates:
$$\exists\varepsilon>0\ \forall a\in A\ (a\le s-\varepsilon)$$

**(b) What it means.** There's some *specific* tolerance $\varepsilon>0$ for
which every element of $A$ sits at or below $s-\varepsilon$ — in other words,
$s-\varepsilon$ is itself an upper bound for $A$, and it's strictly smaller
than $s$ (since $\varepsilon>0$). An upper bound with a strictly smaller upper
bound below it can't be the *least* one, so this statement holding for some
candidate $s$ is exactly a proof that $s\ne\sup A$ (or at least that $s$ fails
the "least" half of the definition, even if it passes the "upper bound" half).

**(c) Apply it.** $A=\{1,2,3\}$, candidate $s=5$. Want $\varepsilon>0$ with
every $a\in A$ satisfying $a\le5-\varepsilon$. Take $\varepsilon=2$:
$5-2=3$, and indeed $1,2,3\le3$. So $\varepsilon=2$ witnesses
$5\ne\sup A$ — a smaller upper bound (namely $3$) already exists below $5$.
(Any $\varepsilon\le2$ works, e.g. $\varepsilon=1$ gives the bound $4$, also
satisfied by every element — the exercise only needs one.)

**(d) $\sup\{3-\tfrac1n:n\in\mathbb{N}\}=3$, from scratch.**

*Upper-bound part:* for every $n\ge1$, $\tfrac1n>0$, so $3-\tfrac1n<3$. Hence
$3$ is an upper bound.

*$\varepsilon$-part:* let $\varepsilon>0$. Want $n\in\mathbb{N}$ with
$3-\tfrac1n>3-\varepsilon$, i.e. $\tfrac1n<\varepsilon$, i.e.
$n>\tfrac1\varepsilon$. **By the Archimedean property** — $\mathbb{N}$ is
unbounded above in $\mathbb{R}$ — such an $n$ exists; pick one. Then
$3-\tfrac1n>3-\varepsilon$, as required.

Both parts hold, so $\sup\{3-\tfrac1n\}=3$. ∎

**The step everyone skips silently:** naming the Archimedean property as the
reason $n$ exists, rather than just asserting "pick $n$ large enough." That
assertion is true, but it's true *because of* a specific, citable fact about
$\mathbb{R}$ — the same fact every $\varepsilon$–$N$ convergence proof leans
on without saying so.

---

## 3. Stretch — a sequence converging to $\sup A$ (optional)

**Claim.** If $A\subseteq\mathbb{R}$ is nonempty and bounded above, there is a
sequence $a_1,a_2,\dots\in A$ with $a_n\to\sup A$.

**Proof.** Let $s=\sup A$. For each $n\in\mathbb{N}$, apply part 2 of the sup
definition with $\varepsilon=\tfrac1n$: there exists $a_n\in A$ with
$a_n>s-\tfrac1n$. Also $a_n\le s$ for every $n$, since $s$ is an upper bound.
So
$$s-\tfrac1n < a_n \le s \qquad\text{for every }n.$$
As $n\to\infty$, $\tfrac1n\to0$, so both ends of that sandwich converge to
$s$; by the squeeze theorem, $a_n\to s=\sup A$. ∎

**The part that's easy to half-do:** producing $a_n>s-\tfrac1n$ and stopping,
without also noting $a_n\le s$ — you need *both* sides of the sandwich to
invoke the squeeze theorem, and the upper side is free (it's just "$s$ is an
upper bound"), but it has to be said.
