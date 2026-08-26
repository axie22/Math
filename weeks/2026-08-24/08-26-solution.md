Problems: [08-26.md](08-26.md) · Your work: [08-26-work.md](08-26-work.md) · Grading: [08-26-feedback.md](08-26-feedback.md)

# Session 7 Solutions — 2026-08-26

---

## 0. Review

### R1 — setup line (odd × odd = odd)

Suppose $a,b\in\mathbb{Z}$ are arbitrary, with $a$ and $b$ both odd. *(Stop here —
the setup is the deliverable, not the proof.)*

### R2 — prove $b_n=1+(-1)^n$ does not converge to $1$

**Take $\varepsilon=1$** (any $\varepsilon\le1$ works; $1$ is cleanest). Note
$b_n-1=(-1)^n$, so $|b_n-1|=1$ for *every* $n$ — no case split on parity needed.
Let $N\in\mathbb{N}$ be arbitrary and take $n=N+1>N$. Then
$$|b_n-1|=|(-1)^{N+1}|=1\ge1=\varepsilon.$$
Since $N$ was arbitrary, $b_n\not\to1$. $\blacksquare$

**The step most people get wrong:** trying to evaluate $(-1)^{N+1}$ as $+1$ or $-1$
by casing on whether $N$ is even or odd. You never need the *sign* — only its
absolute value, which is always $1$. This is the same shortcut as `08-25-solution.md`
§2(c); the problem was built to test whether it transfers to a new instance.

---

## 1. Repair — plain English, not transliteration

### (a) True/false for $R(x,y)$: "$y=x^2$"

$\forall x\exists y\,R(x,y)$: **True.** Given any $x\in\mathbb{R}$, let $y=x^2$;
then $R(x,y)$ holds. $\exists y\forall x\,R(x,y)$: **False** — see (b) for why.

### (b) What each one actually claims

$\forall x\exists y\,R(x,y)$ claims: **every real number has a square** — for each
$x$ you pick, a corresponding $y$ (namely $x^2$) exists, and different $x$'s are
allowed different $y$'s.

$\exists y\forall x\,R(x,y)$ would have required: **a single real number that
equals the square of every real number simultaneously** — one fixed $y$ with
$y=0^2$ and $y=1^2$ and $y=2^2$ and $y=(-3)^2$, all at once. No real number does
this: $0^2=0$ but $1^2=1\ne0$, so already two different $x$'s force two different
values of $y$. That contradiction is why the statement is false — not because
squares are hard to compute, but because one $y$ can't serve every $x$ at once.

---

## 2. Core

### Core 1(a) — $T_2(x)$, $R_2(x)$ for $e^x$ at $a=0$

$f(x)=e^x\Rightarrow f(0)=f'(0)=f''(0)=1$. So
$$T_2(x)=1+x+\frac{x^2}{2}, \qquad R_2(x)=\frac{e^c}{3!}x^3=\frac{e^c}{6}x^3
\ \text{ for some } c \text{ between } 0 \text{ and } x.$$

### Core 1(b) — prove $|R_2(x)|\le\frac{e}{6}$ on $[0,1]$

**Bound on $e^c$:** for $x\in[0,1]$, $c$ lies between $0$ and $x$, so $0\le c\le1$.
Since $e^t$ is increasing, $e^c\le e^1=e$.

**Full argument:** for $x\in[0,1]$,
$$|R_2(x)|=\left|\frac{e^c}{6}x^3\right|=\frac{e^c}{6}\,x^3\le\frac{e}{6}\cdot1=\frac{e}{6},$$
using $e^c\le e$ and $x^3\le1$ (both from $x,c\in[0,1]$). $\blacksquare$

**The step most people get wrong:** bounding $e^c$ using the wrong interval — $c$'s
range is tied to $x$'s range ($c$ is *between* $0$ and $x$), so once $x$ is
restricted to $[0,1]$, so is $c$. Also common: forgetting $x^3\le1$ needs $x\ge0$ to
avoid sign issues — true here since the interval is $[0,1]$.

### Core 2(a) — derive $S_n=\dfrac{1-r^{n+1}}{1-r}$

$$S_n=1+r+r^2+\cdots+r^n,\qquad rS_n=r+r^2+\cdots+r^n+r^{n+1}.$$
Subtract: every term except the first (in $S_n$) and the last (in $rS_n$) cancels:
$$S_n-rS_n=1-r^{n+1}\ \Longrightarrow\ S_n(1-r)=1-r^{n+1}\ \Longrightarrow\
S_n=\frac{1-r^{n+1}}{1-r}\quad(r\ne1).$$

### Core 2(b) — closed form of $\sum_{k=0}^\infty r^k$

Since $|r|<1\Rightarrow r^{n+1}\to0$ (cited, not reproved here — see Core 2(c) for
the specific case $r=\tfrac12$):
$$\sum_{k=0}^\infty r^k=\lim_{n\to\infty}\frac{1-r^{n+1}}{1-r}=\frac{1}{1-r}.$$

### Core 2(c) — prove $\left(\frac12\right)^n\to0$ from the $\varepsilon$-$N$ definition

Given $\varepsilon>0$, choose $N=\left\lceil\log_2\frac1\varepsilon\right\rceil$
(any integer $N\ge\log_2\frac1\varepsilon$ works). For $n>N$:
$$n>\log_2\frac1\varepsilon\ \Longrightarrow\ 2^n>\frac1\varepsilon\
\Longrightarrow\ \left(\frac12\right)^n=\frac1{2^n}<\varepsilon.$$
Since $\left(\frac12\right)^n>0$ always, $\left|\left(\frac12\right)^n-0\right|=
\left(\frac12\right)^n<\varepsilon$ for all $n>N$. Since $\varepsilon$ was
arbitrary, $\left(\frac12\right)^n\to0$. $\blacksquare$

**The step most people get wrong:** picking $N$ *after* checking it works, instead
of deriving it directly from $\varepsilon$ via the logarithm — the definition
requires you to produce $N$ from $\varepsilon$, not guess and verify.

---

## Stretch — Taylor bound for $\sin(0.5)$

$f(x)=\sin x$: $f(0)=0,\ f'(0)=1,\ f''(0)=0,\ f'''(x)=-\cos x$. Degree-3 polynomial:
$T_3(x)=x-\frac{x^3}{6}$. At $x=0.5$: $T_3(0.5)=0.5-\frac{0.125}{6}\approx0.47917$.

Remainder: $R_3(x)=\dfrac{f^{(4)}(c)}{4!}x^4=\dfrac{\sin c}{24}x^4$ for some $c$
between $0$ and $x$. For $x=0.5$: $|\sin c|\le1$ (always true), so
$$|R_3(0.5)|\le\frac{1}{24}(0.5)^4=\frac{0.0625}{24}\approx0.0026<0.003.$$
$\blacksquare$

**The step most people get wrong:** using $f^{(4)}$ (one order past the last kept
term, $x^3$), not $f'''$ — the remainder always uses the derivative *one order
higher* than the highest-order term in $T_n$.
