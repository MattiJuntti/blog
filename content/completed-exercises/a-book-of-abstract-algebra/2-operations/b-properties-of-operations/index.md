+++
title  = "B. Properties of operations"
layout = "solution-single"
+++

<span class = "exnum">1</span> If

$$
    x \ast y = x + 2y +4
$$

then

$$
    y \ast x = 2y + x + 4
$$

which is equal to $x \ast y$, so the operation $\ast$ is
associative.

Because

$$
    \begin{array}{r c l}
        x \ast (y \ast z)
        & = & x \ast (y + 2z + 4)   \\[0.5em]
        & = & x + 2(y + 2z + 4) + 4 \\[0.5em]
        & = & x + 2y + 4z + 12
    \end{array}
$$

and

$$
    \begin{array}{r c l}
        (x \ast y) \ast z
        & = & (x + 2y + 4) \ast z   \\[0.5em]
        & = & (x + 2y + 4) + 2z + 4 \\[0.5em]
        & = & x + 2y + 2z + 8
    \end{array}
$$

which are not equal, the $\ast$ operation is not commutative.

Solving for the identity element $e$ in equation $x \ast e = x$, it
can be seen that

$$
    \phantom{,} \ x \ast e = x + 2e + 4 = x \ ,
$$

so

$$
    2e = -4
$$

which means that

$$
    e = -2.
$$

Substituting $e$ back to $x$ $+$ $2e$ $+$ $4$ $=$ $x$ shows that

$$
    x + 2(-2) + 4 = x - 4 + 4 = x
$$

so $\ast$ operation has an identity.

Because $\ast$ has an identity it's worthwhile to look for an
inverse of $\ast$. This means solving

$$
    x \ast x^\prime = x + 2x^\prime + 4 = 2 = e
$$

for $x^\prime$. Therefore,

$$
    x^\prime = \dfrac{-x -2}{2} = - \dfrac{x}{2} - 1
$$

and substituting $x^\prime$ back to $x$ $+$ $2x^\prime$ $+$ $4$
shows that

$$
    \begin{array}{r c l}
        x \ast x^\prime
        & = & x + 2 \left(- \dfrac{x}{2} - 1\right) + 4 \\[0.5em]
        & = & x - x - 2 + 4 \\[0.5em]
        & = & 2,
    \end{array}
$$

so it's possible that inverse exists.

To be sure of this, $x^\prime \ast x$ also needs to be equal to
newly found identity element $e$, so noticing that

<div class = "widescreen">
$$
    x^\prime \ast x
        \ = \ x^\prime + 2x + 4
        \ = \ \left( - \dfrac{x}{2} - 1 \right) + 2x + 4
        \ = \ - \dfrac{1}{2} x + 2x + 4 - 1
        \ = \ - \dfrac{3}{2}x - 3
        \ \neq \ 2,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        x^\prime \ast x
        & = & x^\prime + 2x + 4 \\[1.0em]
        & = & \left( - \dfrac{x}{2} - 1 \right) + 2x + 4 \\[1.0em]
        & = & - \dfrac{1}{2} x + 2x + 4 - 1 \\[1.0em]
        & = & - \dfrac{3}{2}x - 3 \\[0.5em]
        & \neq & 2,
    \end{array}
$$
</div>

which means that not all elements have inverse.

<span class = "exnum">2</span> Checking for commutativity of

$$
    x \ast y = x + 2y - xy
$$

means evaluating

$$
    y \ast x = y + 2x - yx = 2x + y - yx
$$

Because $x \ast y$ $\neq$ $y \ast x$, the operation is not
associate.

Moreover, since

<div class = "widescreen">
$$
    \begin{array}{r c l}
    x \ast (y \ast z)
        & = & x \ast (y + 2z - yz) \\[0.5em]
        & = & x + 2(y + 2z - yz) - x(y + 2z - yz) \\[0.5em]
        & = & x + 2y + 4z - 2yz - xy - 2xz + xyz
    \end{array}
$$
</div>

<div class = "smallscreen">

$$
    \begin{array}{c l}
          & x \ast (y \ast z) \\[0.5em]
        = & x \ast (y + 2z - yz) \\[0.5em]
        = & x + 2(y + 2z - yz) - x(y + 2z - yz) \\[0.5em]
        = & x + 2y + 4z - 2yz - xy - 2xz + xyz
    \end{array}
$$
</div>

and

<div class = "widescreen">
$$
    \begin{array}{r c l}
        (x \ast y) \ast z
            & = & (x + 2y - xy) \ast z \\[0.5em]
            & = & (x + 2y - xy) + 2z - (x + 2y - xy)z \\[0.5em]
            & = & x + 2y - xy + 2z - zx - 2yz + xyz
    \end{array}
$$

</div>
<div class = "smallscreen">
$$
    \begin{array}{c l}
          & (x \ast y) \ast z \\[0.5em]
        = & (x + 2y - xy) \ast z \\[0.5em]
        = & (x + 2y - xy) + 2z - (x + 2y - xy)z \\[0.5em]
        = & x + 2y - xy + 2z - zx - 2yz + xyz
    \end{array}
$$
</div>

are not equal, operation $\ast$ does not commute.

Solving $x \ast e$ $=$ $x$ for $e$, means that

$$
    \begin{array}{r c l}
        x \ast e
            & = & x + 2e - xe \\[0.5em]
            & = & x + e(2 - x) \\[0.5em]
            & = & x,
    \end{array}
$$

so

$$
    e = \dfrac{x - x}{2 - x} = 0.
$$

Substituting $e$ $=$ $0$ back to $x \ast e$ shows that

$$
    x + 2(0) - x(0)
$$

indeed is $x$, so the operations has an identity.

Checking for inverse, the equation $x \ast x^\prime$ $=$ $e$ needs
to be first solved for $x^\prime$. Because

$$
    x \ast x^\prime = x + 2x^\prime - xx^\prime = 0 = e
$$

and

$$
    x + 2x^\prime - xx^\prime = x + x^\prime(2 - x) = 0
$$

so therefore

$$
    x^\prime(2 - x) = -x    
$$

and hence

$$
    x^\prime = - \dfrac{x}{2 - x}.
$$

Substituting $x^\prime$ back to equation $x \ast x^\prime$ means
that

$$
    \begin{array}{r c l}
        x \ast x^\prime
            & = & x - 2 \dfrac{x}{2 - x} - x \dfrac{x}{2 - x} \\[1.0em]
            & = & x - \dfrac{2x - x}{2 - x} \\[1.0em]
            & = & x - x \\[1.0em]
    \end{array}
$$

which is equal to $0$

$$
    \begin{array}{r c l}
        x^\prime \ast x
            & = & -\dfrac{x}{2 - x} + 2x + \dfrac{x}{2 - x}x \\[0.5em]
            & = & 2x - \dfrac{x + x^2}{2 - x} \\[0.5em]
            & = & 0.
    \end{array}
$$

Multiplying both sides of the equality leads to

$$
    \begin{array}{r c l}
        (2 - x)2x - x + x^2
        & = & 4x - 2x^2 - x + x^2 \\[0.5em]
        & = & -x^2 + 3x \\[0.5em]
        & = & x(-x + 3) \\[0.5em]
        & = & 0.
    \end{array}
$$

Based on the [zero product property][01] the equality leads to two
equations, either $x = 0$ or $-x + 3 = 0$, from where solving the
latter leads to $x = 3$. Because $x$ is either $0$ or $3$, the $x
\ast x^\prime$ is not unique, $x^\prime \ast x$ $\neq$ $x \ast
x^\prime$ and the operation $\ast$ does not have inverses for all
values in $\mathbb{R}$.

[01]:https://www.mathsisfun.com/algebra/zero-product-property.html

<span class = "exnum">3</span> Because

$$
    x \ast y = |x + y| = |y + x| = y \ast x,
$$

the $\ast$ operation is commutative.

Since

$$
    \begin{array}{r c l}
        x \ast (y \ast z) & = & x \ast (|y + z|) \\[0.5em]
                          & = & |x + |y + z|| \\[0.5em]
                          & = & ||x + y| + z| \\[0.5em]
                          & = & (|x + y|) \ast z \\[0.5em]
                          & = & (x \ast y) \ast z,
    \end{array}
$$

the $\ast$ operation is associative.

Identity element exists if the equation can be solved for $e$ in $x
\ast e = x$. Let

$$
    x \ast e = x,
$$

then the equation is equivalent to

$$
    |x + e| = x,
$$

so there's two equations to be solved, $x + e$ $=$ $x$ and $-(x +
e)$ $=$ $x$. Solution for the first is $e$ $=$ $x - x$ $=$ $0$ and
for the second $e$ $=$ $x + x$ $=$ $2x$.

Checking that $x \ast e$ $=$ $e \ast x$ $=$ $x$ for the identities
means that for $x \ast e$ $>$ $0$,

<div class = "widescreen">
$$
    x \ast e = |x + 0| = x + 0 = x = 0 + x = |0 + x| = e \ast x,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        x \ast e & = & |x + 0| \\[0.5em]
                 & = & x + 0   \\[0.5em]
                 & = & x       \\[0.5em]
                 & = & 0 + x   \\[0.5em]
                 & = & |0 + x| \\[0.5em]
                 & = & e \ast x,
    \end{array}
$$
</div>

and for $x \ast r$ $\leq$ $0$,

<div class = "widescreen">
$$
    x \ast e = |x + 2x| = x + 2x = 3x \neq x \neq 2x + x = |2x + x| = e \ast x,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        x \ast e & =    & |x + 2x| \\[0.5em]
                 & =    & x + 2x   \\[0.5em]
                 & =    & 3x       \\[0.5em]
                 & \neq & x        \\[0.5em]
                 & \neq & 2x + x   \\[0.5em]
                 & =    & |2x + x| \\[0.5em]
                 & =    & e \ast x,
    \end{array}
$$
</div>

from which it can be claimed that the latter identity element does
not hold, but the first does. Assuming that the identity is true
for when $x \ast r$ $\leq$ $0$, the previous equation becomes
equal to the first and it holds. Because of this, letting $e$ be
equal to $0$, the identity is unique and exits for the operation
$\ast$.

If the inverse for $\ast$ exists, then the equation $x \ast
x^\prime$ $=$ $e$ can be solved for $x^\prime$. Then, because

$$
    x \ast x^\prime = |x + x^\prime| = e,
$$

so if $|x + x^\prime|$ $>$ $0$ then

$$
    e = x + x^\prime 
$$

or if $|x + x^\prime|$ $\leq$ $0$ then

$$
    e = -(x + x^\prime) = -x - x^\prime.
$$

Solving these cases for $x^\prime$ means that

$$
    x^\prime = e - x = 0 - x = -x,
$$

and

$$
    x^\prime = -e - x = 0 - x = -x,
$$

so substituting $x^\prime$ to equation $x$ $\ast$ $x^\prime$ $=$
$e$ means that

$$
    |x + x^\prime| = |x - x| = |0| = 0,
$$

and same for equation $x^\prime$ $\ast$ $x$ $=$ $e$ means that

$$
    |x^\prime + x| = |-x + x| = |0| = 0,
$$

which means that the inverse exists, namely $x^\prime$ $=$ $-x$,
because $x \ast x^\prime$ leads to $e$.

<span class = "exnum">4</span> Operation $x \ast y$ $=$ $|x - y|$.

**_Commutativity_**: If $x \ast y$ $=$ $y \ast x$ the operation is
commutative. When $x \ast y$ $>$ $0$, $x \ast y$ $=$ $x - y$ and
when $x \ast y$ $\leq$ $0$, $x \ast y$ $=$ $-(x - y)$ $=$ $-x + y$.
Similarly, when the operation is $y \ast x$, the equations are $y - x$
and $-y + x$. Now, when $x \ast y$ and $y \ast x$ are both strictly
greater than $0$, $x \ast y$ $=$ $|x - y|$ $=$ $x - y$ $\neq$ $y -
x$ $=$ $|y - x|$ = $y \ast x$, and when $x \ast y$ and $y \ast x$
are less or equal to $0$, $x \ast y$ $=$ $|x - y|$ $=$ $-(x - y)$ $=$ $-x + y$ 
$\neq$ $-y + x$ $=$ $-(y - x)$ $=$ $|y - x|$, so the operation
$\ast$ does not commute.

**_Associativity_**: The operations is associative if $x \ast (y
\ast z)$ $=$ $(x \ast y) \ast z$. Rewriting the left hand-side as

$$
    x \ast (y \ast z) = x \ast |y - z| = |x - |y - z||
$$

shows that the parentheses lead to nested absolute value equation.
Solving the outer absolute value first means that

$$
    x \ast (y \ast z) = |x - |y - z||
$$

is either $x - |y - z|$ or $-(x - |y - z|)$ $=$ $-x + |y - z|$.
Moreover, the inner absolute means that both of these possible
solutions can have two different solutions, namely:

<div class = "widescreen">
$$
    \begin{array}{ c c c c c c c c }
        (1): & x - (y - z),  &
        (2): & x + (y - z),  &
        (3): & -x + (y - z), &
        (4): & -x - (y - z).
   \\[0.5em] & \| & & \| & & \| & & \| & \\[0.5em]
        (1): & x - y + z,  &
        (2): & x + y - z,  &
        (3): & -x + y - z, &
        (4): & -x - y + z.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c r c c r }
        (1): & x - (y - z)  & = & (1): & x - y + z,  \\
        (2): & x + (y - z)  & = & (2): & x + y - z,  \\
        (3): & -x + (y - z) & = & (3): & -x + y - z,  \\
        (4): & -x - (y - z) & = & (4): & -x - y + z.
    \end{array}
$$
</div>

Doing the same for $(x \ast y) \ast z$ leads to similar results,
that is four different possible solutions:

<div class = "widescreen">
$$
    \begin{array}{ c c c c c c c c }
        (1^\prime): &  (x - y) - z, &
        (2^\prime): & -(x - y) - z, &
        (3^\prime): & -(x - y) + z, &
        (4^\prime): &  (x - y) + z.
          \\[0.5em] & \| & & \| & & \| & & \| & \\[0.5em]
        (1^\prime): &   x - y - z, &
        (2^\prime): &  -x + y - z, &
        (3^\prime): &  -x + y + z, &
        (4^\prime): &   x - y + z.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c r c c r }
        (1): & x - (y - z)  & = & (1): & x - y + z,  \\
        (2): & x + (y - z)  & = & (2): & x + y - z,  \\
        (3): & -x + (y - z) & = & (3): & -x + y - z,  \\
        (4): & -x - (y - z) & = & (4): & -x - y + z.
    \end{array}
$$
</div>

From these we can see that only $(3)$ $=$ $(3^\prime)$, that is,
the $\ast$ operation is associative only when the outer absolute
value is less or equal to $0$ and the inner absolute value strictly
greater than $0$. For the operation to be commutative, all of the
cases $(1), (2), (3)$ and $(4)$ should equal. This does not happen
so the $\ast$ is not associative.

**_Identity_**: Solving for currently not known identity element
$e$ in the equation $x \ast e$ $=$ $|x - e|$ = $x$ leads again to
the two cases: $x - e$ $=$ $x$ or $-x + e$ $=$ $x$. Solving the
first results in $e$ $=$ $0$ and the second in $e$ $=$ $2x$, so
there's no unique identity element. Therefore $\ast$ does not have
identity.

**_Inverses_**: ...

<span class = "exnum">5</span> Because $x \ast y$ $=$ $xy + 1$ and
$y \ast x$ $=$ $yx + 1$ that is equal to $xy + 1$, because
multiplication is commutative, then $x \ast y$ is commutative.
Since $x \ast (y \ast z)$ $=$ $x \ast (yz + 1)$ $=$ $x(yz + 1) + 1$
and $(x \ast y) \ast z$ $=$ $(xy + 1) \ast z$ $=$ $(xy + 1)z + 1$,
the operations are not equal, so $\ast$ is not commutative.
Solving $x \ast e$ $=$ $xe + 1$ $=$ $x$, for $e$, shows that $e$
$=$ $1 - \frac{1}{x}$. When substituting $e$ back to original
equation it can be seen that

<div class = "widescreen">
$$
    x \ast e
        = xe + 1
        = x \left(1 - \dfrac{1}{x} \right) + 1
        = x - 1 + 1
        = x,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c l }
          & x \ast e \\[0.5em]
        = & xe + 1 \\[0.5em]
        = & x \left(1 - \dfrac{1}{x} \right) + 1 \\[0.5em]
        = & x - 1 + 1 \\[0.5em]
        = & x,
    \end{array}
$$
</div>

so the identity exits, i.e. $e = 1 - \frac{1}{x}$. Assuming this,
the inverse seems to exist for $x \ast x^\prime$ $=$ $e$. Because

$$
    x \ast x^\prime = xx^\prime + 1 = 1 - \dfrac{1}{x} = e,
$$

and solving $x^\prime$ means dividing through both sides of the
equals signs, it can be shown that

$$
    x^\prime + \dfrac{1}{x}
        = \dfrac{1}{x} - \dfrac{1}{x} \left( \dfrac{x}{1} \right)
        = \dfrac{1}{x} - 1,
$$

so

$$
    x^\prime = \dfrac{1}{x} - 1 - \dfrac{1}{x} = -1.
$$

Because $x \ast x^\prime$ $=$ $xx^\prime - 1$ $=$ $x(-1) = -1$,
then $x$ $=$ $1$, but $x^\prime x - 1$ $=$ $-x - 1$ $=$ $-1$, that
is $x$ $=$ $0$, the inverse does not exist for the element $\ast$.

<span class = "exnum">6</span> The operation $x \ast y$ $=$
$\max\{x,y\}$ is commutative because $x \ast y$ $=$ $\max\{x,y\}$
$=$ $\max\{y,x\}$ $=$ $y \ast x$. If $\ast$ is associative, then

<div class = "widescreen">
$$
    x \ast (y \ast z) = \max\{x,\max\{y,z\}\} = \max\{\max\{x,y\},z\} = (x \ast y) \ast z.
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        x \ast (y \ast z) & = & \max\{x,\max\{y,z\}\} \\[0.5em]
                          & = & \max\{\max\{x,y\},z\} \\[0.5em]
                          & = & (x \ast y) \ast z.
    \end{array}
$$
</div>

To prove this, solving the following six inequalities need to be
tested<a href =
"https://math.stackexchange.com/questions/222708/how-to-prove-associativity#222711"><sup>1</sup></a><sup>,</sup><a href =
"https://proofwiki.org/wiki/Max_Operation_is_Associative"><sup>2</sup></a>
for both $x \ast (y \ast z)$ and $(x \ast y) \ast z$:

<div class = "widescreen">
$$
    \begin{array}{ l }
        (1) \ x \leq y \leq z: \\[1.0em]
        \qquad \begin{array}{r c r c l}
            x \ast (y \ast z) & = & \max\{x,\max\{y,z\}\} & = & z \\[0.5em]
            (x \ast y) \ast z & = & \max\{\max\{x,y\},z\} & = & z 
        \end{array}
    %
        \\[1.5em]
        (2) \ x \leq z \leq y: \\[1.0em]
        \qquad \begin{array}{r c r c l}
            x \ast (y \ast z) & = & \max\{x,\max\{y,z\}\} & = & y \\[0.5em]
            (x \ast y) \ast z & = & \max\{\max\{x,y\},z\} & = & y 
        \end{array}
    %
        \\[1.5em]
        (3) \ y \leq x \leq z: \\[1.0em]
        \qquad \begin{array}{r c r c l}
            x \ast (y \ast z) & = & \max\{x,\max\{y,z\}\} & = & z \\[0.5em]
            (x \ast y) \ast z & = & \max\{\max\{x,y\},z\} & = & z 
        \end{array}
    %
        \\[1.5em]
        (4) \ y \leq z \leq x: \\[1.0em]
        \qquad \begin{array}{r c r c l}
            x \ast (y \ast z) & = & \max\{x,\max\{y,z\}\} & = & x \\[0.5em]
            (x \ast y) \ast z & = & \max\{\max\{x,y\},z\} & = & x 
        \end{array}
    %
        \\[1.5em]
        (5) \ z \leq x \leq y: \\[1.0em]
        \qquad \begin{array}{r c r c l}
            x \ast (y \ast z) & = & \max\{x,\max\{y,z\}\} & = & y \\[0.5em]
            (x \ast y) \ast z & = & \max\{\max\{x,y\},z\} & = & y 
        \end{array}
    %
        \\[1.5em]
        (6) \ z \leq y \leq x: \\[1.0em]
        \qquad \begin{array}{r c r c l}
            x \ast (y \ast z) & = & \max\{x,\max\{y,z\}\} & = & x \\[0.5em]
            (x \ast y) \ast z & = & \max\{\max\{x,y\},z\} & = & x 
        \end{array}
    %
        \\[1.5em]
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ l }
        (1) \ x \leq y \leq z: \\[1.5em]
        \qquad \begin{array}{c l}
              & x \ast (y \ast z)     \\[0.5em]
            = & \max\{x,\max\{y,z\}\} \\[0.5em]
            = & z                     \\[1.5em]
              & (x \ast y) \ast z     \\[0.5em]
            = & \max\{\max\{x,y\},z\} \\[0.5em]
            = & z 
        \end{array}
    %
        \\[1.5em]
        (2) \ x \leq z \leq y: \\[1.5em]
        \qquad \begin{array}{c l}
              & x \ast (y \ast z)     \\[0.5em]
            = & \max\{x,\max\{y,z\}\} \\[0.5em]
            = & y                     \\[1.5em]
              & (x \ast y) \ast z     \\[0.5em]
            = & \max\{\max\{x,y\},z\} \\[0.5em]
            = & y 
        \end{array}
    %
        \\[1.5em]
        (3) \ y \leq x \leq z: \\[1.5em]
        \qquad \begin{array}{c l}
                & x \ast (y \ast z)   \\[0.5em]
            = & \max\{x,\max\{y,z\}\} \\[0.5em]
            = & z                     \\[1.5em]
              & (x \ast y) \ast z     \\[0.5em]
            = & \max\{\max\{x,y\},z\} \\[0.5em]
            = & z 
        \end{array}
    %
        \\[1.5em]
        (4) \ y \leq z \leq x: \\[1.5em]
        \qquad \begin{array}{c l}
              & x \ast (y \ast z)     \\[0.5em]
            = & \max\{x,\max\{y,z\}\} \\[0.5em]
            = & x                     \\[1.5em]
              & (x \ast y) \ast z     \\[0.5em]
            = & \max\{\max\{x,y\},z\} \\[0.5em]
            = & x 
        \end{array}
    %
        \\[1.5em]
        (5) \ z \leq x \leq y: \\[1.5em]
        \qquad \begin{array}{c l}
              & x \ast (y \ast z)     \\[0.5em]
            = & \max\{x,\max\{y,z\}\} \\[0.5em]
            = & y                     \\[1.5em]
              & (x \ast y) \ast z     \\[0.5em]
            = & \max\{\max\{x,y\},z\} \\[0.5em]
            = & y 
        \end{array}
    %
        \\[1.5em]
        (6) \ z \leq y \leq x: \\[1.5em]
        \qquad \begin{array}{c l}
              & x \ast (y \ast z)     \\[0.5em]
            = & \max\{x,\max\{y,z\}\} \\[0.5em]
            = & x                     \\[1.5em]
              & (x \ast y) \ast z     \\[0.5em]
            = & \max\{\max\{x,y\},z\} \\[0.5em]
            = & x 
        \end{array}
    %
        \\[1.5em]
    \end{array}
$$
</div>

Thus, it can be seen that operation $\ast$ is associative, because
no matter what the order of operation is, $\ast$ always is the
largest element of $x$, $y$ and $z$. Identity of the operation, if
it exists, means that $x \ast e$ $=$ $\max\{x,e\}$ $=$ $x$.
Noticing that when $e$ $=$ $-\infty$, for all $x$, $\max\{x,e\}$
$=$ $x$, and the same holds for $\max\{e,x\}$, so $x \ast e$ $=$ $e
\ast x$ $=$ $x$, and the identify element of $\max$ is $-\infty$.
Finding out the inverse of $\max$ would require that there is a
unique inverse element for each $x$. But, for example,

$$
    \max\{1,1\} = 1 = \max{1,0}
$$

so there are element(s) for which the requirement does not hold
and therefore $\ast$ does not have inverse element.

<span class = "exnum">7</span> Since $x \ast y$ $=$ $\frac{xy}{x +
y + 1}$ $=$ $\frac{yx}{y + x + 1}$ $=$ $y \ast x$, the $\ast$
operation is commutative. The operation $\ast$ is associative
because,

<div class = "widescreen">
$$
    \begin{array}{ r c c c l}
        x \ast (y \ast z)
        & = & x \ast \left( \dfrac{yz}{y + z + 1} \right) \\[1.0em]
        & = & \dfrac{x \left( \dfrac{yz}{y + z + 1} \right)}{x + \left( \dfrac{yz}{y + z + 1} \right) + 1} \\[1.0em]
        & = & \dfrac{\dfrac{xyz}{y + z + 1}}{\dfrac{x(y + z + 1) + yz + (y + z + 1)}{y + z + 1}} \\[1.0em]
        & = & \dfrac{\dfrac{xyz}{y + z + 1}}{\dfrac{xy + xz + x + yz + y + z + 1}{y + z + 1}} \\[1.0em]
        & = & \dfrac{xyz(y + z + 1)}{y + z + 1(xy + xz + x + yz + y + z + 1)} \\[1.0em]
        & = & \dfrac{xyz}{xy + xz + x + yz + y + z + 1} \\[1.0em]
        & = & \dfrac{xyz}{xy + xz + yz + z + x + y + 1} \\[1.0em]
        & = & \dfrac{xyz(x + y + 1)}{x + y + 1(xy + xz + yz + z + x + y + 1)} \\[1.0em]
        & = & \dfrac{ \dfrac{xyz}{x + y + 1} }{ \dfrac{xy + xz + yz + z + x + y + 1}{x + y + 1} } \\[1.0em]
        & = & \dfrac{ \dfrac{xyz}{x + y + 1} }{ \dfrac{xy + z(x + y + 1) + (x + y + 1)}{x + y + 1} } \\[1.0em]
        & = & \dfrac{ \left( \dfrac{xy}{x + y + 1} \right) z }{ \left( \dfrac{xy}{x + y + 1} \right) + z + 1 } \\[1.0em]
        & = & \left( \dfrac{xy}{x + y + 1} \right) \ast z
        & = & (x \ast y) \ast z.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c l }
          & x \ast (y \ast z) \\[1.0em]
        = & x \ast \left( \dfrac{yz}{y + z + 1} \right) \\[1.0em]
        = & \dfrac{x \left( \dfrac{yz}{y + z + 1} \right)}{x + \left( \dfrac{yz}{y + z + 1} \right) + 1} \\[1.0em]
        = & \dfrac{\dfrac{xyz}{y + z + 1}}{\dfrac{x(y + z + 1) + yz + (y + z + 1)}{y + z + 1}} \\[1.0em]
        = & \dfrac{\dfrac{xyz}{y + z + 1}}{\dfrac{xy + xz + x + yz + y + z + 1}{y + z + 1}} \\[1.0em]
        = & \dfrac{xyz(y + z + 1)}{y + z + 1(xy + xz + x + yz + y + z + 1)} \\[1.0em]
        = & \dfrac{xyz}{xy + xz + x + yz + y + z + 1} \\[1.0em]
        = & \dfrac{xyz}{xy + xz + yz + z + x + y + 1} \\[1.0em]
        = & \dfrac{xyz(x + y + 1)}{x + y + 1(xy + xz + yz + z + x + y + 1)} \\[1.0em]
        = & \dfrac{ \dfrac{xyz}{x + y + 1} }{ \dfrac{xy + xz + yz + z + x + y + 1}{x + y + 1} } \\[1.0em]
        = & \dfrac{ \dfrac{xyz}{x + y + 1} }{ \dfrac{xy + z(x + y + 1) + (x + y + 1)}{x + y + 1} } \\[1.0em]
        = & \dfrac{ \left( \dfrac{xy}{x + y + 1} \right) z }{ \left( \dfrac{xy}{x + y + 1} \right) + z + 1 } \\[1.0em]
        = & \left( \dfrac{xy}{x + y + 1} \right) \ast z \\[1.0em]
        = & (x \ast y) \ast z.
    \end{array}
$$
</div>

Moreover, solving $x \ast e$ $=$ $x$, for $e$, means that $x \ast
e$ $=$ $xe$ $/$ $(x$ $+$ $e$ $+$ $1)$ $=$ $x$. Multiplying both
sides with $(x$ $+$ $e$ $+$ $1)$ leads to $xe$ $=$ $x(x$ $+$ $e$
$+$ $1)$ $=$ $x^2$ $+$ $xe$ $+$ $x$, and dividing with $x$ means
that $e$ $=$ $x$ $+$ $e$ $+$ $1$, from where it can be seen that
the equation can not be solved, because $e$ can not be
&ldquo;separated&rdquo; to none of the sides of the equality, so no
identity element exists for the operation $\ast$. Because no
indentity exists, no inverses exist either.
