+++
title  = "Problems 24-28"
layout = "solution-single"
+++

<span class = "exnum">24</span> The linear equation

$$
    \mathbf{Ax} = \begin{bmatrix}
        2 & 3 \\
        4 & 1
    \end{bmatrix} \begin{bmatrix}
        x_1 \\
        x_2
    \end{bmatrix}
    =
    \begin{bmatrix}
         1 \\
        17
    \end{bmatrix}
$$

can be written as augmented matrix

$$
    \left[
        \begin{array}{c c | c}
            2 & 3 &  1 \\
            4 & 1 & 17
        \end{array}
    \right]
$$

that can be brought to upper triangle form by subtracting row one
($R_1$) from row two ($R_2$) twice. In other words,

$$
    \begin{array}{l l}
        \xrightarrow{R_2 - 2R_1}
        &
        \left[
            \begin{array}{c c | c}
                2 &  3 &  1 \\
                0 & -5 & 15
            \end{array}
        \right],
    \end{array}
$$

so

$$
    \mathbf{Ax} = \begin{bmatrix}
        2 &  3 \\
        0 & -5
    \end{bmatrix} \begin{bmatrix}
        x_1 \\
        x_2
    \end{bmatrix}
    =
    \begin{bmatrix}
         1 \\
        15
    \end{bmatrix}
$$

so $x_2$ $=$ $-3$ and $2x_1$ $+$ $3x_2$ $=$ $2x_1$ $+$ $3(-3)$ $=$
$2x_1$ $-$ $9$ $=$ $1$, which shows that $x_1$ $=$ $5$.

<span class = "exnum">25</span> The matrix

$$
    \mathbf{Ab} = \begin{bmatrix}
        1 & 2 & 3 \\
        2 & 3 & 4 \\
        3 & 5 & 7
    \end{bmatrix}
    \begin{bmatrix}
        x \\
        y \\
        z
    \end{bmatrix}
    =
    \begin{bmatrix}
        1 \\
        2 \\
        6
    \end{bmatrix}
$$

has no solution because $\mathbf{A}$ is singular. Row three is a
sum of the first two. But when bottom-right $7$ is changed to $6$,
then the system has solution. This can be shown by solving the
augmented matrix

$$
    \begin{array}{c l}
        \left[
            \begin{array}{c | c}
                \mathbf{A} & \mathbf{b}
            \end{array}
        \right]
        = & \left[
            \begin{array}{c c c | c}
                1 & 2 & 3 & 1 \\
                2 & 3 & 4 & 2 \\
                3 & 5 & 6 & 6
            \end{array}
        \right]
        \\[0.5em] \xrightarrow{R_2 - 2R_1} & \left[
            \begin{array}{c c c | c}
                1 &  2 &  3 & 1 \\
                  & -1 & -2 & 0 \\
                3 &  5 &  6 & 6
            \end{array}
        \right]
        \\[0.5em] \xrightarrow{R_3 - 3R_1} & \left[
            \begin{array}{c c c | c}
                1 &  2 &  3 & 1 \\
                  & -1 & -2 & 0 \\
                  & -1 & -3 & 3
            \end{array}
        \right],
        \\[0.5em] \xrightarrow{R_3 + R_2} & \left[
            \begin{array}{c c c | c}
                1 &  2 &  3 & 1 \\
                  & -1 & -2 & 0 \\
                  &    & -1 & 3
            \end{array}
        \right],
    \end{array}
$$

so $z$ $=$ $-3$, and substituting $z$ back to second row leads to
$-y$ $-$ $2(-3)$ $=$ $-y$ $+$ $6$ $=$ $0$, revealing that $y$ $=$
$6$. Finally solving the first row shows that $x$ $+$ $2y$ $+$
$3z$ $=$ $x$ $+$ $2(6)$ $+$ $3(-3)$ $=$ $x$ $+$ $12$ $-$ $9$ $=$
$x$ $+$ $3$ $=$ $1$, so $x$ $=$ $-2$. Substituting $x$, $y$ and $z$
to $\mathbf{b}$ and taking the product shows that

$$
    \mathbf{Ax} = \begin{bmatrix}
        1 \\
        2 \\
        6
    \end{bmatrix}.
$$
