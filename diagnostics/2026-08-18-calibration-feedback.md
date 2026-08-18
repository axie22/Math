# Calibration Feedback — 2026-08-18

## Verdict

| Section | Score | Read |
|---|---|---|
| A — Proof | **~20%** | Confirms the hypothesis. Three distinct, *named* bugs — not vague weakness |
| B — Linear algebra | **~5%** | Worse than the transcript predicted. Phase 1 stays at 8 weeks, from the axioms |
| C — Calculus | **no data** | Entirely blank. Cannot be scored — see "open questions" |
| D — Days 1–6 retention | **not scoreable as retention** | You only did 3 of the 6 days. What you *did* do, you kept |

**This is a good diagnostic, not a bad one.** You answered honestly, left things blank instead of bluffing, and flagged the Section D caveat unprompted. That's exactly what makes the result usable — a padded diagnostic would have bought you a curriculum calibrated to someone else and you'd have hit the wall in November instead of today.

And the picture is more specific than "weak." Section A failed in three *particular*, *mechanical* ways. Mechanical problems have mechanical fixes.

---

## Section A — Proof

### A1 — n² even ⟹ n even · **setup correct, proof absent**

You wrote:

> Proof by contradiction. […] there must be some $n$ such that $n^2 \bmod 2 = 0$ but $n \bmod 2 = 1$.

**That negation is correct**, and it is the step most people get wrong. Negating "P ⟹ Q" to "P and not-Q" is genuinely non-obvious and you did it cleanly. Note this — it contradicts the A3 result and it matters.

Then you stopped. Everything after the setup is missing, and the setup is maybe 20% of a proof.

**The missing move:** once you've assumed *n* is odd, *write down what odd means*. $n = 2k+1$ for some integer $k$. Then just compute:

$$n^2 = (2k+1)^2 = 4k^2 + 4k + 1 = 2(2k^2+2k) + 1$$

which is odd, contradicting $n^2$ even. Done.

That move — **replace the word with its definition and compute** — is the workhorse of about 60% of all elementary proofs. When stuck, that is almost always the next step.

*Style note:* contradiction works here but it's a heavier tool than needed. The contrapositive ("*n* odd ⟹ *n²* odd") proves the same thing with no contradiction machinery. Worth learning to see when the lighter tool suffices.

---

### A2 — Induction · **the structure of induction is missing**

This is the most important single finding in the diagnostic, so I want to be precise about it.

**Bug 1 — you're reading the formula as the *n*-th term, not the sum of the first *n* terms.**

Two pieces of evidence. First, your base cases:

> $k = 2 \rightarrow \frac{2(2+1)(2(2)+1)}{6} = 4$

That expression equals **5**, not 4. And $1^2 + 2^2 = 5$. You wrote 4 because you were computing $2^2$ — the *term*. Second, your inductive step:

> $k = n+1 \rightarrow (n+1)^2 = \frac{(n+1)(n+2)(2n+3)}{6}$

You set the $(n{+}1)$-th **term** equal to the formula at $n{+}1$. The claim is that the formula equals the **running total** $1^2 + 2^2 + \cdots + n^2$.

**Bug 2 — you never used the induction hypothesis.** This is the deeper problem. Induction has exactly one mechanism: *assume the statement at n, use that assumption to get the statement at n+1.* Your inductive step never references the $n$ case at all — it tries to verify $n{+}1$ from scratch. Without the hypothesis, there is no induction; there's just an algebra check that happens to be false.

**What it should look like:**

Assume $\displaystyle\sum_{k=1}^{n} k^2 = \frac{n(n+1)(2n+1)}{6}$ *(this line is the whole point — it's the hypothesis, and you must write it down)*.

Then
$$\sum_{k=1}^{n+1} k^2 = \underbrace{\sum_{k=1}^{n} k^2}_{\text{use the hypothesis}} + (n+1)^2 = \frac{n(n+1)(2n+1)}{6} + (n+1)^2$$

Factor out $(n+1)$:
$$= (n+1)\left[\frac{n(2n+1)}{6} + (n+1)\right] = (n+1)\cdot\frac{2n^2+n+6n+6}{6} = \frac{(n+1)(2n^2+7n+6)}{6} = \frac{(n+1)(n+2)(2n+3)}{6}$$

which is the formula at $n{+}1$. ∎

**Bug 3 — two arithmetic slips**, much less important than the above but worth naming:

- $n+1 = \frac{2n^2+7n+6}{6}$ → you wrote $n = \frac{2n^2+7n+12}{6}$. Subtracting 1 from the left means subtracting 6 from the numerator, not adding it.
- Then $6n = 2n^2+7n+12$ gives $2n^2+n+12=0$, not $2n^2+13n+12=0$.

**One thing worth seeing:** if you'd done that algebra correctly, your own equation would have collapsed to $2n^2 + n = 0$, i.e. $n(2n+1)=0$, i.e. $n \in \{0, -\tfrac12\}$. Your setup was self-refuting — the algebra was *telling you* the premise was wrong. Learning to hear that signal ("my equation has no sensible solutions, so my setup is wrong") is a real skill and it's worth more than the arithmetic.

---

### A3 — Quantifier negation · **one consistent, highly fixable bug**

Correct answer:

> **There exists** $\varepsilon > 0$ such that **for all** $N \in \mathbb{N}$, **there exists** $n > N$ with $|a_n - L| \ge \varepsilon$.

Yours:

> For every $\epsilon < 0$ there does not exist $N \notin \mathbb{N}$ such that for all $n < N$, $\epsilon < |a_n - L|$

Compare them term by term and the same mistake appears four times:

| | You negated | You should have negated |
|---|---|---|
| $\forall \varepsilon > 0$ | the constraint → $\varepsilon < 0$ | the quantifier → $\exists \varepsilon > 0$ |
| $\exists N \in \mathbb{N}$ | the membership → $N \notin \mathbb{N}$ | the quantifier → $\forall N \in \mathbb{N}$ |
| $\forall n > N$ | the constraint → $n < N$ | the quantifier → $\exists n > N$ |
| $\|a_n - L\| < \varepsilon$ | ✓ flipped it | ✓ (to $\ge$) |

**The rule:** negation walks left to right, flipping **∀ ↔ ∃** and leaving the domain restrictions ($\varepsilon > 0$, $N \in \mathbb{N}$, $n > N$) completely untouched. Only the innermost predicate — the actual inequality at the end — gets negated. You got that last part right; you just also negated everything that shouldn't have been.

This is the **highest-ROI item in the whole diagnostic.** It is one rule, applied mechanically, and it is the gateway to every ε-argument in analysis, every convergence proof, every generalization bound. Two or three sessions of pure drilling should close it permanently.

**Small note:** in (a) you read $L$ as "the loss." It's a **limit**. Understandable given the ML framing, but the distinction matters — this statement is the definition of $a_n \to L$.

---

### A4 — Injective not surjective · blank

No data. Covered in Phase 0.

---

## Section B — Linear algebra

> - linear independence: rows are independent of one another
> - rank: the number of non-empty values in the matrix

**Rank is the dimension of the column space** (equivalently the row space) — the number of genuinely independent directions the matrix maps onto. "Number of non-empty values" counts nonzero entries, which is an unrelated quantity. $\begin{pmatrix}1&1\\1&1\end{pmatrix}$ has four nonzero entries and rank 1.

The linear-independence answer is circular — it uses "independent" to define independence. The real definition: $\{v_1,\dots,v_k\}$ is linearly independent if $\sum c_i v_i = 0$ forces every $c_i = 0$.

Basis, null space, rank–nullity, B3, B4: blank.

**This is the finding that most changes the plan.** You have a B+ in MATH-UA 140 from Spring 2024 and today cannot state what rank is. That's not a memory lapse — those definitions are the first three weeks of the course. It means the B+ was earned on procedures (row-reduce this, invert that) without the conceptual layer underneath, which is exactly the failure mode Phase 1 was designed for.

**Phase 1 stays at 8 weeks and starts from the vector-space axioms.** Do not let anyone, including me, talk you into compressing it. Everything downstream in this curriculum leans on it.

---

## Section C — Calculus · no data

All three blank. I can't score this, and I won't guess — see open questions below.

---

## Section D — retention

Your caveat is correct and I'm honoring it. You did Days 1, 2, and 6; you skipped 3, 4, and 5 (08-12, 08-13, 08-16). So:

- **D1 (partial derivatives — Day 1 material): genuinely good.** $\partial f/\partial x = 2xy - 3y^2$ ✓ and $\partial f/\partial y = x^2 - 6xy$ ✓, both correct and cleanly done. That's real retention from eight days ago.
  - Arithmetic slip on evaluation: $\nabla f(1,1) = (2 - 3,\ 1 - 6) = (-1, -5)$. You wrote $(-7, -5)$ — the second component is right.
  - You didn't compute the Hessian, which the question asked for: $H = \begin{pmatrix} 2y & 2x-6y \\ 2x-6y & -6x\end{pmatrix}$, so $H(1,1) = \begin{pmatrix}2 & -4 \\ -4 & -6\end{pmatrix}$.
  - **The trap you didn't spring:** the question said "classify the critical-point behavior *if you can, and say why or why not*." You can't — $(1,1)$ **isn't a critical point**, since $\nabla f(1,1) = (-1,-5) \neq 0$. The second-derivative test simply doesn't apply. Saying so was the correct answer.
  - Notation: you wrote $f\Delta$ for the gradient. It's $\nabla f$ (nabla, not delta), and $f(x^2, y)$ in your first line should be $f(x,y)$.
- **D2(a) gradient:** "like slope but in 3 dimensions" — the intuition is pointed the right way but it's imprecise, and the three facts that make the gradient *useful* are absent: it's a vector of partials, it points in the direction of steepest ascent, and it's perpendicular to level curves.
- **D2(b), D2(c), D3, D4:** all cover Days 4–6 material you didn't do. Correctly recorded as *not attempted*, not as *forgotten*.

**Net:** Section D is not evidence of poor retention. It's evidence that Day 1 stuck and that you completed half the sessions. Those are two different findings and only the second is a problem.

---

## The three named bugs

Everything in Section A reduces to these. Phase 0 now targets them explicitly:

1. **You stop at the setup.** You can frame a proof — pick the technique, state the assumption, negate the implication — and then don't execute. The missing habit is *unfold the definition and compute*.
2. **Induction has no engine.** You verify at $n{+}1$ instead of building from $n$. The induction hypothesis is never written down, so there's nothing doing the work.
3. **Negation flips the wrong things.** Domain restrictions get negated; quantifiers don't. Exactly backwards, and consistently so.

Consistent bugs are the good kind. Scattered confusion takes months; three named rules take weeks.

---

## What changes in the plan

Proposed (see `CURRICULUM.md` §7 — **not yet applied**, your call at review):

- **Phase 0: 3 weeks → 5 weeks.** Three separate gaps, each needing real time. Three weeks was priced for polish, not for construction.
- **Add a dedicated 3-session induction block.** Bug 2 is structural, not a detail.
- **Add a 2-session quantifier-negation drill** — pure mechanical repetition, ~20 statements negated. Highest ROI item here.
- **Session 2 (tomorrow) starts with A1 redone**, then A4. Re-attempting a failed problem with the mechanism explained is worth more than a fresh one.
- **Phase 1 unchanged at 8 weeks**, and explicitly confirmed to start from the axioms.

Total to research depth moves from ~34 weeks to ~36.

---

## Open questions

Two things I can't determine from the file, and both change the plan:

1. **Section C — out of time, or couldn't do it?** These matter differently. C1 is Calc I chain rule; if that's genuinely gone, calculus repair needs its own sessions rather than being interleaved. If you just ran out of clock, it's a non-finding. You left the timing fields blank so I can't infer it. **Please just redo Section C, timed, and commit it** — 10 minutes, and it's the last hole in the picture.

2. **You completed 3 of 6 sessions.** The whole plan is priced at 5/week; at 3/week the ~36 weeks becomes ~60. If the misses were circumstantial, fine, ignore this. If 3/week is the honest steady state, I'd rather re-price the plan around it than have it silently slip — a plan you actually hit beats a plan that looks better on paper.

---

*Graded 2026-08-17. Evidence recorded in `STATE.md`.*
