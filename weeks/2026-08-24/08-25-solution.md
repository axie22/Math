Problems: [08-25.md](08-25.md) · Your work: [08-25-work.md](08-25-work.md)

# Session 6 (retry) Solutions — 2026-08-25

---

## 0. Review

### R1 — negate $\exists x\in\mathbb{Q},\ x^3=2$

Rule: flip $\exists\to\forall$, domain untouched, negate the predicate.

$$\forall x\in\mathbb{Q},\ x^3\neq2$$

---

## 1. Connectives under negation

### (a) $\forall t\in\mathbb{R},\ (t\ge5\implies2t-1\ge9)$

Rule: negation of $\forall$ (becomes $\exists$), then negation of $\implies$
($A\implies B$ becomes $A\wedge\lnot B$ — antecedent kept, consequent negated).

$$\exists t\in\mathbb{R},\ (t\ge5\ \wedge\ 2t-1<9)$$

### (b) $\exists k\in\mathbb{Z},\ (k\text{ odd}\wedge k<-50)$

Rule: negation of $\exists$ (becomes $\forall$), then De Morgan on the conjunction
($A\wedge B$ becomes $\lnot A\vee\lnot B$).

$$\forall k\in\mathbb{Z},\ (k\text{ even}\ \vee\ k\ge-50)$$

### (c) $\forall\delta>0,\ (|x|<\delta\implies x^2<\delta)$

Rule: negation of $\forall$, restriction $\delta>0$ untouched, negation of
$\implies$.

$$\exists\delta>0,\ (|x|<\delta\ \wedge\ x^2\ge\delta)$$

### (d) $\forall M>0,\ \exists n\in\mathbb{N},\ (n>M\implies a_n<0)$

Four separate moves: $\forall M>0\to\exists M>0$ (restriction untouched);
$\exists n\in\mathbb{N}\to\forall n\in\mathbb{N}$ (restriction untouched);
$\implies$ becomes $\wedge$; $a_n<0$ becomes $a_n\ge0$.

$$\exists M>0,\ \forall n\in\mathbb{N},\ (n>M\ \wedge\ a_n\ge0)$$

**The step most people get wrong:** touching $M>0$ or $n\in\mathbb{N}$ — both are
domain restrictions, not part of the quantified claim, so neither one ever changes.

### (e) Negate $\exists x\in\mathbb{R},\ (x>0\vee x=0)$; true or false?

$$\forall x\in\mathbb{R},\ (x<0)$$

**False.** Take $x=5$: $5\not<0$, so the negation fails on this witness. (Consistent
with the original being true — every real is either $>0$, $=0$, or $<0$, and $5$
satisfies the first disjunct.)

---

## 2. Using a negation to prove divergence

### (a) $\lnot(a_n\to L)$

$$\exists\varepsilon>0,\ \forall N\in\mathbb{N},\ \exists n>N,\ |a_n-L|\ge\varepsilon$$

### (b) The three proof obligations

1. **Choose** a specific $\varepsilon>0$, fixed once, used throughout.
2. **Accept as arbitrary** an index $N\in\mathbb{N}$ handed to you by an opponent —
   the proof must work no matter what $N$ they pick.
3. **Construct** an explicit $n>N$ (a formula in terms of $N$) and verify
   $|a_n-L|\ge\varepsilon$ with real arithmetic.

### (c) Prove $a_n = 2+(-1)^n$ does not converge to $2$

**Take $\varepsilon=1$.** Note $a_n - 2 = (-1)^n$, so $|a_n-2|=1$ for *every* $n$ —
there's no case split needed. Let $N\in\mathbb{N}$ be arbitrary and take
$n=N+1>N$. Then $|a_n-2|=1\ge1=\varepsilon$. Since $N$ was arbitrary, $a_n\not\to2$.
$\blacksquare$

**The step most people get wrong:** case-splitting on the parity of $n$ when it's
unnecessary — $|(-1)^n|=1$ regardless of parity, so any $n>N$ already works, and
reaching for a specific one is extra work that isn't needed here (it *is* needed in
part (d), where you must rule out every $L$ at once).

### (d) Prove $a_n=2+(-1)^n$ converges to no $L$ at all

**Take $\varepsilon=1$** — fixed, independent of $L$. Let $L\in\mathbb{R}$ and
$N\in\mathbb{N}$ be arbitrary. Consider the two consecutive indices $n=N+1$ and
$n'=N+2$: since they have opposite parity, $\{a_n,a_{n'}\}=\{1,3\}$, so
$|a_n-a_{n'}|=2$. By the triangle inequality,
$$|a_n-L|+|a_{n'}-L|\ \ge\ |a_n-a_{n'}|\ =\ 2,$$
so at least one of $|a_n-L|,|a_{n'}-L|$ is $\ge1=\varepsilon$. Either way, some
$n>N$ satisfies $|a_n-L|\ge\varepsilon$. Since $L$ and $N$ were arbitrary, $a_n$
converges to no $L$. $\blacksquare$

**The step most people get wrong:** trying to let $\varepsilon$ depend on $L$ (e.g.
"$\varepsilon=|L-2|$"), which breaks down exactly at $L=2$ and forces a separate
argument for the one $L$ that matters most.

---

## 3. Order of the quantifiers

### (a) $P(x,y)$: "$x+y=0$" over $\mathbb{R}$

**$\forall x\,\exists y\,P(x,y)$ is true.** *Proof:* given any $x\in\mathbb{R}$, let
$y=-x$. Then $x+y=x+(-x)=0$, so $P(x,y)$ holds. Since $x$ was arbitrary, the claim
follows. $\blacksquare$

**$\exists y\,\forall x\,P(x,y)$ is false.** *Negation:* $\forall y\,\exists x,\
x+y\neq0$. *Proof of the negation (this is what makes the original false):* let
$y\in\mathbb{R}$ be arbitrary, and take $x=1-y$. Then
$$x+y=(1-y)+y=1\neq0,$$
so $P(x,y)$ fails for this $x$. Since $y$ was arbitrary, no single $y$ works for
every $x$ — this is a direct proof, no contradiction needed. $\blacksquare$

**The step most people get wrong** (and where 08-25's attempt slipped): computing
$(1-y)+y$. It equals $1$, not $0$ — the constant term survives; only the $y$'s
cancel. Reaching for "contradiction" language here is also unnecessary complexity:
once you've shown $x+y=1\neq0$ directly, you're done, there's nothing to contradict.

### (b) Plain English

$\forall x\exists y\,P(x,y)$: **"every real number has an additive inverse"** — $y$
is allowed to depend on (chase) $x$, so this is unsurprising.

$\exists y\forall x\,P(x,y)$, if it were true, would say: **"a single real number is
the additive inverse of every real number at once."** It's false precisely because
no number does that — whatever $y$ you propose, it fails to be $-x$ for any
$x\neq-y$.

*(The point of this part: "for all x there exists a y" is a restatement of the
symbols, not an answer. The question asks what the statement claims about the
actual mathematical objects — additive inverses — not what the quantifiers are
named.)*

### (c) Swapping $\delta$ and $\varepsilon$'s roles in continuity

$$\exists\delta>0,\ \forall\varepsilon>0,\ \big(|x-a|<\delta\implies|f(x)-f(a)|<\varepsilon\big)$$

This says: there is **one fixed** $\delta$, chosen before $\varepsilon$ even shows
up, such that every $x$ within $\delta$ of $a$ satisfies $|f(x)-f(a)|<\varepsilon$
for **every** $\varepsilon>0$ — including arbitrarily tiny ones. But if
$|f(x)-f(a)|<\varepsilon$ holds for every $\varepsilon>0$, that forces
$|f(x)-f(a)|=0$, i.e. $f(x)=f(a)$ exactly. So the swapped statement forces: **$f$ is
constant on the whole interval $(a-\delta,a+\delta)$** — not just continuous at $a$,
but exactly flat nearby. This is the same phenomenon as swapping $N$ and
$\varepsilon$ in the convergence definition (see `08-24-solution.md` §3c): fixing
the "later" quantity before the "for every" one collapses "arbitrarily close" into
"exactly equal."

---

## Stretch — prove $n/(n+1)\to1$

Given $\varepsilon>0$, note
$$\left|\frac{n}{n+1}-1\right|=\left|\frac{n-(n+1)}{n+1}\right|=\frac{1}{n+1}.$$
Choose $N=\lceil1/\varepsilon\rceil$. For $n>N$: $n+1>N>1/\varepsilon-1$... more
directly, $n+1>N\ge1/\varepsilon\implies\frac{1}{n+1}<\varepsilon$. So for all
$n>N$, $\left|\frac{n}{n+1}-1\right|<\varepsilon$. Since $\varepsilon$ was
arbitrary, $n/(n+1)\to1$. $\blacksquare$

**The step most people get wrong:** simplifying $\left|\frac{n}{n+1}-1\right|$ in
the first place — writing the difference over a common denominator before trying to
bound it is what turns an opaque fraction into something you can directly compare
to $\varepsilon$.
