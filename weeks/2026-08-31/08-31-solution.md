# Solutions — 2026-08-31 (Session 10 — Induction I)

*Posted 2026-09-01, one-day lag. Read after attempting today's (09-01) problems,
not before.*

---

## R1 — $\sqrt5$ is irrational

**Technique: contradiction**, same skeleton as $\sqrt2$/$\sqrt3$ in
`lessons/proof-foundations.md` §4, generalized: whenever $p$ is prime, $p\mid a^2
\implies p\mid a$, because $p$ appears in the prime factorization of $a^2$ with even
multiplicity, so it must already divide $a$.

Suppose $\sqrt5=p/q$ in lowest terms, $\gcd(p,q)=1$. Then $p^2=5q^2$, so $5\mid p^2$,
so (5 prime) $5\mid p$. Write $p=5k$: $25k^2=5q^2 \Rightarrow q^2=5k^2 \Rightarrow
5\mid q^2 \Rightarrow 5\mid q$. Now $5$ divides both $p$ and $q$ — contradicting
$\gcd(p,q)=1$. So no such $p,q$ exist; $\sqrt5$ is irrational. $\blacksquare$

**Step most people get wrong:** stopping at "$p$ and $q$ are both divisible by 5"
without saying *why that's a contradiction*. It only becomes one because you assumed
the fraction was in lowest terms — say that sentence explicitly, every time.

---

## R2 — Negate $\exists x\in\mathbb{R},\ x^2<0$

Rule: flip the quantifier, leave the domain, negate the predicate.

$$\lnot\big(\exists x\in\mathbb{R},\ x^2<0\big) \equiv \forall x\in\mathbb{R},\ x^2\ge0.$$

**Step most people get wrong:** touching $\mathbb{R}$ — it's a domain restriction,
not part of the quantified claim, and it never changes (§5 of
`proof-foundations.md`).

---

## Repair — $Q(x,y)$: "$xy=1$" over $\mathbb{R}\setminus\{0\}$

**(a)** $\forall x\,\exists y\,Q(x,y)$: **true.** Given any nonzero $x$, $y=1/x$ is
nonzero and $xy=1$.
$\exists y\,\forall x\,Q(x,y)$: **false.**

**(b) What $\forall x\,\exists y\,Q(x,y)$ claims:** for every nonzero real $x$, there
is *some* nonzero real $y$ — and it can be a **different** $y$ for each $x$ — such
that $xy=1$. In words: every nonzero number has a multiplicative inverse. $y$ is
allowed to depend on $x$ (concretely, $y=1/x$); that dependence is exactly what
$\exists y$ *after* $\forall x$ means.

**What $\exists y\,\forall x\,Q(x,y)$ would require:** one single fixed number $y$
such that $xy=1$ for *every* nonzero $x$ simultaneously — the same $y$ has to work
whether $x=1$, $x=2$, or $x=1{,}000{,}000$. That forces $y=1/x$ for all those $x$'s
at once, which is impossible unless $x$ never changes. No nonzero real number is
"the" inverse of every other number, so this is false.

**Step most people get wrong:** answering with the symbols again ("$y$ exists such
that $xy=1$") instead of saying what that *means* — that inversion is possible, and
that the inverse depends on the input. Restating the formula is not explaining it.

---

## Core 1 — $1+3+5+\cdots+(2n-1)=n^2$

**Technique: induction, sum recurrence.** $S(n)=1+3+\cdots+(2n-1)$ is the running
total of the first $n$ odd numbers; the $n$-th term itself is $2n-1$. Don't confuse
the two — this is the Σ-reading check.

**Base case** ($n=1$): $S(1)=1=1^2$. ✓

**IH:** assume $S(n)=n^2$ for some $n\ge1$.

**Step:**
$$S(n+1)=S(n)+(2(n+1)-1)=S(n)+(2n+1)\overset{\text{IH}}{=}n^2+2n+1=(n+1)^2.$$

By induction, $S(n)=n^2$ for all $n\ge1$. $\blacksquare$

**Step most people get wrong:** re-deriving $S(n+1)$ from scratch (re-summing
$1+3+\cdots+(2n+1)$) instead of writing $S(n+1)=S(n)+a_{n+1}$ and substituting the
hypothesis for $S(n)$. If you never write the substitution, you haven't used the
hypothesis, and the proof — however correct-looking — isn't induction.

---

## Core 2 — $3\mid(n^3-n)$ for all $n\ge1$

**Technique: induction, definition-unfold + algebra.** $3\mid X$ means $X=3a$ for
some integer $a$ (§1 of `proof-foundations.md`).

**Base case** ($n=1$): $1^3-1=0=3\cdot0$. ✓

**IH:** assume $k^3-k=3m$ for some integer $m$, for some fixed $k\ge1$.

**Step:** expand and regroup so the hypothesis appears as a piece:
$$(k+1)^3-(k+1) = k^3+3k^2+3k+1-k-1 = k^3+3k^2+2k = \underbrace{(k^3-k)}_{=3m\text{ by IH}}+3k^2+3k.$$
Substituting:
$$(k+1)^3-(k+1) = 3m+3k^2+3k = 3(m+k^2+k).$$
Since $m+k^2+k\in\mathbb{Z}$, this is $3\times$ an integer, so $3\mid\big((k+1)^3-(k+1)\big)$.
By induction, $3\mid(n^3-n)$ for all $n\ge1$. $\blacksquare$

**Step most people get wrong (and where 08-31's attempt was slightly off in
presentation, not content):** writing the algebra as a chain of "$3\mid(\dots)$"
restatements instead of an equality chain that concludes with a single divisibility
statement at the end. Prove the equality first; state divisibility once, last.

---

## Stretch — $n!>2^n$ for $n\ge4$

**Technique: induction with a nontrivial base case.** Check small cases directly:
$1!=1$ vs $2^1=2$ (false), $2!=2$ vs $4$ (false), $3!=6$ vs $8$ (false), $4!=24$ vs
$16$ (**true** — this is where the claim starts holding).

**Base case** ($n=4$): $4!=24>16=2^4$. ✓

**IH:** assume $n!>2^n$ for some $n\ge4$.

**Step:**
$$(n+1)! = (n+1)\cdot n! \overset{\text{IH}}{>} (n+1)\cdot 2^n \ge 2\cdot 2^n = 2^{n+1},$$
using $n+1\ge5>2$ for the middle inequality. So $(n+1)!>2^{n+1}$.

By induction, $n!>2^n$ for all $n\ge4$. $\blacksquare$

**Step most people get wrong:** starting the base case at $n=1$ out of habit,
without checking whether the claim is even true there. Induction proves "for all
$n\ge n_0$" — find the real $n_0$ first, by testing, before writing a single line of
proof.
