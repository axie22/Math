Problems: [08-16.md](08-16.md)

# Day 5 Solutions — Linear Algebra II (Foundational)

## Problem 1 — Hessian classification (warm-up)

**What's being asked.** We need the critical point of $f(x,y)=x^2+xy+y^2-3x-3y+4$, then classify it using the second-derivative (Hessian) test from the multivariable calculus unit. This is a direct rerun of the technique from Day 3–4, so the goal is mostly to warm up and to generate the matrix we'll dissect with eigenvalues in Problem 2.

**Step 1: find the critical point.** Set both partial derivatives to zero.
$$f_x = 2x + y - 3 = 0, \qquad f_y = x + 2y - 3 = 0.$$
From the first equation, $y = 3-2x$. Substitute into the second:
$$x + 2(3-2x) - 3 = 0 \implies x + 6 - 4x - 3 = 0 \implies -3x + 3 = 0 \implies x = 1.$$
Then $y = 3-2(1) = 1$. So the only critical point is $(1,1)$. (It's the *only* one because both equations are linear — a quadratic function like this has at most one critical point.)

**Step 2: compute the Hessian.** Second partials: $f_{xx}=2$, $f_{yy}=2$, $f_{xy}=f_{yx}=1$ (equal by Clairaut's theorem, since $f$ is a smooth polynomial). So
$$H = \begin{pmatrix} f_{xx} & f_{xy} \\ f_{xy} & f_{yy} \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 2 \end{pmatrix}.$$
Because $f$ is a pure quadratic (no higher-degree terms), $H$ is the *same* at every point, not just $(1,1)$ — that's why Problem 2 can reuse it without re-deriving anything.

**Step 3: apply the second-derivative test.** $D = \det(H) = (2)(2)-(1)(1) = 4-1=3$. Since $D>0$ and $f_{xx}=2>0$, the test says $(1,1)$ is a **local minimum**.

**Sanity check / intuition.** $D>0$ means the surface curves the same way in every direction near $(1,1)$ (no direction where it curves oppositely, which would create a saddle); $f_{xx}>0$ tells you *which* way — upward, i.e. a bowl. You can also just complete the square: $f(x,y) = (x-1)^2+(x-1)(y-1)+(y-1)^2+ \text{const}$ near $(1,1)$ is a positive-definite quadratic form plus a constant, confirming a genuine minimum, not just a local artifact of the test.

**Answer: $(1,1)$ is a local minimum, with $H=\begin{pmatrix}2&1\\1&2\end{pmatrix}$.**

---

## Problem 2 — Eigenvalues and eigenvectors of the Hessian (core)

**What's being asked, and why this approach.** We want the eigenvalues/eigenvectors of $A = \begin{pmatrix}2&1\\1&2\end{pmatrix}$ — the same matrix from Problem 1. The standard approach (today's lesson, Section 2) is: solve $\det(A-\lambda I)=0$ for $\lambda$, then for each $\lambda$ solve $(A-\lambda I)\mathbf{v}=\mathbf{0}$ for $\mathbf{v}$.

**Step 1: characteristic polynomial.**
$$A - \lambda I = \begin{pmatrix}2-\lambda & 1 \\ 1 & 2-\lambda\end{pmatrix}.$$
$$\det(A-\lambda I) = (2-\lambda)^2 - (1)(1) = (2-\lambda)^2 - 1.$$
Expand: $(2-\lambda)^2 = 4 - 4\lambda + \lambda^2$, so the characteristic polynomial is $\lambda^2 - 4\lambda + 3 = 0$.

*Why we're allowed to just take the determinant:* $(A-\lambda I)\mathbf{v}=\mathbf{0}$ has a nonzero solution $\mathbf{v}$ only if $A - \lambda I$ is singular — an invertible matrix maps only $\mathbf{0}$ to $\mathbf{0}$. A square matrix is singular exactly when its determinant is zero, which is where this equation comes from.

**Step 2: solve for $\lambda$.** Factor $\lambda^2-4\lambda+3 = (\lambda-3)(\lambda-1) = 0$, so $\lambda_1 = 3$, $\lambda_2 = 1$.

*Quick sanity check using the cheat-sheet shortcuts:* $\mathrm{tr}(A) = 2+2 = 4$ should equal $\lambda_1+\lambda_2 = 3+1=4$ ✓. $\det(A)=3$ should equal $\lambda_1\lambda_2 = 3\times 1 = 3$ ✓. Both check out — this is a fast way to catch arithmetic errors before going further.

**Step 3: find the eigenvector for $\lambda_1=3$.** Solve $(A-3I)\mathbf{v}=\mathbf{0}$:
$$A - 3I = \begin{pmatrix}-1&1\\1&-1\end{pmatrix}.$$
Row-reduce: row 2 is $-1\times$ row 1, so this system is really just one equation: $-x+y=0 \implies y=x$. Any vector of the form $(t,t)$ works; take $\mathbf{v}_1 = (1,1)$ (or normalized, $\frac{1}{\sqrt2}(1,1)$).

**Step 4: find the eigenvector for $\lambda_2=1$.** Solve $(A-I)\mathbf{v}=\mathbf{0}$:
$$A - I = \begin{pmatrix}1&1\\1&1\end{pmatrix}.$$
Again one independent equation: $x+y=0 \implies y=-x$. Take $\mathbf{v}_2 = (1,-1)$.

**Step 5: verify.**
$$A\mathbf{v}_1 = \begin{pmatrix}2&1\\1&2\end{pmatrix}\begin{pmatrix}1\\1\end{pmatrix} = \begin{pmatrix}3\\3\end{pmatrix} = 3\begin{pmatrix}1\\1\end{pmatrix} = 3\mathbf{v}_1. \checkmark$$
$$A\mathbf{v}_2 = \begin{pmatrix}2&1\\1&2\end{pmatrix}\begin{pmatrix}1\\-1\end{pmatrix} = \begin{pmatrix}1\\-1\end{pmatrix} = 1\cdot\mathbf{v}_2. \checkmark$$
Both check out exactly. (Note also $\mathbf{v}_1 \cdot \mathbf{v}_2 = 1-1=0$ — they're orthogonal, exactly as the spectral theorem guarantees since $A$ is symmetric. This is precisely the matrix used as the worked example in today's lesson figure, so you can cross-check your answer visually there.)

**Connecting back to Problem 1.** Both eigenvalues are positive ($3>0$ and $1>0$). A symmetric matrix with all-positive eigenvalues is called **positive definite**, and positive-definiteness of the Hessian is the $n$-dimensional generalization of "$D>0$ and $f_{xx}>0$" — they are two different tests for the exact same fact. In 2 variables, $D=\det(H)=\lambda_1\lambda_2$ and $f_{xx}\approx$ (informally) tracks the sign pattern; when $n>2$ there's no simple determinant shortcut, and eigenvalues become the *only* general tool. So Problem 1's "local minimum" conclusion and Problem 2's "both eigenvalues positive" conclusion are the same statement in two different languages — and only the eigenvalue language survives once you leave two dimensions.

**Answer: $\boxed{\lambda_1=3,\ \mathbf{v}_1=(1,1); \quad \lambda_2=1,\ \mathbf{v}_2=(1,-1)}$ — both positive, confirming the local-minimum classification from Problem 1.**

---

## Problem 3 — Principal components of a covariance matrix (stretch)

**What's being asked, and why this approach.** $\Sigma = \begin{pmatrix}5&2\\2&2\end{pmatrix}$ is a (toy) covariance matrix for two centered features. PCA says: the eigenvectors of $\Sigma$ are the principal component directions, and the eigenvalues are the variance captured along each. Same machinery as Problem 2 — characteristic polynomial, then null space — just a different matrix and a different interpretation of the answer.

**Step 1: characteristic polynomial.**
$$\Sigma - \lambda I = \begin{pmatrix}5-\lambda&2\\2&2-\lambda\end{pmatrix}, \qquad \det(\Sigma-\lambda I) = (5-\lambda)(2-\lambda) - 4.$$
Expand $(5-\lambda)(2-\lambda) = 10 -5\lambda-2\lambda+\lambda^2 = \lambda^2 -7\lambda+10$, so
$$\det(\Sigma-\lambda I) = \lambda^2-7\lambda+10-4 = \lambda^2-7\lambda+6=0.$$

**Step 2: solve for $\lambda$.** Factor: $(\lambda-6)(\lambda-1)=0 \implies \lambda_1=6,\ \lambda_2=1$.
*Sanity check:* $\mathrm{tr}(\Sigma)=5+2=7=6+1$ ✓, $\det(\Sigma)=10-4=6=6\times1$ ✓.

**Step 3: eigenvector for $\lambda_1=6$.**
$$\Sigma - 6I = \begin{pmatrix}-1&2\\2&-4\end{pmatrix}.$$
Row 2 is $-2\times$ row 1, so one equation: $-x+2y=0 \implies x=2y$. Take $\mathbf{v}_1=(2,1)$.

**Step 4: eigenvector for $\lambda_2=1$.**
$$\Sigma - I = \begin{pmatrix}4&2\\2&1\end{pmatrix}.$$
Row 1 is $2\times$ row 2, so one equation: $4x+2y=0 \implies y=-2x$. Take $\mathbf{v}_2=(1,-2)$.

*Quick orthogonality check:* $\mathbf{v}_1\cdot\mathbf{v}_2 = (2)(1)+(1)(-2)=0$ ✓ — expected, since $\Sigma$ is symmetric.

**Step 5: interpret as PCA.** Total variance in the data equals $\mathrm{tr}(\Sigma) = \lambda_1+\lambda_2 = 6+1=7$ (this is a general fact: trace is basis-independent, and equals the sum of the individual feature variances $5+2=7$ either way you slice it). The first principal component, direction $\mathbf{v}_1=(2,1)$ (normalize to $\frac{1}{\sqrt5}(2,1)$), captures $\lambda_1=6$ units of variance. As a fraction of the total:
$$\frac{\lambda_1}{\lambda_1+\lambda_2} = \frac{6}{7} \approx 85.7\%.$$

**Intuition.** If you scatter-plotted this 2-feature dataset, the cloud of points would look like a tilted ellipse, elongated along the $(2,1)$ direction and much narrower along $(1,-2)$. Projecting the data onto just the first principal component ($\mathbf{v}_1$) would throw away only about 14.3% of the total variance — in a real ML pipeline with hundreds of features, this is exactly the calculation (repeated across all eigenvalues) that tells you how many components to keep for a target amount of "variance explained," e.g. "keep the top $k$ components that together capture 95% of variance."

**Answer: $\boxed{\lambda_1=6\ (\mathbf{v}_1=(2,1)),\ \lambda_2=1\ (\mathbf{v}_2=(1,-2));\ \text{first PC captures } 6/7\approx85.7\%\text{ of total variance}}$.**

---

## Takeaway

All three problems used the *same* two-step recipe — characteristic polynomial, then null space — on three different symmetric $2\times2$ matrices, but the eigenvalues meant three different things depending on where the matrix came from: curvature sign (Problem 1→2, Hessian) and variance share (Problem 3, covariance). That's the real power of eigenvalues/eigenvectors: the linear algebra doesn't change, only the interpretation does. Next up in this topic: diagonalization and using $A=PDP^{-1}$ to compute matrix powers efficiently, followed by the Singular Value Decomposition for matrices that aren't square or symmetric.
