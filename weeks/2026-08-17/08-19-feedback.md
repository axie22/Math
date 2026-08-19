# Feedback — Session 3 (2026-08-19)

Work graded: [`08-19-work.md`](08-19-work.md). Problems: [`08-19.md`](08-19.md).

## Headline

**Both of yesterday's mechanical bugs look fixed.** Every setup today (R2, Core 1(a),
Core 2(a), Core 2(b)) states only what's given — no circularity. Every witness today
used $\mathbb{Z}$, not $\mathbb{N}$ ("$k \in \mathbb{Z}$" in Core 2(a), "$c \in
\mathbb{Z}$" in Core 2(b)). That's four-for-four on both counts, across problems that
didn't exist yesterday — real, independent evidence, not a fluke on one repeated
example.

Two new things showed up instead:

1. **Core 1(b) has no actual argument in it.** You were asked why an
   injective-not-surjective function can't exist when domain and codomain are the same
   *finite* set, and the answer restates the question ("it must be injective... but it
   can't be surjective") without saying *why* it can't be surjective. This isn't a
   slip — it's a missing piece of machinery (pigeonhole), and it's already sitting in
   the lesson file at **§8, "The finite case"** — which today's session didn't point
   you at (it only pointed to §4). That's on the session, not on you; it's fixed
   below and pulled into tomorrow's Core.
2. **Core 2(b) stops one sentence before the finish.** You correctly derive $3 \mid a$
   and then, using the lemma from (a) again, $3 \mid b$ — and then the file ends. The
   whole point of the setup was $\gcd(a,b)=1$; you have to say "$3 \mid a$ **and**
   $3 \mid b$ contradicts $\gcd(a,b)=1$, so the assumption that $\sqrt3$ is rational is
   false, hence $\sqrt3$ is irrational." Every piece was on the page. It just never got
   assembled into the sentence that ends the proof. This is bug #1 again, in a longer
   proof than the ones it looked fixed on yesterday — see "What this changes" below.

---

## Item-by-item

### R1 — contrapositive vs. contradiction, when/why

**Correct**, and well put: contrapositive gives you a specific target ($\lnot P$) to
aim at, contradiction just gives you license to find *any* absurdity. That's the right
distinction. Keep this exact framing in mind for Core 2(a) below — it's the thing that
slipped there.

### R2 — setup line: sum of two evens is even

**Correct.** "Let's assume that $a,b$ are two even integers" assumes only the
hypothesis. Self-check line was left blank — worth actually writing the answer
("only that $a,b$ are"), since the self-check is what catches this bug in real time
before you've built ten lines on top of a bad setup.

### Core 1(a) — $f:\mathbb{Z}\to\mathbb{Z}$ injective, not surjective

**Correct proof, one notation problem to fix.** "My function: $2a=2b$" isn't a
function — it's an equation. What you mean is $f(n) = 2n$; write that as the very
first line, before you use it. Everything downstream is consistent with $f(n)=2n$ (and
correctly switches between calling the input $a$/$b$ in the injectivity check and $n$
in the surjectivity check — pick one letter and stick with it, but that's cosmetic).

**Injectivity:** correct — assume $f(a)=f(b)$, so $2a=2b$, divide by 2, $a=b$.

**Non-surjectivity:** correct in substance. Cleaner phrasing: "consider the target
value $1$ in the codomain; suppose some $n$ satisfies $f(n)=1$, i.e. $2n=1$, so
$n=\tfrac12 \notin \mathbb{Z}$ — contradiction, so no such $n$ exists." Same logic you
wrote, just naming the object (a value in the codomain) instead of calling it "the
target codomain."

### Core 1(b) — why impossible on a finite set of the same size

**Not correct — no mechanism given.** "It must be injective... but it can't be
surjective which makes it impossible" restates the claim; it doesn't derive it. The
actual argument (pigeonhole): an injective $f$ from a set of size $n$ to itself sends
$n$ *distinct* inputs to $n$ *distinct* outputs (that's what injective means — no
collisions). $n$ distinct outputs inside a codomain of size $n$ **is** all of the
codomain — there's no room left for anything to be missed. So on a finite set of equal
size, injective forces surjective; there's no way to "use up" all the room without
covering it.

This is written out in **lesson §8, "The finite case"** — worth reading before
tomorrow, since tomorrow's Core reuses this exact idea.

### Core 1(c) — finite vs. infinite

**Blank.** Once (b) has an actual mechanism behind it, (c) falls out of it directly:
on an infinite set there's always "room" left over even after an injective map uses up
infinitely many outputs — $n \mapsto 2n$ on $\mathbb{Z}$ hits all the even integers and
never touches the odd ones, and there are still infinitely many of those left over.
That's the sense in which pigeonhole *fails* for infinite sets, and it's close to the
actual definition of what makes a set infinite.

### Core 2(a) — $3 \mid n^2 \implies 3 \mid n$

**Computation correct, one transcription slip, one framing error.**

Case $n=3k+1$: $n^2 = 9k^2+6k+1 = 3(3k^2+2k)+1$. Correct.

Case $n=3k+2$: you wrote "$9k^2+12k\,3+1$" — a dropped operator, should read
$9k^2+12k+4$. You then correctly simplified to $3(3k^2+4k+1)+1$, which *is* the right
answer for $9k^2+12k+4$ (check: $3(3k^2+4k+1)+1 = 9k^2+12k+3+1 = 9k^2+12k+4$ ✓) — so
the arithmetic that mattered was right, but that intermediate line as written doesn't
parse. Write $(3k+2)^2 = 9k^2+12k+4$ in one clean step next time, before you start
pulling factors of 3 out of it.

**Framing:** the problem told you to use the contrapositive (assume $3\nmid n$, show
$3\nmid n^2$), which is exactly what you did — but the closing sentence describes it
as a contradiction: "...but our original statement was **given** $3\mid n^2$ so we
have reached a contradiction." There is no "given" here. A contrapositive proof of
$3\mid n^2 \implies 3\mid n$ is: assume $3 \nmid n$, derive $3 \nmid n^2$, done — that
*is* the contrapositive, and by itself it establishes the original implication with no
contradiction step needed. What you wrote is correct *content* wearing the wrong
proof's clothing. This is worth noticing because you stated the contrapositive/contradiction
distinction correctly in R1 above, in the abstract — the gap is between knowing the
distinction and applying it to your own proof as you're writing it. Quick fix for next
time: after you finish a proof, ask "which technique did I just use?" and check the
closing sentence matches it.

### Core 2(b) — $\sqrt3$ is irrational

**Correct through the last real step, then stops before the landing.** Setup is
clean (assumes $\sqrt3=a/b$ in lowest terms — the negation of the goal, correctly
stated, nothing extra smuggled in). $3b^2=a^2$ is right. One imprecision: "$a^2$ must
be a factor of 3" has it backwards — $3$ is a factor of $a^2$ (i.e. $3 \mid a^2$), not
the other way around; small wording thing but worth being exact about, since divisor
and multiple aren't interchangeable. From there, $a=3c$, $b^2=3c^2$, and — correctly,
citing part (a) explicitly this time — $3 \mid b$.

**And then the file ends.** You've shown $3\mid a$ and $3\mid b$. The proof needed one
more sentence: *both* $a$ and $b$ being multiples of 3 contradicts the lowest-terms
assumption $\gcd(a,b)=1$ from the setup — that contradiction is the entire reason the
original assumption ($\sqrt3$ rational) must be false, which is what makes $\sqrt3$
irrational. Every fact needed to write that sentence was already on the page.

### Stretch — $\sqrt p$ irrational for any prime $p$

Not attempted — optional, no penalty. Solution posted anyway; it's the same skeleton
as Core 2(b) with Euclid's lemma standing in for the by-hand case-split in Core 2(a).

---

## What this changes

- **Setup discipline: advancing.** Clean, independent uses across R2, Core 1(a), Core
  2(a), Core 2(b) — four for four, no exceptions. REVIEW-QUEUE interval advances
  1d → 3d.
- **Existential witnesses in $\mathbb{Z}$: advancing.** Clean in both places a witness
  was needed (Core 2(a), Core 2(b)). Interval advances 1d → 3d.
- **Bug #1 (landing) is not closed, and today added a caution rather than a second
  clean instance.** Core 2(b) is a *relapse* on a longer, multi-step proof, right after
  a clean short one on 08-18. The pattern looks like: landing holds on short, single-move
  proofs, and drops on proofs with three or more chained deductions. Staying open;
  retest is tomorrow's review block (recall the $\sqrt3$ proof cold, land it out loud).
- **New: pigeonhole / finite injective ⟹ surjective.** Core 1(b) and (c) show the
  mechanism isn't there yet, and it's the kind of gap that will resurface anywhere
  finiteness matters. Already written in lesson §8 — tomorrow's Core reuses it directly
  rather than spending a whole session re-deriving it from scratch.
- **Injective/surjective, narrowed.** Constructing the example and proving both halves
  (1(a)) is genuinely solid now — first real data, and it's clean modulo notation.
  What's missing is specifically the finite-case argument, not the general
  injective/surjective mechanics. Evidence log updated to reflect that split.

**Difficulty: advance to the next new topic (quantifier negation, §5), not held.**
Everything that failed today is narrow and specific — a missing lemma (pigeonhole, now
pointed at directly) and one incomplete landing on the hardest problem in the session.
Nothing here is a method-level misunderstanding of what was actually being taught
today (contradiction, contrapositive-in-the-abstract, existential witnesses, setup
discipline all landed). Repair goes into tomorrow's review block and one Core problem
that connects the new topic back to today's gap, rather than spending a whole
additional session standing still.
