+++
title  = "Problems 1-16"
layout = "solution-single"
+++

<span class = "exnum">1</span> If $\mathbf{A}$ is a $3\times5$,
$\mathbf{B}$ a $5\times3$, $\mathbf{C}$ a $5\times1$ and
$\mathbf{D}$ a $3\times1$ matrices with all entries being $1$ and
if matrix multiplication is allowed if and and only if number of
columns of the left handside matrix is equal to the number of rows
of the right handside matrix. In other words, only a matrix
multiplication $\mathbf{A}_{n \times k}\mathbf{B}_{k \times m}$ is
allowed, where $n$, $m$ and $k$ numbers of rows and columns.
Therefore; $\mathbf{B} \mathbf{A}$ $=$ $\mathbf{B}_{5 \times 3}$
$\cdot$ $\mathbf{A}_{3 \times 5}$ is allowed, $\mathbf{A}
\mathbf{B}$ $=$ $\mathbf{A}_{3 \times 5}$ $\cdot$ $\mathbf{B}_{5
\times 3}$ is allowed, $\mathbf{A} \mathbf{B} \mathbf{D}$ $=$
$\mathbf{A}_{3 \times 5}$ $\cdot$ $\mathbf{B}_{5 \times 3}$ $\cdot$
$\mathbf{D}_{3 \times 1}$ is allowed, $\mathbf{D} \mathbf{C}$ $=$
$\mathbf{D}_{3 \times 1}$ $\cdot$ $\mathbf{C}_{5 \times 1}$ is not
allowed because operand dimensions don't match, and $\mathbf{A}
(\mathbf{B} + \mathbf{C})$ $=$ $\mathbf{A}_{3 \times 5}$ $\cdot$
$(\mathbf{B}_{5 \times 3}$ $+$ $\mathbf{C}_{5 \times 1})$ is not
allowed because dimensions of $\mathbf{B}$ and $\mathbf{C}$ don't
match.

<span class = "exnum">2</span> Given some matrices $\mathbf{A}$ and
$\mathbf{B}$ **(a)** the second column of product $\mathbf{A}
\mathbf{B}$ is $\mathbf{Ab}_2$, where $\mathbf{b}_2$ is third
column of $\mathbf{B}$, **(b)** the first row of $\mathbf{AB}$ is
$\mathbf{a}_{1m}\mathbf{B}$, **(c)** the entry in row $3$, column
$5$ of $\mathbf{AB}$ is $\mathbf{a}_{3m} \cdot \mathbf{b}_{n5}$ and
**(d)** the entry in row $1$, column $1$ of $\mathbf{CDE}$ $=$
$\mathbf{E}_{1k} \cdot \mathbf{d}_{kk} \cdot \mathbf{e}_{k1}$.

<span class = "exnum">3</span> If

<div class = "widescreen">
$$
    \mathbf{A} = \begin{bmatrix}
        1 & 5 \\
        2 & 3
    \end{bmatrix}
, \quad
    \mathbf{B} = \begin{bmatrix}
        0 & 2 \\
        0 & 1
    \end{bmatrix}
, \quad
    \mathbf{C} = \begin{bmatrix}
        3 & 1 \\
        0 & 0
    \end{bmatrix}
,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c}
        \mathbf{A} = \begin{bmatrix}
            1 & 5 \\
            2 & 3
        \end{bmatrix},
    \\[1.0em]
        \mathbf{B} = \begin{bmatrix}
            0 & 2 \\
            0 & 1
        \end{bmatrix},
    \\[1.0em]
        \mathbf{C} = \begin{bmatrix}
            3 & 1 \\
            0 & 0
        \end{bmatrix},
    \end{array}
$$
</div>

then

$$
    \mathbf{AB} = \begin{bmatrix}
        1(0) + 5(0) & 2(1) + 1(5) \\
        2(0) + 3(0) & 2(2) + 1(3)
    \end{bmatrix}
    =
    \begin{bmatrix}
        0 & 7 \\
        0 & 7
    \end{bmatrix}
$$

and

$$
    \mathbf{AC} = \begin{bmatrix}
        1(3) + 5(0) & 1(1) + 1(0) \\
        2(3) + 3(0) & 2(1) + 1(0)
    \end{bmatrix}
    =
    \begin{bmatrix}
        3 & 1 \\
        6 & 2
    \end{bmatrix}
$$

so

$$
    \begin{array}{r c l}
        \mathbf{AB} + \mathbf{AC} & = & \begin{bmatrix}
            0 + 3 & 7 + 1 \\
            0 + 6 & 7 + 2
        \end{bmatrix}
        \\[0.5em] & = &
        \begin{bmatrix}
            3 & 8 \\
            6 & 9
        \end{bmatrix}
    \end{array}
$$

and

<div class = "widescreen">
$$
    \begin{array}{r c l}
        \mathbf{A}(\mathbf{B} + \mathbf{C})
    & = &
        \mathbf{A}\begin{bmatrix}
            0 + 3 & 2 + 1 \\
            0 + 0 & 1 + 0
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            1 & 5 \\
            2 & 3
        \end{bmatrix}
        \begin{bmatrix}
            3 & 3 \\
            0 & 1
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            1(3) + 5(0) & 1(3) + 5(1) \\
            2(3) + 3(0) & 2(3) + 3(1)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            3 & 8 \\
            6 & 9
        \end{bmatrix},
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
              &   &
        \mathbf{A}(\mathbf{B} + \mathbf{C})
    \\[0.5em] & = &
        \mathbf{A}\begin{bmatrix}
            0 + 3 & 2 + 1 \\
            0 + 0 & 1 + 0
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            1 & 5 \\
            2 & 3
        \end{bmatrix}
        \begin{bmatrix}
            3 & 3 \\
            0 & 1
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            1(3) + 5(0) & 1(3) + 5(1) \\
            2(3) + 3(0) & 2(3) + 3(1)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            3 & 8 \\
            6 & 9
        \end{bmatrix},
    \end{array}
$$
</div>

which means that for the given matrices $\mathbf{A}$, $\mathbf{B}$
and $\mathbf{C}$, $\mathbf{AB} + \mathbf{AC}$ $=$
$\mathbf{A}(\mathbf{B} + \mathbf{C})$.

<span class = "exnum">4</span> Continuing with the previous
exercises matrices

<div class = "widescreen">
$$
    \begin{array}{r c l}
        \mathbf{A}(\mathbf{BC})
            & = &
                \begin{bmatrix}
                    1 & 5 \\
                    2 & 3
                \end{bmatrix}
                \begin{bmatrix}
                    0(3) + 2(0) & 1(0) + 0(2) \\
                    0(3) + 1(0) & 1(0) + 0(1)
                \end{bmatrix}
            \\[0.5em] & = &
                \begin{bmatrix}
                    1 & 5 \\
                    2 & 3
                \end{bmatrix}
                \begin{bmatrix}
                    0 & 0 \\
                    0 & 0
                \end{bmatrix}
            \\[0.5em] & = &
                \begin{bmatrix}
                    0 & 0 \\
                    0 & 0
                \end{bmatrix}
            \\[0.5em] & = &
            \begin{bmatrix}
                0(3) + 7(0) & 0(1) + 7(0) \\
                0(3) + 7(0) & 0(1) + 7(0) \\
            \end{bmatrix}
            \\[0.5em] & = &
            \begin{bmatrix}
                0 & 7 \\
                0 & 7
            \end{bmatrix}
            \begin{bmatrix}
                3 & 1 \\
                0 & 0 
            \end{bmatrix}
            \\[0.5em] & = &
            (\mathbf{AB})\mathbf{C}.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
            & &
            \mathbf{A}(\mathbf{BC})
            \\[0.5em] & = & \begin{bmatrix}
                1 & 5 \\
                2 & 3
            \end{bmatrix}
            \begin{bmatrix}
                0(3) + 2(0) & 1(0) + 0(2) \\
                0(3) + 1(0) & 1(0) + 0(1)
            \end{bmatrix}
            \\[0.5em] & = &
                \begin{bmatrix}
                    1 & 5 \\
                    2 & 3
                \end{bmatrix}
                \begin{bmatrix}
                    0 & 0 \\
                    0 & 0
                \end{bmatrix}
            \\[0.5em] & = &
                \begin{bmatrix} 0 & 0 \\
                    0 & 0
                \end{bmatrix}
            \\[0.5em] & = &
                \begin{bmatrix}
                    0(3) + 7(0) & 0(1) + 7(0) \\
                    0(3) + 7(0) & 0(1) + 7(0) \\
                \end{bmatrix}
            \\[0.5em] & = &
                \begin{bmatrix}
                    0 & 7 \\
                    0 & 7
                \end{bmatrix}
                \begin{bmatrix}
                    3 & 1 \\
                    0 & 0 
                \end{bmatrix}
            \\[0.5em] & = &
                (\mathbf{AB})\mathbf{C}.
    \end{array}
$$
</div>

<span class = "exnum">5</span> When

$$
    \mathbf{A} = \begin{bmatrix}
        1 & b \\
        0 & 1
    \end{bmatrix}
$$

and when

$$
    \mathbf{A} = \begin{bmatrix}
        2 & 2 \\
        0 & 0
    \end{bmatrix},
$$

the product

<div class = "widescreen">
$$
    \begin{array}{r c l}
            \mathbf{A}^3
        & = &
            (\mathbf{A}^2)\mathbf{A}
        \\[0.5em] & = &
            (\mathbf{AA})\mathbf{A}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    1 & b \\
                    0 & 1
                \end{bmatrix}
                \begin{bmatrix}
                    1 & b \\
                    0 & 1
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                1 & b \\
                0 & 1
            \end{bmatrix}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    1(1) + b(0) & 1(b) + b(1) \\
                    0(1) + 1(0) & 0(b) + 1(1) \\
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                1 & b \\
                0 & 1
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1 & 2b \\
                0 & 1
            \end{bmatrix}
            \begin{bmatrix}
                1 & b \\
                0 & 1
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1(1) + 2b(0) & 1(b) + 2b(1) \\
                0(1) + 1(0)  & 0(b) + 1(1)  \\
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1 & 3b \\
                0 &  1 \\
            \end{bmatrix}
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        & &
            \mathbf{A}^3
        \\[0.25em] & = &
            (\mathbf{A}^2)\mathbf{A}
        \\[0.5em] & = &
            (\mathbf{AA})\mathbf{A}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    1 & b \\
                    0 & 1
                \end{bmatrix}
                \begin{bmatrix}
                    1 & b \\
                    0 & 1
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                1 & b \\
                0 & 1
            \end{bmatrix}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    1(1) + b(0) \hspace{-0.25em} & 1(b) + b(1) \\
                    0(1) + 1(0) \hspace{-0.25em} & 0(b) + 1(1) \\
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                1 & b \\
                0 & 1
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1 & 2b \\
                0 & 1
            \end{bmatrix}
            \begin{bmatrix}
                1 & b \\
                0 & 1
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1(1) + 2b(0) & 1(b) + 2b(1) \\
                0(1) + 1(0)  & 0(b) + 1(1)  \\
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1 & 3b \\
                0 &  1 \\
            \end{bmatrix}
    \end{array}
$$
</div>

so the pattern is

$$
    \mathbf{A}^n = \begin{bmatrix}
        1 & nb \\
        0 & 1  \\
    \end{bmatrix}
$$

and

<div class = "widescreen">
$$
    \begin{array}{r c l}
            \mathbf{A}^3
        & = &
            (\mathbf{A}^2)\mathbf{A}
        \\[0.5em] & = &
            (\mathbf{AA})\mathbf{A}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    2 & 2 \\
                    0 & 0
                \end{bmatrix}
                \begin{bmatrix}
                    2 & 2 \\
                    0 & 0
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                2 & 2 \\
                0 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    2(2) + 2(0) & 2(2) + 2(0) \\
                    0(2) + 0(0) & 0(2) + 0(0) \\
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                2 & 2 \\
                0 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                4 & 4 \\
                0 & 0
            \end{bmatrix}
            \begin{bmatrix}
                2 & 2 \\
                0 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                4(2) + 4(0) & 4(2) + 4(0) \\
                0(2) + 0(0) & 0(2) + 0(0) \\
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                8 & 8 \\
                0 & 0 \\
            \end{bmatrix}.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        & &
            \mathbf{A}^3
        \\[0.5em] & = &
            (\mathbf{A}^2)\mathbf{A}
        \\[0.5em] & = &
            (\mathbf{AA})\mathbf{A}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    2 & 2 \\
                    0 & 0
                \end{bmatrix}
                \begin{bmatrix}
                    2 & 2 \\
                    0 & 0
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                2 & 2 \\
                0 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \left(
                \begin{bmatrix}
                    2(2) + 2(0) & \hspace{-0.35em} 2(2) + 2(0) \\
                    0(2) + 0(0) & \hspace{-0.35em} 0(2) + 0(0) \\
                \end{bmatrix}
            \right)
            \begin{bmatrix}
                2 & 2 \\
                0 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                4 & 4 \\
                0 & 0
            \end{bmatrix}
            \begin{bmatrix}
                2 & 2 \\
                0 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                4(2) + 4(0) & 4(2) + 4(0) \\
                0(2) + 0(0) & 0(2) + 0(0) \\
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                8 & 8 \\
                0 & 0 \\
            \end{bmatrix}.
    \end{array}
$$
</div>

so

$$
    \mathbf{A}^n = \begin{bmatrix}
        2^n & 2^n \\
        0   & 0
    \end{bmatrix}.
$$

<span class = "exnum">6</span> When

$$
    \mathbf{A} = \begin{bmatrix}
        1 & 2 \\
        0 & 0
    \end{bmatrix}
    \quad
    \mathbf{B} = \begin{bmatrix}
        1 & 0 \\
        3 & 0
    \end{bmatrix},
$$

then

<div class = "widescreen">
$$
    \begin{array}{r c l}
        (\mathbf{A} + \mathbf{B})^2
    & = &
        \begin{bmatrix}
            2 & 2 \\
            3 & 0
        \end{bmatrix}^2
    \\[0.5em] & = &
        \begin{bmatrix}
            2 & 2 \\
            3 & 0
        \end{bmatrix}
        \begin{bmatrix}
            2 & 2 \\
            3 & 0
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            2(2) + 2(3) & 2(2) + 2(0) \\
            3(2) + 0(3) & 3(2) + 0(0)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            10 & 4 \\
            6  & 6
        \end{bmatrix},
    \end{array}
$$
</div>
<div class = "smallscreen">
$$
    \begin{array}{r c l}
    & &
        (\mathbf{A} + \mathbf{B})^2
    \\[0.5em] & = &
        \begin{bmatrix}
            2 & 2 \\
            3 & 0
        \end{bmatrix}^2
    \\[0.5em] & = &
        \begin{bmatrix}
            2 & 2 \\
            3 & 0
        \end{bmatrix}
        \begin{bmatrix}
            2 & 2 \\
            3 & 0
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            2(2) + 2(3) & 2(2) + 2(0) \\
            3(2) + 0(3) & 3(2) + 0(0)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            10 & 4 \\
            6  & 6
        \end{bmatrix}.
    \end{array}
$$
</div>

but

<div class = "widescreen">
$$
    \begin{array}{r c l}
        \mathbf{A}^2 + 2\mathbf{AB} + \mathbf{B}^2
    \\[0.5em] & = & \begin{bmatrix}
            1 & 2 \\
            0 & 0
        \end{bmatrix}^2
    +
        2 \begin{bmatrix}
            1 & 2 \\
            0 & 0
        \end{bmatrix}
        \begin{bmatrix}
            1 & 0 \\
            3 & 0
        \end{bmatrix}
    +
        \begin{bmatrix}
            1 & 0 \\
            3 & 0
        \end{bmatrix}^2.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
    & &
        \mathbf{A}^2 + 2\mathbf{AB} + \mathbf{B}^2
    \\[0.5em] & = & \begin{bmatrix}
            1 & 2 \\
            0 & 0
        \end{bmatrix}^2
    +
        2 \begin{bmatrix}
            1 & 2 \\
            0 & 0
        \end{bmatrix}
        \begin{bmatrix}
            1 & 0 \\
            3 & 0
        \end{bmatrix}
    +
        \begin{bmatrix}
            1 & 0 \\
            3 & 0
        \end{bmatrix}^2.
    \end{array}
$$
</div>
        
The terms of the previous equation are

$$
    \begin{array}{r c l}
        \mathbf{A}^2
    & = & 
        \begin{bmatrix}
            1(1) + 0(2) & 2(1) + 0(2) \\
            1(0) + 0(0) & 2(0) + 0(0)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            1 & 2 \\
            0 & 0
        \end{bmatrix},
    \\[0.0em] & & \\[0.0em]
        2\mathbf{AB}
    & = &
        2 \begin{bmatrix}
            1(1) + 3(2) & 0(1) + 0(2) \\
            1(0) + 3(0) & 0(0) + 0(0)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            2(7) & 2(0) \\
            2(0) & 0(0)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            14 & 0 \\
             0 & 0
        \end{bmatrix},
    \\[0.0em] & & \\[0.0em]
        \mathbf{B}^2
    & = &
        \begin{bmatrix}
            1(1) + 3(0) & 0(1) + 0(0) \\
            1(3) + 3(0) & 0(3) + 0(0)
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            1 & 0 \\
            3 & 0
        \end{bmatrix},
    \end{array}
$$

which adds to

$$
    \begin{array}{r c l}
        \begin{bmatrix}
            1 + 14 + 1 & 2 + 0 + 0 \\
            0 +  0 + 3 & 0 + 0 + 0
        \end{bmatrix}
    & = &
        \begin{bmatrix}
            16 & 2 \\
             3 & 0
        \end{bmatrix},
    \end{array} 
$$

so $(\mathbf{A} + \mathbf{B})^2$ $\neq$ $\mathbf{A}^2$ $+$
$2\mathbf{AB}$ $+$ $\mathbf{B}^2$ for the given matrices. The
correct rule for $(\mathbf{A}$ $+$ $\mathbf{B})$$(\mathbf{A}$ $+$
$\mathbf{B})$ $=$ $\mathbf{AA}$ $+$ $\mathbf{AB}$ $+$ $\mathbf{BA}$
$+$ $\mathbf{BB}$ $=$ $\mathbf{A}^2$ $+$ $\mathbf{AB}$ $+$
$\mathbf{BA}$ $+$ $\mathbf{B}^2$, and that's it, because matrix
multiplication operation does not (always) commute.
