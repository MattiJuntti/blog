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

<span class = "exnum">26</span> Solving the equations

$$
    \begin{bmatrix}
        1 & 4 \\
        2 & 7
    \end{bmatrix}
    \begin{bmatrix}
        x \\
        y
    \end{bmatrix}
    =
    \begin{bmatrix}
        1 \\
        0
    \end{bmatrix}
    \qquad
    \begin{bmatrix}
        1 & 4 \\
        2 & 7
    \end{bmatrix}
    \begin{bmatrix}
        u \\
        v
    \end{bmatrix}
    =
    \begin{bmatrix}
        0 \\
        1
    \end{bmatrix}
$$

at the same time can be used by solving by using &ldquo;doubly
augmented&rdquo; matrix

$$
    \left[
        \begin{array}{c c | c c}
            1 & 4 & 1 & 0 \\
            2 & 7 & 0 & 1
        \end{array}
    \right].
$$

The solution starts by subtracting the first row from the second
twice. This means that the matrix becomes

$$
    \left[
        \begin{array}{c c | c c}
            1 &  4 &  1 & 0 \\
            0 & -1 & -2 & 1
        \end{array}
    \right].
$$

revealing that $y$ $=$ $2$ and $v$ $=$ $-1$. Substituting $y$ and
$v$ back to the first equations gives two equations:

$$
    \begin{array}{ c l c c l }
          & x + 4y   & \quad &   & u + 4v    \\
        = & x + 4(2) & \quad & = & u + 4(-1) \\
        = & x + 8    & \quad & = & u - 4     \\
        = & 1        & \quad & = & 0
    \end{array}
$$

From these outcomes it can be seen that $x$ $=$ $-7$ and $u$ $=$
$4$.

<span class = "exnum">27</span> If augmented matrix is

$$
    \left[
        \begin{array}{ c c c c }
            1 & 2 & 3 & a \\
            0 & 4 & 5 & b \\
            0 & 0 & d & c
        \end{array}
    \right],
$$

then **(a)** if $d$ $=$ $0$ anc $c$ $\neq$ $0$, the matrix of the
augmented matrix does not have solutions. **(b)** If the $c$
something else than zero, the matrix has infinitely many solutions.

<span class = "exnum">28</span> Since $\mathbf{AB}$ $=$
$\mathbf{I}$ and $\mathbf{BC}$ $=$ $\mathbf{I}$, then $\mathbf{A}$
$=$ $\mathbf{AI}$ $=$ $\mathbf{A}(\mathbf{BC})$ $=$
$(\mathbf{AB})\mathbf{C}$ $=$ $\mathbf{IC}$ $=$ $\mathbf{C}$.
