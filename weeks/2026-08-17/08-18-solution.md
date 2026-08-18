Problems: [08-18.md](08-18.md) · Your work: [08-18-work.md](08-18-work.md) · Grading: [08-18-feedback.md](08-18-feedback.md)

# Session 2 Solutions — 2026-08-18

**Core 2 (injective/surjective) and the Stretch (3 | n² ⟹ 3 | n) are withheld from this
file.** Both were left blank yesterday, and both reappear in today's session (08-19) —
Core 2 as the opening problem, the stretch lemma as part of today's Core 2. Posting the
answer key for them now would hand you the answer to a problem you haven't attempted
yet, which defeats the entire point of the one-day lag. Their solutions post tomorrow,
after you've actually had a run at them.

---

## R1 — $n^2$ even $\implies$ $n$ even, by contrapositive

**Contrapositive.** If $n$ is odd, then $n^2$ is odd.

*Proof.* Suppose $n$ is odd. **Unfold:** $n = 2k+1$ for some $k \in \mathbb{Z}$ — not
$\mathbb{N}$; $n$ could be negative (e.g. $n=-3=2(-2)+1$).

**Work:**
$$n^2 = (2k+1)^2 = 4k^2+4k+1.$$

**Land.** $4k^2$ is even because it's $2\cdot(2k^2)$ — an integer multiple of 2. This
holds regardless of whether $k$ (or $k^2$) is itself even; it's not "$k^2$ is even," it's
"4 times anything is even." Likewise $4k$ is even. So $4k^2+4k$ is a sum of two evens,
hence even (this is exactly Core 1(a), done correctly), and
$$n^2 = \underbrace{4k^2+4k}_{\text{even, call it } 2m} + 1 = 2m+1, \qquad m = 2k^2+2k \in \mathbb{Z}.$$

By definition, $n^2$ is odd. Since "$n$ odd $\implies n^2$ odd" is the contrapositive of
"$n^2$ even $\implies n$ even," the original claim holds. $\blacksquare$

**The technique to name:** contrapositive turns an awkward implication (hard to extract
info about $n$ from a statement about $n^2$) into a direct one (easy to compute from $n$
forward to $n^2$). **The step most people get wrong:** stating the contrapositive
correctly but not noticing it needs its *own* explicit "land" back to the original claim
— it's not enough to prove "$n$ odd $\implies n^2$ odd" and stop; say explicitly that
this is equivalent to the original statement.

---

## R2 — definitions

(a) $n$ is even: $\exists k \in \mathbb{Z}$ such that $n = 2k$.

(b) $n$ is odd: $\exists k \in \mathbb{Z}$ such that $n = 2k+1$.

(c) $a \mid b$: $\exists k \in \mathbb{Z}$ such that $b = ak$.

**The one fix needed everywhere:** $k \in \mathbb{Z}$, never $\mathbb{N}$. $\mathbb{N}$
excludes negative integers (and, depending on convention, 0), so restricting to
$\mathbb{N}$ silently throws away half the integers a definition needs to cover. Rule of
thumb: unless a problem is explicitly about positive integers or counting, the witness
lives in $\mathbb{Z}$.

---

## Core 1(a) — sum of two evens is even

*Proof.* **Setup:** let $a, b$ be even integers. (Not "let $a+b$ be even" — that's the
conclusion, not a hypothesis.)

**Unfold:** $a = 2x$, $b = 2y$ for some $x, y \in \mathbb{Z}$.

**Work:**
$$a + b = 2x + 2y = 2(x+y).$$

**Land:** $x + y \in \mathbb{Z}$, so $a+b$ has the form $2m$ with $m = x+y$. By
definition, $a+b$ is even. $\blacksquare$

**Technique to name:** direct proof — assume the hypothesis, unfold, compute, land.
**The step most people get wrong (and the one to watch for in your own work):**
starting the setup from the conclusion instead of the hypothesis. A fast self-check:
after you write your Setup line, ask "is this something I was *given*, or something I'm
*trying to show*?" If it's the second, restart.

---

## Core 1(b) — product of two odds is odd

*Proof.* **Setup:** let $a, b$ be odd integers.

**Unfold:** $a = 2x+1$, $b = 2y+1$ for some $x, y \in \mathbb{Z}$.

**Work.** Expand term by term (FOIL, explicitly, to avoid the stray exponent from
yesterday):
$$ab = (2x+1)(2y+1) = (2x)(2y) + (2x)(1) + (1)(2y) + (1)(1) = 4xy + 2x + 2y + 1.$$

**Land:** $4xy+2x+2y = 2(2xy+x+y)$ is even (it's 2 times the integer $2xy+x+y$), so
$$ab = 2\underbrace{(2xy+x+y)}_{m} + 1, \qquad m \in \mathbb{Z}.$$

By definition, $ab$ is odd. $\blacksquare$

**Technique to name:** direct proof again — same shape as (a), one more expansion step.
**The step most people get wrong:** rushing the FOIL from memory. $(2x+1)(2y+1)$ has
four terms before combining; write all four out before simplifying, especially under
time pressure — that's exactly where the stray $y^2$ crept in yesterday.

---

## Core 1(c) — $a \mid b$ and $b \mid c$ $\implies$ $a \mid c$

*Proof.* **Setup:** let $a,b,c$ be integers with $a \mid b$ and $b \mid c$.

**Unfold** (twice — two hypotheses, two witnesses, different letters):
$b = am$ for some $m \in \mathbb{Z}$, and $c = bn$ for some $n \in \mathbb{Z}$.

**Work:** substitute the first into the second:
$$c = bn = (am)n = a(mn).$$

**Land:** $mn \in \mathbb{Z}$, so $c = ak$ with $k = mn$. By definition, $a \mid c$.
$\blacksquare$

This is the one from yesterday that was already correct end to end — included here for
completeness and as the template the other two should match: setup states only
hypotheses, unfold uses distinct witnesses, work is one substitution, land names the
final witness explicitly.

**What goes wrong if you name both integers $k$:** nothing breaks *notationally* — you'd
still derive $c = a(k \cdot k) = ak^2$ if you (incorrectly) reused the same symbol for
both witnesses and treated them as equal, which they aren't in general. The two
divisibility relations are independent facts with independent witnesses; reusing a
letter silently asserts they're the same integer, which is an unjustified extra
assumption smuggled in through notation.
