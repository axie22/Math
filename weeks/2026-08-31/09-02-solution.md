# Solutions — 2026-09-02 (Session 12 — Sup/inf, strong induction retry)

*Posted 2026-09-02 per the standing one-day lag, regardless of the work file
coming back blank — same as every prior blank session (08-24, 08-27, 08-28).*

---

## R1. Existential witness — $n<-200$ and $n\equiv1\pmod6$

**Witness:** the residues $\equiv1\pmod6$ going downward from $1$ are
$1,-5,-11,-17,\dots$, i.e. $n=1-6k$ for $k\in\mathbb{N}$. Want $1-6k<-200$, i.e.
$6k>201$, i.e. $k>33.5$. Take $k=34$: $n=1-6(34)=1-204=-203$.

**Proof.** Let $n=-203$.

- $n<-200$: true, since $-203<-200$. ✓
- $n\equiv1\pmod6$: $n-1=-204=6\cdot(-34)$, so $6\mid(n-1)$, i.e. $n\equiv1\pmod6$. ✓

Both conditions hold, so $n=-203$ is the required witness. ∎

**The step most people get wrong:** checking the congruence by trying to do
"$-203 \bmod 6$" as a mental-arithmetic vibe instead of writing $n-1=6k$ and
solving for an integer $k$ (which is allowed to be negative). The domain point
from §1 of the lesson is exactly this: existence in $\mathbb{Z}$ means *some*
integer $k$, sign unrestricted — don't reach for $\mathbb{N}$ by default.

---

## Repair. Divergence proof — $d_n=5-2(-1)^n$, does not converge to $5$

**$\lnot(a_n\to L)$ symbolically.** The statement $a_n\to L$ is
$$\forall\varepsilon>0\ \exists N\in\mathbb{N}\ \forall n>N:\ |a_n-L|<\varepsilon.$$
Negating (flip each quantifier, leave every domain restriction alone, negate the
final inequality):
$$\exists\varepsilon>0\ \forall N\in\mathbb{N}\ \exists n>N:\ |a_n-L|\ge\varepsilon.$$

**The three moves this requires:**
1. Produce a single $\varepsilon>0$ that will work against *every* $N$.
2. For that $\varepsilon$, given an arbitrary $N$, produce a specific $n>N$.
3. Verify $|a_n-L|\ge\varepsilon$ for that $n$.

**Proof that $d_n\not\to5$.**

Compute $|d_n-5|$ directly, for *every* $n$ at once:
$$|d_n-5| = \big|5-2(-1)^n-5\big| = \big|{-2(-1)^n}\big| = 2\,\big|(-1)^n\big| = 2\cdot1 = 2.$$

This doesn't depend on whether $n$ is even or odd — $|(-1)^n|=1$ either way, so the
sign cancels inside the absolute value before it ever matters.

Take $\varepsilon=1$ (any $\varepsilon\le2$ works). Given any $N\in\mathbb{N}$,
take $n=N+1$ (so $n>N$). Then
$$|d_n-5| = 2 \ge 1 = \varepsilon.$$

Since this holds for every $N$, $d_n\not\to5$. ∎

**The step most people get wrong:** trying to figure out whether $n$ is even or
odd *before* computing, as if the proof needs a case split. It doesn't —
$|d_n-5|=2$ is constant, so the case split that broke the last two attempts
(evaluating the *sign* of $(-1)^n$ instead of using $|\cdot|$) never needs to
happen. The absolute value is doing the work of erasing the parity dependence;
computing the sign first throws that away.

---

## Core 1 — strong induction: every $n\ge1$ is a sum of distinct powers of $2$

**One-line answer first.** Given $n+1$, the largest power of $2$ that is $\le n+1$
is some $2^k$; the leftover $r=(n+1)-2^k$ satisfies $0\le r<2^k\le n+1$ — strictly
less than $n+1$, and in fact strictly less than $2^k$ itself, because $2^k$ was
the *largest* such power (so $2^{k+1}>n+1$).

**Base case** ($n=1$): $1=2^0$. ✓

**Strong induction hypothesis:** assume every integer $m$ with $1\le m\le n$ can be
written as a sum of distinct nonnegative powers of $2$.

**Inductive step, for $n+1$.** Let $2^k$ be the largest power of $2$ with
$2^k\le n+1$ (this exists: $2^0=1\le n+1$, and powers of $2$ grow without bound,
so there is a largest one not exceeding $n+1$). Let $r=(n+1)-2^k\ge0$.

*Case $r=0$:* then $n+1=2^k$ is itself a single power of $2$ — done.

*Case $r>0$:* Since $2^k$ was the *largest* power of $2$ that is $\le n+1$, the
next power up overshoots: $2^{k+1}>n+1$. So
$$r = (n+1)-2^k < 2^{k+1}-2^k = 2^k.$$
In particular $r<2^k\le n+1$, so $r\le n$ — the strong hypothesis applies to $r$.
Write $r=2^{j_1}+2^{j_2}+\cdots+2^{j_s}$ with $j_1>j_2>\cdots>j_s\ge0$ (strong IH).

Because $r<2^k$, none of the powers in that representation can be $\ge2^k$ (if
some $2^{j_i}\ge2^k$ then $r\ge2^{j_i}\ge2^k$, contradicting $r<2^k$). So $j_1<k$.

Therefore
$$n+1 = 2^k + r = 2^k + 2^{j_1}+\cdots+2^{j_s},$$
with $k>j_1>\cdots>j_s\ge0$ — a valid representation with strictly decreasing,
distinct exponents. ∎

**The step most people get wrong:** asserting "$r$ is smaller, so the hypothesis
applies" without actually showing $r\le n$ from the maximality of $2^k$ — and
separately, forgetting to argue that every exponent inside $r$'s representation is
strictly below $k$, which is exactly what keeps the final list of powers distinct.
Both gaps are easy to paper over with "clearly."

---

## Core 2 — $\sup\left\{\dfrac{n}{n+1}:n\in\mathbb{N},\,n\ge1\right\}=1$

**Part 1 — upper bound.** For every $n\ge1$,
$$\frac{n}{n+1} = 1-\frac{1}{n+1} < 1,$$
since $\frac1{n+1}>0$. So $1$ is an upper bound for the set. ✓

**Part 2 — least.** Let $\varepsilon>0$. Using the rewrite above, want $n$ with
$$1-\frac1{n+1}>1-\varepsilon \iff \frac1{n+1}<\varepsilon \iff n+1>\frac1\varepsilon \iff n>\frac1\varepsilon-1.$$
By the Archimedean property $\mathbb{N}$ is unbounded above, so such an $n$
exists; take $n=\max\!\left(1,\left\lceil\frac1\varepsilon\right\rceil\right)$ to
also guarantee $n\ge1$. Then $\dfrac{n}{n+1}>1-\varepsilon$. ✓

Both parts hold, so $\sup\left\{\dfrac{n}{n+1}\right\}=1$. ∎

**The step most people get wrong:** attacking $\frac{n}{n+1}>1-\varepsilon$ by
cross-multiplying directly instead of first rewriting $\frac{n}{n+1}=1-\frac1{n+1}$
— the rewrite turns the problem into *exactly* the worked example's inequality
($\frac1{n+1}<\varepsilon$), one algebraic step removed. Skipping the rewrite makes
the cross-multiplied inequality ($n>(1-\varepsilon)(n+1)$, i.e. $n\varepsilon>1-\varepsilon$)
correct but much easier to fumble under time pressure.

---

## Stretch (optional) — $\sup(A+B)=\sup A+\sup B$

Let $s=\sup A$, $t=\sup B$ (both exist by completeness: $A,B$ nonempty and
bounded above).

**Direction 1 — $s+t$ is an upper bound for $A+B$.** Let $a\in A$, $b\in B$ be
arbitrary. Since $s=\sup A$, $a\le s$; since $t=\sup B$, $b\le t$. Adding,
$a+b\le s+t$. Since $a+b$ was an arbitrary element of $A+B$, $s+t$ is an upper
bound for $A+B$.

**Direction 2 — nothing smaller than $s+t$ works.** Let $\varepsilon>0$. Apply the
$\varepsilon$-part of $\sup A$'s definition to $\varepsilon/2$: there exists
$a\in A$ with $a>s-\varepsilon/2$. Apply the same to $\sup B$ with $\varepsilon/2$:
there exists $b\in B$ with $b>t-\varepsilon/2$. Then $a+b\in A+B$ and
$$a+b > \left(s-\frac\varepsilon2\right)+\left(t-\frac\varepsilon2\right) = s+t-\varepsilon.$$

Both parts hold ($s+t$ is an upper bound for $A+B$, and for every $\varepsilon>0$
some element of $A+B$ exceeds $s+t-\varepsilon$), so $\sup(A+B)=s+t=\sup A+\sup B$. ∎

**The step most people get wrong:** using the *same* $\varepsilon$ against both
$A$ and $B$ (getting $a>s-\varepsilon$, $b>t-\varepsilon$, hence
$a+b>s+t-2\varepsilon$) instead of splitting into $\varepsilon/2+\varepsilon/2$ up
front. The two-$\varepsilon$ version isn't wrong — $\varepsilon$ was arbitrary
either way — but it leaves a stray factor of $2$ that then needs an extra
rescaling step to clean up. Splitting into halves at the start is the standard
move precisely because it avoids that.
