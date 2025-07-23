+++
title  = "Problems 1-10"
layout = "solution-single"
+++

<span class = "exnum">1</span> Given the two equations

$$
    \phantom{,} \quad
        \left\{
            \begin{array}{r r r}
                2x  & + & 3y & = &  1 \\
                10x & + & 9y & = & 11
            \end{array}
        \right.
    \quad ,
$$

a multiple of $\frac{l_{21}}{l_{11}}$ $=$ $\frac{10}{2}$ $=$ $5$ of the
first row needs to be subtracted from the second row to eliminate $x$ in
that row.

In other words

<div class = "widescreen">
$$
    \begin{array}{c l}
          & \left\{ \
            \begin{array}{l c l}
                2x        & + & 3y       & = & 1 \\
                10x - 10x & + & 9y - 15y & = & 11 - 5
            \end{array}
        \right. & = & \left\{ \
            \begin{array}{l c l}
                \mathbf{2}x & + & 3y          & = & 1 \\
                            & - & \mathbf{6}y & = & 6
            \end{array}
        \right. \quad ,
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
        & \left\{ \
            \begin{array}{l c l}
                2x        & + & 3y       & = & 1 \\
                10x - 10x & + & 9y - 15y & = & 11 - 5
            \end{array}
        \right. \\[1em] = & \left\{ \
            \begin{array}{l c l}
                \mathbf{2}x & + & 3y          & = & 1 \\
                            & - & \mathbf{4}y & = & 6
            \end{array}
        \right. \quad ,
    \end{array}
$$
</div>

where the pivots are boldened.

Now, solving $y$ for in the equation of the second row, shows that:

$$
    \begin{array}{r c c c c | l}
        -6y & = & 6            &   &    & (\div -6) \\
          y & = & -\frac{6}{6} & = & -1 &
    \end{array}
$$

Substituting $\frac{3}{2}$ to $y$ in the first row of the original equation
leads to

$$
    2x + 3 \left( -1 \right) = 2x - 3 = 1,
$$

so

$$
    x = 2.
$$

Now, substituting $x$ and $y$ into the first equation shows that

$$
    2(2) + 3(-1) = 4 - 3 = 1.
$$

<span class = "exnum">2</span> Given the original system of equations in
<span class = "exnum">1</span>, letting the equations equal to $(4,44)$ the
system of equations becomes

$$
    \phantom{,} \quad
        \left\{
            \begin{array}{r c l}
                2x  & + & 3y & = & 4  \\
                10x & + & 9y & = & 44
            \end{array}
        \right.
    \quad ,
$$

and subtracting the first row five times from the second leads to

$$
    \phantom{,} \quad
        \left\{
            \begin{array}{r c l}
                2x  & + & 3y & = & 4  \\
                    & - & 6y & = & 24
            \end{array}
        \right.
    \quad,
$$

so $y = - 4$.

Substituting this to $y$ of the first equation allows for solving $x$, that
is,

$$
    2x + 3(-4) = 2x - 12 = 4,
$$

so

$$
    x = 8,
$$

and

$$
    2(8) + 3(-4) = 16 - 12 = 4.
$$

The pair $(x,y)$ $=$ $(8,4)$ is a multiple of four of the exercise <span
class = "exnum">1</span>'s $(x,y)$ $=$ $(2,1)$, which means that, when
considered as a vector, both solutions lie on a same line.

<span class = "exnum">3</span> When the system of equations is

$$
    \left\{ \
        \begin{array}{ c c c c c }
            2x & - & 4y & = & 6 \\ 
            -x & + & 5y & = & 0
        \end{array}
    \right.
$$

The multiplier of the first equation is

$$
    \phantom{.} \dfrac{l_{21}}{l_{11}} = -\dfrac{1}{2} \ ,
$$

so multiplying the second equation with the multiplier means that

$$
    \begin{array}{ c c c c c c }
                        & -\dfrac{1}{2}(2x) & + & \dfrac{1}{2}(4y) & = & -\dfrac{1}{2}(6) \\
        \Longrightarrow & -x & + & 2y & = & -3.
    \end{array}
$$

Now subtracting the new form of the equation from the second means
multplying the first equation by $-1$ and adding it to the second, that is,

$$
    \phantom{,} \ -x + x + 5y - 2y = 3y = 3 = 0 + 3 \ ,
$$

so $y = -1$ and the upper triangular form of the equation is

$$
    \left\{ \
        \begin{array}{ c c c c c }
            2x & - & 4y & = & 6 \\ 
               &   &  y & = & 1
        \end{array}
    \right. \ .
$$

Substituting $y = 1$ to the first equation, i.e. applying the
backsubstitution part of solving a system of equations, shows that

$$
    2x - 4(1) = 2x - 4 = 6 \tag{1}
$$

so solving for $x$ shows that $x = 5$.

Testing out the solution vector $(5,1)$, say, with the first equations
shows that

$$
    2(5) - 4(1) = 6
$$

that is equal to the right handside of the first equation of the system
under inspection.

Changing the $6$ to $-6$ in the first equation, and solving for $x$ in
$(1)$ means that

$$
    2x - 4(1) = 2x - 4 = -6, 
$$

so $x = -1$, and the solution vector becomes $(-1,1)$. Testing out the
first equation with the vector shows that

$$
    2(-1) - 4(1) = -6.
$$

<span class = "exnum">4</span> Given the set of equations

...

<span class = "exnum">5</span>

When the right side of the unknown value in given system of equations is
$20$, the bottom row is a multiple of $2$ of the upper row, so the system
becomes singular and so has infinitely many solutions.

To show this, it is sufficient to show that subtracting this multiple of
the top row from the bottom row leads to

$$
    \phantom{,} \ 0y = 0 \ ,
$$

as is discussed in the page $48$ of the book. With any other number the end
results will always be

$$
    \phantom{,} \ 0y = c \ , \quad c \neq 20,
$$

that is, there there will never be any solutions to the system due to $0y$,
as is also discussed in the same page.

<span class = "exnum">6</span> If $b$ is equal to $3$m, then this leads to
singular system if $g$ is equal to $8$, because the second row is just a
multiple of $2$ of the first row. This makes $g$ equal to 32.

Now subtracting the multiple of $\frac{l_{21}}{l_{11}}$ $=$ $\frac{4}{2}$ $=$
$2$ of the first row from the second, leads to

$$
    \phantom{.} \quad
        \left\{ \
            \begin{array}{c c c c c}
                2x & + & 4y & = & 16 \\
                   &   & 0y & = &  0
            \end{array}
        \ \right.
    \quad .
$$

so the system becomes singular with infinitely many solutions.

<span class = "exnum">8</span> When $k = 1$ the multiplier is $3$ and the
system leads to $0y = -12$ so the system end up in a permanent failure with
no solutions.

When $k = 0$, trying the solve the system leads to 

$$
    \phantom{.} \quad
        \left\{ \
            \begin{array}{c c c c c}
                0x & + & 3y & = & \phantom{-}6 \\
                3x & + & 0y & = &           -6
            \end{array}
        \ \right.
    \quad ,
$$

that is, division by zero, but exchanging the first row with second is

$$
    \phantom{.} \quad
        \left\{ \
            \begin{array}{c c c c c}
                3x & + & 0y & = &           -6 \\
                0x & + & 3y & = & \phantom{-}6
            \end{array}
        \ \right.
    \quad ,
$$

and the system becomes solvable: $y = 2$ and $x = -2$.

When $k = -1$ the multiplier is $-\frac{1}{3}$, so multiplying the first
row with this multiplier is

$$
    \phantom{,} \ -\dfrac{1}{3}(3x) + \dfrac{1}{3}(3y) = -\dfrac{1}{3}6 \ ,
$$

which means that

$$
    \phantom{.} \ -x + y = -2 \ \ .
$$

Subtracting this form the second equation leads to

$$
    \phantom{.} \quad
        \left\{ \
            \begin{array}{c c r c c}
                -x & + & 3y & = & 6 \\
                   &   &  y & = & 4
            \end{array}
        \ \right.
    \quad .
$$

Solving for $x$ by substituting $y$ into the first row means that $x = 6$.

<span class = "exnum">9</span> The second row is the first row multiplied
by $2$, so $b_2 = 2b_1$. That is the system of equations can be written as

$$
    \begin{array}{c l}
        & \left\{
            \begin{array}{ c c c c c }
                3x & - & 2y & = & b_1 \\
                6x & - & 4y & = & b_2
            \end{array}
        \right. \\[1em] = & \left\{
            \begin{array}{ c c c c r }
                3x & - & 2y & = & b_1 \\
                6x & - & 4y & = & 2b_1
            \end{array}
        \right.
    \end{array}
$$

from where it can be seen that the system has multiple solutions.

<span class = "exnum">10</span> 

...
