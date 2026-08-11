Problem: [08-11.md](08-11.md)

# Solution — Directional Derivatives and Steepest Ascent

**What's being asked, and why this approach:** We have a scalar function of two variables, $f(x,y) = x^2y - 3xy^2 + 2y^3$. Part (a) is a warm-up gradient computation like yesterday. Parts (b) and (c) push further: the gradient isn't just a pair of partial derivatives — it's a vector that encodes *how fast $f$ changes in every possible direction* from a point, all at once. The tool for extracting "rate of change in direction $\mathbf{u}$" from the gradient is the **directional derivative**, defined as

$$D_{\mathbf{u}}f(x,y) = \nabla f(x,y) \cdot \mathbf{u}, \qquad \|\mathbf{u}\| = 1.$$

This formula itself comes from the multivariable chain rule: if you walk along the line $\mathbf{r}(t) = (x,y) + t\mathbf{u}$, then $\frac{d}{dt}f(\mathbf{r}(t))\big|_{t=0} = \nabla f \cdot \mathbf{r}'(0) = \nabla f \cdot \mathbf{u}$. So the directional derivative is just "ordinary derivative along a straight-line path," and the dot product with the gradient is what the chain rule collapses it to.

## Step 1 — Compute the gradient at (2,1)

$$\frac{\partial f}{\partial x} = 2xy - 3y^2, \qquad \frac{\partial f}{\partial y} = x^2 - 6xy + 6y^2$$

*Why these terms:* differentiate term-by-term treating the other variable as a constant. For $\partial f/\partial x$: $x^2y \to 2xy$, $-3xy^2 \to -3y^2$, $2y^3 \to 0$ (no $x$). For $\partial f/\partial y$: $x^2y \to x^2$, $-3xy^2 \to -6xy$, $2y^3 \to 6y^2$.

Evaluate at $(2,1)$:

$$f_x(2,1) = 2(2)(1) - 3(1)^2 = 4 - 3 = 1$$
$$f_y(2,1) = (2)^2 - 6(2)(1) + 6(1)^2 = 4 - 12 + 6 = -2$$

$$\boxed{\nabla f(2,1) = (1, -2)}$$

**Sanity check:** the sign of each component tells you the "local slope" along that axis. $f_x = 1 > 0$ means moving in $+x$ (holding $y=1$ fixed) increases $f$; $f_y = -2 < 0$ means moving in $+y$ decreases $f$. That's consistent with what a directional query should reflect below.

## Step 2 — Directional derivative along v = (3,4)

The gradient dotted with an *arbitrary* vector doesn't give a directional derivative unless that vector has length 1 — otherwise you're also scaling by how fast you're "walking," not just which way. So first normalize:

$$\|\mathbf{v}\| = \sqrt{3^2+4^2} = \sqrt{25} = 5 \quad\Rightarrow\quad \mathbf{u} = \left(\tfrac{3}{5}, \tfrac{4}{5}\right)$$

(This is the classic 3-4-5 right triangle, so the arithmetic stays clean on purpose.)

Now apply the formula:

$$D_{\mathbf{u}}f(2,1) = \nabla f(2,1)\cdot \mathbf{u} = (1)\left(\tfrac{3}{5}\right) + (-2)\left(\tfrac{4}{5}\right) = \tfrac{3}{5} - \tfrac{8}{5} = -\tfrac{5}{5}$$

$$\boxed{D_{\mathbf{u}}f(2,1) = -1}$$

**Interpretation:** if you stand at $(2,1)$ and take a small step in the direction $(3/5, 4/5)$, $f$ decreases at rate $1$ per unit distance moved — even though moving in pure $+x$ would have increased $f$. The $y$-component of that direction (which decreases $f$ strongly, since $f_y=-2$) dominates.

## Step 3 — Steepest ascent and descent

This is the deepest fact about the gradient, and it's worth actually seeing *why* it's true rather than just quoting it. We want to know which unit vector $\mathbf{u}$ maximizes $D_{\mathbf{u}}f = \nabla f \cdot \mathbf{u}$. Using the dot-product-as-cosine identity,

$$\nabla f \cdot \mathbf{u} = \|\nabla f\| \, \|\mathbf{u}\| \cos\theta = \|\nabla f\| \cos\theta$$

where $\theta$ is the angle between $\nabla f$ and $\mathbf{u}$ (and $\|\mathbf{u}\|=1$). This is maximized when $\cos\theta = 1$, i.e. $\theta = 0$ — meaning $\mathbf{u}$ points in *exactly the same direction as* $\nabla f$. So:

- **Steepest ascent direction:** $\mathbf{u} = \nabla f / \|\nabla f\|$
- **Steepest descent direction:** $\mathbf{u} = -\nabla f/\|\nabla f\|$ (minimizes $\cos\theta$ at $-1$)

Compute the magnitude:

$$\|\nabla f(2,1)\| = \sqrt{1^2 + (-2)^2} = \sqrt{5}$$

So:

$$\boxed{\text{Steepest ascent: } \mathbf{u} = \left(\tfrac{1}{\sqrt5}, \tfrac{-2}{\sqrt5}\right), \text{ rate } = \sqrt5}$$
$$\boxed{\text{Steepest descent: } \mathbf{u} = \left(\tfrac{-1}{\sqrt5}, \tfrac{2}{\sqrt5}\right), \text{ rate of decrease } = \sqrt5}$$

**Sanity check:** compare to Step 2. The direction $(3/5,4/5)$ we tested is *not* aligned with $\nabla f = (1,-2)$ (in fact it's more aligned with $-\nabla f$, since $f_y$ dominates and both have negative-ish alignment), which is exactly why it gave a negative directional derivative of $-1$ rather than the true max descent rate of $-\sqrt5 \approx -2.236$. The steepest-descent rate is always the largest-magnitude decrease available at that point — no other direction can beat it.

## Why this matters for ML (and what's coming)

This "steepest descent" result is *the* mathematical justification for gradient descent. When you train a neural network and update weights via $\theta \leftarrow \theta - \eta \nabla L(\theta)$, you're moving in exactly the direction we just derived: the direction that decreases the loss $L$ fastest, locally, per unit step. Everything about why gradient descent "points the right way" traces back to the $\cos\theta$ argument above — nothing more mysterious than that.

**Key takeaway:** the gradient's direction and magnitude jointly answer "which way is uphill, and how steep," and directional derivatives let you query the slope in *any* direction by a single dot product — no new differentiation needed once you have $\nabla f$.

**Next up:** we'll look at the *second-order* picture — how curvature (via the Hessian) tells you whether a critical point (where $\nabla f = 0$) is a min, max, or saddle, which is the multivariable generalization of the second derivative test and shows up constantly in loss-landscape analysis.
