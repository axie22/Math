# Solutions — 2026-09-04 (Session 14 — Friday review)

*Posted one day after the fact, per the standing lag — regardless of whether
`09-04-work.md` had anything in it. It didn't this time (sixth entirely-blank
session in the repo). These are here for whenever you come back to them.*

---

## Repair. Divergence proof — $f_n=-2+3(-1)^n$, does not converge to $-2$

**Negation, symbolically.** $a_n\to L$ means: $\forall\varepsilon>0\,\exists N\,
\forall n\ge N,\ |a_n-L|<\varepsilon$. Negating a three-quantifier statement flips
each quantifier and negates the innermost claim:

$$\lnot(a_n\to L):\quad \exists\varepsilon>0\ \forall N\ \exists n\ge N,\ \ |a_n-L|\ge\varepsilon.$$

**The three moves this requires** (in order):

1. **Exhibit a specific $\varepsilon>0$** — not "for all $\varepsilon$," a single
   number you choose and commit to.
2. **Given an arbitrary $N$**, produce a specific $n\ge N$ (you don't get to pick
   $N$; you have to handle whatever $N$ is thrown at you).
3. **Compute $|a_n-L|$ for that $n$ and show it's $\ge\varepsilon$** — a direct
   inequality, not an estimate.

**Proof that $f_n\not\to-2$.**

Compute the quantity that actually matters: $f_n-(-2) = -2+3(-1)^n+2 = 3(-1)^n$.
So
$$|f_n-(-2)| = |3(-1)^n| = 3\cdot|(-1)^n| = 3\cdot 1 = 3 \quad\text{for every } n.$$

This is the cleanest possible version of this problem: the distance to $-2$ is
*exactly* $3$ regardless of whether $n$ is even or odd — parity doesn't even come
up, because $|(-1)^n|=1$ either way. That's exactly the step this problem has
been testing since 08-25: the temptation is to track the *sign* of $(-1)^n$ (is
$f_n-(-2)$ equal to $+3$ or $-3$?) instead of its *absolute value*. The sign
alternates; the absolute value doesn't, and it's the absolute value the
definition asks about.

Now execute the three moves. Let $\varepsilon=1>0$ (any $\varepsilon\le 3$ works,
since $|f_n-(-2)|=3$ always — no need to pick something clever). Let $N$ be
arbitrary. Take $n=N$ itself. Then
$$|f_n-(-2)| = 3 \ge 1 = \varepsilon.$$
Since this held for an arbitrary $N$ (using $n=N$, no larger $n$ needed), we've
shown $\exists\varepsilon>0\,\forall N\,\exists n\ge N,\ |f_n-(-2)|\ge\varepsilon$
— exactly the negation above. Hence $f_n\not\to -2$. $\blacksquare$

**The step most people get wrong:** reaching for a large or small $\varepsilon$
"to be safe" instead of noticing that $|f_n-(-2)|$ is *constant* here — this
instance doesn't even require the usual "look at even $n$ vs. odd $n$ separately"
move that harder versions of this problem need, because the absolute value erases
the parity dependence entirely. Once you compute $f_n - L$ and take $|\cdot|$
*first*, the rest is arithmetic.

---

## R1. Induction (bug #2) — $\sum_{k=1}^n k^3=\left(\dfrac{n(n+1)}{2}\right)^2$

**Base case** ($n=1$): LHS $=1^3=1$. RHS $=\left(\frac{1\cdot2}{2}\right)^2=1^2=1$.
Equal. ✓

**Inductive step.** Assume $\displaystyle\sum_{k=1}^n k^3=\left(\frac{n(n+1)}{2}\right)^2$
(the hypothesis) for some $n\ge1$. Show it for $n+1$:

$$\sum_{k=1}^{n+1}k^3 = \underbrace{\sum_{k=1}^{n}k^3}_{\text{substitute the hypothesis here}} + (n+1)^3 = \left(\frac{n(n+1)}{2}\right)^2+(n+1)^3.$$

This is the substitution step — the one bug #2 is specifically about: the
hypothesis gets used as a *known value*, not re-derived. Now factor out
$(n+1)^2$ from both terms:

$$= (n+1)^2\left[\frac{n^2}{4}+(n+1)\right] = (n+1)^2\cdot\frac{n^2+4n+4}{4} = (n+1)^2\cdot\frac{(n+2)^2}{4} = \left(\frac{(n+1)(n+2)}{2}\right)^2.$$

That's exactly the formula evaluated at $n+1$ (since $(n+1)+1=n+2$), so the claim
holds for $n+1$. By induction, it holds for all $n\ge1$. $\blacksquare$

**Technique named:** weak induction, same engine as 08-31 and 09-01 — split off
the last term, substitute the IH, then do algebra to land on the target shape.
**Step most people get wrong:** stopping after substituting the hypothesis
without finishing the factoring — $\frac{n^2}{4}+(n+1)$ doesn't visibly equal
$\frac{(n+2)^2}{4}$ until you clear the denominator and expand $(n+2)^2$; leaving
it as two separate terms and declaring victory is the most common way this kind
of induction step goes incomplete.

---

## R2. Contrapositive, applied — if $n^3+5$ is even, then $n$ is odd

**Which technique, and why it settles the claim.** This is proved by
**contrapositive**: instead of proving $P\Rightarrow Q$ directly (where $P$: "$n^3+5$
is even," $Q$: "$n$ is odd"), we prove $\lnot Q\Rightarrow\lnot P$ (if $n$ is
*even*, then $n^3+5$ is *odd*). This settles the original claim because
$P\Rightarrow Q$ and $\lnot Q\Rightarrow\lnot P$ are **logically equivalent** —
they have the same truth value for every $n$ — so proving one proves the other.

**Proof.** Suppose $n$ is even, so $n=2k$ for some integer $k$. Then
$$n^3 = (2k)^3 = 8k^3,$$
which is even. An even number plus $5$ (odd) is odd, so $n^3+5$ is odd — in
particular, *not* even. This proves $\lnot Q\Rightarrow\lnot P$, which by the
equivalence above proves $P\Rightarrow Q$: if $n^3+5$ is even, then $n$ is odd.
$\blacksquare$

**The step most people get wrong** (the exact gap this problem is a retention
check for): stopping after the algebra — showing $n$ even $\Rightarrow n^3+5$
odd — without writing the sentence that connects it back to the original claim.
The algebra alone proves a *different* statement (the contrapositive); the
missing piece is explicitly saying that the contrapositive's truth guarantees the
original implication's truth, because they're the same statement in two forms.

---

## R3. Plain-English quantifier meaning — $P(x,y)$: "$x^2=y$" (over $\mathbb{R}$)

**What $\forall x\,\exists y\,P(x,y)$ actually claims, in words:** *every* real
number, when squared, gives you *some* real number — i.e., every real number has
a square. Each $x$ is allowed to produce its own $y$; different $x$'s can (and
do) use different $y$'s.

**True or false, and proof:** **True.** Given any $x\in\mathbb{R}$, choose
$y=x^2$. Then $P(x,y)$ holds by construction. Since $x$ was arbitrary, this works
for every $x$. $\blacksquare$

**What $\exists y\,\forall x\,P(x,y)$ actually claims, in words:** there is *one
single* real number $y$ that equals the square of *every* real number $x$
simultaneously — the same $y$ has to work for $x=0$, $x=1$, $x=2$, all at once.

**True or false, and counterexample:** **False.** Suppose such a $y$ existed.
Taking $x=0$ forces $y=0^2=0$. Taking $x=1$ forces $y=1^2=1$. So $y$ would have
to equal both $0$ and $1$ — contradiction, since $0\ne1$. So no single $y$ works
for all $x$. $\blacksquare$

**The step most people get wrong:** translating $\exists y\,\forall x\,P(x,y)$
symbol-by-symbol as "there exists a $y$ for every $x$ such that $x^2=y$," which
*sounds* like it's just restating $\forall x\exists y$ with the words shuffled.
The plain-English test is whether $y$ is allowed to depend on $x$: in
$\forall x\exists y$ it can (quantifier order: $y$ comes after, and inside the
scope of, $x$); in $\exists y\forall x$ it cannot ($y$ is fixed *before* $x$ is
even chosen). That dependency, not the words "for all" and "there exists"
themselves, is what the two statements actually differ on.

---

## Synthesis — uniqueness of the supremum

**Setup (what you're assuming for contradiction).** Let $A\subseteq\mathbb{R}$ be
nonempty and bounded above, and suppose $s=\sup A$ and $t=\sup A$ with $s\ne t$.
WLOG $s<t$ — the setup is symmetric in $s$ and $t$ (both are defined identically,
as suprema of the same set), so if instead $t<s$, just swap the labels $s$ and
$t$ and rerun the identical argument below.

**Choice of $\varepsilon$.** Since $t=\sup A$, the $\varepsilon$-part of its
definition says: for every $\varepsilon>0$, there exists $a\in A$ with
$a>t-\varepsilon$. Choose $\varepsilon = t-s$ — this is $>0$ since $s<t$, and it's
not an arbitrary choice: it's exactly the gap between the two candidate suprema,
chosen so that $t-\varepsilon$ lands exactly on $s$.

**The contradiction.** By that choice, there exists $a\in A$ with
$$a > t-\varepsilon = t-(t-s) = s.$$
So $a>s$ for some $a\in A$. But $s=\sup A$ means in particular that $s$ is an
**upper bound** for $A$ (the first part of its own definition), so $a\le s$ for
*every* $a\in A$ — including this one. That gives $a>s$ and $a\le s$
simultaneously: a contradiction. Hence the assumption $s\ne t$ is false, so
$s=t$. $\blacksquare$

**Technique named:** proof by contradiction (§4, the same technique retired
2026-08-21 on $\sqrt3$'s irrationality), combined with the $\varepsilon$-part of
sup's two-part definition (§9, taught 09-02). **The step most people get wrong:**
leaving $\varepsilon$ generic ("for some small $\varepsilon>0$...") instead of
picking the *specific* value $t-s$ that makes $t-\varepsilon$ collapse exactly
onto $s$. A generic $\varepsilon$ gives you $a>t-\varepsilon$, which is a bound
you can't directly compare to $s$; the whole proof hinges on choosing the one
$\varepsilon$ that turns "$a$ is close to $t$" into "$a$ is bigger than $s$."
This is also the reason the problem is legitimately harder than computing a
specific sup or inf: the right $\varepsilon$ has to be *derived from the
contradiction hypothesis itself* ($s<t$), not read off the set $A$.
