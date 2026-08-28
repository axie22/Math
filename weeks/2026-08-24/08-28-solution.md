# Solutions — 2026-08-28 (Session 9, Friday review)

> Posted one day late, per the standing rule. `08-28-work.md` came back blank — no
> timestamps, no attempts anywhere — so there is nothing to grade against, but the
> solutions post on schedule regardless, per the one-day lag applying to the problem
> set, not to whether it was attempted. If you're reading this before trying the
> problems cold, close the file and go do that first; the lag is the whole point.

---

## 1. Existential witness — $n<-50$, divisible by $3$

**Claim:** $\exists n\in\mathbb{Z}$ such that $n<-50$ and $3\mid n$.

**Witness:** $n=-51$.

**Verification:** $-51<-50$ ✓. $-51=3\cdot(-17)$, so $3\mid-51$ ✓. Both conjuncts
hold, so the statement is true.

**The point:** same habit as every prior instance of this problem — nothing about
"there exists $n$" restricts you to $\mathbb{N}$. The moment you see "$n<-50$" you
should be reaching into the negative integers, not hunting for a positive multiple of
$3$ and then trying to make it negative as an afterthought.

---

## 2. Contrapositive vs. contradiction — $n^2$ odd $\Rightarrow n$ odd

**Contrapositive statement:** if $n$ is even, then $n^2$ is even.

**Proof of the contrapositive.** Suppose $n$ is even. Unfold: $n=2k$ for some
$k\in\mathbb{Z}$. Then
$$n^2 = (2k)^2 = 4k^2 = 2(2k^2).$$
Since $2k^2\in\mathbb{Z}$, this has the form $2m$, so $n^2$ is even. $\blacksquare$

**Why this establishes the original claim.** The original claim is
$$n^2\text{ odd}\ \Rightarrow\ n\text{ odd},$$
and its contrapositive is
$$\lnot(n\text{ odd})\ \Rightarrow\ \lnot(n^2\text{ odd}),\quad\text{i.e.}\quad n\text{ even}\ \Rightarrow\ n^2\text{ even}.$$
$P\Rightarrow Q$ and $\lnot Q\Rightarrow\lnot P$ are **logically equivalent** — they are
true in exactly the same cases, because an implication is only ever false when the
hypothesis holds and the conclusion fails, and $P\wedge\lnot Q$ is the same event as
$\lnot Q\wedge\lnot(\lnot P)$ read the other way. So proving one *is* proving the
other; there is no extra gap to close, no second step where you go from "the
contrapositive is true" to "so the original is true." They were never two different
facts — one statement, two ways of writing it. This is the exact piece that's been
missing on 08-19 and 08-21: naming the technique is not the same as stating *why*
naming it finishes the job.

---

## 3. Plain English — $P(x,y)$: "$x+y=0$" over $\mathbb{R}$

**(a)** $\forall x\,\exists y\,P(x,y)$: **true.** $\exists y\,\forall x\,P(x,y)$:
**false.**

**(b)** $\forall x\,\exists y\,P(x,y)$ claims: *every real number has an additive
inverse.* Concretely, $y=-x$ always works — the $y$ **depends on $x$**: pick a
different $x$, you need a different $y$. This is just "every real number, when added
to some other real number, gives $0$," which is true because $-x$ exists for every
real $x$.

$\exists y\,\forall x\,P(x,y)$ would have required: **one single real number $y$**,
fixed in advance, such that $x+y=0$ for *every* $x$ at once — the same $y$ would have
to satisfy $1+y=0$ **and** $2+y=0$ **and** $100+y=0$ simultaneously. That forces
$y=-1$ and $y=-2$ and $y=-100$ all at the same time, which is impossible unless all
those numbers are equal — they aren't. No real number can be $-x$ for every $x$ at
once, so no such $y$ exists.

**The step most people get wrong:** reading $\exists y\,\forall x$ as "there's some
$y$ that works for the $x$'s I care about" rather than "one $y$, fixed before any $x$
is chosen, that has to survive being tested against literally every real $x$." The
order of the quantifiers is what makes the second statement enormously stronger than
the first, even though the symbols inside are identical.

---

## 4. Divergence proof — $c_n=3+5(-1)^n$ does not converge to $3$

**$\lnot(a_n\to L)$, symbolically:**
$$\exists\varepsilon>0\ \text{such that}\ \forall N\in\mathbb{N},\ \exists n>N\ \text{with}\ |a_n-L|\ge\varepsilon.$$

**The three moves, named:** (1) pick a fixed $\varepsilon>0$ that will witness the
failure; (2) let $N$ be *arbitrary* (you don't get to choose it — it's handed to
you, universally quantified); (3) *construct* a specific $n>N$, built from $N$, and
verify $|a_n-L|\ge\varepsilon$ for that $n$.

**My $\varepsilon$:** $\varepsilon=1$.

*(Any $\varepsilon\le5$ works — the computation below shows $|c_n-3|=5$ always, so
anything not exceeding $5$ is a valid witness tolerance.)*

**Arbitrary $N$; the $n$ I construct:** let $N\in\mathbb{N}$ be arbitrary. Take
$n=N+1$.

**Verification.**
$$c_n-3 = \bigl(3+5(-1)^n\bigr)-3 = 5(-1)^n \quad\Longrightarrow\quad |c_n-3| = 5\left|(-1)^n\right| = 5\cdot1 = 5,$$
because $(-1)^n\in\{1,-1\}$ for every integer $n$, and $|1|=|-1|=1$ — this holds
**regardless of whether $n$ is even or odd**, so there is nothing to case-split on.
With $n=N+1>N$:
$$|c_n-3| = 5 \ge 1 = \varepsilon.$$
Since such an $n$ exists for every $N$, $c_n$ does not converge to $3$. $\blacksquare$

**The question to ask before computing anything (and the answer):** *do I need to
know whether $N+1$ is even or odd, or does $|\cdot|$ already settle it?* Here it
already settles it — $|(-1)^{\text{anything}}|=1$ unconditionally, so the sign of
$(-1)^n$ never needs to be resolved. This is the identical obstacle that stopped the
08-25 and 08-26 attempts at exactly this step; the shortcut is to take the absolute
value *before* asking about sign, not after.

---

## 5. Synthesis — pigeonhole + formal existence statement

**(a) Proof.** Let $a_1,a_2,\dots,a_6$ be any six integers. For each $i$, let $r_i$
denote the remainder when $a_i$ is divided by $5$, so $r_i\in\{0,1,2,3,4\}$. This
defines a function $r:\{1,\dots,6\}\to\{0,1,2,3,4\}$.

Suppose, for contradiction, that $r_1,\dots,r_6$ were all **distinct**. Then
$\{r_1,\dots,r_6\}$ would be a set of $6$ distinct elements, all lying inside
$\{0,1,2,3,4\}$ — a set of size $5$. That's impossible: a set of $6$ distinct
elements cannot be a subset of a set with only $5$ elements. Contradiction.

So the $r_i$ are **not** all distinct — some two of them, say $r_i=r_j$ with $i\neq
j$. That means $a_i$ and $a_j$ leave the same remainder when divided by $5$.
$\blacksquare$

**(b) As a formal $\exists$ statement:**
$$\exists\,i,j\in\{1,\dots,6\}\ \text{with}\ i\neq j\ \text{such that}\ a_i\equiv a_j\pmod5,$$
i.e., $a_i$ and $a_j$ have the same remainder on division by $5$. The quantified
objects are a **pair of indices** (equivalently, a pair of the six integers) drawn
from $\{1,\dots,6\}$, and the property they satisfy is "same residue mod $5$."

**General pigeonhole principle, stated precisely:** if $A$ and $B$ are finite sets
with $|A|>|B|$, then **no function $f:A\to B$ is injective** — equivalently,
$$\exists\,a,a'\in A\ \text{with}\ a\neq a'\ \text{such that}\ f(a)=f(a').$$
"More pigeons than holes" is the mnemonic; the actual claim is about the
non-injectivity of any map from the larger set to the smaller one. Here $A=\{1,\dots,6\}$
(the six integers, indexed), $B=\{0,1,2,3,4\}$ (the five residues), and $f$ is "take
the remainder mod $5$" — $|A|=6>5=|B|$ forces the collision.
