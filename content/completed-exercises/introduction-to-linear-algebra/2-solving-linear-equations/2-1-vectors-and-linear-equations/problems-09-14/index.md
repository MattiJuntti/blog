+++
title  = "Problems 09-14"
date   = "2025-01-01T00:00:00+03:00"
layout = "solution-single"
+++

<span class = "exercise-tag">9</span> **(a)** Computing

$$
    \mathbf{Ax}
    =
    \begin{bmatrix}
        \phantom{-}1 & 2 & 4 \\
                  -1 & 3 & 1 \\
                  -4 & 1 & 2
    \end{bmatrix}
    \begin{bmatrix}
        2 \\ 2 \\ 3
    \end{bmatrix}
    =
    \mathbf{b}
$$

by dot products of the rows with the column vector

<div class = "widescreen">
$$
    \phantom{.} \
    \mathbf{Ax}
    =
    \begin{bmatrix}
        (\phantom{-}1,2,4) \cdot \mathbf{x} \\
        (          -2,3,1) \cdot \mathbf{x} \\
        (          -4,1,2) \cdot \mathbf{x} \\
    \end{bmatrix}    
    =
    \begin{bmatrix}
        (\phantom{-}1 \cdot 2) + (2 \cdot 2) + (4 \cdot 3) \\
        (          -2 \cdot 2) + (3 \cdot 2) + (1 \cdot 3) \\
        (          -4 \cdot 2) + (1 \cdot 2) + (2 \cdot 3) \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        18 \\ 5 \\ 0
    \end{bmatrix}
    =
    \mathbf{b}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    & &
        \mathbf{Ax}
    & \phantom{=} \\[1em] & = &
        \begin{bmatrix}
            (\phantom{-}1,2,4) \cdot \mathbf{x} \\
            (          -2,3,1) \cdot \mathbf{x} \\
            (          -4,1,2) \cdot \mathbf{x} \\
        \end{bmatrix}    
    \\[1em] & = &
        \begin{bmatrix}
            (\phantom{-}1 \cdot 2) + (2 \cdot 2) + (4 \cdot 3) \\
            (          -2 \cdot 2) + (3 \cdot 2) + (1 \cdot 3) \\
            (          -4 \cdot 2) + (1 \cdot 2) + (2 \cdot 3) \\
        \end{bmatrix}
    & \phantom{=} \\[1em] & = &
        \begin{bmatrix}
            18 \\ 5 \\ 0
        \end{bmatrix}
    & \phantom{=} \\[1em] & = &
        \phantom{.} \ \mathbf{b} \ .
    \end{array}
$$
</div>

**(b)** Similarily

<div class = "widescreen">
$$
    \phantom{.} \
    \mathbf{Ax}
    =
    \begin{bmatrix}
        2 & 1 & 0 & 0 \\
        1 & 2 & 1 & 0 \\
        0 & 1 & 2 & 1 \\
        0 & 0 & 1 & 2
    \end{bmatrix}
    \begin{bmatrix}
        1 \\ 1 \\ 1 \\ 2
    \end{bmatrix}
    =
    \begin{bmatrix}
        (2 \cdot 1) + (1 \cdot 1) + (0 \cdot 1) + (0 \cdot 2) \\
        (1 \cdot 1) + (2 \cdot 1) + (1 \cdot 1) + (0 \cdot 2) \\
        (0 \cdot 1) + (1 \cdot 1) + (2 \cdot 1) + (1 \cdot 2) \\
        (0 \cdot 2) + (0 \cdot 1) + (1 \cdot 1) + (2 \cdot 2)
    \end{bmatrix}
    =
    \begin{bmatrix}
        3 \\ 4 \\ 4 \\ 3
    \end{bmatrix}
    =
    \mathbf{b}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    &
        \mathbf{Ax}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            2 & 1 & 0 & 0 \\
            1 & 2 & 1 & 0 \\
            0 & 1 & 2 & 1 \\
            0 & 0 & 1 & 2
        \end{bmatrix}
        \begin{bmatrix}
            1 \\ 1 \\ 1 \\ 2
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            (2 \cdot 1) + (1 \cdot 1) + (0 \cdot 1) + (0 \cdot 2) \\
            (1 \cdot 1) + (2 \cdot 1) + (1 \cdot 1) + (0 \cdot 2) \\
            (0 \cdot 1) + (1 \cdot 1) + (2 \cdot 1) + (1 \cdot 2) \\
            (0 \cdot 2) + (0 \cdot 1) + (1 \cdot 1) + (2 \cdot 2)
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            3 \\ 4 \\ 4 \\ 3
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \phantom{.} \ \mathbf{b} \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">10</span>

Computing the $\mathbf{Ax}$ of <span class = "exercise-tag">9</span> as a
compination of column means that

<div class = "widescreen">
$$
    \phantom{.} \
    \mathbf{Ax}
    =
    2 \begin{bmatrix}
        \phantom{-}1 \\ -2 \\ -4 
    \end{bmatrix}
    +
    2 \begin{bmatrix}
        2 \\ 3 \\ 1
    \end{bmatrix}
    +
    3 \begin{bmatrix}
        4 \\ 1 \\ 2
    \end{bmatrix}
    =
    \begin{bmatrix}
       \phantom{-} 2 \\ -4 \\ -8
    \end{bmatrix}
    +
    \begin{bmatrix}
        4 \\ 6 \\ 2
    \end{bmatrix}
    +
    \begin{bmatrix}
        12 \\ 3 \\ 6
    \end{bmatrix}
    =
    \begin{bmatrix}
        18 \\ 2 \\ 0
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    &
        \mathbf{Ax}
    \phantom{=} \\[0.5em] = &
        2 \begin{bmatrix}
            \phantom{-}1 \\ -2 \\ -4 
        \end{bmatrix}
        +
        2 \begin{bmatrix}
            2 \\ 3 \\ 1
        \end{bmatrix}
        +
        3 \begin{bmatrix}
            4 \\ 1 \\ 2
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        \begin{bmatrix}
           \phantom{-} 2 \\ -4 \\ -8
        \end{bmatrix}
        +
        \begin{bmatrix}
            4 \\ 6 \\ 2
        \end{bmatrix}
        +
        \begin{bmatrix}
            12 \\ 3 \\ 6
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        \phantom{.} \
        \begin{bmatrix}
            18 \\ 2 \\ 0
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

No matter what method one uses to multiply matrices, the nuber of
multiplications is the same. However, the computation of as a combination
of column can be taken to be clearer notationally.

<span class = "exercise-tag">11</span>

**(a)**

By rows:

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        2 & 3 \\
        5 & 1
    \end{bmatrix}
    \begin{bmatrix}
        4 \\ 2
    \end{bmatrix}
    =
    \begin{bmatrix}
        (2 \cdot 4) + (3 \cdot 2) \\
        (5 \cdot 4) + (1 \cdot 2) \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        8 + 6 \\
        20 + 2
    \end{bmatrix}
    =
    \begin{bmatrix}
        14 \\
        22
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    \phantom{=} &
        \begin{bmatrix}
            2 & 3 \\
            5 & 1
        \end{bmatrix}
        \begin{bmatrix}
            4 \\ 2
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        \begin{bmatrix}
            (2 \cdot 4) + (3 \cdot 2) \\
            (5 \cdot 4) + (1 \cdot 2) \\
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            8 + 6 \\
            20 + 2
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \phantom{.} \
        \begin{bmatrix}
            14 \\
            22
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

By column:

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        2 & 3 \\
        5 & 1
    \end{bmatrix}
    \begin{bmatrix}
        4 \\ 2
    \end{bmatrix}
    =
    4 \begin{bmatrix}
        2 \\ 5
    \end{bmatrix}
    +
    2 \begin{bmatrix}
        3 \\ 1
    \end{bmatrix}
    =
    \begin{bmatrix}
        8 + 6 \\
        20 + 2
    \end{bmatrix}
    =
    \begin{bmatrix}
        14 \\
        22
    \end{bmatrix}
    \ .
$$ 
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
        \begin{array}{r c l}
        \phantom{=} &
            \begin{bmatrix}
                2 & 3 \\
                5 & 1
            \end{bmatrix}
            \begin{bmatrix}
                4 \\ 2
            \end{bmatrix}
        & \phantom{=} \\[1em] = &
            4 \begin{bmatrix}
                2 \\ 5
            \end{bmatrix}
            +
            2 \begin{bmatrix}
                3 \\ 1
            \end{bmatrix}
        & \phantom{=} \\[1em] = &
            \begin{bmatrix}
                8 + 6 \\
                20 + 2
            \end{bmatrix}
        & \phantom{=} \\[1em] = &
            \phantom{.} \
            \begin{bmatrix}
                14 \\
                22
            \end{bmatrix}
            \ .
        \end{array}
    \end{array}
$$ 
</div>

**(b)**

By rows:

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        3 & 6 \\
        6 & 12
    \end{bmatrix} 
    \begin{bmatrix}
        \phantom{-}2 \\
        -1
    \end{bmatrix}
    =
    \begin{bmatrix}
        (3 \cdot 2) + [6 \cdot (-1)] \\
        (6 \cdot 2) + [12 \cdot (-1)]
    \end{bmatrix}
    =
    \begin{bmatrix}
        6 - 6 \\
        12 - 12
    \end{bmatrix}
    =
    \begin{bmatrix}
        0 \\ 0
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    &
        \begin{bmatrix}
            3 & 6 \\
            6 & 12
        \end{bmatrix} 
        \begin{bmatrix}
            \phantom{-}2 \\
            -1
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            (3 \cdot 2) + [6 \cdot (-1)] \\
            (6 \cdot 2) + [12 \cdot (-1)]
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            6 - 6 \\
            12 - 12
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \phantom{.} \
        \begin{bmatrix}
            0 \\ 0
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

By column:

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        3 & 6 \\
        6 & 12
    \end{bmatrix} 
    \begin{bmatrix}
        \phantom{-}2 \\
        -1
    \end{bmatrix}
    =
    2 \begin{bmatrix}
        3 \\ 6
    \end{bmatrix}
    -
    1 \begin{bmatrix}
        6 \\ 12
    \end{bmatrix}
    =
    \begin{bmatrix}
        6 - 6 \\
        12 - 12
    \end{bmatrix}
    =
    \begin{bmatrix}
        0 \\ 0
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    \phantom{=} &
        \begin{bmatrix}
            3 & 6 \\
            6 & 12
        \end{bmatrix} 
        \begin{bmatrix}
            \phantom{-}2 \\
            -1
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        2 \begin{bmatrix}
            3 \\ 6
        \end{bmatrix}
        -
        1 \begin{bmatrix}
            6 \\ 12
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            6 - 6 \\
            12 - 12
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \phantom{.} \
        \begin{bmatrix}
            0 \\ 0
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

**(c)**

By rows:

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        1 & 2 & 4 \\
        2 & 0 & 1
    \end{bmatrix}
    \begin{bmatrix}
        3 \\ 1 \\ 1
    \end{bmatrix}
    =
    \begin{bmatrix}
        (1 \cdot 3) + (2 \cdot 1) + (4 \cdot 1) \\
        (2 \cdot 3) + (0 \cdot 1) + (1 \cdot 1) \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        3 + 2 + 4 \\
        6 + 0 + 1
    \end{bmatrix}
    =
    \begin{bmatrix}
        9 \\ 7
    \end{bmatrix}
    \ .
$$
</div>

asdasd

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    &
        \begin{bmatrix}
            1 & 2 & 4 \\
            2 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            3 \\ 1 \\ 1
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            (1 \cdot 3) + (2 \cdot 1) + (4 \cdot 1) \\
            (2 \cdot 3) + (0 \cdot 1) + (1 \cdot 1) \\
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            3 + 2 + 4 \\
            6 + 0 + 1
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            9 \\ 7
        \end{bmatrix}
    \end{array}
$$
</div>

By column:

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        1 & 2 & 4 \\
        2 & 0 & 1
    \end{bmatrix}
    \begin{bmatrix}
        3 \\ 1 \\ 1
    \end{bmatrix}
=
    3 \begin{bmatrix}
        1 \\ 2
    \end{bmatrix}
    +
    \begin{bmatrix}
        2 \\ 0
    \end{bmatrix}
    +
    \begin{bmatrix}
        4 \\ 1
    \end{bmatrix}
=
    \begin{bmatrix}
        3 + 2 + 4 \\
        6 + 0 + 1
    \end{bmatrix}
=
    \begin{bmatrix}
        9 \\ 7
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    \phantom{=} &
        \begin{bmatrix}
            1 & 2 & 4 \\
            2 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            3 \\ 1 \\ 1
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        3 \begin{bmatrix}
            1 \\ 2
        \end{bmatrix}
        +
        \begin{bmatrix}
            2 \\ 0
        \end{bmatrix}
        +
        \begin{bmatrix}
            4 \\ 1
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        \begin{bmatrix}
            3 + 2 + 4 \\
            6 + 0 + 1
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        \phantom{.} \
        \begin{bmatrix}
            9 \\ 7
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">12</span>

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        0 & 0 & 1 \\
        0 & 1 & 0 \\
        1 & 0 & 0
    \end{bmatrix}
    \begin{bmatrix}
        x \\ y \\  z
    \end{bmatrix}
    =
    x \begin{bmatrix}
        0 \\ 0 \\ 1
    \end{bmatrix}
    +
    y \begin{bmatrix}
        0 \\ 1 \\ 0
    \end{bmatrix}
    +
    z \begin{bmatrix}
        1 \\ 0 \\ 0
    \end{bmatrix}
    =
    \begin{bmatrix}
        z \\ y \\ x
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    &
        \begin{bmatrix}
            0 & 0 & 1 \\
            0 & 1 & 0 \\
            1 & 0 & 0
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y \\  z
        \end{bmatrix}
    \\[1em] = &
        x \begin{bmatrix}
            0 \\ 0 \\ 1
        \end{bmatrix}
        +
        y \begin{bmatrix}
            0 \\ 1 \\ 0
        \end{bmatrix}
        +
        z \begin{bmatrix}
            1 \\ 0 \\ 0
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \phantom{.} \
        \begin{bmatrix}
            z \\ y \\ x
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">13</span>

**(a)** A matrix with $m$ rows and $n$ columns multiplies a vector with $m$
components to produce a vector with $n$ components. As an example, let $n =
3$ and $n = 2$, then

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        a_{11} & a_{12} & a_{13} \\
        a_{21} & a_{22} & a_{23}
    \end{bmatrix}
    \begin{bmatrix}
        x \\ y \\ z
    \end{bmatrix}
    =
    x \begin{bmatrix}
        a_{11} \\ a_{21}
    \end{bmatrix}
    +
    y \begin{bmatrix}
        a_{12} \\ a_{22}
    \end{bmatrix}
    +
    z \begin{bmatrix}
        a_{13} \\ a_{23}
    \end{bmatrix}
    =
    \begin{bmatrix}
        xa_{11} + ya_{12} + za_{13} \\
        xa_{21} + ya_{22} + za_{23}
    \end{bmatrix}
    =
    \begin{bmatrix}
        b_1 \\ b_2 \\ b_3
    \end{bmatrix}
    \ ,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    &
        \begin{bmatrix}
            a_{11} & a_{12} & a_{13} \\
            a_{21} & a_{22} & a_{23}
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y \\ z
        \end{bmatrix}
    & \\[1em] = &
        x \begin{bmatrix}
            a_{11} \\ a_{21}
        \end{bmatrix}
        +
        y \begin{bmatrix}
            a_{12} \\ a_{22}
        \end{bmatrix}
        +
        z \begin{bmatrix}
            a_{13} \\ a_{23}
        \end{bmatrix}
    & \\[1em] = &
        \begin{bmatrix}
            xa_{11} + ya_{12} + za_{13} \\
            xa_{21} + ya_{22} + za_{23}
        \end{bmatrix}
    & \\[1em] = &
        \begin{bmatrix}
            b_1 \\ b_2 \\ b_3
        \end{bmatrix} \ ,
    \end{array}
$$
</div>

from where it can be seen that $\mathbf{b}$ has $n = 6$ components.

**(b)**

The planes from the $m$ equations $\mathbf{Ax} = \mathbf{b}$ are in $m - 1$
dimensional space. The combination of the columns of $\mathbf{A}$ is in
$m$-dimensional space.

<span class = "exercise-tag">14</span>

One way to write the equation

$$
    2x + 2y + z + 5t = 8
$$

in a matrix form is to gather the coefficients into a matrix $\textbf{A}$
and the variables into vector and then multiply the variable vector with
the coefficient matrix. In other words,

<div class = "widescreen">
$$
    \phantom{,} \
        \mathbf{Ax}
    =
        \begin{bmatrix}
            2 & 2 & 1 & 8
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y \\ z \\  t
        \end{bmatrix}
    =
        x \begin{bmatrix}
            2
        \end{bmatrix}
    +
        y \begin{bmatrix}
            2
        \end{bmatrix}
    +
        z \begin{bmatrix}
            1
        \end{bmatrix}
    +
        t \begin{bmatrix}
            8
        \end{bmatrix}
    =
        2x + 2y + z + 5t
    = 8
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
            & \mathbf{Ax} &
        \\[1em] = &
            \begin{bmatrix}
                2 & 2 & 1 & 8
            \end{bmatrix}
            \begin{bmatrix}
                x \\ y \\ z \\  t
            \end{bmatrix}
        & \\[1em] = &
            x \begin{bmatrix}
                2
            \end{bmatrix}
        +
            y \begin{bmatrix}
                2
            \end{bmatrix}
        +
            z \begin{bmatrix}
                1
            \end{bmatrix}
        +
            t \begin{bmatrix}
                5
            \end{bmatrix}
        & \\[1em] = &
            2x + 2y + z + 5t
        & \\[0.5em] = &
            8
        & \\[0.5em] = &
            \phantom{.} \ \mathbf{b} \ .
    \end{array}
$$
</div>

The multiplying matrix $\mathbf{A}$ then has $1$ row.
