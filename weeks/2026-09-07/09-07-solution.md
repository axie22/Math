# Solutions — 2026-09-07 (Session 15 — sup/inf worked scaffold)

*Posted one day after the fact, per the standing lag — regardless of the work
file coming back blank, the fourth entirely-blank session in a row (09-02, 09-03,
09-04, now 09-07). These are here for whenever you come back to them. Core 2a was
already a full worked proof inside the problem file itself, so there's nothing to
add for it here — these solutions cover R1, 2b, 2c, and the stretch.*

---

## R1. Induction (bug #2 retention) — $\sum_{k=1}^{n}k^2=\dfrac{n(n+1)(2n+1)}{6}$

**Base case** ($n=1$): LHS $=1^2=1$. RHS $=\dfrac{1\cdot2\cdot3}{6}=1$. Equal. ✓

**Inductive step.** Assume $\displaystyle\sum_{k=1}^{n}k^2=\frac{n(n+1)(2n+1)}{6}$
(the hypothesis) for some $n\ge1$. Show it for $n+1$:

$$\sum_{k=1}^{n+1}k^2 = \underbrace{\sum_{k=1}^{n}k^2}_{\text{substitute the hypothesis here}} + (n+1)^2 = \frac{n(n+1)(2n+1)}{6}+(n+1)^2.$$

This is the step bug #2 is specifically about: the hypothesis is used as a
*known value*, not re-derived. Factor out $(n+1)$ from both terms:

$$= (n+1)\left[\frac{n(2n+1)}{6}+(n+1)\right] = (n+1)\cdot\frac{n(2n+1)+6(n+1)}{6} = (n+1)\cdot\frac{2n^2+7n+6}{6}.$$

Factor the quadratic: $2n^2+7n+6=(n+2)(2n+3)$. So

$$\sum_{k=1}^{n+1}k^2 = \frac{(n+1)(n+2)(2n+3)}{6} = \frac{(n+1)\big((n+1)+1\big)\big(2(n+1)+1\big)}{6},$$

which is exactly the formula evaluated at $n+1$. By induction, the identity holds
for all $n\ge1$. $\blacksquare$

**Technique named:** weak induction, the same engine as every prior instance
(08-31, 09-01, 09-04) — split off the last term, substitute the hypothesis,
factor down to the target shape. **The step most people get wrong:** stopping
after substituting the hypothesis and before finishing the factoring —
$\frac{n(2n+1)}{6}+(n+1)$ doesn't visibly match the target until you clear the
denominator, expand, and correctly factor $2n^2+7n+6$. Guessing the factorization
by trial (looking for two numbers that multiply to $12$ and add to $7$: $3$ and
$4$, giving $(n+2)(2n+3)$ once you track the leading coefficient $2$) is faster
and more reliable here than long division.

---

## Core 2b. $\inf\left\{1+\dfrac1n : n\in\mathbb{N}\right\}=1$

This is the mirror image of the worked example in 2a — same $\varepsilon$–$N$
machinery, opposite direction on both parts.

**Part 1 — lower bound.** For every $n\ge1$, $\frac1n>0$, so $1+\frac1n>1$. Hence
$1$ is a lower bound for the set.

**Part 2 — the $\varepsilon$-part (nothing bigger works).** Let $\varepsilon>0$
be arbitrary. We need an element of the set *smaller* than $1+\varepsilon$ (the
self-check question in the work file is exactly this: the direction flips because
this is an infimum, not a supremum — we're bounding from below and showing
nothing bigger than $1$ still bounds from below). By the Archimedean property,
there exists $N\in\mathbb{N}$ with $\frac1N<\varepsilon$. Then the element
$1+\frac1N$ of the set satisfies

$$1+\frac1N < 1+\varepsilon.$$

So no number bigger than $1$ is a lower bound — for any candidate $1+\varepsilon$,
we exhibited a set element below it.

Both parts done $\Rightarrow \inf\{1+\frac1n\}=1$. $\blacksquare$

**Technique named:** same Archimedean "find an $N$" move as 2a and as every
$\varepsilon$–$N$ divergence/convergence proof this month — the direction of
every inequality flips (lower bound instead of upper bound, "below" instead of
"above"), but the move itself doesn't change. **The step most people get wrong:**
keeping the *same* inequality direction as the sup example out of habit — writing
$1+\frac1N>1+\varepsilon$ instead of $<$. The tell that something's wrong: that
version says the set has elements *arbitrarily far above* $1+\varepsilon$, which
is true but irrelevant to showing $1$ is the *greatest* lower bound. The
$\varepsilon$-part of an infimum's definition is always about finding something
*close to and below* the candidate, never above it.

---

## Core 2c. If $s=\sup A$, then for every $n\in\mathbb{N}$ there is $a\in A$ with $a>s-\tfrac1n$

**Proof.** By definition, $s=\sup A$ means two things: $s$ is an upper bound for
$A$, and for every $\varepsilon>0$ there exists $a\in A$ with $a>s-\varepsilon$
(the $\varepsilon$-part). Given any $n\in\mathbb{N}$, set $\varepsilon=\frac1n$,
which is a positive real number. Applying the $\varepsilon$-part of the
definition with this specific $\varepsilon$: there exists $a\in A$ with

$$a > s-\frac1n.$$

Since $n$ was an arbitrary natural number, this holds for every $n\in\mathbb{N}$.
$\blacksquare$

**Technique named:** this is not a new proof technique — it's a direct
instantiation of sup's own $\varepsilon$-part with the specific choice
$\varepsilon=\frac1n$, the same "plug a chosen value into a $\forall\varepsilon$
statement" move used throughout Phase 0's quantifier work. **The step most
people get wrong:** trying to re-derive the claim from scratch (going back to
first principles about upper bounds, or trying to construct $a$ explicitly)
instead of recognizing that the entire proof is one substitution into a
definition that's already been proved once, back in the worked example. This
problem exists specifically to make that recognition automatic — it is also
exactly the building block used later to construct a sequence inside $A$ that
converges to $s$ (taking $a_n$ to be that witness for each $n$), which is why
it's worth internalizing now rather than re-deriving each time it's needed.

---

## Stretch (optional) — $\inf A=-\sup(-A)$

Let $A\subseteq\mathbb{R}$ be nonempty and bounded below, and let
$-A=\{-a:a\in A\}$.

**Setup.** If $m$ is a lower bound for $A$ (i.e. $a\ge m$ for all $a\in A$), then
$-a\le -m$ for all $a\in A$, i.e. $-m$ is an upper bound for $-A$. So $-A$ is
nonempty and bounded above, and $t:=\sup(-A)$ exists. Claim: $-t=\inf A$.

**Part 1 — $-t$ is a lower bound for $A$.** For every $a\in A$, $-a\in -A$, so
$-a\le t$ (since $t$ is an upper bound for $-A$). Multiplying by $-1$ flips the
inequality: $a\ge -t$. Since $a\in A$ was arbitrary, $-t$ is a lower bound for
$A$.

**Part 2 — nothing bigger than $-t$ is a lower bound.** Let $\varepsilon>0$.
Since $t=\sup(-A)$, its $\varepsilon$-part gives an element $-a\in -A$ (for some
$a\in A$) with

$$-a > t-\varepsilon.$$

Multiply by $-1$ (flip the inequality again):

$$a < -t+\varepsilon.$$

So there is an element $a\in A$ smaller than $(-t)+\varepsilon$ — exactly the
$\varepsilon$-part of $\inf A$'s own definition, confirming $-t$ is the *greatest*
lower bound.

Both parts hold, so $\inf A = -t = -\sup(-A)$. $\blacksquare$

**Technique named:** working directly with elements of $A$ and $-A$ and
multiplying inequalities by $-1$, rather than trying to translate the two
definitions (sup's and inf's) symbol-by-symbol into each other. **The step most
people get wrong:** forgetting to flip the inequality direction when multiplying
by $-1$ (a classic and specific slip, distinct from the general "arithmetic under
time pressure" line in `STATE.md` — this one is conceptual, not careless, because
it's easy to not notice you've multiplied by a negative number when you're moving
between an element and its negative rather than doing algebra on an explicit
equation). Getting both flips right (once in each part) is what makes the whole
proof work; missing either one silently proves the wrong statement.
