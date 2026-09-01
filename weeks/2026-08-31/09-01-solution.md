# Solutions — 2026-09-01 (Session 11 — Induction II)

*Posted 2026-09-02, one-day lag. Read after attempting today's (09-02) problems, not
before.*

---

## R1 — $2+4+6+\cdots+2n=n(n+1)$

**Technique: induction, sum recurrence.** $S(n)$ is the running total of the first
$n$ even numbers; $S(n+1)=S(n)+2(n+1)$.

**Base case** ($n=1$): $S(1)=2=1\cdot2$. ✓

**IH:** assume $S(k)=k(k+1)$ for some $k\ge1$.

**Step:**
$$S(k+1)=S(k)+2(k+1)\overset{\text{IH}}{=}k(k+1)+2(k+1)=(k+1)(k+2).$$

By induction, $S(n)=n(n+1)$ for all $n\ge1$. $\blacksquare$

**Step most people get wrong:** stopping right after the algebra lands instead of
writing the closing sentence. The factoring being correct isn't the same as the
proof being finished — say explicitly that this is the formula at $n=k+1$, and that
therefore, by induction, it holds for all $n\ge1$.

---

## R2 — Contrapositive: "if $5n+3$ is even, then $n$ is odd"

**Technique: contrapositive.** $P\implies Q$ and $\lnot Q\implies\lnot P$ are the
same statement (logically equivalent), so proving one proves the other.

**Contrapositive:** if $n$ is even, then $5n+3$ is odd.

**Proof:** let $n=2k$ for some integer $k$. Then
$$5n+3=5(2k)+3=10k+3=2(5k+1)+1,$$
which is $2\times(\text{integer})+1$ — the definition of odd. $\blacksquare$

**Why this proves the original claim (the sentence itself):** $P\implies Q$ and
$\lnot Q\implies\lnot P$ have identical truth tables — they are true and false in
exactly the same cases — so establishing one *is* establishing the other, not just
evidence for it.

**Step most people get wrong:** proving the contrapositive correctly and then never
writing that one sentence — treating "prove the contrapositive" as a free-floating
instruction instead of a technique whose validity rests on a specific logical fact
you should be able to state.

---

## Repair — $T(x,y)$: "$x-y=1$" over $\mathbb{R}$

**(a)** $\forall x\,\exists y\,T(x,y)$: **true** ($y=x-1$ always works).
$\exists y\,\forall x\,T(x,y)$: **false.**

**(b) What $\forall x\,\exists y\,T(x,y)$ claims:** for every real $x$, there is
*some* real $y$ — specifically $y=x-1$, which **changes as $x$ changes** — with
$x-y=1$. In words: every real number has something exactly $1$ less than it.

**What $\exists y\,\forall x\,T(x,y)$ would require:** one single fixed $y$ with
$x-y=1$ for *every* real $x$ at once. Concretely: $x=0$ forces $y=-1$; but then
$x=5$ gives $5-(-1)=6\ne1$. Since $y$ has to be chosen *before* $x$ varies, no fixed
number can be "$1$ less than" every real simultaneously.

**Step most people get wrong:** restating the formula ($x-y=1$) instead of saying
what it *means* in context — that the required offset moves with $x$ in the first
statement and can't be pinned to one value in the second. A concrete counterexample
(pick a candidate $y$, then break it with a second $x$) is the fastest way to make
"no such $y$ exists" more than an assertion.

---

## Core 1 — a set of size $n$ has $2^n$ subsets

**Technique: induction via a case split**, not a sum recurrence — the hypothesis
enters through counting two disjoint groups, not through substituting into an
algebraic total.

**Base case** ($n=0$): the empty set has exactly one subset (itself), and $2^0=1$. ✓

**IH:** assume every set of size $k$ has exactly $2^k$ subsets.

**Step:** let $A$ have size $k+1$, pick $x\in A$. Every subset of $A$ either
contains $x$ or doesn't:
- **Doesn't contain $x$:** exactly the subsets of $A\setminus\{x\}$ (size $k$) — by
  IH, $2^k$ of them.
- **Contains $x$:** exactly $\{x\}\cup S$ for $S$ a subset of $A\setminus\{x\}$ — a
  bijection with the subsets of $A\setminus\{x\}$, so also $2^k$ of them.

These two groups are disjoint and cover every subset of $A$, so $A$ has
$2^k+2^k=2\cdot2^k=2^{k+1}$ subsets. By induction, a set of size $n$ has $2^n$
subsets for all $n\ge0$. $\blacksquare$

**Step most people get wrong:** trying to force the sum-recurrence shape
($S(n+1)=S(n)+a_{n+1}$) onto a problem that isn't a running total, or skipping the
"contains $x$" bijection and just asserting there are also $2^k$ such subsets
without saying why (it's the same count because adding a fixed element back in is a
bijection, not a coincidence).

---

## Core 2 — every integer $n\ge2$ is a product of primes

**Technique: strong induction.** Ordinary induction only hands you the statement at
$n$; here $n+1$ can split into two factors $a,b$ that are both smaller than $n+1$
but neither has to equal $n$ — you need the statement at *every* integer from $2$ up
to $n$, which is exactly what strong induction assumes.

**Base case** ($n=2$): $2$ is itself prime, so it's a (length-one) product of
primes. ✓

**Strong IH:** assume every integer $m$ with $2\le m\le n$ can be written as a
product of primes.

**Step, for $n+1$:**
- **If $n+1$ is prime:** it's a length-one product of primes. Done.
- **If $n+1$ is composite:** by definition, $n+1=ab$ for integers $1<a,b<n+1$, i.e.
  $1<a,b\le n$ (since $a,b$ are integers strictly less than $n+1$, the largest they
  can be is $n$). Both $a$ and $b$ are in the range $[2,n]$, so the strong
  hypothesis applies to *both*: $a=p_1\cdots p_i$ and $b=q_1\cdots q_j$ for primes
  $p_i,q_j$. Then $n+1=ab=p_1\cdots p_i\, q_1\cdots q_j$, a product of primes.

By strong induction, every integer $n\ge2$ is a product of primes. $\blacksquare$

**Step most people get wrong:** writing "$a,b<n+1$" and stopping — the strong
hypothesis needs $a,b\le n$, and while that's the same set of integers, the proof
should say explicitly why $a,b\le n$ (they're integers strictly below $n+1$, so the
largest integer value either can take is $n$) rather than leaving the reader to
notice it. The other common miss: forgetting the prime case entirely and only
handling composite $n+1$, which leaves the induction with no way to terminate.

---

## Stretch — every $n\ge8$ is $3a+5b$ for nonnegative integers $a,b$

**Technique: strong induction, three base cases.** A single base case isn't enough
here because the inductive step will subtract $3$ from $n+1$ to reach $n-2$, which
needs its *own* representation already established — and depending on parity/residue
mod 3, $n-2$ might be several steps back, not always $n$. Concretely: if $n-2$ (i.e.
three below $n+1$) is representable, add one more $3$. That means you need the
**three smallest cases** ($n=8,9,10$) nailed down directly, so that every larger
case can always reach back exactly three steps into already-proven territory.

**Base cases:** $8=3+5$, $9=3+3+3$, $10=5+5$. ✓✓✓

**Strong IH:** assume every integer $m$ with $8\le m\le n$ (for some $n\ge10$) can
be written as $3a+5b$.

**Step, for $n+1\ge11$:** then $n+1-3=n-2\ge8$, and $n-2\le n$, so the hypothesis
applies to $n-2$: $n-2=3a'+5b'$ for some nonnegative integers $a',b'$. Then
$$n+1=(n-2)+3=3(a'+1)+5b',$$
a valid representation with nonnegative integers. By strong induction, every
$n\ge8$ is $3a+5b$. $\blacksquare$

**Step most people get wrong:** trying to run this as ordinary induction from a
single base case ($n=8$) and getting stuck, because $n+1-3$ isn't always the
immediately preceding case — it's three cases back, so the base needs to cover an
entire window of that width before the recursion is safe to run.
