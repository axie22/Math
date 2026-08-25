# Calculus repair

**Phase 0 reference.** These are the two items that came back blank on both the
calibration and the 08-21 timed redo — not new content exactly, but content that
never actually landed the first time around, so it's taught here properly instead
of just re-tested. Consult this when a problem sends you here; it isn't meant to be
read front to back.

---

## Taylor's theorem, with remainder

**The idea:** the degree-$n$ Taylor polynomial of $f$ at $a$ is the *unique*
polynomial that matches $f$ and its first $n$ derivatives at $a$. Taylor's theorem
says the gap between $f$ and that polynomial — the part everyone forgets — is
itself expressible, not just "small."

**Statement (Lagrange form).** If $f$ has $n+1$ continuous derivatives on an
interval containing $a$ and $x$, then
$$
f(x) = \underbrace{f(a) + f'(a)(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \cdots +
\frac{f^{(n)}(a)}{n!}(x-a)^n}_{\text{degree-}n\text{ Taylor polynomial, }T_n(x)}
\;+\; R_n(x),
$$
where the remainder has the explicit form
$$
R_n(x) = \frac{f^{(n+1)}(c)}{(n+1)!}(x-a)^{n+1} \quad\text{for some } c \text{ strictly between } a \text{ and } x.
$$

**Why this matters, not just as a formula:** $c$ is unknown, but it's *some specific
real number in a known interval* — so if you can bound $f^{(n+1)}$ on that interval,
you can bound the error without knowing $c$ exactly. That's the whole use case:
Taylor's theorem converts "the approximation is close" into a number you can prove.

**Micro-example.** $f(x)=e^x$, $a=0$, degree $n=1$: $T_1(x) = 1+x$. The remainder is
$R_1(x) = \frac{e^c}{2}x^2$ for some $c$ between $0$ and $x$. On $[0,1]$: $e^c\le
e^1=e$, so $|R_1(x)|\le \frac{e}{2}x^2\le\frac{e}{2}\approx1.36$ — a real, provable
bound, even though $c$ itself is never pinned down.

**The step everyone gets wrong:** forgetting that $c$ depends on $x$ (it is *some*
point in the interval, not a fixed constant), and forgetting that the remainder
formula uses the $(n+1)$-th derivative, one order higher than the last term kept in
$T_n$.

---

## Geometric series

**Finite sum.** For $r\neq1$,
$$
S_n = \sum_{k=0}^{n} r^k = 1+r+r^2+\cdots+r^n = \frac{1-r^{n+1}}{1-r}.
$$

**Derivation (multiply-and-subtract, not induction):**
$$
S_n = 1+r+\cdots+r^n, \qquad rS_n = r+r^2+\cdots+r^{n+1}.
$$
Subtracting, every middle term cancels: $S_n - rS_n = 1 - r^{n+1}$, so
$S_n(1-r) = 1-r^{n+1}$, giving the formula above. *(Induction gives the same
result and is worth revisiting once induction itself is taught — this derivation is
independent of it.)*

**Infinite sum.** If $|r|<1$, then $r^{n+1}\to0$ as $n\to\infty$ (provable directly
from the $\varepsilon$-$N$ definition — see this week's material), so
$$
\sum_{k=0}^{\infty} r^k = \lim_{n\to\infty}\frac{1-r^{n+1}}{1-r} = \frac{1}{1-r}.
$$
If $|r|\ge1$, the terms don't shrink to $0$, so the series cannot converge — that
condition is doing all the work.

**The step everyone gets wrong:** using the infinite-sum formula $\frac1{1-r}$ when
$|r|\ge1$ (it's derived *from* the finite sum by taking a limit that only exists
when $|r|<1$ — outside that range the formula is meaningless, not just "less
accurate").
