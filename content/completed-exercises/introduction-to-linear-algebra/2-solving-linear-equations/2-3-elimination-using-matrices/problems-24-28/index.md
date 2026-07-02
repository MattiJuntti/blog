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
