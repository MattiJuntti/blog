+++
title  = "Problems 16-23"
layout = "solution-single"
+++

<span class = "exnum">16</span> **(a)** If $X$ is twice as old as
$Y$ and their ages add to $33$, then

$$
    X + Y = 2Y + Y = 33.
$$

The equation can be expressed as linear system

$$
    \mathbf{Ab}
    =
    \begin{bmatrix}
        2 & 1 \\
        0 & 0 \\
    \end{bmatrix}
    \begin{bmatrix}
        Y \\ Y
    \end{bmatrix}
    =
    \begin{bmatrix}
        3Y \\ 0
    \end{bmatrix}
    =
    \begin{bmatrix}
        33 \\ 0
    \end{bmatrix}
    =
    \mathbf{b}.
$$

The first component of $\mathbf{Ab}$ is $3Y$ $=$ $33$, so $Y$ $=$
$11$. Substituting this back to the original equation means that

$$
    X + 11 = 33,
$$

so $X$ $=$ $22$.

**(b)** When $(x,y)$ $=$ $(2,5)$ or $(3,7)$ and the slope-intersect
form of a line is the well known $y$ $=$ $mx$ $+$ $c$, a linear
equation represented as

$$
    \left[
        \begin{array}{c c | c}
            2 & 5 & m \\
            3 & 7 & c \\
        \end{array}
    \right]
    \Longleftrightarrow
    \left\{
        \begin{array}{l}
            5 = 2m + c \\
            7 = 3m + c.
        \end{array}
    \right.
$$

Subtracting first row $\frac{3}{2}$ times from the second leads to

$$
        \left\{
            \begin{array}{l l l}
                5                  & = & 2m + c                                    \\
                7 - \frac{3}{2}(5) & = & 3m - \frac{3}{2}(3m) + c - \frac{3}{2}(c) \\
            \end{array}
        \right.
        \ = \
        \left\{
            \begin{array}{l l l}
                5             & = & 2m + c          \\
                - \frac{1}{2} & = & -\frac{1}{2}(c) \\
            \end{array}
        \right. \quad ,
$$

so $c$ $=$ $1$ and subsituting it back to, say, $5$ $=$ $2m$ $+$
$c$, shows that $2m$ $+$ $1$ $=$ $5$, so $m$ $=$ $2$.

<span class = "exnum">17</span> When parabola $y$ $=$ $a$ $+$ $bx$
$+$ $cx^2$ goes through points $(1,4)$, $(2,8)$, $(3,14)$ and a
given unknown solution is $(a,b,c)$, the problem can be modeled as
a system of linear functions

<div class = "widescreen">
$$
\begin{array}{r c l}
    \left\{
        \begin{array}{r c r}
            a & + &  b & + &  c^2 & = & 4  \\
            a & + & 2b & + & 2c^2 & = & 8  \\
            a & + & 3b & + & 3c^2 & = & 14 \\
        \end{array}
    \right.
    & \Longleftrightarrow &
    \begin{bmatrix}
        1 & 1 & 1 \\
        1 & 2 & 4 \\
        1 & 3 & 9 \\
    \end{bmatrix}
    \begin{bmatrix}
        a \\
        b \\
        c \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        4 \\
        8 \\
       14 \\
    \end{bmatrix}
    \\[0.5em] & \Longleftrightarrow &
    \left[
        \begin{array}{c c c | c}
            1 & 1 & 1 &  4 \\
            1 & 2 & 4 &  8 \\
            1 & 3 & 9 & 14 \\
        \end{array}
    \right]
    .
\end{array}
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{c}
    \left\{
        \begin{array}{r c r}
            a & + &  b & + &  c & = & 4  \\
            a & + & 2b & + & 4c & = & 8  \\
            a & + & 3b & + & 9c & = & 14 \\
        \end{array}
    \right.
    \\[1em] \Big\Updownarrow \\[1em]
    \begin{bmatrix}
        1 & 1 & 1 \\
        1 & 2 & 4 \\
        1 & 3 & 9 \\
    \end{bmatrix}
    \begin{bmatrix}
        a \\
        b \\
        c \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        4 \\
        8 \\
       14 \\
    \end{bmatrix}
    \\[1em] \Big\Updownarrow \\[1em]
    \left[
        \begin{array}{c c c | c}
            1 & 1 & 1 &  4 \\
            1 & 2 & 4 &  8 \\
            1 & 3 & 9 & 14 \\
        \end{array}
    \right]
    .
\end{array}
$$
</div>

and then just applying elimination operations

$$
\begin{array}{c c}
    \xrightarrow{\mathbf{E}_{31} \cdot} &
    \left[
        \begin{array}{c c c | c}
            1 & 3 & 9 & 14 \\
            1 & 2 & 4 &  8 \\
            1 & 1 & 1 &  4 \\
        \end{array}
    \right]
    \\[1em] \xrightarrow{2_3 - R_1} &
    \left[
        \begin{array}{c c c | c}
            1 &  3 &  9 & 14 \\
            0 & -1 & -5 & -6 \\
            1 &  1 &  1 &  4 \\
        \end{array}
    \right]
    \\[1em] \xrightarrow{R_3 - R_1} &
    \left[
        \begin{array}{c c c | c}
            1 &  3 &  9 &  14 \\
            0 & -1 & -5 &  -6 \\
            0 & -2 & -8 & -10 \\
        \end{array}
    \right]
    \\[1em] \xrightarrow{R_3 + 2R_2} &
    \ \phantom{.}
    \left[
        \begin{array}{c c c | c}
            1 &  3 &  9 &  14 \\
            0 & -1 & -5 &  -6 \\
            0 &  0 &  2 &   2 \\
        \end{array}
    \right]
    \ .
\end{array}
$$

Third row shows that $2c$ $=$ $2$, so $c$ $=$ $1$. Substituting $c$
back to second row, leads to $-b$ $-$ $5c$ $=$ $-$ $b$ $-$ $5$ =
$-6$, so multiplying with $-1$ and subtracting $5$, shows that $b$
$=$ $1$. Substuting $b$ and $c$ to first row shows that, $a$ $+$
$3b$ $+$ $9c$ $=$ $a$ $+$ $3$ $+$ $9$ $=$ $a$ $+$ $12$ $=$ $14$, so
$a$ $=$ $2$.

Substituting $a$ $=$ $2$, $b$ $=$ $1$ and $c$ $=$ $1$ to the first
matrix equation and evaluating the product shows that

$$
    \begin{bmatrix}
        1 & 1 & 1 \\
        1 & 2 & 4 \\
        1 & 3 & 9 \\
    \end{bmatrix}
    \begin{bmatrix}
        2 \\
        1 \\
        1 \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        2(1) + 1(1) + 1(1) \\
        2(1) + 1(2) + 1(4) \\
        2(1) + 1(3) + 1(9) \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        4 \\
        8 \\
        14 \\
    \end{bmatrix}
$$

as was to be exptected.
