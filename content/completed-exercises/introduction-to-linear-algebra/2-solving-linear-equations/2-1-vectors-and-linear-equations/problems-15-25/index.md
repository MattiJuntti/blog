+++
title = "Problems 15-25"
layout = "solution-single"
+++

<span class = "exercise-tag">15</span>

**(a))** When

$$
    \phantom{.} \
    \mathbf{I} = \begin{bmatrix}
        1 & 0 \\
        0 & 1
    \end{bmatrix}
    \ ,
$$

the matrix multiplication

<div class = "widescreen">
$$
    \phantom{.} \
    \mathbf{Ix}
    =
    \begin{bmatrix}
        1 & 0 \\
        0 & 1
    \end{bmatrix}
    \begin{bmatrix}
        x \\ y
    \end{bmatrix}
    =
    x \begin{bmatrix}
        1 \\ 0
    \end{bmatrix}
    +
    y \begin{bmatrix}
        0 \\ 1
    \end{bmatrix}
    =
    \begin{bmatrix}
        x + 0 \\
        0 + y
    \end{bmatrix}
    =
    \begin{bmatrix}
        x \\ y
    \end{bmatrix}
    =
    \mathbf{b}
    \ .
$$
</div>

<div class = "smallscreen">
    \begin{array}{c c c}
        \phantom{=} &
        \mathbf{Ix}
        & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            1 & 0 \\
            0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        x \begin{bmatrix}
            1 \\ 0
        \end{bmatrix}
        +
        y \begin{bmatrix}
            0 \\ 1
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            x + 0 \\
            0 + y
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        \phantom{.} \ \mathbf{b} \ .
    \end{array}
</div>

**(b)** When

$$
    \phantom{.} \
    \mathbf{P} = \begin{bmatrix}
        0 & 1 \\
        1 & 0
    \end{bmatrix}
    \ ,
$$

the matrix multiplication

<div class = "widescreen">
$$
    \phantom{.} \
    \mathbf{Px}
    =
    \begin{bmatrix}
        0 & 1 \\
        1 & 0
    \end{bmatrix}
    \begin{bmatrix}
        x \\ y
    \end{bmatrix}
    =
    x \begin{bmatrix}
        0 \\ 1
    \end{bmatrix}
    +
    y \begin{bmatrix}
        1 \\ 0
    \end{bmatrix}
    =
    \begin{bmatrix}
        0 + y \\
        x + 0
    \end{bmatrix}
    =
    \begin{bmatrix}
        y \\ x
    \end{bmatrix}
    =
    \mathbf{b}
    \ .
$$
</div>

<div class = "smallscreen">
    \begin{array}{c c c}
        \phantom{=} &
        \mathbf{Px}
        & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            0 & 1 \\
            1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        x \begin{bmatrix}
            0 \\ 1
        \end{bmatrix}
        +
        y \begin{bmatrix}
            1 \\ 0
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            0 + y \\
            x + 0
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
        & \phantom{=} \\[1em] = &
        \phantom{.} \ \mathbf{b} \ .
    \end{array}
</div>

<span class = "exercise-tag">16</span>

**(a)** When

$$
    \phantom{.} \
    \mathbf{R} = \begin{bmatrix}
        \phantom{-}0 & 1 \\
                  -1 & 0
    \end{bmatrix}
    \ ,
$$

the matrix multiplication

<div class = "widescreen">
$$
    \mathbf{Rx}
    =
    \begin{bmatrix}
        \phantom{-}0 & 1 \\
                  -1 & 0
    \end{bmatrix}
    \begin{bmatrix}
        x \\ y
    \end{bmatrix}
    =
    x \begin{bmatrix}
        \phantom{-}0 \\
                  -1
    \end{bmatrix}
    +
    y \begin{bmatrix}
        1 \\
        0
    \end{bmatrix}
    =
    \begin{bmatrix}
        \phantom{-}0 + y \\
                  -x + 0
    \end{bmatrix}
    =
    \begin{bmatrix}
        y \\ -x
    \end{bmatrix}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    \phantom{=} &
        \mathbf{Rx}
    \phantom{=} \\[1em] = &
        \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        x \begin{bmatrix}
            \phantom{-}0 \\
                      -1
        \end{bmatrix}
        y \begin{bmatrix}
            1 \\
            0
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        \begin{bmatrix}
            \phantom{-}0 + y \\
                      -x + 0
        \end{bmatrix}
    \phantom{=} \\[1em] = &
        \begin{bmatrix}
            \phantom{-}y \\ -x
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

As an example, let

<div class = "widescreen">
$$
    \mathbf{x}_1 = \begin{bmatrix}
        1 \\ 1
    \end{bmatrix}
    , \quad
    \mathbf{x}_2 = \begin{bmatrix}
        -1 \\ 1
    \end{bmatrix}
    , \quad
    \mathbf{x}_3 = \begin{bmatrix}
        -1 \\ -1
    \end{bmatrix}
    , \quad
    \mathbf{x}_4 = \begin{bmatrix}
        1 \\ -1
    \end{bmatrix}
    , \quad
$$
</div>

<div class = "smallscreen">
    \begin{array}{c}
        \mathbf{x}_1 = \begin{bmatrix}
            \phantom{-}1 \\ \phantom{-}1
        \end{bmatrix}
        , \quad \\[1em]
        \mathbf{x}_2 = \begin{bmatrix}
            -1 \\ \phantom{-}1
        \end{bmatrix}
        , \quad \\[1em]
        \mathbf{x}_3 = \begin{bmatrix}
            -1 \\ -1
        \end{bmatrix}
        , \quad \\[1em]
        \mathbf{x}_4 = \begin{bmatrix}
            \phantom{-}1 \\ -1
        \end{bmatrix}
        , \quad
    \end{array}
</div>

then

$$
    \begin{array}{c c c}
        \mathbf{Rx}_1 & = & \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            1 \\ 1
        \end{bmatrix}
    & = &
        \begin{bmatrix}
            1 \\ -1
        \end{bmatrix}
    \ , \\[1em]
        \mathbf{Rx}_2 & = & \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            -1 \\ \phantom{-}1
        \end{bmatrix}
    & = &
        \begin{bmatrix}
            1 \\ 1
        \end{bmatrix}
    \ , \\[1em]
        \mathbf{Rx}_3 & = & \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            -1 \\ -1
        \end{bmatrix}
    & = &
        \begin{bmatrix}
            -1 \\ \phantom{-}1
        \end{bmatrix}
    \ , \\[1em]
        \mathbf{Rx}_4 & = & \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            \phantom{-}1 \\ -1
        \end{bmatrix}
    & = &
        \begin{bmatrix}
            1 \\ -1
        \end{bmatrix}
        \ .
    \end{array}
$$

From where it's also possible to see that

$$
    \begin{array}{r c l}
        \phantom{.} \ \mathbf{Rx}_1 & = & \mathbf{x}_4 \ , \\[0.5em]
        \phantom{.} \ \mathbf{Rx}_2 & = & \mathbf{x}_1 \ , \\[0.5em]
        \phantom{.} \ \mathbf{Rx}_3 & = & \mathbf{x}_2 \ , \\[0.5em]
        \phantom{.} \ \mathbf{Rx}_4 & = & \mathbf{x}_3 \ .
    \end{array} 
$$

**(b)** A matrix that rotates a vector $\mathbf{x} = (x,y)^\top$ full $\pi$
radians is equal to matrix that rotates the $\mathbf{x}$ vector twice
$\pi/2$ radians. That is

<div class = "widescreen">
$$
    \phantom{.} \
        \mathbf{R}(\mathbf{Rx})
    =
        \mathbf{R} \left( \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
        \right)
    =
        \mathbf{R}
        \begin{bmatrix}
            y \\ -x
        \end{bmatrix}
    =
        \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            y \\ -x
        \end{bmatrix}
    =
        \begin{bmatrix}
            -x \\ -y
        \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
        & \mathbf{R}(\mathbf{Rx})
    & \phantom{=} \\[1em] = &
        \mathbf{R} \left( \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
        \right)
    & \phantom{=} \\[1em] = &
        \mathbf{R}
        \begin{bmatrix}
            y \\ -x
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            \phantom{-}0 & 1 \\
                      -1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            y \\ -x
        \end{bmatrix}
    & \phantom{=} \\[1em] = &
        \begin{bmatrix}
            -x \\ -y
        \end{bmatrix} \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">17</span>

Find the matrix $\mathbf{P}$ that multiplies $[x,y,z]^\top$ to give
$[y,z,x]^\top$ is a kind of matrix that multiplies $x$ and $y$ by $0$
and $z$ by $1$ at the first column, $y$ and $z$ by $0$ and $y$ with $1$ at
the second column, and $x$ and $z$ by $0$ and $z$ by $1$ in the third
column.

Such a matrix is a matrix

$$
    \phantom{.} \
    \begin{bmatrix}
        0 & 1 & 0 \\
        0 & 0 & 1 \\
        1 & 0 & 0
    \end{bmatrix}
    \ ,
$$

because

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        0 & 1 & 0 \\
        0 & 0 & 1 \\
        1 & 0 & 0
    \end{bmatrix}
    \begin{bmatrix}
        x \\ y \\ z
    \end{bmatrix}
=
    x \begin{bmatrix}
        0 \\ 0 \\ 1
    \end{bmatrix}
+
    y \begin{bmatrix}
        1 \\ 0 \\ 0
    \end{bmatrix}
+
    z \begin{bmatrix}
        0 \\ 1 \\ 0
    \end{bmatrix}
=
    \begin{bmatrix}
        0x           + \phantom{0}y + 0z \\
        0x           + 0y          + \phantom{0}z \\
        \phantom{0}x + 0y          + 0z
    \end{bmatrix}
=
    \begin{bmatrix}
        y \\ z \\ x
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
    &
        \begin{bmatrix}
            0 & 1 & 0 \\
            0 & 0 & 1 \\
            1 & 0 & 0
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y \\ z
        \end{bmatrix}
    & \\[1em] = &
        x \begin{bmatrix}
            0 \\ 0 \\ 1
        \end{bmatrix}
    +
        y \begin{bmatrix}
            1 \\ 0 \\ 0
        \end{bmatrix}
    +
        z \begin{bmatrix}
            0 \\ 1 \\ 0
        \end{bmatrix}
    & \\[1em] = &
        \begin{bmatrix}
            0x           + \phantom{0}y + 0z \\
            0x           + 0y          + \phantom{0}z \\
            \phantom{0}x + 0y          + 0z
        \end{bmatrix}
    & \\[1em] = & \phantom{.} \
        \begin{bmatrix}
            y \\ z \\ x
        \end{bmatrix} \ .
    \end{array}
$$
</div>

A matrix $\mathbf{Q}$ that brings back the $[y,x,z]^\top$ to $[x,y,z]^\top$
is a matrix

$$
    \phantom{.} \
    \begin{bmatrix}
        0 & 0 & 1 \\ 
        1 & 0 & 0 \\ 
        0 & 1 & 0
    \end{bmatrix}
    \ .
$$

because

<div class = "widescreen">
$$
    \phantom{.} \
    \begin{bmatrix}
        0 & 0 & 1 \\ 
        1 & 0 & 0 \\ 
        0 & 1 & 0
    \end{bmatrix}
    \begin{bmatrix}
        y \\ z \\ x
    \end{bmatrix}
=
    y \begin{bmatrix}
        0 \\ 1 \\ 0
    \end{bmatrix}
+
    z \begin{bmatrix}
        0 \\ 0 \\ 1
    \end{bmatrix}
+
    x \begin{bmatrix}
        1 \\ 0 \\ 0
    \end{bmatrix}
=
    \begin{bmatrix}
        0y           + 0z           + \phantom{0}x \\
        \phantom{0}y + 0z           + 0x \\
        0y           + \phantom{0}z + 0x
    \end{bmatrix}
=
    \begin{bmatrix}
        x \\ y \\ z
    \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
    \phantom{=} &
        \begin{bmatrix}
            0 & 0 & 1 \\ 
            1 & 0 & 0 \\ 
            0 & 1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            y \\ z \\ x
        \end{bmatrix}
    & \\[1em] = &
        y \begin{bmatrix}
            0 \\ 1 \\ 0
        \end{bmatrix}
    +
        z \begin{bmatrix}
            0 \\ 0 \\ 1
        \end{bmatrix}
    +
        x \begin{bmatrix}
            1 \\ 0 \\ 0
        \end{bmatrix}
    & \\[1em] = &
        \begin{bmatrix}
            0y           + 0z           + \phantom{0}x \\
            \phantom{0}y + 0z           + 0x \\
            0y           + \phantom{0}z + 0x
        \end{bmatrix}
    & \\[1em] = & \phantom{.} \
        \begin{bmatrix}
            x \\ y \\ z
        \end{bmatrix}
    \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">18</span>

The situation is comparable to situation of two equations where

$$
    (1 \cdot 3) + (0 \cdot 5) = 3
$$

and

$$
    \phantom{.} \ ((-1) \cdot 3) + (1 \cdot 5) = 2 \ .
$$

Observing the coefficients in the above two equations, and rewriting the
computations in a matrix form leads to matrix multiplication

<div class = "widescreen">
$$
    \phantom{.} \
        \begin{bmatrix}
            \phantom{-}1 & 0 \\
            -1           & 1
        \end{bmatrix}
        \begin{bmatrix}
            3 \\
            5
        \end{bmatrix}
    =
        3 \begin{bmatrix}
            \phantom{-}1 \\
                      -1
        \end{bmatrix}
    +
        5 \begin{bmatrix}
            0 \\
            1
        \end{bmatrix}
    =
        \begin{bmatrix}
            3(1) + 5(0) \\
            3(-1) + 5(1) \\
        \end{bmatrix}
    =
        \begin{bmatrix}
            \phantom{-}3 + 0 \\
            -3           + 5 
        \end{bmatrix}
    =
        \begin{bmatrix}
            3 \\
            2
        \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
    \phantom{=} &
        \begin{bmatrix}
            \phantom{-}1 & 0 \\
            -1           & 1
        \end{bmatrix}
        \begin{bmatrix}
            3 \\
            5
        \end{bmatrix}
    & \\[1em] = &
        3 \begin{bmatrix}
            \phantom{-}1 \\
                      -1
        \end{bmatrix}
    +
        5 \begin{bmatrix}
            0 \\
            1
        \end{bmatrix}
    & \\[1em] = &
        \begin{bmatrix}
            3(1) + 5(0) \\
            3(-1) + 5(1) \\
        \end{bmatrix}
    & \\[1em] = &
        \begin{bmatrix}
            \phantom{-}3 + 0 \\
            -3           + 5 
        \end{bmatrix}
    & \\[1em] = & \phantom{.} \
        \begin{bmatrix}
            3 \\
            2
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

The situation is similar to the second equation. Written in anohter way,
the equations are

$$
    \phantom{,} \ \phantom{-}1(3) + 0(5) + 0(7) = 3 \ ,
$$

$$
    \phantom{,} \ -1(3) + 1(5) + 0(7) = 3 \ ,
$$

and

$$
    \phantom{,} \ 0(3) + 0(5) + 1(7) = 3 \ ,
$$

so the subtracting matrix computation becomes

<div class = "widescreen">
$$
    \phantom{.} \
        \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
            -1           & 1 & 0 \\
            \phantom{-}0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            3 \\ 5 \\ 7
        \end{bmatrix}
    =
        3 \begin{bmatrix}
            \phantom{-}1 \\
            -1 \\
            0
        \end{bmatrix}
    +
        5 \begin{bmatrix}
            0 \\
            1 \\
            0
        \end{bmatrix}
    +
        7 \begin{bmatrix}
            0 \\
            0 \\
            1
        \end{bmatrix}
    =
        \begin{bmatrix}
            \phantom{-}3 + 0 + 0 \\
            -3           + 5 + 0 \\
            \phantom{-}0 + 0 + 7
        \end{bmatrix}
    =
        \begin{bmatrix}
            3 \\
            2 \\
            7
        \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
    \phantom{=} &
        \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
            -1           & 1 & 0 \\
            \phantom{-}0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            3 \\ 5 \\ 7
        \end{bmatrix}
    \phantom{=} & \\[1em] = &
        3 \begin{bmatrix}
            \phantom{-}1 \\
            -1 \\
            0
        \end{bmatrix}
    +
        5 \begin{bmatrix}
            0 \\
            1 \\
            0
        \end{bmatrix}
    +
        7 \begin{bmatrix}
            0 \\
            0 \\
            1
        \end{bmatrix}
    \phantom{=} & \\[1em] = &
        \begin{bmatrix}
            \phantom{-}3 + 0 + 0 \\
            -3           + 5 + 0 \\
            \phantom{-}0 + 0 + 7
        \end{bmatrix}
    \phantom{=} & \\[1em] = & \phantom{.} \
        \begin{bmatrix}
            3 \\
            2 \\
            7
        \end{bmatrix}
        \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">19</span>

When

$$
    \phantom{,} \
    \mathbf{E}^{-1} = \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 1 & 0 \\
        1 & 0 & 1
    \end{bmatrix}
    \ ,
$$

<div class = "widescreen">
$$
    \phantom{.} \
        \mathbf{E}^{-1} \begin{bmatrix}
            x \\
            y \\
            z
        \end{bmatrix}
        =
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
            1 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            x \\
            y \\
            z
        \end{bmatrix}
        =
        \begin{bmatrix}
            x + 0 + 0 \\
            0 + y + 0 \\
            x + 0 + z
        \end{bmatrix}
        =
        \begin{bmatrix}
            x \\ y \\ z + x
        \end{bmatrix}
    \ ,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
        \phantom{=} &
            \mathbf{E}^{-1} \begin{bmatrix}
                x \\
                y \\
                z
            \end{bmatrix}
        & \phantom{=} \\[1em] = &
            \begin{bmatrix}
                1 & 0 & 0 \\
                0 & 1 & 0 \\
                1 & 0 & 1
            \end{bmatrix}
            \begin{bmatrix}
                x \\
                y \\
                z
            \end{bmatrix}
        & \phantom{=} \\[1em] = &
            \begin{bmatrix}
                x + 0 + 0 \\
                0 + y + 0 \\
                x + 0 + z
            \end{bmatrix}
        & \phantom{=} \\[1em] = & \phantom{,} \
            \begin{bmatrix}
                x \\ y \\ z + x
            \end{bmatrix}
        \ ,
    \end{array}
$$
</div>

and when

$$
    \phantom{,} \
    \mathbf{E}^{-1} = \begin{bmatrix}
        \phantom{-}1 & 0 & 0 \\
        \phantom{-}0 & 1 & 0 \\
                  -1 & 0 & 1
    \end{bmatrix}
    \ ,
$$

<div class = "widescreen">
$$
    \phantom{.} \
        \mathbf{E}^{-1} \begin{bmatrix}
            x \\
            y \\
            z
        \end{bmatrix}
        =
        \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
            \phantom{-}0 & 1 & 0 \\
                      -1 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            x \\
            y \\
            z
        \end{bmatrix}
        =
        \begin{bmatrix}
            \phantom{-}x + 0 + 0 \\
            \phantom{-}0 + y + 0 \\
                      -x + 0 + z
        \end{bmatrix}
        =
        \begin{bmatrix}
            x \\ y \\ z - x
        \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
        \phantom{=} &
            \mathbf{E}^{-1} \begin{bmatrix}
                x \\
                y \\
                z
            \end{bmatrix}
        & \phantom{=} \\[1em] = &
            \begin{bmatrix}
                \phantom{-}1 & 0 & 0 \\
                \phantom{-}0 & 1 & 0 \\
                          -1 & 0 & 1
            \end{bmatrix}
            \begin{bmatrix}
                x \\
                y \\
                z
            \end{bmatrix}
        & \phantom{=} \\[1em] = &
            \begin{bmatrix}
                \phantom{-}x + 0 + 0 \\
                \phantom{-}0 + y + 0 \\
                -x + 0 + z
            \end{bmatrix}
        & \phantom{=} \\[1em] = & \phantom{,} \
            \begin{bmatrix}
                x \\ y \\ z + x
            \end{bmatrix}
        \ .
    \end{array}
$$
</div>

The next multiplication brings the original vector back, because

<div class = "widescreen">
$$
    \phantom{.} \
        \mathbf{E} \begin{bmatrix}
            3 \\ 4 \\ 5
        \end{bmatrix}
    =
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
            1 & 0 & 1 \\
        \end{bmatrix}
        \begin{bmatrix}
            3 \\ 4 \\ 5
        \end{bmatrix}
    =
        \begin{bmatrix}
            3 \\
            4 \\
            5 + 3
        \end{bmatrix}
    =
        \begin{bmatrix}
            3 \\
            4 \\
            8
        \end{bmatrix}
        \ ,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
        \phantom{=} &
            \mathbf{E} \begin{bmatrix}
                3 \\ 4 \\ 5
            \end{bmatrix}
        \phantom{=} \\[1em] = &
            \begin{bmatrix}
                1 & 0 & 0 \\
                0 & 1 & 0 \\
                1 & 0 & 1 \\
            \end{bmatrix}
            \begin{bmatrix}
                3 \\ 4 \\ 5
            \end{bmatrix}
        \phantom{=} \\[1em] = &
            \begin{bmatrix}
                3 \\
                4 \\
                5 + 3
            \end{bmatrix}
        \phantom{=} \\[1em] = & \phantom{.} \
            \begin{bmatrix}
                3 \\
                4 \\
                8
            \end{bmatrix}
            \ ,
    \end{array}
$$
</div>

and

<div class = "widescreen">
$$
    \phantom{.} \
        \mathbf{E}^{-1} \begin{bmatrix}
            3 \\ 4 \\ 8
        \end{bmatrix}
    =
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
            1 & 0 & 1 \\
        \end{bmatrix}
        \begin{bmatrix}
            3 \\ 4 \\ 8
        \end{bmatrix}
    =
        \begin{bmatrix}
            3 \\
            4 \\
            8 - 3
        \end{bmatrix}
    =
        \begin{bmatrix}
            3 \\
            4 \\
            5
        \end{bmatrix}
        \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
        \phantom{=} &
            \mathbf{E}^{-1} \begin{bmatrix}
                3 \\ 4 \\ 8
            \end{bmatrix}
        \phantom{=} \\[1em] = &
            \begin{bmatrix}
                1 & 0 & 0 \\
                0 & 1 & 0 \\
                1 & 0 & 1 \\
            \end{bmatrix}
            \begin{bmatrix}
                3 \\ 4 \\ 8
            \end{bmatrix}
        \phantom{=} \\[1em] = &
            \begin{bmatrix}
                3 \\
                4 \\
                8 + 3
            \end{bmatrix}
        \phantom{=} \\[1em] = & \phantom{.} \
            \begin{bmatrix}
                3 \\
                4 \\
                5
            \end{bmatrix}
            \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">20</span>

The matrix multiplication

$$
    \phantom{,} \
        \mathbf{P}_1 \begin{bmatrix}
            x \\
            y
        \end{bmatrix}
    =
        \begin{bmatrix}
            1 & 0 \\
            0 & 0
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y
        \end{bmatrix}
    =
        \begin{bmatrix}
            x \\ 0
        \end{bmatrix}
    \ ,
$$

which is a $[x,y]^{-t}$ vector projection onto the $x$-axis.

When

$$
    \phantom{,} \
        \mathbf{P}_2 = \begin{bmatrix}
            0 & 0 \\
            0 & 1
        \end{bmatrix}
    \ ,
$$

$$
    \phantom{.} \
        \mathbf{P}_2 \begin{bmatrix}
            x \\ y 
        \end{bmatrix}
        =
        \begin{bmatrix}
            0 \\ y
        \end{bmatrix}
    \ .
$$

which in turn is a $[x,y]^{-t}$ vector projection onto the $y$-axis.

Moreover,

$$
    \phantom{.} \
        \mathbf{P}_2 (\mathbf{P}_1 \mathbf{x})
        =
        \mathbf{P}_2 \begin{bmatrix}
            x \\ 0
        \end{bmatrix}
        =
        \mathbf{0}
    \ ,
$$

i.e. $\mathbf{P}_2(\mathbf{P}_1 \mathbf{x})$ is equal to the zero matrix
$\mathbf{0}$.

<span class = "exercise-tag">21</span>

--

<span class = "exercise-tag">22</span>

The equation written  as a linear combinarion is

<div class = "widescreen">
$$
    \phantom{.} \
        \mathbf{Ax} = \begin{bmatrix}
            1 & 4 & 5
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y \\ z
        \end{bmatrix}
        =
            x + 4y + 5 z
        =
        0
        =
        \mathbf{0}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c }
        \phantom{=} & \mathbf{Ax} & \phantom{=}
        \\[0.5em] = &
            \begin{bmatrix}
                1 & 4 & 5
            \end{bmatrix}
            \begin{bmatrix}
                x \\ y \\ z
            \end{bmatrix}
        & \\[0.5em] = &
            x + 4y + 5 z
        & \\[1em] = &
            0
        & \\[1em] = &
            \phantom{.} \ \mathbf{0} \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">23</span>

The MATLAB/Octave command for the matrix $\mathbf{A}$ is

```matlab
>> A = [1, 2; 3, 4];
```

for the vector $\mathbf{x}$ the command is

```matlab
>> x = [5; -2];
```

and for the solution vector $\mathbf{b}$ the command is

```matlab
>> b = [1; 7];
```

A command that would test whether or not $\mathbf{Ax} = \mathbf{b}$ is

```matlab
>> isequal(A * x, b)
```

Running these command in the order of appearance says reveals that
$\mathbf{Ax} = \mathbf{b}$ is true.

<span class = "exercise-tag">24</span>

The output of command

```matlab
>> A * v
```

is

```matlab
ans =

   3
   4
   5
```

and the output of the command

```matlab
>> v' * v
```

is

```matlab
ans =

  50
```

Trying to run the command

```matlab
>> v * A;
```

produces an error, because trying to multpy a $3 \times 1$ and $3 \times 3$
is not defined in general.

<span class = "exercise-tag">25</span>

The output of the command

```matlab
>> A * v
```

is

```matlab
ans =

  4
  4
  4
  4
```

and the output of the second command is

```matlab
>> B * w
```

is

```matlab
ans =

  10
  10
  10
  10
```
