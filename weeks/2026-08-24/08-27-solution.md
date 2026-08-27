# Solutions — 2026-08-27 (Session 8)

> Posted one day late, per the standing rule. If you're reading this before attempting
> `08-27-work.md`, close this file and go do the problems cold — the whole benefit of
> the lag is retrieval before you see this.

---

## 0. Review

### R1 — existential witness: $n<-3$, $n$ even

**Claim:** $\exists n\in\mathbb{Z}$ such that $n<-3$ and $n$ is even.

**Witness:** $n=-4$.

**Verification:** $-4<-3$ ✓. $-4=2\cdot(-2)$, so $-4$ is even ✓. Both conjuncts hold, so
the existential statement is true.

**The point of this problem:** the domain has to be $\mathbb{Z}$, not $\mathbb{N}$. If
you instinctively reached for a positive number and only then noticed the statement
needs $n<-3$, that's the habit this problem checks — nothing in "there exists $n$"
restricts you to positive integers unless the problem says so.

### R2 — plain English, $T(x,y)$: "$x<y$" over $\mathbb{R}$

**(a)** $\forall x\,\exists y\,T(x,y)$: **true.** $\exists y\,\forall x\,T(x,y)$:
**false.**

**(b)** $\forall x\,\exists y\,T(x,y)$ claims: *every real number has some real number
bigger than it.* The $y$ depends on $x$ — concretely $y=x+1$ always works, but any
value greater than $x$ does. This says $\mathbb{R}$ has no largest element.

$\exists y\,\forall x\,T(x,y)$ would have required: *one single real number $y$ that is
bigger than every real number $x$ at once* — the same $y$ has to beat $x=1$, $x=100$,
$x=y$ itself, all of them. No real number can do this, because for any candidate $y$,
$y+1$ is also a real number and $y+1>y$ — so $y$ fails to beat $x=y+1$. The candidate
defeats itself.

**The step most people get wrong:** treating "$\exists y \forall x$" as if it just
means "some upper-bound-ish number," rather than checking whether a *single fixed* $y$
can survive being tested against *every* $x$, including $x$'s built from $y$ itself.

---

## 1. Repair — prove $d_n = 4-2(-1)^n$ does not converge to $4$

**Setup — what we must show:** $\lnot(d_n\to4)$ means
$$\exists\varepsilon>0\ \text{such that}\ \forall N\in\mathbb{N},\ \exists n>N\ \text{with}\ |d_n-4|\ge\varepsilon.$$
Three moves: pick $\varepsilon$, take an arbitrary $N$, construct an explicit $n>N$ that
survives, then verify.

**Proof.**

Compute $d_n-4 = \bigl(4-2(-1)^n\bigr)-4 = -2(-1)^n$, so
$$|d_n-4| = 2\left|(-1)^n\right| = 2\cdot 1 = 2\quad\text{for every }n,$$
since $(-1)^n$ is always $\pm1$ and $|\pm1|=1$ — this holds regardless of whether $n$
is even or odd, so there is no case split to do.

Take $\varepsilon = 1$. Let $N\in\mathbb{N}$ be arbitrary. Choose $n=N+1$. Then $n>N$,
and by the computation above, $|d_n-4|=2\ge1=\varepsilon$.

Since this $n$ exists for every $N$, $d_n$ does not converge to $4$. $\blacksquare$

**The exact shortcut this problem is built to force:** don't ask "is $N+1$ even or
odd?" The quantity you need a handle on is $|(-1)^{N+1}|$, and that equals $1$
*unconditionally* — the sign of $(-1)^{N+1}$ never enters the argument at all, because
you took an absolute value before it could matter.

---

## 2. Core

### Core 1(a) — $T_2(x)$ and $R_2(x)$ for $f(x)=\cos x$ at $a=0$

$f(x)=\cos x,\ f'(x)=-\sin x,\ f''(x)=-\cos x,\ f'''(x)=\sin x$.

$f(0)=1,\ f'(0)=0,\ f''(0)=-1$.

$$T_2(x) = f(0)+f'(0)x+\frac{f''(0)}{2}x^2 = 1 - \frac{x^2}{2}.$$

Lagrange remainder (third-order term, since $T_2$ stops at degree 2):
$$R_2(x) = \frac{f'''(c)}{3!}x^3 = \frac{\sin c}{6}x^3,\quad\text{for some }c\text{ between }0\text{ and }x.$$

### Core 1(b) — prove $|R_2(x)|\le\frac16$ on $[0,1]$

**Bound and why:** $|\sin c|\le1$ for *every* real $c$ — this is the one-line fact, and
it needs no restriction on $c$'s location, unlike bounding $e^c$ (which needs $c$
confined to the interval to bound it by $e^1$). $\sin$ is bounded by $1$ everywhere,
so whatever $c\in(0,x)$ turns out to be, $|\sin c|\le1$ for free.

**Full argument:**
$$|R_2(x)| = \left|\frac{\sin c}{6}x^3\right| = \frac{|\sin c|}{6}\,|x|^3 \le \frac{1}{6}\cdot1^3 = \frac16,$$
using $|\sin c|\le1$ and, for $x\in[0,1]$, $0\le x\le1\Rightarrow x^3\le1$. So
$|R_2(x)|\le\frac16$ for every $x\in[0,1]$. $\blacksquare$

### Core 2(a) — derive $S_n$ for $r=-\frac13$

$$S_n = \sum_{k=0}^n r^k = 1+r+r^2+\cdots+r^n.$$
$$rS_n = r+r^2+\cdots+r^{n+1}.$$
$$S_n-rS_n = \bigl(1+r+\cdots+r^n\bigr)-\bigl(r+\cdots+r^{n+1}\bigr) = 1-r^{n+1}$$
(every middle term cancels — the whole point of the trick). So
$$(1-r)S_n = 1-r^{n+1}\quad\Longrightarrow\quad S_n=\frac{1-r^{n+1}}{1-r}.$$

With $r=-\frac13$: $1-r=\frac43$, so
$$S_n = \frac{1-\left(-\frac13\right)^{n+1}}{4/3} = \frac34\left(1-\left(-\frac13\right)^{n+1}\right).$$

### Core 2(b) — closed form of $\sum_{k=0}^\infty\left(-\frac13\right)^k$

Since $\left|-\frac13\right|=\frac13<1$, $r^{n+1}\to0$ (given, not reproved). Taking
$n\to\infty$ in (a):
$$\sum_{k=0}^\infty\left(-\frac13\right)^k = \frac{1}{1-r} = \frac{1}{1-\left(-\frac13\right)} = \frac{1}{4/3} = \frac34.$$

---

## Stretch — $\ln(1.5)$ via the degree-3 Taylor polynomial for $\ln(1+x)$

$f(x)=\ln(1+x)$: $f(0)=0$, $f'(x)=\frac{1}{1+x}\Rightarrow f'(0)=1$,
$f''(x)=-\frac{1}{(1+x)^2}\Rightarrow f''(0)=-1$, $f'''(x)=\frac{2}{(1+x)^3}\Rightarrow f'''(0)=2$.

$$T_3(x) = x-\frac{x^2}{2}+\frac{x^3}{3}.$$

At $x=0.5$:
$$T_3(0.5) = 0.5-0.125+\frac{0.125}{3} = 0.5-0.125+0.041\overline{6} \approx 0.4167.$$

**Error bound, proved.** The next term's Lagrange remainder ($f^{(4)}(x)=-\frac{6}{(1+x)^4}$):
$$R_3(x) = \frac{f^{(4)}(c)}{4!}x^4 = \frac{-6/(1+c)^4}{24}x^4 = -\frac{x^4}{4(1+c)^4},\quad c\in(0,x).$$

For $x=0.5$, $c\in(0,0.5)$ so $1+c\in(1,1.5)$, hence $(1+c)^4\ge1$ (the *smallest* it
can be, which gives the *worst-case largest* bound on $|R_3|$ — this is the step most
people skip: you must use the value of $c$ that makes the bound largest, not the value
that happens to be true). So:
$$|R_3(0.5)| = \frac{(0.5)^4}{4(1+c)^4} \le \frac{0.0625}{4\cdot1} = 0.015625.$$

Since $0.015625<0.02$, the approximation $\ln(1.5)\approx0.4167$ is accurate to within
$0.02$ (in fact within $0.0157$). $\blacksquare$

*(Check: $\ln(1.5)\approx0.405465$; actual error $\approx0.0112$ — consistent with, and
smaller than, the $0.0157$ bound, as a bound should be.)*
