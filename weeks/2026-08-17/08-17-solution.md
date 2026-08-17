Problems: [08-17.md](08-17.md)

# Day 6 Solutions — Linear Algebra II (Foundational+)

## Problem 1 — Eigendecomposition of a symmetric matrix

**What's being asked:** find eigenvalues/eigenvectors of $A = \begin{pmatrix}4&1\\1&4\end{pmatrix}$ by hand, and confirm orthogonality of the eigenvectors.

**Approach:** eigenvalues come from the characteristic equation $\det(A-\lambda I) = 0$; each eigenvector comes from solving $(A-\lambda I)\mathbf{v} = \mathbf{0}$ for that eigenvalue.

**Step 1 — characteristic polynomial.**

$$\det(A-\lambda I) = \det\begin{pmatrix}4-\lambda & 1\\ 1 & 4-\lambda\end{pmatrix} = (4-\lambda)^2 - 1.$$

Expand: $(4-\lambda)^2 - 1 = \lambda^2 - 8\lambda + 16 - 1 = \lambda^2 - 8\lambda + 15$. Setting this to zero and factoring: $\lambda^2-8\lambda+15 = (\lambda-3)(\lambda-5) = 0$, so $\lambda_1 = 5$, $\lambda_2 = 3$.

*Why this works:* $(A-\lambda I)\mathbf{v}=\mathbf{0}$ has a nonzero solution $\mathbf{v}$ only when $A-\lambda I$ is singular, and a matrix is singular exactly when its determinant is zero — that's the whole justification for solving $\det(A-\lambda I)=0$ instead of guessing.

**Step 2 — eigenvector for $\lambda=5$.** Solve $(A-5I)\mathbf{v}=\mathbf{0}$:

$$\begin{pmatrix}-1 & 1\\ 1 & -1\end{pmatrix}\begin{pmatrix}v_1\\v_2\end{pmatrix} = \begin{pmatrix}0\\0\end{pmatrix} \implies -v_1+v_2=0 \implies v_1=v_2.$$

So $\mathbf{v}_1 = (1,1)$ (any nonzero scalar multiple works — eigenvectors are only defined up to scale).

**Step 3 — eigenvector for $\lambda=3$.** Solve $(A-3I)\mathbf{v}=\mathbf{0}$:

$$\begin{pmatrix}1 & 1\\ 1 & 1\end{pmatrix}\begin{pmatrix}v_1\\v_2\end{pmatrix} = \begin{pmatrix}0\\0\end{pmatrix} \implies v_1+v_2=0 \implies v_1=-v_2.$$

So $\mathbf{v}_2 = (1,-1)$.

**Step 4 — check orthogonality.** $\mathbf{v}_1 \cdot \mathbf{v}_2 = (1)(1) + (1)(-1) = 0$. Orthogonal, as claimed.

**Why this was guaranteed in advance:** $A$ is symmetric ($A = A^\top$), and the spectral theorem says every real symmetric matrix has real eigenvalues *and* can always have its eigenvectors chosen orthonormal — you didn't need to check, you could have predicted it. This is special to symmetric matrices; Problem 3's matrix is *not* symmetric, which is exactly why we need the heavier SVD machinery there instead of a plain eigendecomposition.

**Sanity check:** $\mathrm{tr}(A) = 4+4 = 8 = \lambda_1+\lambda_2 = 5+3$ ✓, and $\det(A) = 16-1=15 = \lambda_1\lambda_2 = 5\times 3$ ✓.

$$\boxed{\lambda_1=5,\ \mathbf{v}_1=(1,1); \quad \lambda_2=3,\ \mathbf{v}_2=(1,-1); \quad \mathbf{v}_1\perp\mathbf{v}_2}$$

---

## Problem 2 — Diagonalization to evolve a linear system

**What's being asked:** given $A=\begin{pmatrix}3&1\\1&3\end{pmatrix}$ and $\mathbf{x}_0=(1,0)$, compute $\mathbf{x}_4 = A^4\mathbf{x}_0$ via diagonalization (not repeated multiplication), then interpret the long-run behavior.

**Why diagonalization instead of just multiplying $A$ by itself:** computing $A^4$ directly takes 3 matrix multiplications, and for large exponents (or in a real control loop running thousands of timesteps) that cost adds up. Diagonalizing once and reusing it is $O(n^3)$ *one time*, then each subsequent power is just raising scalars — this is the actual reason diagonalization matters practically, not just as an algebra exercise.

**Step 1 — find eigenvalues.** $\det(A-\lambda I) = (3-\lambda)^2 - 1 = \lambda^2-6\lambda+9-1=\lambda^2-6\lambda+8=(\lambda-4)(\lambda-2)=0$. So $\lambda_1=4$, $\lambda_2=2$.

**Step 2 — find eigenvectors.**
For $\lambda=4$: $(A-4I)\mathbf{v}=0 \implies \begin{pmatrix}-1&1\\1&-1\end{pmatrix}\mathbf{v}=0 \implies v_1=v_2$, so $\mathbf{v}_1=(1,1)$.
For $\lambda=2$: $(A-2I)\mathbf{v}=0 \implies \begin{pmatrix}1&1\\1&1\end{pmatrix}\mathbf{v}=0 \implies v_1=-v_2$, so $\mathbf{v}_2=(1,-1)$.

**Step 3 — assemble $P$, $D$, $P^{-1}$.**

$$P = \begin{pmatrix}1&1\\1&-1\end{pmatrix}, \qquad D = \begin{pmatrix}4&0\\0&2\end{pmatrix}.$$

$\det(P) = (1)(-1)-(1)(1) = -2$. For a $2\times 2$ matrix $\begin{pmatrix}a&b\\c&d\end{pmatrix}$, the inverse is $\frac{1}{ad-bc}\begin{pmatrix}d&-b\\-c&a\end{pmatrix}$, so

$$P^{-1} = \frac{1}{-2}\begin{pmatrix}-1&-1\\-1&1\end{pmatrix} = \begin{pmatrix}0.5&0.5\\0.5&-0.5\end{pmatrix}.$$

**Step 4 — compute $A^4\mathbf{x}_0 = PD^4P^{-1}\mathbf{x}_0$, working right to left.**

First, $P^{-1}\mathbf{x}_0$ — this expresses $\mathbf{x}_0$ in the eigenbasis (how much of each eigenvector direction is present):

$$P^{-1}\begin{pmatrix}1\\0\end{pmatrix} = \begin{pmatrix}0.5\\0.5\end{pmatrix}.$$

Makes sense: $(1,0) = 0.5(1,1) + 0.5(1,-1)$, i.e. $\mathbf{x}_0$ is an equal 50/50 mix of both eigendirections.

Next, apply $D^4 = \mathrm{diag}(4^4, 2^4) = \mathrm{diag}(256,16)$ — in the eigenbasis this is just per-coordinate scaling:

$$D^4\begin{pmatrix}0.5\\0.5\end{pmatrix} = \begin{pmatrix}128\\8\end{pmatrix}.$$

Finally, convert back to the standard basis with $P$:

$$P\begin{pmatrix}128\\8\end{pmatrix} = \begin{pmatrix}1&1\\1&-1\end{pmatrix}\begin{pmatrix}128\\8\end{pmatrix} = \begin{pmatrix}128+8\\128-8\end{pmatrix} = \begin{pmatrix}136\\120\end{pmatrix}.$$

**Sanity check by brute force:** $A^2 = \begin{pmatrix}3&1\\1&3\end{pmatrix}\begin{pmatrix}3&1\\1&3\end{pmatrix} = \begin{pmatrix}10&6\\6&10\end{pmatrix}$, and $A^4=(A^2)^2=\begin{pmatrix}10&6\\6&10\end{pmatrix}\begin{pmatrix}10&6\\6&10\end{pmatrix}=\begin{pmatrix}136&120\\120&136\end{pmatrix}$. Then $A^4\mathbf{x}_0 = (136,120)$ — matches exactly. The diagonalization shortcut is correct, and for larger exponents it would have saved far more work than this small example shows.

**Step 5 — interpret the long-run direction.** $\mathbf{x}_0=(1,0)$ started purely along the standard basis, with no particular alignment to either eigendirection. After 4 steps, $\mathbf{x}_4=(136,120)$ has a component ratio of $136:120 \approx 1.13:1$ — much closer to the $1:1$ ratio of $\mathbf{v}_1=(1,1)$ than the $0.5{:}0.5$ split it started as. This isn't a coincidence: since $\lambda_1=4 > \lambda_2=2$, the $\lambda_1$ component gets multiplied by $4^k$ while the $\lambda_2$ component only gets multiplied by $2^k$, so the $\mathbf{v}_1$ direction dominates more and more as $k$ grows. As $k\to\infty$, $\mathbf{x}_k$ becomes arbitrarily well-aligned with $\mathbf{v}_1=(1,1)$, regardless of the starting direction (as long as $\mathbf{x}_0$ has *any* nonzero component along $\mathbf{v}_1$).

This is exactly **power iteration** — the algorithm behind PageRank's dominant-eigenvector computation, and the reason the largest eigenvalue of a Hessian controls the maximum stable learning rate in gradient descent (mentioned in the lesson's Connections section): repeated application of a linear map amplifies the dominant eigendirection exponentially faster than the rest.

$$\boxed{\mathbf{x}_4 = (136,\,120); \quad \text{direction converges toward } \mathbf{v}_1=(1,1) \text{ as } k\to\infty \text{ since } \lambda_1=4 > \lambda_2=2}$$

---

## Problem 3 — Computing an SVD from scratch

**What's being asked:** find the SVD $A=U\Sigma V^\top$ of the non-symmetric matrix $A=\begin{pmatrix}3&0\\4&5\end{pmatrix}$.

**Why we can't just eigendecompose $A$ directly:** $A$ is not symmetric, so the spectral theorem doesn't apply — $A$'s own eigenvectors (if real at all) aren't guaranteed orthogonal. The lesson's key trick is to instead eigendecompose $A^\top A$, which is *always* symmetric and positive semi-definite no matter what $A$ looks like, and build the SVD from that.

**Step 1 — compute $A^\top A$.**

$$A^\top = \begin{pmatrix}3&4\\0&5\end{pmatrix}, \qquad A^\top A = \begin{pmatrix}3&4\\0&5\end{pmatrix}\begin{pmatrix}3&0\\4&5\end{pmatrix} = \begin{pmatrix}9+16 & 0+20\\ 0+20 & 0+25\end{pmatrix} = \begin{pmatrix}25&20\\20&25\end{pmatrix}.$$

Note $A^\top A$ came out symmetric, exactly as promised — this holds for *any* matrix $A$, square or not, symmetric or not.

**Step 2 — eigenvalues of $A^\top A$.**

$$\det(A^\top A - \lambda I) = (25-\lambda)^2 - 400 = 0 \implies (25-\lambda)^2 = 400 \implies 25-\lambda = \pm 20.$$

So $\lambda = 45$ or $\lambda=5$. Both are non-negative, as guaranteed for $A^\top A$ (it's positive semi-definite: $\mathbf{x}^\top A^\top A\mathbf{x} = \|A\mathbf{x}\|^2 \geq 0$ for any $\mathbf{x}$, which forces every eigenvalue $\geq 0$).

**Step 3 — eigenvectors of $A^\top A$ (these become the right singular vectors $V$).**

For $\lambda=45$: $(25-45)v_1 + 20v_2 = 0 \implies -20v_1+20v_2=0 \implies v_1=v_2$. Normalized: $\mathbf{v}_1 = \frac{1}{\sqrt2}(1,1)$.

For $\lambda=5$: $(25-5)v_1+20v_2=0 \implies 20v_1+20v_2=0 \implies v_1=-v_2$. Normalized: $\mathbf{v}_2 = \frac{1}{\sqrt2}(1,-1)$.

**Step 4 — singular values.** $\sigma_i = \sqrt{\lambda_i}$, so $\sigma_1 = \sqrt{45} = 3\sqrt5 \approx 6.708$ and $\sigma_2=\sqrt5\approx2.236$.

**Step 5 — left singular vectors via $\mathbf{u}_i = \frac{1}{\sigma_i}A\mathbf{v}_i$.**

$$A\mathbf{v}_1 = \begin{pmatrix}3&0\\4&5\end{pmatrix}\frac{1}{\sqrt2}\begin{pmatrix}1\\1\end{pmatrix} = \frac{1}{\sqrt2}\begin{pmatrix}3\\9\end{pmatrix}.$$

$$\mathbf{u}_1 = \frac{1}{\sigma_1}A\mathbf{v}_1 = \frac{1}{3\sqrt5}\cdot\frac{1}{\sqrt2}\begin{pmatrix}3\\9\end{pmatrix} = \frac{1}{3\sqrt{10}}\begin{pmatrix}3\\9\end{pmatrix} = \begin{pmatrix}1/\sqrt{10}\\3/\sqrt{10}\end{pmatrix}.$$

$$A\mathbf{v}_2 = \begin{pmatrix}3&0\\4&5\end{pmatrix}\frac{1}{\sqrt2}\begin{pmatrix}1\\-1\end{pmatrix} = \frac{1}{\sqrt2}\begin{pmatrix}3\\-1\end{pmatrix}, \qquad \mathbf{u}_2 = \frac{1}{\sqrt5}\cdot\frac1{\sqrt2}\begin{pmatrix}3\\-1\end{pmatrix} = \begin{pmatrix}3/\sqrt{10}\\-1/\sqrt{10}\end{pmatrix}.$$

**Check $\mathbf{u}_1,\mathbf{u}_2$ are unit length and orthogonal:** $\|\mathbf{u}_1\|^2 = (1+9)/10=1$ ✓, $\|\mathbf{u}_2\|^2=(9+1)/10=1$ ✓, $\mathbf{u}_1\cdot\mathbf{u}_2 = (1\cdot3 + 3\cdot(-1))/10 = 0$ ✓. These didn't have to come out orthonormal by luck — the lesson's derivation guarantees it automatically whenever $\mathbf{v}_i$ are orthonormal eigenvectors of $A^\top A$.

**Step 6 — assemble the SVD.**

$$U = \begin{pmatrix}1/\sqrt{10} & 3/\sqrt{10}\\ 3/\sqrt{10} & -1/\sqrt{10}\end{pmatrix}, \quad \Sigma = \begin{pmatrix}3\sqrt5 & 0\\ 0 & \sqrt5\end{pmatrix}, \quad V^\top = \begin{pmatrix}1/\sqrt2 & 1/\sqrt2\\ 1/\sqrt2 & -1/\sqrt2\end{pmatrix}.$$

**Sanity check — reconstruct $A$.** $U\Sigma = \begin{pmatrix}3/\sqrt2 & 3/\sqrt2\\ 9/\sqrt2 & -1/\sqrt2\end{pmatrix}$ (using $\sigma_1/\sqrt{10}=3/\sqrt2$, etc.). Multiplying by $V^\top$: row 1 gives $\left(\frac{3}{\sqrt2}\cdot\frac1{\sqrt2}+\frac3{\sqrt2}\cdot\frac1{\sqrt2},\ \frac3{\sqrt2}\cdot\frac1{\sqrt2}-\frac3{\sqrt2}\cdot\frac1{\sqrt2}\right) = (3,0)$, row 2 gives $(4,5)$ — exactly $A$. The decomposition checks out.

**Geometric picture:** $V$'s columns are an orthonormal basis in the *input* space, $U$'s columns are an orthonormal basis in the *output* space, and $A$ stretches the unit circle into an ellipse whose semi-axes point along $\mathbf{u}_1,\mathbf{u}_2$ with lengths $\sigma_1,\sigma_2$. This is the exact mechanism behind low-rank approximation (Eckart–Young): keeping only the $\sigma_1,\mathbf{u}_1,\mathbf{v}_1$ term already captures most of what $A$ does, since $\sigma_1 \approx 3\times\sigma_2$.

$$\boxed{\sigma_1=3\sqrt5,\ \sigma_2=\sqrt5;\quad V=\tfrac1{\sqrt2}\begin{pmatrix}1&1\\1&-1\end{pmatrix};\quad U=\tfrac1{\sqrt{10}}\begin{pmatrix}1&3\\3&-1\end{pmatrix}}$$

---

## Takeaway

All three problems lean on the same core move: once you have eigenvectors (of $A$ itself, or of $A^\top A$ when $A$ isn't symmetric), the matrix's action collapses to simple per-axis scaling in that basis — that's what makes repeated application (Problem 2) and decomposition into rank-1 pieces (Problem 3) tractable. Problem 2's convergence-to-the-dominant-eigenvector behavior is worth remembering: it's the same mechanism behind power iteration, PageRank, and why the top eigenvalue of a loss Hessian sets your maximum stable learning rate. Next up in the curriculum: ordinary differential equations, where this exact eigenvalue machinery reappears to determine whether a rocket's attitude dynamics are stable or not.
