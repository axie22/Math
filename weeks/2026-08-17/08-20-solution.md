Problems: [08-20.md](08-20.md) · Your work: [08-20-work.md](08-20-work.md) · Grading: [08-20-feedback.md](08-20-feedback.md)

# Session 4 Solutions — 2026-08-20

---

## Core 1 — negate these

**Rule used throughout:** walk left to right. Each quantifier flips. Each domain
restriction stays exactly as written. $A\implies B$ negates to $A\wedge\lnot B$.
"And"/"or" swap under negation (De Morgan).

### (a) $\forall n\in\mathbb{Z},\ n^2\ge0$

$$\exists n\in\mathbb{Z},\ n^2<0$$

Single quantifier, single predicate — flip the quantifier, negate $\ge$ to $<$, leave
$n\in\mathbb{Z}$ alone.

### (b) $\exists x\in\mathbb{R},\ x^2=2$

$$\forall x\in\mathbb{R},\ x^2\ne2$$

### (c) $\forall x\in\mathbb{R},\ (x>0 \implies x^2>0)$

$$\exists x\in\mathbb{R},\ \big(x>0 \wedge x^2\le0\big)$$

**The step most people get wrong:** treating $x>0$ as if the whole thing were "$\forall
x$ satisfying $x>0$" (a domain restriction, which would stay put) rather than as the
antecedent of an implication (which becomes a conjunct, unchanged, while only the
consequent gets negated). Both readings *look* similar on the page — the giveaway is
that a domain restriction narrows which $x$ you're quantifying over from the start,
while an implication's antecedent is part of the claim itself.

### (d) Bounded: $\exists M>0,\ \forall n\in\mathbb{N},\ |a_n|\le M$. Negate for unbounded.

$$\forall M>0,\ \exists n\in\mathbb{N},\ |a_n|>M$$

**In words:** no matter how large a bound you propose, some term of the sequence
exceeds it. **The step most people get wrong:** touching the $M>0$ restriction. It's
scope-setting ("we're talking about positive bounds"), not part of what's being
negated — only the $\exists/\forall$ in front of it flips.

### (e) $\forall x\in S,\ (P(x)\vee Q(x))$

$$\exists x\in S,\ \big(\lnot P(x)\wedge\lnot Q(x)\big)$$

**The step most people get wrong:** negating only one disjunct, or forgetting to swap
$\vee\to\wedge$. "Not (P or Q)" means neither happens — both sides get negated **and**
the connective flips. Test it with a sentence: "not (it's raining or snowing)" = "it's
not raining **and** it's not snowing," never "it's not raining or it's snowing."

### (f) Negate $\forall x\in\mathbb{R},\ x^2\ge x$, then prove the negation

**Negation:** $\exists x\in\mathbb{R},\ x^2<x$.

**Proof.** Take $x=\tfrac12$. Then $x^2 = \tfrac14$, and $\tfrac14 < \tfrac12$. So
$x=\tfrac12$ satisfies $x^2<x$, proving the negation is true. $\blacksquare$

(Any $x\in(0,1)$ works — the inequality $x^2<x$ rearranges to $x(x-1)<0$, true exactly
on that interval. $\tfrac12$ is just the simplest choice.)

---

## Core 2 — pigeonhole

### (a) Negation of "$f$ is injective" ($f(a)=f(b)\implies a=b$)

$$\exists a,b,\ \big(f(a)=f(b)\ \wedge\ a\ne b\big)$$

Same implication-negation rule as 1(c), applied to a definition instead of an
inequality: keep the antecedent ($f(a)=f(b)$) as a conjunct, negate the consequent
($a=b\to a\ne b$).

### (b) No injective $f:\{1,\dots,6\}\to\{1,\dots,5\}$ exists

*Proof.* Suppose, for contradiction, that $f:\{1,\dots,6\}\to\{1,\dots,5\}$ is
injective. By definition, injective means the six values $f(1),\dots,f(6)$ are
pairwise distinct — six *distinct* elements of $\{1,\dots,5\}$. But $\{1,\dots,5\}$
has only five elements total, so it cannot contain six distinct elements. This is a
contradiction. Hence no such injective $f$ exists. $\blacksquare$

**Technique to name:** contradiction, with the pigeonhole counting argument doing the
actual work in the middle. **The step most people get wrong:** stating the conclusion
("it can't be injective") without deriving *why* — the derivation is specifically
"$n$ distinct outputs can't fit inside a codomain smaller than $n$," and it has to
appear on the page, not just the conclusion it implies.

### (c) General principle + connection to yesterday

**General principle (pigeonhole):** if $A,B$ are finite sets with $|A|>|B|$, no
injective function $f:A\to B$ exists. More inputs than the codomain has room for
forces at least two inputs to collide.

**Connection to yesterday:** yesterday's Core 1(b) was the equal-size case,
$|A|=|B|$, where the claim runs the *other* direction — an injective $f$ is
automatically surjective, because using up all $|A|$ distinct outputs in a codomain
of the same size $|B|$ leaves nothing uncovered. Today's problem is the boundary
pushed one step further: $|A|>|B|$ strictly, where injective isn't just "forced to be
surjective," it's *impossible*. Both are the same finite-counting fact — "you can't
fit more distinct things into a smaller finite set than it holds" — read on either
side of $|A|=|B|$.

---

## Stretch — negation of surjective, applied to $f(n)=2n$

*(optional — not attempted; solution posted anyway, same one-day lag as always.)*

### (a) Negation of "$f$ is surjective" ($\forall y\in\text{codomain},\exists x, f(x)=y$)

$$\exists y\in\text{codomain},\ \forall x,\ f(x)\ne y$$

### (b) Applied to $f(n)=2n$, $f:\mathbb{Z}\to\mathbb{Z}$

**Witness:** $y=1$.

**Verification.** Suppose, for some $x\in\mathbb{Z}$, $f(x)=1$. Then $2x=1$, so
$x=\tfrac12$. But $\tfrac12\notin\mathbb{Z}$ — no integer $x$ satisfies this. So
$f(x)\ne1$ for every $x\in\mathbb{Z}$, which is exactly the negation's remaining
condition. Hence $f$ is not surjective. $\blacksquare$

Notice this is the same non-surjectivity argument from 08-19's Core 1(a), just now
explicitly framed through the negation's $\exists y,\forall x$ structure instead of
argued freehand — the mechanical rule and the freehand argument are the same fact
seen two ways.
