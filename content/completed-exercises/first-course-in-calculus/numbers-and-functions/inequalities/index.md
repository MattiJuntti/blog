+++
title  = "02: Inequalities"
date   = "2025-01-01T00:00:00+03:00"
layout = "solution-single"
+++

<span class = "exnum">1</span> Following the example in the section $|x| <
3$ leads two cases: $x < 3$ and $-x < 3$. Multiplying both sides of the
second case with $-1$ (**Rule 3**) means that $x > -3$. So the interval of
numbers satisfying the given equation is

$$
    \phantom{.} \ |x| < 3 \ .
$$

<span class = "exnum">2</span> The inequality leads to two cases: $2x + 1
\leq 1$ and $-(2x + 1) = -2x - 1 \leq 1$. Solving the first case means that

$$
    \begin{array}{r c l | r}
        2x + 1 & \leq & 1 & -1 \\
            2x & \leq & 1 - 1 = 0 & \div 2 \\
             x & \leq & 0
    \end{array}
$$

and 

$$
    \begin{array}{r c l | r}
        -2x - 1 & \leq & 1         & +1        \\
            -2x & \leq & 1 + 1 = 2 & \div (-2) \\
              x & \leq & -1
    \end{array}    
$$

Gathering the results it can be seen that the numbers satisfying the
equation are

$$
    \phantom{.} \ x \leq 0 \ .
$$

<span class = "exnum">3</span> As above, the two cases are $x^2 - 2 \leq 1$
and $-(x^2 - 2) = -x^2 + 2 \leq 1$. Solving for $x$ in both cases means
adding $2$ to the former case and subtracting $-2$ in the latter. Then both
sides of the second case are multiplied by $-1$ and both sides of both
cases are squred. This leads to the fact that $x \leq \sqrt{3}$ and $x \geq
\sqrt{1}$, so the numbers $x$ satisfyin the inequality are $\sqrt{1} \leq
x \leq \sqrt{3}$.

<span class = "exnum">4</span> Since $|x - 5| = \pm\sqrt{x - 5}^2 =
\pm(x-5)$.  The inequality $|x - 5| = \pm(x - 5) > 2$ leads to two
inequalities, $x - 5 > 2$ and $-(x - 5) = -x + 5 > 2$. Solving for $x$ in
both inequalities, means adding $5$ to both sides of the first inequality,
subtracting $-5$ from the second inequality and multiplying it by $-1$.
Then the solution for the inequality are the number $x > 7$ and numbers $x
< -3$.

<span class = "exnum">5</span> Even though it can be seen from the
inequality, letting $y = (x - 1)(x + 2) = x^2 + x - 2$ be equal to $0$, and
solving the roots of this quadratic by applying the quadratic formula, the
roots of the equation are $x = 1$ or $x = -2$. This divides the $x$-axis
into three sections $x < -2$, $-2 < x < 1$, and $x > 1$.

Let $\epsilon > 0$ be arbitrarily close to $0$, then $x - \epsilon \leq x <
-2$. Then substituting $x - \epsilon$ in to the inequality leads to
inequality $(x - \epsilon)^2 + (x - \epsilon) - 2 < 2$, from where it can
be seen that the $(x - \epsilon) - 2$ is very close to zero too, and
$(x - \epsilon)^2$ is always nearly $2$ for arbitrarily small $\epsilon$,
so $(x - \epsilon)^2$ is always a bit more than $4$, and since $4 > 2$, $x
\not < -2$ (that is, $x$ can not be less than $-2$).

Let $x = -\frac{1}{2}$, i.e. the midway at interval $-2 < x < 1$, then

$$
    \phantom{,} \
        \left( -\frac{1}{2} \right)^2 + \frac{1}{2} - 2
            = \dfrac{1}{4} + \dfrac{1}{2} - 2
            = \dfrac{5}{4}
    \ ,
$$

which is at the interval.

Lastly let $x = 1 + \epsilon$, then substituting $x$ to $x^2 + x - 2$ leads
to

<div class = "widescreen">
$$
    \phantom{.} \
    (1 + \epsilon)^2 + (1 + \epsilon) - 2
        = 1 + 2\epsilon + \epsilon^2 + 1 + \epsilon - 2
        = \epsilon^2 + 3 \epsilon
    \ ,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
                & (1 + \epsilon)^2 + (1 + \epsilon) - 2
            \\= & 1 + 2\epsilon + \epsilon^2 + 1 + \epsilon - 2
            \\= & \epsilon^2 + 3 \epsilon \ ,
    \end{array}
$$
</div>

which obviously is not greater than $1$ so $x \not > 1$.

Because $x$ is not less than $-2$, not greater than $1$, and $-2 < x < 1$,
the interval for where $x$ is defined, when $(x - 1)(x + 2) < 0$ is the
interval

$$
    \phantom{.} \ -2 < x < 1 \ .
$$
