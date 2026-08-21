Problems: [08-21.md](08-21.md) · Your work: [08-21-work.md](08-21-work.md) · Grading: [08-21-feedback.md](08-21-feedback.md)

# Session 5 Solutions — 2026-08-21 (Review day)

*Posted late — this should have gone up alongside Session 6's build on 08-24 and was
missed. Backfilled 2026-08-25.*

---

## Part 1 — Section C

### C1 — $f(x) = \ln\!\left(\sqrt{1+e^{2x}}\right)$

Rewrite first: $f(x) = \tfrac12\ln(1+e^{2x})$ — pulling the square root out through
the log as a factor of $\tfrac12$ avoids ever differentiating a square root.

$$f'(x) = \frac12 \cdot \frac{2e^{2x}}{1+e^{2x}} = \frac{e^{2x}}{1+e^{2x}}$$

**The step most people get wrong:** differentiating $\sqrt{1+e^{2x}}$ directly (chain
rule inside chain rule inside chain rule) instead of using $\ln\sqrt{u} = \tfrac12\ln u$
to strip the square root first. Same answer either way, but the log-rewrite cuts the
problem from three nested chain rules to one.

### C2 — Taylor series of $e^x$, approximate $e^{0.1}$

$$e^x = \sum_{k=0}^{\infty} \frac{x^k}{k!} = 1 + x + \frac{x^2}{2} + \frac{x^3}{6} + \cdots$$

Three terms at $x = 0.1$:

$$e^{0.1} \approx 1 + 0.1 + \frac{0.01}{2} = 1.105$$

**Error size:** the first dropped term is $\frac{x^3}{6} = \frac{0.001}{6} \approx 0.00017$,
and Taylor's theorem with remainder says the true error is bounded by that term times a
factor close to 1 (since $e^x$ near $x=0$ is close to 1) — so the approximation is good
to about $10^{-4}$. (True value: $e^{0.1} \approx 1.10517$; actual error $\approx 0.00017$,
matching the estimate.)

**The step most people get wrong:** not having a way to bound the error at all — "it's
probably close" isn't a bound. The right move is *the next term you didn't include is
the right order of magnitude for the error*, which is the informal form of the Lagrange
remainder.

### C3 — $\displaystyle\int_0^\infty x e^{-x}\,dx$

Integration by parts: $u = x$, $dv = e^{-x}dx$, so $du = dx$, $v = -e^{-x}$.

$$\int_0^\infty xe^{-x}dx = \Big[-xe^{-x}\Big]_0^\infty + \int_0^\infty e^{-x}dx$$

The boundary term is $0$ at both ends ($x=0$ kills it; as $x\to\infty$, $e^{-x}$ decays
faster than $x$ grows, so $xe^{-x}\to0$ — this needs a word of justification, not just
silence). The remaining integral is $\big[-e^{-x}\big]_0^\infty = 0-(-1) = 1$.

$$\int_0^\infty xe^{-x}\,dx = 1$$

**The step most people get wrong:** asserting $xe^{-x}\to 0$ as $x\to\infty$ without
saying why — exponential decay beats polynomial growth, always, and that's worth one
sentence rather than a silent limit.

---

## Part 2 — Mixed retrieval

### 2a — $\sqrt3$ is irrational, from memory

Suppose for contradiction $\sqrt3 = a/b$ with $a,b\in\mathbb{Z}$, $\gcd(a,b)=1$. Then
$3b^2 = a^2$, so $3\mid a^2$, so $3\mid a$ (3 is prime). Write $a=3c$. Then
$3b^2 = 9c^2$, so $b^2 = 3c^2$, so $3\mid b^2$, so $3\mid b$.

**Last sentence, spelled out:** but then $3$ divides both $a$ and $b$, contradicting
$\gcd(a,b)=1$. Hence no such $a,b$ exist, and $\sqrt3$ is irrational. $\blacksquare$

**The step most people get wrong (historically, in this repo):** deriving both
divisibility facts correctly and then stopping — the proof isn't finished until the
sentence naming *which* assumption they contradict is actually written.

### 2b — Tuesday's Core 2(a): technique and correct ending

**Technique:** contrapositive. The claim $3\mid n^2 \implies 3\mid n$ was proved by
showing the contrapositive $3\nmid n \implies 3\nmid n^2$.

**Correct ending:** "...so $3\nmid n^2$. This proves the contrapositive
$3\nmid n\implies 3\nmid n^2$, and since a statement and its contrapositive are
logically equivalent, this establishes $3\mid n^2\implies 3\mid n$."

**The step most people get wrong:** proving the contrapositive statement correctly and
then never saying *why that settles the original claim* — the logical-equivalence
sentence is not optional decoration, it's the piece that turns "I proved a related
fact" into "I proved the theorem."

### 2c — negate, connective rule explicit

**(i)** $\forall x\in\mathbb{R},\ (x<0\implies x^2>0)$

Rule: $\lnot(A\implies B)\equiv A\wedge\lnot B$ — arrow disappears, antecedent
asserted, consequent negated.

$$\exists x\in\mathbb{R},\ \big(x<0 \wedge x^2\le0\big)$$

**(ii)** $\exists n\in\mathbb{Z},\ (n\text{ even}\wedge n>100)$

Rule: quantifier flips ($\exists\to\forall$); De Morgan on the conjunction
($\lnot(A\wedge B)\equiv\lnot A\vee\lnot B$).

$$\forall n\in\mathbb{Z},\ \big(n\text{ odd}\vee n\le100\big)$$

**The step most people get wrong:** in (i), touching $x<0$ (it's the antecedent of the
implication, asserted not negated — the arrow removal already accounts for it) and
mistakenly writing $x^2\le0 \to x^2<0$ wrong direction; in (ii), swapping $\wedge\to\vee$
correctly but forgetting to negate *each* conjunct ("even" must become "odd," not stay
"even," and $n>100$ must become $n\le100$, not $n<100$).

### 2d — pigeonhole, general principle

**In words:** if you have more items than containers, at least one container must hold
more than one item — you cannot place more distinct objects into a finite collection of
slots than the number of slots without a collision.

**Connecting Tuesday and Thursday:** Tuesday's Core 1(b) was the *equal-size* case,
$|A|=|B|$ — there, an injective function is automatically surjective, because using up
all $|B|$ slots with $|A|=|B|$ distinct outputs leaves nothing uncovered. Thursday's
problem pushed to $|A|>|B|$ strictly — there, injective isn't just "forced to be
surjective," it's *impossible*, because there aren't even enough slots to hold all the
distinct outputs an injection would require.

---

## Part 3 — Synthesis

### 3a — general pigeonhole: finite $A,B$, $|A|>|B|$ $\implies$ no injective $f:A\to B$

*Proof.* Suppose for contradiction that $f:A\to B$ is injective, with $A,B$ finite and
$|A|>|B|$. Since $f$ is injective, the elements $f(a)$ for $a\in A$ are pairwise
distinct, so the image $f(A)\subseteq B$ has exactly $|A|$ elements. But $f(A)\subseteq
B$ forces $|f(A)|\le|B|$. Combining, $|A| = |f(A)| \le |B|$, contradicting $|A|>|B|$.
Hence no injective $f:A\to B$ exists. $\blacksquare$

**Technique:** contradiction, with the counting fact "$|f(A)|=|A|$ when $f$ is
injective, and $f(A)\subseteq B$ forces $|f(A)|\le|B|$" doing the real work — this is
the general version of Thursday's $\{1,\dots,6\}\to\{1,\dots,5\}$ argument, with $n=6$,
$m=5$ replaced by arbitrary $|A|>|B|$.

### 3b — why finiteness is required, connected to $f(n)=2n$ on $\mathbb{Z}$

The proof above leans on $|A| = |f(A)| \le |B|$ being a genuine numerical inequality —
that only makes sense because $|A|$ and $|B|$ are finite counting numbers you can
compare with $\le$. For $f(n)=2n$ on $\mathbb{Z}\to\mathbb{Z}$, both $A=\mathbb{Z}$ and
$B=\mathbb{Z}$ are infinite, and "$|A|>|B|$" isn't even a meaningful hypothesis in the
same sense — $\mathbb{Z}$ and $\mathbb{Z}$ have the "same size" as infinite sets (both
countably infinite), yet $f(n)=2n$ is injective and *not* surjective (no odd number is
hit). The finite pigeonhole argument's entire mechanism — "using up all the room" —
depends on there being a fixed finite amount of room to use up. An infinite set can
absorb an injective image of "the same size" as itself and still have room left over
(here, all the odd numbers); there is no analogous "running out of slots" step for
infinite cardinalities, which is exactly why injective does not imply surjective (or
vice versa) once either set is infinite.
