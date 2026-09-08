# Solutions — 2026-09-08 (Session 16)

*Posted 2026-09-08, one-day lag, regardless of the blank work file — same as every
prior blank session (08-24, 08-27, 08-28, 09-02, 09-03, 09-04, 09-07).*

---

## Review. Contrapositive, applied — if $n^2+4n$ is odd, then $n$ is odd

**Technique:** proof by contrapositive.

**Contrapositive statement:** if $n$ is even, then $n^2+4n$ is even.

**Proof.** Suppose $n$ is even, so $n=2k$ for some integer $k$. Then
$$n^2+4n = 4k^2+8k = 4(k^2+2k),$$
which is an integer multiple of $4$, hence even. This proves the contrapositive. $\blacksquare$

**The sentence this problem is actually testing:** because $P\Rightarrow Q$ is
logically equivalent to $\lnot Q\Rightarrow\lnot P$, proving "$n$ even
$\Rightarrow n^2+4n$ even" *is* a proof of "$n^2+4n$ odd $\Rightarrow n$ odd" — not
a related fact, the same statement in a more convenient direction.

**Where most people get this wrong:** not the algebra — factoring $4k^2+8k$ as
$4(k^2+2k)$ is routine — but stopping right after showing the contrapositive is
true and never writing the equivalence sentence above. A grader reading only the
factoring step has no way to tell whether the writer knows *why* that step
proves the original claim, as opposed to having memorized "assume the negation
of the conclusion, show the negation of the hypothesis" as a ritual. This is
exactly the gap this retention check exists to catch — it caught it once already
(09-04, blank) and is being offered one more time before being logged as
untested rather than repaired.

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
So no number bigger than $1$ is a lower bound — for any candidate $1+\varepsilon$,
we exhibited a set element beneath it.

Both parts done $\Rightarrow \inf\{1+\frac1n\}=1$. $\blacksquare$

**Where most people get this wrong:** flipping the wrong inequality. The
worked-example instinct from a supremum problem is "find something *bigger* than
the candidate minus $\varepsilon$"; for an infimum you need something *smaller*
than the candidate plus $\varepsilon$. Writing $1+\frac1N>1+\varepsilon$ instead
of $<$ is the single most common way this exact problem goes wrong, and it's an
easy mistake to make on autopilot precisely because the sup version was worked
first.

---

## Core 2c. If $s=\sup A$, then for every $n\in\mathbb{N}$ there's $a\in A$ with $a>s-\tfrac1n$

**Proof.** Let $n\in\mathbb{N}$ be arbitrary. Since $s=\sup A$, $s$ satisfies the
two-part definition of supremum, and in particular its $\varepsilon$-part: for
every $\varepsilon>0$ there exists $a\in A$ with $a>s-\varepsilon$ (otherwise
$s-\varepsilon$ would itself be an upper bound for $A$ smaller than $s$,
contradicting $s$ being the *least* upper bound). Apply this with
$\varepsilon=\frac1n$ — a legal choice since $n\in\mathbb{N}$ means $n\ge1>0$, so
$\frac1n>0$. This gives $a\in A$ with $a>s-\frac1n$. Since $n$ was arbitrary, the
claim holds for every $n\in\mathbb{N}$. $\blacksquare$

**Where most people get this wrong:** not recognizing that this problem *is* the
definition, with $\varepsilon$ substituted, and instead trying to re-derive it
from scratch — usually by contradiction (assume no such $a$ exists, so
$a\le s-\frac1n$ for all $a\in A$, so $s-\frac1n$ is an upper bound less than $s$,
contradiction). That route also works and is worth knowing, but it's three times
longer than noticing that "for every $n\in\mathbb{N}$" is just "for every
$\varepsilon>0$" restricted to the specific family $\varepsilon=\frac1n$, and
substituting is enough. The skill this problem is actually testing is
*recognizing a definition already in hand*, not re-proving it.

---

## Stretch (optional). $\inf A=-\sup(-A)$

Let $A$ be nonempty and bounded below, and let $-A=\{-a:a\in A\}$.

**$-A$ is bounded above.** If $L$ is a lower bound for $A$ (i.e. $a\ge L$ for all
$a\in A$), then $-a\le -L$ for all $a\in A$, i.e. $-L$ is an upper bound for $-A$.
So $-A$ is bounded above and $s:=\sup(-A)$ exists by completeness.

**Claim: $-s=\inf A$.**

*Lower-bound part.* For every $a\in A$, $-a\in -A$, so $-a\le s$ (since $s$ is an
upper bound for $-A$). Rearranging, $a\ge -s$. So $-s$ is a lower bound for $A$.

*$\varepsilon$-part.* Let $\varepsilon>0$. Since $s=\sup(-A)$, there exists an
element of $-A$ — say $-a$ for some $a\in A$ — with $-a>s-\varepsilon$.
Rearranging: $a<-s+\varepsilon$. So we've exhibited $a\in A$ below $(-s)+\varepsilon$,
which is exactly the $\varepsilon$-part of the infimum definition for the
candidate $-s$.

Both parts done $\Rightarrow \inf A=-s=-\sup(-A)$. $\blacksquare$

**Where most people get this wrong:** converting the definitions symbol-by-symbol
without tracking that negation flips inequality direction — e.g. writing
"$a\ge L$ for all $a\in A$" becomes "$-a\ge -L$" instead of "$-a\le -L$." The
hint in the original problem file (work from the definition of $\inf A$ directly,
rather than converting sup's definition term-by-term) is aimed at exactly this
trap.
