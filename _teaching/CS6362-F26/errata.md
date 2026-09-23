---
layout: page
title: Lecture Errata and Clarifications
description: Corrections and clarifications to CS 6362 lecture slides
permalink: /courses/CS6362-F26/errata/
nav: false
---

[← Back to CS 6362 course page](/courses/CS6362-F26/)

Page numbers count the title slide as page 1. The two _Lecture 5_ files are distinguished by week.

**1. Clarification: Hoeffding probability bound — Lecture 2, p.8**

Under the usual Hoeffding assumptions, the displayed $$1-\delta$$ bound is valid for $$0<\delta\le\tfrac12$$, but weaker than the standard bound. Replace $$1-\delta$$ with $$\delta$$ to express the sharper failure-probability guarantee. The corresponding good event holds with probability at least $$1-\delta$$.

The original expression is not generally guaranteed for arbitrary $$\delta\in(0,1)$$.

**2. Strict convexity and the Hessian — Lecture 2, pp.29, 31; Lecture 3, p.43; Lecture 4, pp.13, 18**

Replace "strict convexity implies positive definiteness" with:

> For a twice-differentiable function on an open convex domain, a positive-definite Hessian everywhere is sufficient for strict convexity.

The converse does not hold: $$f(x)=x^4$$ is strictly convex, but $$f''(0)=0$$. In the Lecture 4 comparison table, the positive-definite Hessian condition is **sufficient**, not necessary.

**3. Clarification: the first-order strict-convexity inequality is correct — Lecture 2, p.29; Lecture 3, p.41; Lecture 4, p.16**

The displayed expression

$$
f(x)<f(y)+\nabla f(x)^\top(x-y)
$$

rearranges to

$$
f(y)>f(x)+\nabla f(x)^\top(y-x),\qquad x\ne y.
$$

These are equivalent; no mathematical correction is needed.

**4. Strong-convexity convention — week3/Lecture 5, pp.24–26**

Use the following convention consistently:

$$
f(y)\ge f(x)+\nabla f(x)^\top(y-x)
+\frac c2\|y-x\|^2.
$$

Insert the missing factor $$1/2$$ on p.24. The subsequent bound

$$
2c(F(w)-F_*)\le\|\nabla F(w)\|^2
$$

and its use on p.26 remain valid.

**5. Momentum recurrence — week4/Lecture 5, p.51**

The correct recurrence is

$$
w_t-w_{t-1}
=-\alpha_{t-1}\nabla F(w_{t-1})
+\beta(w_{t-1}-w_{t-2}).
$$

The momentum term has a **plus sign**. Lecture 6, p.6 already uses the correct sign. The expanded history sum assumes constant step size and zero initial velocity.

**6. Stochastic momentum — week4/Lecture 5, p.53; Lecture 6, p.22**

Inside the history sum, replace

$$
\nabla f(w_t;\xi_k)\quad\text{with}\quad\nabla f(w_k;\xi_k).
$$

Past gradients were evaluated at the corresponding past iterates.

**7. Index and notation corrections — week4/Lecture 5**

- **pp.40–41:** the two-sample average should be

  $$
  \frac12\bigl(\nabla f(w_t;\xi_{t,1})+\nabla f(w_t;\xi_{t,2})\bigr).
  $$

- **p.26:** for $$\alpha_t=a/(b+t)$$, the prose should refer to $$a,b$$, not beta and gamma. The initial step is $$a/(b+1)$$; larger $$b$$ gives slower relative decay.
- **p.27:** replace the unexplained $$\lambda$$ with $$c$$, the strong-convexity constant.
