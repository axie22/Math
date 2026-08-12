Problems: [08-12.md](08-12.md)

# Day 3 Solutions — Hessian & Second Derivative Test

## Problem 1 (Warm-up): Directional derivative of $g(x,y) = x^2+2xy-y^2$

**What's being asked:** find the gradient at a point, then use it to get the directional derivative in a specific direction. This is exactly yesterday's tool ($D_{\mathbf u}f = \nabla f \cdot \mathbf u$) applied to a new function — the goal is to make computing gradients and dotting with a normalized direction feel automatic before we lean on it inside today's harder problems.

**Step 1 — compute the gradient.**

$$\frac{\partial g}{\partial x} = 2x + 2y, \qquad \frac{\partial g}{\partial y} = 2x - 2y$$

(For $\partial g/\partial x$: differentiate term by term treating $y$ as constant — $x^2 \to 2x$, $2xy \to 2y$, $-y^2 \to 0$. Symmetric logic for $\partial g/\partial y$.)

At $(2,-1)$:

$$\nabla g(2,-1) = (2(2)+2(-1),\ 2(2)-2(-1)) = (4-2,\ 4+2) = (2, 6)$$

**Step 2 — normalize the direction.** $\mathbf v = (1,-1)$ has $\|\mathbf v\| = \sqrt{1^2+(-1)^2} = \sqrt2$, so $\mathbf u = \frac{1}{\sqrt2}(1,-1)$. This step is not optional: the directional derivative formula is defined for *unit* vectors, since it's meant to answer "rate of change per unit distance traveled." Skipping normalization would silently scale your answer by $\|\mathbf v\|=\sqrt2$.

**Step 3 — dot product.**

$$D_{\mathbf u}g(2,-1) = \nabla g(2,-1)\cdot \mathbf u = (2,6)\cdot\frac{1}{\sqrt2}(1,-1) = \frac{2(1)+6(-1)}{\sqrt2} = \frac{2-6}{\sqrt2} = \frac{-4}{\sqrt2} = -2\sqrt2$$

**Sanity check / intuition:** the answer is negative, meaning $g$ is *decreasing* as you move in direction $(1,-1)$ from $(2,-1)$. That's plausible: $\nabla g = (2,6)$ points mostly in the $+y$ direction, while $\mathbf v=(1,-1)$ moves in the $-y$ direction — the two vectors are more than 90° apart (their dot product is negative), so moving along $\mathbf v$ works against the gradient.

$$\boxed{\nabla g(2,-1) = (2,6), \quad D_{\mathbf u}g(2,-1) = -2\sqrt2 \approx -2.83}$$

---

## Problem 2 (Core): Critical points of $f(x,y) = x^3 - 3xy + y^3$

**What's being asked:** find every critical point (where $\nabla f = \mathbf 0$), then use the Hessian and the second derivative test from today's lesson (Section 3) to classify each one. This is the central skill of the day: turning "the gradient vanishes" into a full geometric picture of the surface at that point.

### Part (a): finding critical points

$$\frac{\partial f}{\partial x} = 3x^2 - 3y, \qquad \frac{\partial f}{\partial y} = -3x + 3y^2$$

Set both to zero:

$$3x^2 - 3y = 0 \implies y = x^2 \tag{i}$$
$$-3x + 3y^2 = 0 \implies x = y^2 \tag{ii}$$

**Why substitute rather than solve simultaneously by inspection:** with two nonlinear equations, the cleanest path is to express one variable in terms of the other from (i), then substitute into (ii) to collapse to a single-variable equation. From (i), $y = x^2$. Substitute into (ii):

$$x = (x^2)^2 = x^4 \implies x^4 - x = 0 \implies x(x^3-1) = 0$$

So $x = 0$ or $x^3 = 1 \Rightarrow x = 1$ (the only real cube root of 1).

- $x=0 \Rightarrow y = 0^2 = 0$. Critical point: $(0,0)$.
- $x=1 \Rightarrow y = 1^2 = 1$. Critical point: $(1,1)$.

**Check both satisfy (ii):** $x=0$: $0 = 0^2=0$ ✓. $x=1$: $1 = 1^2=1$ ✓. Good — two critical points, $(0,0)$ and $(1,1)$.

### Part (b): classify with the Hessian

Second partials:

$$f_{xx} = 6x, \qquad f_{yy} = 6y, \qquad f_{xy} = f_{yx} = -3$$

(the mixed partial $-3$ comes from differentiating $-3xy$ once with respect to each variable — it's a constant regardless of $(x,y)$, since the term is bilinear in $x,y$.)

$$H(x,y) = \begin{pmatrix} 6x & -3 \\ -3 & 6y\end{pmatrix}, \qquad D(x,y) = \det H = 36xy - 9$$

**At $(0,0)$:**

$$D = 36(0)(0) - 9 = -9 < 0$$

$D<0$ means the two principal curvatures have opposite signs — the surface rises in one direction and falls in another right at this point. By the second derivative test, **$(0,0)$ is a saddle point.** (We don't even need $f_{xx}$ here — a negative $D$ settles it as a saddle regardless of the sign of $f_{xx}$.)

**At $(1,1)$:**

$$D = 36(1)(1) - 9 = 36 - 9 = 27 > 0, \qquad f_{xx} = 6(1) = 6 > 0$$

$D>0$ tells us both principal curvatures share a sign, so this is a genuine min or max — not a mixed saddle. $f_{xx}>0$ then tells us which: the surface curves *upward* along its principal axes, so **$(1,1)$ is a local minimum.**

**Intuition / sanity check:** near $(0,0)$, walk along $y=0$: $f(x,0) = x^3$, which has an inflection (not an extremum) at $x=0$ in 1D — consistent with $(0,0)$ not being a clean min/max in 2D either. Near $(1,1)$, the function value is $f(1,1) = 1 - 3 + 1 = -1$; nearby points like $(1.1,1) $ give $f = 1.331 - 3.3 + 1 = -0.969$ (larger, i.e. above $-1$) and $(0.9,1)$ gives $f= 0.729-2.7+1=-0.971$ (also larger) — both nearby samples sit above $-1$, consistent with a local min.

$$\boxed{(0,0): \text{saddle point} \qquad (1,1): \text{local minimum}, \ f(1,1)=-1}$$

---

## Problem 3 (Stretch): Critical points of the "double-well" loss $L(w_1,w_2) = w_1^4 - 4w_1^2 + w_2^2$

**What's being asked:** the same critical-point-then-Hessian workflow as Problem 2, but now $L$ has a *quartic* term, which produces three critical points instead of one or two — closer to what a real (if tiny) loss landscape can look like, with multiple minima separated by a saddle. Part (c) asks you to connect the math to why this matters for training neural networks.

### Part (a): finding critical points

$$\frac{\partial L}{\partial w_1} = 4w_1^3 - 8w_1 = 4w_1(w_1^2-2), \qquad \frac{\partial L}{\partial w_2} = 2w_2$$

Setting $\partial L/\partial w_2 = 0$ immediately forces $w_2 = 0$ — the $w_2$-dependence of $L$ is a simple upward parabola, so it only ever has one critical value in that coordinate, independent of $w_1$.

Setting $\partial L/\partial w_1 = 0$: $4w_1(w_1^2-2) = 0 \Rightarrow w_1 = 0$ or $w_1^2 = 2 \Rightarrow w_1 = \pm\sqrt2$.

So there are **three critical points**: $(0,0)$, $(\sqrt2, 0)$, $(-\sqrt2, 0)$.

### Part (b): classify with the Hessian

$$L_{w_1w_1} = 12w_1^2 - 8, \qquad L_{w_2w_2} = 2, \qquad L_{w_1w_2}=0$$

The Hessian is diagonal here (no cross term), which happens because $L$ separates into a function of $w_1$ alone plus a function of $w_2$ alone — there's no term mixing the two variables, so $\partial^2L/\partial w_1\partial w_2 = 0$ everywhere, simplifying $D$ to just $D = L_{w_1w_1}\cdot L_{w_2w_2}$.

**At $(0,0)$:** $L_{w_1w_1} = 12(0)-8 = -8$, $L_{w_2w_2}=2$.

$$D = (-8)(2) - 0^2 = -16 < 0 \implies \text{saddle point}$$

**At $(\pm\sqrt2, 0)$:** $L_{w_1w_1} = 12(2) - 8 = 24-8=16$, $L_{w_2w_2}=2$.

$$D = (16)(2) - 0^2 = 32 > 0, \quad L_{w_1w_1}=16>0 \implies \text{local minimum at both points}$$

**Function values:** $L(0,0) = 0$. $L(\pm\sqrt2, 0) = (\sqrt2)^4 - 4(\sqrt2)^2 + 0 = 4 - 8 = -4$. Both minima sit at the same lower value $-4$, with a saddle at $0$ sitting above them at height $0$ — a textbook symmetric double well.

$$\boxed{(0,0):\text{saddle}\ (L{=}0) \qquad (\pm\sqrt2,0):\text{local minima}\ (L{=}-4\ \text{each})}$$

### Part (c): why saddle points are troublesome for gradient descent

Near a true local maximum, *every* direction is downhill, so gradient descent (which always moves in the $-\nabla f$ direction) escapes almost immediately — the gradient's magnitude stays healthy in all directions pointing away from the max. Near a saddle, though, the gradient vanishes and the surface is nearly *flat along the directions that are actually descending* (here, the $w_2$-direction near $(0,0)$ has curvature $2$, mild compared to the $-8$ curvature along $w_1$, but in higher dimensions saddles routinely have many near-zero eigenvalue directions). Gradient descent can crawl along these nearly-flat directions for a very long time before the (small) downhill signal accumulates into real progress — this is exactly why saddle points, not local minima, are considered the main obstacle to fast convergence in high-dimensional non-convex optimization like neural network training.

---

## Takeaway

All three problems used the same two-step recipe — solve $\nabla f = \mathbf 0$, then read off the type of critical point from $D=\det H$ and $f_{xx}$ — but the payoff scales with dimension: even this toy 2-variable loss already shows the saddle-flanked-by-minima structure that makes real, million-parameter loss landscapes hard to optimize. Next time multivariable calculus comes back around, we'll push further into this topic (e.g. multiple integrals or constrained critical points) before moving on to linear algebra II (eigenvalues/SVD) — which will give you an even sharper lens on the Hessian, since its eigenvalues are precisely what "$D>0$ vs. $D<0$" was standing in for today.
