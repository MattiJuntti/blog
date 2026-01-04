+++
title  = "Problems 21-28"
date   = 2025-01-01T00:00:00+03:00
layout = "solution-single"
+++

<span class = "exnum">21</span> The left hand-side matrix is

$$
    \ \phantom{,}
        \begin{bmatrix}
            2x & + &  y &   &    &   &    \\
             x & + & 2y & + &  z &   &    \\
               &   &  y & + & 2z & + &  t \\
               &   &    &   &  z & + & 2t 
        \end{bmatrix}
    =
        \begin{bmatrix}
            0 \\
            0 \\
            0 \\
            5
        \end{bmatrix}
    \ ,
$$

so the first pivot is $\frac{l_{21}}{l_{11}} = \frac{1}{2}$. Multiplying
the first row by the pivot and subtracting the given product from the
second row leads to matrix

$$
    \phantom{.}
        \begin{bmatrix}
            2x & + & y            &   &    &   &    \\
               &   & \frac{3}{2}y & + & z  &   &    \\
               &   & y            & + & 2z & + & t  \\
               &   &              &   & z  & + & 2t
        \end{bmatrix}
    =
        \begin{bmatrix}
            0 \\
            0 \\
            0 \\
            5
        \end{bmatrix}
    \ .
$$

The next pivot is $\frac{2}{3}$, so subtracting the second row multiplied
by the pivot from the third row results in matrix

$$
    \phantom{.}
        \begin{bmatrix}
            2x & + & y            &   &              &   &    \\
               &   & \frac{3}{2}y & + & z            &   &    \\
               &   &              &   & \frac{4}{3}z & + & t  \\
               &   &              &   & z            & + & 2t
        \end{bmatrix}
    =
        \begin{bmatrix}
            0 \\
            0 \\
            0 \\
            5
        \end{bmatrix}
    \ .
$$

The last pivot is $\frac{3}{4}$ and continuing the elimination, that is,
subtracting the third row multiplied by the pivot from the fourth is

$$
    \phantom{.}
        \begin{bmatrix}
            2x & + & y            &   &              &   &              \\
               &   & \frac{3}{2}y & + & z            &   &              \\
               &   &              &   & \frac{4}{3}z & + & t            \\
               &   &              &   &              &   & \frac{5}{4}t
        \end{bmatrix}
    =
        \begin{bmatrix}
            0 \\
            0 \\
            0 \\
            5
        \end{bmatrix}
    \ .
$$

from where it can be seen that

$$
    \begin{array}{l c r c r}
        t & = &  5 \left( \dfrac{4}{5} \right) & = &  4 \ , \\[0.5em]
        z & = & -4 \left( \dfrac{3}{4} \right) & = & -3 \ , \\[0.5em]
        y & = &  3 \left( \dfrac{2}{3} \right) & = &  2 \ \phantom{,}
    \end{array}
$$

and

$$
    \begin{array}{l c r c r}
        x & = & -2 \left( \dfrac{1}{2} \right) & = & -1 \ .
    \end{array}
$$

The first pivot of the right hand-side equation $\frac{l_{21}}{l_{11}}$ $=$
$-\frac{1}{2}$, so multiplying the first row by the pivot and subtracting
the row from the second means that

$$
    \ \phantom{,}
        \begin{bmatrix}
            2x & - & y            &   &    &   & \\
               & - & \frac{3}{2}y & + & z  &   & \\
               & - & y            & + & 2z & + & t \\
               &   &              & - & z  & + & 2t
        \end{bmatrix}
    =
        \begin{bmatrix}
            0 \\
            0 \\
            0 \\
            5
        \end{bmatrix}
    \ .
$$

The second pivot is $\frac{l_{32}}{l_{22}}$ $=$ $\frac{-1}{-(3/2)}$ $=$
$\frac{2}{3}$. Multiplying the second row with the second pivot and
subtracting the row from the third leads to

$$
    \ \phantom{,}
        \begin{bmatrix}
            2x & - & y            &   &              &   &   \\
               & - & \frac{3}{2}y & + & z            &   &   \\
               &   &              &   & \frac{4}{3}z & + & t \\
               &   &              & - & z            & + & 2t
        \end{bmatrix}
    =
        \begin{bmatrix}
            0 \\
            0 \\
            0 \\
            5
        \end{bmatrix}
    \ .
$$

The last, i.e. the third pivot is $\frac{l_{43}}{l_{33}}$ $=$
$-\frac{1}{4/3}$ $=$ $-\frac{3}{4}$, so after multiplying the third row
with the pivot and subtracting this product from the fourth row, the system
of equations becomes

$$
    \phantom{.}
        \begin{bmatrix}
            2x & - & y            &   &              &   &   \\
               & - & \frac{3}{2}y & + & z            &   &   \\
               &   &              &   & \frac{4}{3}z & + & t \\
               &   &              &   &              & - & \frac{5}{4}t
        \end{bmatrix}
    =
        \begin{bmatrix}
            0 \\
            0 \\
            0 \\
            5
        \end{bmatrix}
    \ .
$$

As with the left hand-side, applying the back substitution means that

$$
    \begin{array}{l c r c r}
        t & = & 5 \left( -\dfrac{4}{5} \right) & = & -4 \ , \\[0.5em]
        z & = & -4 \left( \dfrac{3}{4} \right) & = & -3 \ , \\[0.5em]
        y & = & -3 \left( \dfrac{2}{3} \right) & = & -2 \ \phantom{,}
    \end{array}
$$

and

$$
    \begin{array}{l c r c r}
        x & = & -2 \left( \dfrac{1}{2} \right) & = & -1 \ .
    \end{array}
$$

<span class = "exnum">22</span>

--

<span class = "exnum">23</span> If the system of equation leads to

$$
    \phantom{,} \
        \left\{ \
            \begin{array}{r r r r r}
                x & + &  y & = & 1 \\
                  &   & 2y & = & 3
            \end{array}
        \ \right.
    \ ,
$$

then the original system of equations could've been

$$
    \phantom{,} \
        \left\{ \
            \begin{array}{r r r r r}
                x & + &  y & = & 1 \\
               2x & + & 4y & = & 5
            \end{array}
        \ \right.
    \ ,
$$

because subtracting the first row multiplied by the pivot this setup gives,
leads to the system of equations defined in the problem statement.

A original system of equations could have been also 

$$
    \phantom{,} \
        \left\{ \
            \begin{array}{r r r r r}
                x & + &  y & = & 1 \\
               0x & + & 2y & = & 3
            \end{array}
        \ \right.
    \ ,
$$

because it leads to the given system of equations. In this form no
elimination is needed.

Lastly, the original system of equations could have been

$$
    \phantom{,} \
        \left\{ \
            \begin{array}{r r r r r}
                x & + &  y & = & 1 \\
                x & + & 3y & = & 4
            \end{array}
        \ \right.
    \ ,
$$

because after finding out the pivot, multiplying the second row with it and
subtracting the product leads the given systems of equations.

<span class = "exnum">24</span> When $a = 2$ or $a = 0$, the elimination
leads to failure with infinitely many solutions because these numbers lead
to zeros in the pivot values.

<span class = "exnum">25 &ndash; 26</span> Any number $a \in \mathbb{R}$ means that
for matrix

$$
    A = \left[ \
        \begin{array}{c c c}
            a & 2 & 3 \\
            a & a & 4 \\
            a & a & a
        \end{array}
    \ \right]
$$

leads to zeros in the pivots ($a - a = 0$) and into situation where the
elimination fails with permanent failure with no solution.

<span class = "exnum">27</span> Solving the system of equations

$$
    \left\{ \ \
        \begin{array}{ c c c c c c }
            3x &   &    &   &   & = & 3 \\
            6x & + & 2y &   &   & = & 8 \\
            9x & - & 2y & + & z & = & 9
        \end{array}
    \right.
$$

by the suggested <i>forward susbstitution</i>, means that starting from the
first row, on can see that $x = 1$. Substituting $x$ to the second equation
means that $2y + 6 = 8$ so $y = 1$. Substituting $x$ and $y$ to the third
equation leads to $9 - 2 + z = 9$, so $z = 2$. Substituting $x$, $y$ and
$z$ to the given equation shows that forward substitution yielded right
answers.

<span class = "exnum">28</span> Let matrix

$$
    \phantom{.} \
        \mathbf{A} = \left[ \
            \begin{array}{c c c}
                a & b \\
                c & d
            \end{array}
        \ \right]
    \ .
$$

The transpose of $\mathbf{A}$ is

$$
    \phantom{.} \
        \mathbf{A}^\top = \left[ \
            \begin{array}{c c c}
                a & c \\
                b & d
            \end{array}
        \ \right]
    \ .
$$

Multiplying $\mathbf{A}^\top$ with partial identity matrix

$$
    \mathbf{P} = \left[ \
        \begin{array}{c c c}
            0 & 0 \\
            0 & 1
        \end{array}
    \ \right]
$$

means that

$$
    \phantom{.} \
        \mathbf{A}^\top \mathbf{P}
        = \left[ \
            \begin{array}{c c c}
                a & c \\
                b & d
            \end{array}
        \ \right]
        \left[ \
            \begin{array}{c c c}
                0 & 0 \\
                0 & 1
            \end{array}
        \ \right]
        =
        \left[ \
            \begin{array}{c c c}
                0 & c \\
                0 & d
            \end{array}
        \ \right]
    \ ,
$$

so 

$$
    \phantom{,} \
        (\mathbf{A}^\top \mathbf{P})^\top
        =
        \left[ \
            \begin{array}{c c c}
                0 & 0 \\
                c & d
            \end{array}
        \ \right]
    \ .
$$

Multiplying this transpose with exchange matrix

$$
    \mathbf{E}
    =
    \left[ \
        \begin{array}{c c c}
            0 & 1 \\
            1 & 0
        \end{array}
    \ \right]
$$

leads to

$$
    \phantom{,} \
        \mathbf{E}(\mathbf{A}^\top \mathbf{P})^\top
        =
        \left[ \
            \begin{array}{c c c}
                c & d \\
                0 & 0
            \end{array}
        \ \right]
    \ ,
$$

which can be multiplied with $-3$ to get a subtraction expression that
subtracts $\mathbf{A}$'s second row three times subtracted from
$\mathbf{A}$, that is,

<div class = "widescreen">
$$
    \phantom{,} \
        \mathbf{A} -3\mathbf{E} (\mathbf{A}^\top \mathbf{P})^\top
        =
        \left[ \
            \begin{array}{c c c}
                 a & b \\
                 c & d
            \end{array}
        \ \right]
        -
        \left[ \
            \begin{array}{c c c}
                3c & 3d \\
                 0 &  0
            \end{array}
        \ \right]
        =
        \left[ \
            \begin{array}{c c c}
                a - 3c & b - 3d \\
                c      & d
            \end{array}
        \ \right]
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
        & & \mathbf{A} -3\mathbf{E} (\mathbf{A}^\top \mathbf{P})^\top
        \\[1em] & = &
        \left[ \
            \begin{array}{c c c}
                 a & b \\
                 c & d
            \end{array}
        \ \right]
        -
        \left[ \
            \begin{array}{c c c}
                3c & 3d \\
                 0 &  0
            \end{array}
        \ \right]
        \\[1em] & = &
        \left[ \
            \begin{array}{c c c}
                a - 3c & b - 3d \\
                c      & d
            \end{array}
        \ \right]
    \end{array}
$$
</div>

Encoding the subtraction expression into a simple MATLAB expression could
be done by writing a

```MATLAB {class = listing}
function result = subtract_second_row_thrice(A)
    result = A - (3 * E * (A' * P)');
end
```

which is enough to solve the given problem.
