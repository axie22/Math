Problems: [08-24.md](08-24.md) · Your work: [08-24-work.md](08-24-work.md)

# Session 6 Solutions — 2026-08-24

*Posted on the usual one-day lag even though 08-24 wasn't attempted (the work file came
back entirely blank) — the lag rule doesn't depend on completion, and today's problems
(08-25) are fresh instances of the same skills, not this same content, so nothing here
gives away today's answers.*

---

## 0. Review

### R1 — negate $\forall x\in\mathbb{R},\ (x>2\implies x^2>4)$

Rule: $\lnot(A\implies B)\equiv A\wedge\lnot B$ — the arrow disappears, becomes "and";
the antecedent is asserted, the consequent negated.

$$\exists x\in\mathbb{R},\ \big(x>2 \wedge x^2\le4\big)$$

---

## 1. Connectives under negation

### (a) $\forall n\in\mathbb{Z},\ (n>5\implies n^2>25)$

Rule: implication $\to$ conjunction, antecedent kept, consequent negated.

$$\exists n\in\mathbb{Z},\ \big(n>5 \wedge n^2\le25\big)$$

### (b) $\exists x\in\mathbb{R},\ (x\ge1\wedge x\le0)$

Rule: quantifier flips; De Morgan on "and" $\to$ "or," each side negated.

$$\forall x\in\mathbb{R},\ \big(x<1 \vee x>0\big)$$

### (c) $\forall f,\ (f\text{ differentiable}\implies f\text{ continuous})$

$$\exists f,\ \big(f\text{ differentiable} \wedge f\text{ not continuous}\big)$$

**Reading the answer:** this negation is *false* — differentiable functions are always
continuous, so no such $f$ exists — but producing the negation correctly is a separate
skill from evaluating its truth value.

### (d) $\forall x\in\mathbb{R},\ (x\in\mathbb{Q}\vee x\in\mathbb{R}\setminus\mathbb{Q})$

$$\exists x\in\mathbb{R},\ \big(x\notin\mathbb{Q} \wedge x\notin\mathbb{R}\setminus\mathbb{Q}\big)$$

Also false (every real is rational or irrational), for the same reason as (c).

### (e) $\forall\varepsilon>0,\ \exists\delta>0,\ (|x-a|<\delta\implies|f(x)-f(a)|<\varepsilon)$

Three moves: flip $\forall\varepsilon\to\exists\varepsilon$ (restriction $\varepsilon>0$
untouched), flip $\exists\delta\to\forall\delta$ (restriction $\delta>0$ untouched),
implication $\to$ conjunction.

$$\exists\varepsilon>0,\ \forall\delta>0,\ \big(|x-a|<\delta \wedge |f(x)-f(a)|\ge\varepsilon\big)$$

**The step most people get wrong:** touching $\varepsilon>0$ or $\delta>0$ — both are
domain restrictions (they say *which* $\varepsilon,\delta$ we mean), not the quantified
claim itself, so they never change under negation.

### (f) — trap. Negate $\exists n\in\mathbb{N},\ (n\text{ prime}\wedge n>10^6)$

$$\forall n\in\mathbb{N},\ \big(n\text{ not prime} \vee n\le10^6\big)$$

**True or false:** false. The negation claims every natural number is either not prime
or at most a million — but there are primes larger than $10^6$ (infinitely many, by
Euclid's proof), so the negation fails on any such prime. Since the negation is false,
the original statement is true, consistent with the fact that arbitrarily large primes
exist.

---

## 2. Using a negation to prove divergence

### (a) $\lnot(a_n\to L)$

Starting from $\forall\varepsilon>0,\exists N\in\mathbb{N},\forall n>N,\ |a_n-L|<\varepsilon$:

$$\exists\varepsilon>0,\ \forall N\in\mathbb{N},\ \exists n>N,\ |a_n-L|\ge\varepsilon$$

### (b) The three proof obligations

1. **Choose a specific $\varepsilon>0$** — this must be fixed once, at the start, and
   used throughout.
2. **Let $N\in\mathbb{N}$ be arbitrary** — you don't get to pick $N$; the proof must
   work no matter what $N$ your reader hands you.
3. **Construct an explicit $n>N$** (typically as a formula in terms of $N$) and show
   $|a_n-L|\ge\varepsilon$ with real arithmetic, not "clearly."

### (c) Prove $(-1)^n$ does not converge to $0$

**$\varepsilon = 1$.** Let $N\in\mathbb{N}$ be arbitrary. Take $n = N+1$. Then
$a_n = (-1)^{N+1} = \pm1$, so $|a_n - 0| = 1 \ge 1 = \varepsilon$. Since $N$ was
arbitrary and $n=N+1>N$ always, this shows $(-1)^n\not\to0$. $\blacksquare$

**The step most people get wrong:** picking $\varepsilon$ that depends on $N$ (backwards
— $\varepsilon$ must be fixed before $N$ is introduced), or asserting $|a_n-0|\ge1$
without noting that $(-1)^{N+1}$ is always exactly $\pm1$ regardless of parity of $N$,
so the bound holds unconditionally.

### (d) Prove $(-1)^n$ converges to no $L$ at all

Take $\varepsilon = 1$ (doesn't depend on $L$ — the hint's key move). Let $L\in\mathbb{R}$
and $N\in\mathbb{N}$ be arbitrary. Consider $n=N+1$ and $n'=N+2$: these are consecutive,
so $a_n$ and $a_{n'}$ are $1$ and $-1$ in some order, and $|a_n - a_{n'}| = 2$. By the
triangle inequality, $|a_n-L| + |a_{n'}-L| \ge |a_n-a_{n'}| = 2$, so at least one of
$|a_n-L|,|a_{n'}-L|$ is $\ge 1 = \varepsilon$. Either way, some $n>N$ has
$|a_n-L|\ge\varepsilon$. Since $L$ and $N$ were arbitrary, $(-1)^n$ converges to no
$L$. $\blacksquare$

**The step most people get wrong:** trying to pick $\varepsilon$ depending on $L$ (e.g.
"$\varepsilon = |L|$"), which breaks down when $L=0$ or produces a proof that only
handles one $L$ at a time instead of all of them at once.

---

## 3. Order of the quantifiers

### (a) $P(x,y)$: "$y>x$" over $\mathbb{R}$

**$\forall x\,\exists y\,P(x,y)$ is true.** *Proof:* given any $x\in\mathbb{R}$, let
$y = x+1$. Then $y = x+1 > x$, so $P(x,y)$ holds. Since $x$ was arbitrary, this proves
the claim. $\blacksquare$

**$\exists y\,\forall x\,P(x,y)$ is false.** *Negation:* $\forall y\,\exists x,\ y\le x$.
*Counterexample:* let $y$ be any real number, and take $x=y$. Then $y\le x$ (in fact
$y=x$), so $P(x,y)$ ("$y>x$") fails for this $x$. Since $y$ was arbitrary, no single $y$
works for every $x$, proving $\exists y\,\forall x\,P(x,y)$ false.

### (b) Plain English

$\forall x\exists y$: *"every real number has some larger real number"* — true, and
unsurprising, since $y$ is allowed to chase $x$.

$\exists y\forall x$: *"there is a single real number larger than every real number"* —
false; no number is bigger than all of them, including itself and everything above it.

### (c) Swapping $\varepsilon$ and $N$ in the convergence definition

$$\exists N\in\mathbb{N},\ \forall\varepsilon>0,\ \forall n>N,\ |a_n-L|<\varepsilon$$

This says: there's a single $N$, fixed in advance, such that *every* term past index
$N$ is within *every* positive $\varepsilon$ of $L$ — including arbitrarily tiny ones.
But if $|a_n-L|<\varepsilon$ for every $\varepsilon>0$, that forces $|a_n-L|=0$, i.e.
$a_n = L$ exactly. So the swapped statement says: **the sequence becomes exactly equal
to $L$ from some point on and stays there** — eventually constant, not just eventually
close. **Which sequences satisfy it:** exactly the eventually-constant sequences (e.g.
$a_n = 5$ for all $n$, or $a_n = 1/n$ for $n\le3$ then $a_n=0$ for $n>3$) — a much
narrower class than "convergent."

---

## Stretch — prove $1/n\to0$

Given $\varepsilon>0$, choose $N = \lceil 1/\varepsilon\rceil$ (any natural number
$>1/\varepsilon$ works). For $n>N$: $n > 1/\varepsilon \implies 1/n < \varepsilon$
(since $n>0$). Also $|1/n - 0| = 1/n$ (as $n\ge1>0$, $1/n>0$). So $|1/n-0| =
1/n<\varepsilon$ for all $n>N$. Since $\varepsilon$ was arbitrary, $1/n\to0$.
$\blacksquare$

**The step most people get wrong:** picking $N$ without checking it's actually a
natural number ($1/\varepsilon$ itself might not be), which is why the ceiling function
(or "$N$ = any integer exceeding $1/\varepsilon$") matters — it's a one-word fix but an
easy thing to skip.
