# Solutions — 2026-09-03 (Session 13 — Sup/inf's first real attempt)

*Posted 2026-09-04 per the standing one-day lag, regardless of the work file
coming back blank — same as every prior blank session (08-24, 08-27, 08-28,
09-02). This is the fifth entirely blank session in the repo, and the second
time two have landed back-to-back (09-02, 09-03) — see `STATE.md` and
`CURRICULUM.md` §7 for the full accounting.*

---

## R1. Existential witness — $n<-500$ and $n\equiv3\pmod7$

**Witness:** integers $\equiv3\pmod7$ have the form $n=3-7k$, $k\in\mathbb{Z}$.
Want $3-7k<-500$, i.e. $7k>503$, i.e. $k>71.857\ldots$. Take $k=72$:
$n=3-7(72)=3-504=-501$.

**Proof.** Let $n=-501$.

- $n<-500$: true, since $-501<-500$. ✓
- $n\equiv3\pmod7$: $n-3=-504=7\cdot(-72)$, so $7\mid(n-3)$, i.e. $n\equiv3\pmod7$. ✓

Both conditions hold, so $n=-501$ is the required witness. ∎

**The step most people get wrong:** the same one flagged on every prior instance
of this problem — trying to evaluate "$-501 \bmod 7$" as a single mental
operation instead of writing $n-3=7k$ and solving for an integer $k$ (sign
unrestricted). This is the fourth time this exact class of problem has been
offered since the domain point was first taught (08-19); it remains untested
for a second consecutive session, not because it's hard, but because neither
offering since the 08-28 pause has been reached at all.

---

## Repair. Divergence proof — $e_n=3+4(-1)^n$, does not converge to $3$

**$\lnot(a_n\to L)$ symbolically.** The statement $a_n\to L$ is
$$\forall\varepsilon>0\ \exists N\in\mathbb{N}\ \forall n>N:\ |a_n-L|<\varepsilon.$$
Negating (flip each quantifier, leave domain restrictions alone, negate the
final inequality):
$$\exists\varepsilon>0\ \forall N\in\mathbb{N}\ \exists n>N:\ |a_n-L|\ge\varepsilon.$$

**The three moves this requires:**
1. Produce a single $\varepsilon>0$ that will work against *every* $N$.
2. For that $\varepsilon$, given an arbitrary $N$, produce a specific $n>N$.
3. Verify $|a_n-L|\ge\varepsilon$ for that $n$.

**Proof that $e_n\not\to3$.**

Compute $|e_n-3|$ directly, for *every* $n$ at once:
$$|e_n-3| = \big|3+4(-1)^n-3\big| = \big|4(-1)^n\big| = 4\,\big|(-1)^n\big| = 4\cdot1 = 4.$$

This is constant — it doesn't depend on whether $n$ is even or odd, because
$|(-1)^n|=1$ either way and the sign is erased by the absolute value before it
can matter.

Take $\varepsilon=1$ (any $\varepsilon\le4$ works). Given any $N\in\mathbb{N}$,
take $n=N+1$ (so $n>N$). Then
$$|e_n-3| = 4 \ge 1 = \varepsilon.$$

Since this holds for every $N$, $e_n\not\to3$. ∎

**The step most people get wrong:** splitting into cases on whether $n$ is even
or odd before computing $|e_n-3|$, which is exactly the move that broke the
one genuine attempt on record (08-26). The absolute value makes the case split
unnecessary — $|e_n-3|=4$ regardless of parity, so there's nothing to split on.
This problem, in one form or another ($d_n$, $c_n$, now $e_n$), has been
offered five times since 08-25 and has one wrong attempt and four blanks on
record — still the single most-offered, least-attempted item in the repo.

---

## Core 1 — $\inf\left\{\dfrac1n : n\in\mathbb{N},\,n\ge1\right\}=0$

**Part 1 — lower bound.** For every $n\ge1$, $\frac1n>0$. So $0$ is a lower
bound for the set. ✓

**Part 2 — greatest (nothing bigger works).** Let $\varepsilon>0$. Want $n$
with
$$\frac1n<0+\varepsilon=\varepsilon \iff n>\frac1\varepsilon.$$
By the Archimedean property, $\mathbb{N}$ is unbounded above, so such an $n$
exists; take $n=\left\lceil\frac1\varepsilon\right\rceil+1$ to also guarantee
$n\ge1$. Then $\frac1n<\varepsilon$. ✓

Both parts hold, so $\inf\left\{\dfrac1n\right\}=0$. ∎

**The step most people get wrong:** stating "$0$ is obviously the greatest
lower bound because $\frac1n$ gets arbitrarily close to $0$" without the
$\varepsilon$-witness — "gets arbitrarily close" is the intuition the
$\varepsilon$-part exists to formalize, not a substitute for producing $n$.
The lesson's worked example (§9, $\sup\{1-\frac1n\}=1$) is the mirror image of
this proof with $\le$ and $\ge$ swapped — same Archimedean move, opposite
direction.

---

## Core 2 — $\sup\left\{\dfrac{2n-1}{n} : n\in\mathbb{N},\,n\ge1\right\}=2$

**Rewrite first:** $\dfrac{2n-1}{n} = 2-\dfrac1n$.

**Part 1 — upper bound.** For every $n\ge1$, $2-\frac1n<2$ since $\frac1n>0$.
So $2$ is an upper bound. ✓

**Part 2 — least.** Let $\varepsilon>0$. Using the rewrite, want $n$ with
$$2-\frac1n>2-\varepsilon \iff \frac1n<\varepsilon \iff n>\frac1\varepsilon.$$
Such an $n$ exists (Archimedean property); take
$n=\left\lceil\frac1\varepsilon\right\rceil+1$. Then $2-\frac1n>2-\varepsilon$,
i.e. $\dfrac{2n-1}{n}>2-\varepsilon$. ✓

Both parts hold, so $\sup\left\{\dfrac{2n-1}{n}\right\}=2$. ∎

**The step most people get wrong:** attacking $\frac{2n-1}{n}>2-\varepsilon$ by
cross-multiplying before rewriting — it's not wrong, but $\frac{2n-1}{n}=2-\frac1n$
turns the problem into the *identical* inequality as Core 1 and the lesson's
worked example, one algebra step removed. Doing the rewrite first is what makes
every $\sup$/$\inf$ Archimedean-property problem look like the same three lines
instead of a fresh fight each time.

---

## Stretch (optional, unreached again) — $\sup(A+B)=\sup A+\sup B$

Identical problem to 09-02's stretch, carried forward unchanged because it was
never reached then either. Full solution already posted in
[`09-02-solution.md`](09-02-solution.md#stretch-optional--supab--supasupb) —
not repeated here since nothing about the problem changed. It remains exit-gate
item 5, still with zero attempt evidence across two offerings.
