# Solution — Day 1: Partial Derivatives and the Gradient

Problem: [08-10.md](08-10.md)

## What's being asked, and why this approach

We have a function of two variables, $f(x, y) = 3x^2y - 2xy^3 + 5$, and we want its **partial derivatives** and its **gradient** at a point.

A partial derivative $\frac{\partial f}{\partial x}$ asks: "if I nudge $x$ a tiny bit while holding $y$ perfectly still, how fast does $f$ change?" Because $y$ is frozen during that question, every term that only involves $y$ (or is a plain constant) contributes **zero** to $\frac{\partial f}{\partial x}$ — it behaves exactly like a constant would in ordinary single-variable calculus. This is the whole trick to partial differentiation: you already know how to differentiate; you just temporarily pretend all the other variables are numbers.

The **gradient**, $\nabla f = \left(\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}\right)$, packages both partial derivatives into a vector. Geometrically, this vector points in the direction where $f$ increases fastest, and its magnitude tells you how fast. This is precisely the object that gradient descent uses in ML — every time a neural network "learns," it's computing something structurally identical to what we're about to do, just in thousands of dimensions instead of two.

## Step 1 — Partial derivative with respect to $x$

Treat $y$ as a constant and differentiate term by term:

- $3x^2y$: here $3y$ is just a constant coefficient multiplying $x^2$. Using the power rule ($\frac{d}{dx} x^n = nx^{n-1}$), $\frac{\partial}{\partial x}(3x^2y) = 3y \cdot 2x = 6xy$.
- $-2xy^3$: here $-2y^3$ is the constant coefficient multiplying $x^1$. Its derivative with respect to $x$ is just the coefficient itself: $\frac{\partial}{\partial x}(-2xy^3) = -2y^3$.
- $5$: a pure constant (no $x$ or $y$ dependence at all), so it vanishes entirely — its derivative is $0$.

Adding these up:

$$\frac{\partial f}{\partial x} = 6xy - 2y^3$$

**Sanity check:** every remaining term still contains $x$ or $y$ or both, which makes sense — differentiating shouldn't reintroduce more variables than the terms already had.

## Step 2 — Partial derivative with respect to $y$

Now flip roles: treat $x$ as a constant and differentiate term by term with respect to $y$:

- $3x^2y$: here $3x^2$ is the constant coefficient multiplying $y^1$, so $\frac{\partial}{\partial y}(3x^2y) = 3x^2$.
- $-2xy^3$: here $-2x$ is the constant coefficient multiplying $y^3$. Power rule gives $\frac{\partial}{\partial y}(-2xy^3) = -2x \cdot 3y^2 = -6xy^2$.
- $5$: constant again, derivative $0$.

Adding these up:

$$\frac{\partial f}{\partial y} = 3x^2 - 6xy^2$$

Notice the nice symmetry: differentiating with respect to $x$ knocked the power of $x$ down by one and left $y$'s power untouched (aside from removing terms with no $x$); differentiating with respect to $y$ did the mirror-image thing. That symmetry is a good way to catch algebra mistakes — if your two partials don't have this kind of "each term loses exactly one power of its own variable" structure, go back and recheck.

## Step 3 — Evaluate the gradient at $(1, 2)$

Now plug $x = 1, y = 2$ into each partial derivative separately. Do this carefully and in order (exponents before multiplication, multiplication before subtraction):

$$\frac{\partial f}{\partial x}(1,2) = 6(1)(2) - 2(2)^3 = 12 - 2(8) = 12 - 16 = -4$$

$$\frac{\partial f}{\partial y}(1,2) = 3(1)^2 - 6(1)(2)^2 = 3(1) - 6(1)(4) = 3 - 24 = -21$$

## Final answer

$$\boxed{\nabla f(1,2) = (-4,\ -21)}$$

## What this means, and why it matters

At the point $(1,2)$, $f$ is decreasing in both the $x$ and $y$ directions — both components are negative, so moving in the positive $x$ or positive $y$ direction makes $f$ smaller. The vector $(-4, -21)$ points in the direction of **steepest ascent**; its negative, $(4, 21)$, points in the direction of **steepest descent**. The much larger magnitude in the $y$-component ($-21$ vs. $-4$) tells you $f$ is far more sensitive to changes in $y$ than in $x$ at this point — a small step in $y$ moves $f$ about 5x more than the same size step in $x$.

This is exactly the quantity gradient descent computes at every iteration: given a loss function (instead of our toy $f$) and current parameter values (instead of $(1,2)$), it computes the gradient and steps in the *negative* gradient direction to reduce the loss. You've just done, by hand, the core arithmetic operation that trains every neural network you've worked with in your ML coursework.

**Coming up:** we'll build on this with the chain rule for multivariable functions (needed for backprop) and then move to computing gradients of functions with more variables and eventually vector-valued functions (Jacobians).
