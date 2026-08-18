# Calibration Work — 2026-08-18

**Closed book.** Write what you actually know. "Don't know" is a valid and useful answer.

Time started: ___
Time finished: ___

---

## Section A — Proof

### A1 — n² even ⟹ n even
Proof by contradiction. We want to prove that if $n^2$ is even then $n$ is even. For this to be false, there must be some $n$ such that, $n^2 \bmod 2 = 0$ but $n \bmod 2 = 1$.
### A2 — induction, sum of squares
Prove $\displaystyle\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6}$
$k = 1 \rightarrow \frac{1(1 + 1)(2(1) + 1)}{6} = 1$
$k = 2 \rightarrow \frac{2(2 + 1)(2(2)+1)}{6} = 4$
$k = n + 1 \rightarrow (n + 1)^2 = \frac{(n + 1)(n+2)(2n+3)}{6}$
$n + 1 = \frac{(n + 2)(2n+3)}{6}$
$n+1 = \frac{2n^2 + 7n + 6}{6}$
$n=\frac{2n^2 + 7n + 12}{6}$
$2n^2 + 13n + 12 = 0$
### A3 — quantifiers and negation
For every $\varepsilon > 0$ there exists $N \in \mathbb{N}$ such that for all $n > N$, $|a_n - L| < \varepsilon$.
(a) For every error greater than 0, there exists an integer N such that for all n greater than N, the absolute value of $a_n$ minus the loss is less than the error

(b) For every $\epsilon < 0$ there does not exist $N \notin \mathbb{N}$ such taht for all $n < N$, $\epsilon < |a_n - L|$

(c) For every error less than 0, there does not exist an integer N such that for all integers n less than N, the error is less than $a_n$ - L

### A4 — injective not surjective

_(your work)_

**Section A — time taken: ___ / confidence (1–5): ___**

---

## Section B — Linear algebra

### B1 — definitions

- linear independence: rows are independent of one another
- basis:
- rank: the number of non-empty values in the matrix
- null space:

### B2 — rank–nullity + intuition

_(your work)_

### B3 — rank and null space basis

_(your work)_

### B4 — diagonalizability, both directions

_(your work)_

**Section B — time taken: ___ / confidence (1–5): ___**

---

## Section C — Calculus

### C1 — chain rule

_(your work)_

### C2 — Taylor series and error

_(your work)_

### C3 — integral

_(your work)_

**Section C — time taken: ___ / confidence (1–5): ___**

---

## Section D — Days 1–6 retention

**Note that I did not do days 8-12, 8-13, 8-16**
### D1 — gradient and Hessian

$f(x^2, y) = x^2 y - 3xy^2$
$dx = 2xy - 3y^2$
$dy = x^2 - 6xy$
$f\Delta = (2xy - 3y^2, x^2 - 6xy)$
$f(1, 1) = (-7, -5)$

### D2 — conceptual recall

(a) gradient: gradient is like slope but in 3 dimensions. We're looking at the change in direction in more than just x and y planes

(b) eigenvector:

(c) spectral theorem:

### D3 — Lagrange multipliers + meaning of λ

_(your work)_

### D4 — singular values from an eigendecomposition

_(your work)_

**Section D — time taken: ___ / confidence (1–5): ___**

---

## Notes to self

*Anything that felt shaky, anything you've clearly never seen before, anything you
knew a year ago and don't now. This is signal too.*
