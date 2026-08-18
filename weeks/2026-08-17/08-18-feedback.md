# Feedback — Session 2 (2026-08-18)

Work graded: [`08-18-work.md`](08-18-work.md). Problems: [`08-18.md`](08-18.md).

## Headline

**Bug #1 (stopping at the setup) did not happen once.** Every problem you attempted
was carried through to a landing — that's new, and it's the thing this whole session
was designed to test. Don't undersell that.

Two new, more specific issues showed up instead, both mechanical and both fixable
fast:

1. **Setup sometimes assumes the conclusion.** In 1(a) and 1(b) you wrote "assume the
   sum is even" / "let there be odd integers $a,b,c$ such that $a\cdot b=c$" — that
   bakes the thing you're trying to prove into the setup. 1(c) didn't do this, and
   1(c) is also your cleanest proof of the four. Not a coincidence.
2. **"For some integer $k$" became "for some $k \in \mathbb{N}$," everywhere.** Every
   unfold today used $\mathbb{N}$ instead of $\mathbb{Z}$. Harmless for the specific
   claims you were proving (none needed a negative witness), but it's silently wrong
   as a general habit — try unfolding "$-3$ is odd" with $k \in \mathbb{N}$ and there's
   no such $k$.

Core 2 (injective/surjective) and the stretch problem are blank. Core 2 is now **two
sessions in a row** untouched (calibration A4, now here) — that's a real gap in the
evidence, not a scheduling accident, and it's the first thing in today's session.

---

## Item-by-item

### R1 — $n^2$ even $\implies$ $n$ even, by contrapositive

**Partially correct.** Contrapositive stated correctly. Unfold correct: $n=2k+1$,
$k \in \mathbb{N}$ (should be $\mathbb{Z}$ — see above). Expansion $n^2 = 4k^2+4k+1$ is
correct.

Then: *"We know that $k^2$ must be even and that $4k$ must also be even… therefore
$4k^2+4k+1$ is odd."*

**$k^2$ must be even is false in general** — take $k=1$: $k^2=1$, odd. The claim you
actually need is that $4k^2$ is even, which is true, but for a different reason: it's
$2\cdot(2k^2)$, an integer multiple of 2, regardless of whether $k$ itself is even or
odd. You reached for a fact about $k$ that isn't true instead of a fact about $4k^2$
that is. The conclusion survived because the false step happened to not matter here —
that won't always be true.

**Landing was also incomplete.** "$4k^2+4k+1$ is odd" is the claim, not yet the proof
of it — the definition of odd requires exhibiting the witness. Missing final line:
*"so $n^2 = 2m+1$ where $m = 2k^2+2k \in \mathbb{Z}$, hence $n^2$ is odd by
definition."* That sentence is what "Land" means — say why the result matches the
definition you're targeting, not just that it does.

**Diagnosis:** method correct, execution has one false intermediate claim (not an
arithmetic slip — a wrong justification for a true fact) and an under-specified
landing.

### R2 — definitions

Correct up to the $\mathbb{N} \to \mathbb{Z}$ issue, consistently applied to all three.
Fix this one thing and R2 is clean.

### Core 1(a) — sum of two evens is even

**Setup assumes the conclusion.** "We assume that there exists two integers $a,b$
such that the sum $a+b$ is even" — this should only assume $a,b$ are even; whether
$a+b$ is even is what you're proving, not what you're given. Everything downstream
inherited this: "Unfold" then unfolds $c$ (the sum) as $2z$, which only makes sense if
you'd already assumed it was even.

The arithmetic that follows is fine — $2x+2y=2z \Rightarrow x+y=z$ — but it's proving
the wrong thing: given that $a+b$ is even, $x+y=z$. That's not the claim.

**What the setup should say:** assume $a,b$ are even, i.e. $a=2x, b=2y$ for
$x,y\in\mathbb{Z}$. **Work:** $a+b=2x+2y=2(x+y)$. **Land:** since $x+y\in\mathbb{Z}$,
this has the form $2m$ with $m=x+y$, so $a+b$ is even by definition. No assumption
about $a+b$'s parity anywhere until the last line, where it's concluded, not assumed.

**Diagnosis:** wrong method (circular — assumes what's to be shown), not an arithmetic
error. The computation itself is correct; it answers a different question than the one
asked.

### Core 1(b) — product of two odds is odd

Same setup issue as 1(a): "$a,b,c\in\mathbb{N}$ such that $a\cdot b=c$" with $c$
already declared odd. Fix is the same shape as 1(a)'s.

**Also an algebra error, independent of the setup issue:**
$(2x+1)(2y+1) = 4xy+2x+2y+1$. You wrote $4xy^2+2x+2y+1$ — an extra, unjustified power
of $y$. Didn't change your conclusion (any $4xy^k$ term is even for the same reason as
R1's $4k^2$), but it's worth re-doing this expansion by hand, term by term, rather than
from memory: $(2x+1)(2y+1) = 2x\cdot 2y + 2x\cdot 1 + 1\cdot 2y + 1\cdot 1$.

**Diagnosis:** two independent issues — circular setup (method) and a FOIL slip
(arithmetic). Different fixes; don't let the setup conversation distract from also
just re-doing the algebra carefully.

### Core 1(c) — $a\mid b \wedge b\mid c \implies a\mid c$

**Correct, and the best-executed proof in the file.** Setup states only the two
hypotheses — no circularity. Unfold correctly uses two different letters ($m$, $n$)
for the two divisibility witnesses, which is exactly the trap the problem was
checking for. Work substitutes cleanly. Land names the witness ($k=mn$) explicitly
and states the conclusion in definitional form. This is the template — 1(a) and 1(b)
should read like this.

### Core 2 — injective / surjective

**Not attempted, second time.** No penalty beyond what's already true: this is now
the first item in today's session, and it isn't optional this time.

### Stretch — $3\mid n^2 \implies 3 \mid n$

Not attempted — it was marked optional, so that's fine on its own. But today's session
needs this exact lemma, so it's being asked again, non-optionally, as a step toward a
bigger result.

---

## What this changes

- **Bug #1 is not closed, but it's genuinely better.** The failure mode moved from
  "doesn't finish" to "finishes with a weak landing" — real progress, worth one more
  clean instance before calling it closed.
- **New item: setup discipline** — state the hypothesis, never the conclusion, in
  Setup. Tracked in `REVIEW-QUEUE.md` and `STATE.md`.
- **New item: existential witnesses live in $\mathbb{Z}$, not $\mathbb{N}$.** Small,
  mechanical, easy to drill out. Tracked.
- **Core 2 moves to the top of today's Core**, not because of punishment, but because
  two sessions of "no data" on injective/surjective is a real hole and the plan can't
  see around it.

Difficulty: **hold.** Today's session stays in repair mode — same unfolding/contrapositive
family, plus contradiction (today's new technique per the rolling horizon), not a level up.
