# Alex's Daily Math Practice — Progress Log

Append-only historical log. For where things stand *now* see [`START-HERE.md`](START-HERE.md)
and [`STATE.md`](STATE.md); for where they're going see [`CURRICULUM.md`](CURRICULUM.md).

> **2026-08-17 — restructured.** Retargeted from "ML/AI + rockets/aerospace" to **ML at
> research depth + mathematical maturity**. Days 1–6 below are reclassified as a
> *preview* of Phase 2 material rather than completed coverage — and Days 3, 4, and 5
> were never actually attempted, so no mastery can be inferred from any of it.

| Date | Topic | Difficulty | Problem Summary | Link |
|------|-------|------------|------------------|------|
| 2026-08-10 | Multivariable Calculus | Foundational | Partial derivatives and gradient of $f(x,y)=3x^2y-2xy^3+5$ | [weeks/2026-08-10/08-10.md](weeks/2026-08-10/08-10.md) |
| 2026-08-11 | Multivariable Calculus | Foundational+ | Directional derivative and steepest ascent/descent of $f(x,y)=x^2y-3xy^2+2y^3$ | [weeks/2026-08-10/08-11.md](weeks/2026-08-10/08-11.md) |
| 2026-08-12 | Multivariable Calculus | Intermediate | *(not attempted)* Warm-up directional derivative; critical points/Hessian classification of $f(x,y)=x^3-3xy+y^3$; double-well loss $L(w_1,w_2)=w_1^4-4w_1^2+w_2^2$ | [weeks/2026-08-10/08-12.md](weeks/2026-08-10/08-12.md) |
| 2026-08-13 | Multivariable Calculus | Advanced | *(not attempted)* Lagrange multipliers minimizing $x^2+y^2$ s.t. $x+y=6$; 3-variable minimum-energy thrust allocation | [weeks/2026-08-10/08-13.md](weeks/2026-08-10/08-13.md) |
| 2026-08-16 | Linear Algebra II | Foundational | *(not attempted)* Eigenvalues/eigenvectors of $\begin{pmatrix}2&1\\1&2\end{pmatrix}$; PCA-style eigen-decomposition of a covariance matrix | [weeks/2026-08-10/08-16.md](weeks/2026-08-10/08-16.md) |
| 2026-08-17 | Linear Algebra II | Foundational+ | Eigendecomposition of $\begin{pmatrix}4&1\\1&4\end{pmatrix}$; diagonalization $A=PDP^{-1}$ for $A^4\mathbf{x}_0$; SVD of $\begin{pmatrix}3&0\\4&5\end{pmatrix}$ via $A^\top A$ | [weeks/2026-08-17/08-17.md](weeks/2026-08-17/08-17.md) |
| 2026-08-17 | **Calibration diagnostic** | Assessment | Closed-book baseline across proof, linear algebra, calculus mechanics, and Days 1–6 retention. **A ~20% · B ~5% · C no data · D n/a.** Three named bugs identified | [diagnostic](diagnostics/2026-08-18-calibration.md) — [feedback](diagnostics/2026-08-18-calibration-feedback.md) |
| 2026-08-18 | **Proof Foundations** (Phase 0) | Foundational (repair) | $n^2$ even $\Rightarrow n$ even by contrapositive; sum of evens, product of odds, transitivity of divisibility; injective-not-surjective $f:\mathbb{Z}\to\mathbb{Z}$ and why it fails on finite sets; stretch: $3 \mid n^2 \Rightarrow 3 \mid n$. **Graded:** R1/R2/Core 1 attempted (1c clean; 1a/1b assumed the conclusion in Setup); Core 2 and stretch not attempted (2nd blank on injective/surjective). Bug #1 improved — every attempt reached a landing. | [weeks/2026-08-17/08-18.md](weeks/2026-08-17/08-18.md) — [feedback](weeks/2026-08-17/08-18-feedback.md) — Lesson: [lessons/proof-foundations.md](lessons/proof-foundations.md) |
| 2026-08-19 | **Proof Foundations** (Phase 0) | Foundational (repair, held) | Injective/surjective (non-optional, 3rd attempt); $3\mid n^2 \Rightarrow 3\mid n$ by contrapositive; $\sqrt3$ irrational by contradiction; stretch: $\sqrt p$ irrational for any prime $p$. Two standing rules added: Setup states only the hypothesis, witnesses in $\mathbb{Z}$ not $\mathbb{N}$. **Graded:** setup discipline and $\mathbb{Z}$-witnesses clean 4/4; injective/not-surjective example correct (notation fix needed); pigeonhole mechanism missing (1b/1c); $\sqrt3$ proof derived everything but never wrote the closing contradiction (bug #1 relapse); contrapositive in 2(a) narrated as contradiction. | [weeks/2026-08-17/08-19.md](weeks/2026-08-17/08-19.md) — [feedback](weeks/2026-08-17/08-19-feedback.md) |
| 2026-08-20 | **Proof Foundations** (Phase 0) | Foundational, new topic | Quantifier negation drill (6 statements incl. one requiring a witness proof); pigeonhole proof that no injective $\{1,\dots,6\}\to\{1,\dots,5\}$ exists, repairing 08-19's Core 1(b)/(c); stretch: negation of surjective applied to $f(n)=2n$. Review block retests the $\sqrt3$ landing and the contrapositive/contradiction framing slip from 08-19. | [weeks/2026-08-17/08-20.md](weeks/2026-08-17/08-20.md) |
