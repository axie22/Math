# Calibration Diagnostic — 2026-08-18

**60 minutes. Closed book. No lesson files, no notes, no internet, no LLM.**

This is not a test you can fail. It is the first real data this system has ever had
about what you actually know — six days of problems have been generated and nothing
anywhere recorded how a single one went, which means every difficulty decision so far
was a guess. Phase 0's length, and where Phase 1 starts, get set from this.

**Deliberately answer honestly.** A blank answer is more useful than a bluffed one. If
you don't know, write "don't know" and move on — that is a *clean signal* and it is
worth more than a half-remembered gesture. Overstating here just buys you a curriculum
calibrated to someone else.

Write your work in [`2026-08-18-calibration-work.md`](2026-08-18-calibration-work.md).
Note roughly how long each section took.

---

## Section A — Proof (20 min) — *the section that matters most*

**A1.** Prove that for every integer $n$, if $n^2$ is even then $n$ is even.
State which proof technique you're using and why that one.

**A2.** Prove by induction: $\displaystyle\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6}$.
Write out the base case and the inductive step explicitly.

**A3.** Consider the statement:

> For every $\varepsilon > 0$ there exists $N \in \mathbb{N}$ such that for all $n > N$, $|a_n - L| < \varepsilon$.

(a) Say in plain English what this asserts.
(b) Write its **negation**, correctly, with quantifiers in the right order.
(c) Say in plain English what the negation asserts.

**A4.** Give a function $f : \mathbb{Z} \to \mathbb{Z}$ that is injective but not
surjective, and justify both claims. Then explain why no such function can exist if the
domain and codomain are both a *finite* set of the same size.

---

## Section B — Linear algebra fundamentals (15 min)

**B1.** Define, without looking anything up: *linear independence*, *basis*, *rank*,
*null space*. One or two sentences each, precisely.

**B2.** State the rank–nullity theorem. Then explain in your own words *why* it should
be true — the intuition, not the proof.

**B3.** Let $A = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 1 & 1 & 1 \end{pmatrix}$.
Find $\operatorname{rank}(A)$ and a basis for its null space.

**B4.** True or false, with justification: *if a square matrix has $n$ distinct
eigenvalues, it is diagonalizable.* And: *if a square matrix is diagonalizable, it has
$n$ distinct eigenvalues.*

---

## Section C — Calculus mechanics (10 min)

**C1.** Differentiate $f(x) = \ln\!\left(\sqrt{1 + e^{2x}}\right)$. Show the chain rule
steps.

**C2.** Write the Taylor series of $e^x$ about $0$, and use the first three terms to
approximate $e^{0.1}$. Roughly how large is the error, and how do you know?

**C3.** Compute $\displaystyle\int_0^\infty x e^{-x}\,dx$.

---

## Section D — Retention check on Days 1–6 (15 min)

*Cold recall of material covered Aug 10–17. This measures how much of the last six
sessions survived — the answer directly determines how much re-teaching Phase 2 needs.*

**D1.** For $f(x,y) = x^2 y - 3xy^2$, compute $\nabla f$ and the Hessian $H$ at $(1,1)$.
Classify the critical-point behavior at that point if you can, and say why or why not.

**D2.** In one or two sentences each, without notes:
(a) What does the gradient mean geometrically?
(b) What does an eigenvector mean geometrically?
(c) What does the spectral theorem say, and why does it matter for Hessians and
covariance matrices?

**D3.** Minimize $x^2 + y^2$ subject to $x + y = 6$ using Lagrange multipliers. Then
say what the value of $\lambda$ *means*.

**D4.** Without computing anything: given a matrix $A$, how do you get its singular
values from an eigen-decomposition, and of *which* matrix?

---

## Scoring — how this gets read

| Section | What it measures | If weak → |
|---|---|---|
| A | Proof fluency (the suspected bottleneck) | Phase 0 runs the full 3 weeks, possibly 4 |
| B | Linear algebra foundation | Phase 1 starts from vector-space axioms, no shortcuts |
| C | Calculus mechanics | Calculus repair interleaved throughout Phase 0 |
| D | Retention from Days 1–6 | Determines how much Phase 2 must re-teach |

The most informative outcome is a **weak Section A with a strong Section D**. That
would confirm the transcript's story exactly — fluent at executing procedures, not yet
at justifying them — and it is the pattern this whole restructure is built to fix.

---

*Return here when done. The next run reads your work file and sets Phase 0's real
length from it.*
