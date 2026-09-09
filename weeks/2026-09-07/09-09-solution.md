# Solutions — 2026-09-09 (Session 17)

*Posted 2026-09-09, one-day lag, regardless of the blank work file — same as every
prior blank session (08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07, 09-08).*

---

## Review. Plain-English meaning — $\forall n\in\mathbb{Z}\,\exists m\in\mathbb{Z}\,(n+m=0)$

**(a) Symbol-by-symbol transliteration:** "for every integer $n$, there exists an
integer $m$ such that $n+m=0$."

**(b) Actual plain-English meaning:** "every integer has an additive inverse
(a negative) that is also an integer." That's the fact being asserted — the
integers are closed under negation — stated the way someone would actually say
it, not the way the quantifiers read aloud.

**Where most people get this wrong:** (a) and (b) coming out as the same
sentence with different word order. The transliteration is a faithful reading of
the symbols; the plain-English version has to name what the statement is *for* —
here, that taking a negative never leaves the integers. If a rewritten version of
(a) still contains the phrase "there exists," it almost certainly hasn't moved
from transliteration to meaning yet. This is the same gap the worked example
($xy=1$, "every nonzero real has a multiplicative inverse") was built to
demonstrate, and it is now the second time this exact instance ($n+m=0$) has
been presented with a scaffold in front of it and still logged zero attempt.

---

## Core 2b. $\inf\left\{1+\dfrac1n : n\in\mathbb{N}\right\}=1$

**Lower-bound part.** For every $n\ge1$, $\frac1n>0$, so $1+\frac1n>1$. Hence $1$
is a lower bound for the set.

**$\varepsilon$-part (greatest lower bound — nothing bigger works).** Let
$\varepsilon>0$ be arbitrary. We need an element of the set *below* $1+\varepsilon$
(this is the direction that flips relative to the sup worked example: for an
infimum, the witness must come in under the candidate, not over it). By the
Archimedean property, there exists $N\in\mathbb{N}$ with $\frac1N<\varepsilon$.
Then the element $1+\frac1N$ of the set satisfies
$$1+\frac1N < 1+\varepsilon.$$
So no number bigger than $1$ is a lower bound.

Both parts done $\Rightarrow \inf\{1+\frac1n\}=1$. $\blacksquare$

**Where most people get this wrong:** flipping the wrong inequality — writing
$1+\frac1N>1+\varepsilon$ out of habit from the sup direction, instead of $<$.

---

## Core 2c. If $s=\sup A$, then for every $n\in\mathbb{N}$ there's $a\in A$ with $a>s-\tfrac1n$

**Proof.** Let $n\in\mathbb{N}$ be arbitrary. Since $s=\sup A$, $s$ satisfies the
$\varepsilon$-part of the supremum definition: for every $\varepsilon>0$ there
exists $a\in A$ with $a>s-\varepsilon$ (otherwise $s-\varepsilon$ would be an
upper bound smaller than $s$, contradicting $s$ being *least*). Apply this with
$\varepsilon=\frac1n$ — legal since $n\ge1>0$ means $\frac1n>0$. This gives
$a\in A$ with $a>s-\frac1n$. Since $n$ was arbitrary, the claim holds for every
$n\in\mathbb{N}$. $\blacksquare$

**Where most people get this wrong:** not recognizing this problem *is* the
definition with $\varepsilon=\frac1n$ substituted in, and re-deriving it from
scratch by contradiction instead — which also works but is three times longer.
The skill being tested is recognizing a definition already in hand.

---

## Stretch (optional). $\inf A=-\sup(-A)$

Let $A$ be nonempty and bounded below, $-A=\{-a:a\in A\}$.

**$-A$ is bounded above.** If $L$ is a lower bound for $A$, then $-a\le -L$ for
all $a\in A$, so $-L$ is an upper bound for $-A$; $s:=\sup(-A)$ exists by
completeness.

**Claim: $-s=\inf A$.**

*Lower-bound part.* For every $a\in A$, $-a\in -A$, so $-a\le s$, i.e. $a\ge -s$.
So $-s$ is a lower bound for $A$.

*$\varepsilon$-part.* Let $\varepsilon>0$. Since $s=\sup(-A)$, there is $-a\in -A$
with $-a>s-\varepsilon$, i.e. $a<-s+\varepsilon$ — exactly the $\varepsilon$-part
of the infimum definition for the candidate $-s$.

Both parts done $\Rightarrow \inf A=-s=-\sup(-A)$. $\blacksquare$

**Where most people get this wrong:** converting the definitions symbol-by-symbol
without tracking that negation flips inequality direction.
