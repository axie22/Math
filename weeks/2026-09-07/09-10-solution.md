# Solutions — 2026-09-10 (Session 18)

*Posted 2026-09-11, one-day lag. `09-10-work.md` came back entirely blank — the
seventh consecutive blank session, the tenth in the repo's history — so there is
nothing to grade against these; they're here purely so the retrieval attempt,
whenever it happens, has something to check against afterward, never before.*

---

## Review. Pigeonhole — general principle

**Precise statement.** If $f:A\to B$ with $A,B$ finite and $|A|>|B|$, then $f$
is not injective — i.e., there exist $a_1\ne a_2\in A$ with $f(a_1)=f(a_2)$.

**Proof (by contradiction).** Suppose $f$ is injective. Then $f$ is a bijection
from $A$ onto its image $f(A)\subseteq B$, so $|A|=|f(A)|$. But $f(A)\subseteq B$
gives $|f(A)|\le|B|$, so $|A|\le|B|$ — contradicting $|A|>|B|$. Hence $f$ is not
injective. $\blacksquare$

(Direct works too: if $f$ were injective, the $|A|$ distinct outputs would all
have to fit inside $B$, needing $|B|\ge|A|$, contradiction — same idea without
the formal bijection-onto-image language.)

**Hash-table application (31 buckets, 40 keys).** Let $A$ = the 40 keys, $B$ =
the 31 buckets, $f$ = the hash function. $|A|=40>31=|B|$. By the general
principle, $f$ is not injective: some two distinct keys $k_1\ne k_2$ satisfy
$f(k_1)=f(k_2)$ — i.e., some bucket receives at least two keys. $\blacksquare$

**The step most people get wrong:** naming which set is $A$ and which is $B$
backwards, or skipping it — the principle only fires once you've said "40 keys
map into 31 buckets," not the reverse. A second common slip: stating the
conclusion as "some bucket gets $\lceil 40/31\rceil = 2$ keys" without
connecting *why* — that arithmetic is the strong form (average load), and the
qualitative pigeonhole statement above is weaker but is what was actually
asked for and is the reusable form.

---

## Core. $\sup\{2-\tfrac1n : n\in\mathbb{N}\}=2$

**Upper-bound part.** For every $n\ge1$, $\tfrac1n>0$, so $2-\tfrac1n<2$. Hence
$2$ is an upper bound.

**$\varepsilon$-part.** Let $\varepsilon>0$. Want $n$ with
$2-\tfrac1n>2-\varepsilon$, i.e. $\tfrac1n<\varepsilon$, i.e. $n>\tfrac1\varepsilon$.
By the Archimedean property, $\mathbb{N}$ is unbounded above, so such an $n$
exists — pick one. Then $2-\tfrac1n>2-\varepsilon$.

Both parts hold $\implies \sup\{2-\tfrac1n\}=2$. $\blacksquare$

**The step most people get wrong:** proving the upper-bound half and stopping,
as if "2 is an upper bound" were the whole claim. It's exactly half — the
$\varepsilon$-part (nothing smaller works) is the part every sup proof in this
repo has gone unattempted on so far, seven sessions running. The second most
common slip, when the $\varepsilon$-part *is* attempted: asserting "such $n$
exists" without naming the Archimedean property as the reason — the existence
isn't free, it's the one substantive fact being used.

---

## Stretch (optional). $\sup(cA)=c\cdot\sup A$ for $c>0$

Let $s=\sup A$.

**Upper bound.** For every $a\in A$, $a\le s$. Since $c>0$, multiplying
preserves the inequality: $ca\le cs$. So $cs$ is an upper bound for $cA$.

**Least.** Let $\varepsilon>0$. Want some $ca\in cA$ with $ca>cs-\varepsilon$,
i.e. $a>s-\tfrac{\varepsilon}{c}$. Since $\tfrac{\varepsilon}{c}>0$, and $s=\sup A$,
part 2 of $\sup A$'s definition gives exactly such an $a\in A$. Then
$ca>c\left(s-\tfrac{\varepsilon}{c}\right)=cs-\varepsilon$.

Both parts hold $\implies\sup(cA)=cs=c\cdot\sup A$. $\blacksquare$

**The trap:** reusing the same $\varepsilon$ in the $a>s-\varepsilon$ step
instead of rescaling to $\varepsilon/c$ — the gap you need to close in $A$ isn't
the same size as the gap you're closing in $cA$ once $c\ne1$ stretches or
shrinks it.
