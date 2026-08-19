Problems: [08-19.md](08-19.md) · Your work: [08-19-work.md](08-19-work.md) · Grading: [08-19-feedback.md](08-19-feedback.md)

# Session 3 Solutions — 2026-08-19

---

## R1 — contrapositive vs. contradiction, when/why

Reach for the **contrapositive** when the negated conclusion $\lnot Q$ gives you
concrete, computable starting material — a specific target ($\lnot P$) to aim at.
Reach for **contradiction** when there's no positive statement to grab (non-existence,
irrationality claims) — you assume $P \wedge \lnot Q$ and search for *any* absurdity,
which is a heavier tool because you don't know in advance what will break.

---

## R2 — setup line: sum of two evens is even

Setup: let $a,b$ be even integers, i.e. $a=2x,\,b=2y$ for some $x,y\in\mathbb{Z}$.

This assumes only that $a,b$ are even — nothing about $a+b$'s parity appears until it's
concluded at the end of the proof.

---

## Core 1 — injective / surjective

### (a) $f:\mathbb{Z}\to\mathbb{Z}$ injective but not surjective

**The function:** $f(n) = 2n$.

**Injective.** Suppose $f(a)=f(b)$. Then $2a=2b$, so $a=b$ (divide both sides by 2).
By definition, $f$ is injective. $\blacksquare$

**Not surjective.** Consider the value $1$ in the codomain. Suppose, for contradiction,
that some $n \in \mathbb{Z}$ satisfies $f(n)=1$. Then $2n=1$, so $n=\tfrac12$. But
$\tfrac12 \notin \mathbb{Z}$ — contradiction. So no integer maps to $1$, and $f$ is not
surjective. $\blacksquare$

**Technique to name:** direct proof for injectivity; a small contradiction sub-argument
for the non-surjectivity witness (assume a preimage exists, derive it isn't an
integer). **The step most people get wrong:** stating the function as an equation
($2a=2b$) instead of a mapping rule ($f(n)=2n$) — write the function itself as the very
first line, separately from any property you're about to prove about it.

### (b) why impossible on a finite set of the same size

Let $|A|=|B|=n<\infty$ and suppose $f:A\to B$ is injective. Injective means the $n$
elements of $A$ map to $n$ *pairwise distinct* elements of $B$ (no two inputs share an
output). That's $n$ distinct outputs, sitting inside a codomain $B$ that has exactly
$n$ elements total — so those $n$ distinct outputs must be *all* of $B$. Every element
of $B$ is hit. That's exactly the definition of surjective.

This is the **pigeonhole principle**: $n$ pigeons (inputs), $n$ holes (outputs), no two
pigeons sharing a hole (injective) $\implies$ every hole has a pigeon (surjective).
There's no room for anything to be left out.

### (c) what this says about finite vs. infinite

On a finite set, injective *forces* surjective because there's no "room" left over once
every input has a distinct output — full usage of the domain's size automatically fills
the codomain. On an infinite set that link breaks: $f(n)=2n$ on $\mathbb{Z}$ is
injective but only ever hits the even integers, leaving infinitely many outputs
(the odds) untouched — there's always room left over. That "always room left over even
after an injective map" property is close to a working definition of what makes a set
infinite (a set is infinite iff it admits an injection into a proper subset of itself —
exactly what $n \mapsto 2n$ demonstrates).

---

## Core 2 — contradiction

### (a) $3 \mid n^2 \implies 3 \mid n$

**Contrapositive.** Assume $3 \nmid n$. Then $n=3k+1$ or $n=3k+2$ for some
$k \in \mathbb{Z}$.

**Case $n=3k+1$:**
$$n^2 = (3k+1)^2 = 9k^2+6k+1 = 3(3k^2+2k)+1.$$
This has the form $3x+1$, so $3 \nmid n^2$.

**Case $n=3k+2$:**
$$n^2 = (3k+2)^2 = 9k^2+12k+4 = 3(3k^2+4k+1)+1.$$
This also has the form $3x+1$, so $3 \nmid n^2$.

In both cases $3 \nmid n^2$. This proves $3 \nmid n \implies 3 \nmid n^2$, which is the
contrapositive of $3 \mid n^2 \implies 3 \mid n$ — and a contrapositive proof ends
*right there*, no separate contradiction step needed. $\blacksquare$

**Technique to name:** contrapositive, full stop — there's no "given" to contradict in
this style of proof; you assume $\lnot Q$, derive $\lnot P$, and that alone establishes
$P \implies Q$. **The step most people get wrong:** narrating a correct contrapositive
proof using contradiction language ("we assumed X, which contradicts the given Y") when
there is no external "given" being contradicted — the two techniques end differently,
and the ending sentence should match which one you actually used.

### (b) $\sqrt3$ is irrational

*Proof.* Suppose, for contradiction, $\sqrt3$ is rational: $\sqrt3 = a/b$ with
$a,b\in\mathbb{Z}$, $b\neq0$, $\gcd(a,b)=1$ (lowest terms).

Squaring: $3 = a^2/b^2$, so $3b^2 = a^2$. This means $3 \mid a^2$ (it's $3$ times the
integer $b^2$). By part (a), $3 \mid a$, so $a = 3c$ for some $c \in \mathbb{Z}$.

Substitute: $3b^2 = (3c)^2 = 9c^2$, so $b^2 = 3c^2$. This means $3 \mid b^2$, and by
part (a) again, $3 \mid b$.

**Land.** Both $a$ and $b$ are multiples of $3$ — but that contradicts $\gcd(a,b)=1$
from the setup. So the assumption that $\sqrt3$ is rational is false. Therefore
$\sqrt3$ is irrational. $\blacksquare$

**Technique to name:** contradiction, reusing a lemma proved in (a) twice (once for
$a$, once for $b$) — small proved facts compounding, same move as the $\sqrt2$ proof in
the lesson. **The step most people get wrong:** doing all the algebra correctly and
then not writing the actual contradiction sentence. Every proof by contradiction needs
an explicit final line naming *which* two things clash (here: "$3\mid a$ and $3\mid b$"
vs. "$\gcd(a,b)=1$") — without it, the proof has assembled all its parts but never
declares itself finished.

---

## Stretch — $\sqrt p$ irrational for any prime $p$

*Proof.* First, the general lemma via Euclid's lemma: if $p \mid n^2 = n \cdot n$, then
(by Euclid's lemma with $a=b=n$) $p \mid n$.

Now suppose, for contradiction, $\sqrt p$ is rational: $\sqrt p = a/b$ with
$a,b \in \mathbb{Z}$, $b \neq 0$, $\gcd(a,b)=1$. Squaring, $p b^2 = a^2$, so
$p \mid a^2$, so by the lemma $p \mid a$. Write $a=pc$. Then $pb^2 = p^2c^2$, so
$b^2 = pc^2$, so $p \mid b^2$, so $p \mid b$.

Both $a$ and $b$ are multiples of $p$, contradicting $\gcd(a,b)=1$. So $\sqrt p$ is
irrational. $\blacksquare$

**The one thing that changed from Core 2(b):** Core 2(a)'s hand case-split
($n=3k+1$ or $3k+2$) is exactly the $p=3$ special case of Euclid's lemma. For a
general prime you can't case-split by hand (there are $p-1$ cases), so Euclid's lemma
is what buys you the same conclusion — "$p \mid n^2 \implies p \mid n$" — without
grinding through residues.
