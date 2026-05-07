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
$c$, shows that $2m$ $+$ $1$ $=$ $5$, so $m$ $=$ $2$. In matrix
speak the product

$$
    \begin{array}{r c l}
        \begin{bmatrix}
            1            & 0 \\
            -\frac{3}{2} & 1 \\
        \end{bmatrix}
        \left[
            \begin{array}{c c | c}
                2 & 5 & m \\
                3 & 7 & c \\
            \end{array}
        \right]
        & = &
        \left[
            \begin{array}{c c | c}
                2(1)            + 3(0) & 5(1)            + 7(0) & m(1)            + c(0) \\
                2(-\frac{3}{2}) + 3(1) & 5(-\frac{3}{2}) + 7(1) & m(-\frac{3}{2}) + c(1) \\
            \end{array}
        \right]
        \\[1em] & = &
        \left[
            \begin{array}{c c | c}
                5 & 12            & m                  \\
                0 & - \frac{1}{2} & -\frac{3}{2} m + c \\
            \end{array}
        \right]
    \end{array}
$$
