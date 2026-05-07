+++
title  = "Problems 1-15"
layout = "solution-single"
+++

<span class = "exnum">1</span> **(a)** When matrix

$$
    \mathbf{E}_{21} = \begin{bmatrix}
         \phantom{-}1 & 0 & 0 \\
                   -5 & 1 & 0 \\
         \phantom{-}0 & 0 & 1
    \end{bmatrix}
$$

the product

<div class = "widescreen">
$$
    \phantom{,}
        \mathbf{E}_{21}\mathbf{A} = \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
                      -5 & 1 & 0 \\
            \phantom{-}0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            a_{11} & a_{12} & a_{13} \\
            a_{21} & a_{22} & a_{23} \\
            a_{31} & a_{32} & a_{33}
        \end{bmatrix}
    =
        \begin{bmatrix}
            a_{11}           & a_{12}           & a_{13}           \\
            a_{21} - 5a_{11} & a_{22} - 5a_{12} & a_{23} - 5a_{13} \\
            a_{31}           & a_{32}           & a_{33}
        \end{bmatrix}
    ,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
         & \mathbf{E}_{21}\mathbf{A}
    \\[0.5em] = & \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
                      -5 & 1 & 0 \\
            \phantom{-}0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            a_{11} & a_{12} & a_{13} \\
            a_{21} & a_{22} & a_{23} \\
            a_{31} & a_{32} & a_{33}
        \end{bmatrix}
    \\[0.5em] = &
        \begin{bmatrix}
            a_{11}           & a_{12}           & a_{13}           \\
            a_{21} - 5a_{11} & a_{22} - 5a_{12} & a_{23} - 5a_{13} \\
            a_{31}           & a_{32}           & a_{33}
        \end{bmatrix}
    \end{array}
$$
</div>

so the first row of $\mathbf{A}$ gets subtracted from the second five times.

**(b)** For matrix $\mathbf{E}_{32}$ that subtracts $-7$, that is,
adds $7$ times the second row from the third row the logic is
similar, i.e., when

$$
    \mathbf{E}_{32} = \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 1 & 0 \\
        0 & 7 & 1
    \end{bmatrix}
$$

the product

<div class = "widescreen">
$$
    \phantom{.}
        \mathbf{E}_{32}\mathbf{A} = \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
            0 & 7 & 1
        \end{bmatrix}
        \begin{bmatrix}
            a_{11} & a_{12} & a_{13} \\
            a_{21} & a_{22} & a_{23} \\
            a_{31} & a_{32} & a_{33}
        \end{bmatrix}
    =
        \begin{bmatrix}
            a_{11}           & a_{12}           & a_{13} \\
            a_{21}           & a_{22}           & a_{23} \\
            a_{31} + 7a_{21} & a_{32} + 7a_{22} & a_{33} + 7a_{23}
        \end{bmatrix}
    .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
            & \mathbf{E}_{32}\mathbf{A}
        \\[0.5em] = &
            \begin{bmatrix}
                1 & 0 & 0 \\
                0 & 1 & 0 \\
                0 & 7 & 1
            \end{bmatrix}
            \begin{bmatrix}
                a_{11} & a_{12} & a_{13} \\
                a_{21} & a_{22} & a_{23} \\
                a_{31} & a_{32} & a_{33}
            \end{bmatrix}
        \\[0.5em] = &
            \begin{bmatrix}
                a_{11}           & a_{12}           & a_{13} \\
                a_{21}           & a_{22}           & a_{23} \\
                a_{31} + 7a_{21} & a_{32} + 7a_{22} & a_{33} + 7a_{23}
            \end{bmatrix}
    \end{array}
$$
</div>

**(c)** Matrix

$$
    \mathbf{P}_{12}
    =
    \begin{bmatrix}
        0 & 1 & 0 \\
        1 & 0 & 0 \\
        0 & 0 & 1
    \end{bmatrix}
$$

and

$$
    \mathbf{P}_{23}
    =
    \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 0 & 1 \\
        0 & 1 & 0
    \end{bmatrix}
$$

the multiplication

$$
    \begin{array}{r c l}
        \mathbf{P}_{21} \mathbf{A}
    & = &
        \begin{bmatrix}
            0 & 1 & 0 \\
            1 & 0 & 0 \\
            0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            \textcolor{red}{a_{11}}  & \textcolor{red}{a_{12}}  & \textcolor{red}{a_{13}}  \\
            \textcolor{blue}{a_{21}} & \textcolor{blue}{a_{22}} & \textcolor{blue}{a_{23}} \\
            a_{31}                   & a_{32}                   & a_{33}
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            0\textcolor{red}{a_{11}} + 1\textcolor{blue}{a_{21}} + 0a_{31} & 0\textcolor{red}{a_{12}} + 1\textcolor{blue}{a_{22}} + 0a_{32} & 0\textcolor{red}{a_{13}} + 1\textcolor{blue}{a_{23}} + 0a_{33}\\
            1\textcolor{red}{a_{11}} + 0\textcolor{blue}{a_{21}} + 0a_{31} & 1\textcolor{red}{a_{12}} + 0\textcolor{blue}{a_{22}} + 0a_{32} & 1\textcolor{red}{a_{13}} + 0\textcolor{blue}{a_{23}} + 0a_{33}\\
            0\textcolor{red}{a_{11}} + 0\textcolor{blue}{a_{21}} + 1a_{31} & 0\textcolor{red}{a_{12}} + 0\textcolor{blue}{a_{22}} + 1a_{32} & 0\textcolor{red}{a_{13}} + 0\textcolor{blue}{a_{23}} + 1a_{33}
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            \textcolor{blue}{a_{21}} & \textcolor{blue}{a_{22}} & \textcolor{blue}{a_{23}} \\
            \textcolor{red}{a_{11}}  & \textcolor{red}{a_{12}}  & \textcolor{red}{a_{13}} \\
            a_{31} & a_{32} & a_{33}
        \end{bmatrix}
    \end{array}
$$

and so multiplying the product further with $\mathbf{P}_{23}$ means
that

$$
    \phantom{.}
        \mathbf{P}_{23} \mathbf{P}_{21} \mathbf{A}
    =
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 0 & 1 \\
            0 & 1 & 0
        \end{bmatrix}
        \begin{bmatrix}
            \textcolor{blue}{a_{21}} & \textcolor{blue}{a_{22}} & \textcolor{blue}{a_{23}} \\
            \textcolor{red}{a_{11}}  & \textcolor{red}{a_{12}}  & \textcolor{red}{a_{13}}  \\
            a_{31}                   & a_{32}                   & a_{33}
        \end{bmatrix}
    =
        \begin{bmatrix}
            \textcolor{blue}{a_{21}} & \textcolor{blue}{a_{22}} & \textcolor{blue}{a_{23}} \\
            a_{31}                   & a_{32}                   & a_{33}                   \\
            \textcolor{red}{a_{11}}  & \textcolor{red}{a_{12}}  & \textcolor{red}{a_{13}}
        \end{bmatrix}
    .
$$

<span class = "exnum">2</span> The matrix multiplication

$$
    \begin{array}{r c l}
        \mathbf{E}_{32} \mathbf{E}_{21} \mathbf{b}
    & = &
        \mathbf{E}_{32}
        \left(
            \begin{bmatrix}
                \phantom{-}1 & 0 & 0 \\            
                          -5 & 1 & 0 \\            
                \phantom{-}0 & 0 & 1 \\            
            \end{bmatrix}
            \begin{bmatrix}
                b_1 \\ b_2 \\ b_3
            \end{bmatrix}
        \right)
    \\[0.5em] & = &
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
            0 & 7 & 1 \\
        \end{bmatrix}
        \begin{bmatrix}
            b_1 \\ b_2  - 5b_1 \\ b_3
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            b_1 \\ b_2  - 5b_1 \\ b_3 + 7(b_2 - 5b_1)
        \end{bmatrix}
    \end{array}
$$

while the matrix multiplication

$$
    \begin{array}{r c l}
        \mathbf{E}_{21} \mathbf{E}_{32} \mathbf{b}
    & = &
        \mathbf{E}_{21}
        \left(
            \begin{bmatrix}
                1 & 0 & 0 \\            
                0 & 1 & 0 \\            
                0 & 7 & 1
            \end{bmatrix}
            \begin{bmatrix}
                b_1 \\ b_2 \\ b_3
            \end{bmatrix}
        \right)
    \\[0.5em] & = &
        \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
                      -5 & 1 & 0 \\
            \phantom{-}0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            b_1 \\ b_2 \\ b_3 + 7b_2
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            b_1 \\ b_2 - 5b_1 \\ b_3 + 7_b2
        \end{bmatrix},
    \end{array}
$$

so the associativity does now hold between $\mathbf{E}_{21}$ and
$\mathbf{E}_{32}$. When $\mathbf{E}_{32}$ comes first, row _three_
feels no eddect from row _two_.

<span class = "exnum">3</span> Solving the $\mathbf{A}$ with the
elimination method reveals the matrices. The steps are as follows,
the first row gets subtracts from the second two times, so

$$
    \mathbf{E}_{21} = \begin{bmatrix}
        \phantom{-}1 & 0 & 0 \\
                  -4 & 1 & 0 \\
        \phantom{-}0 & 0 & 1
    \end{bmatrix}.
$$

The matrix multiplication

<div class = "widescreen">
$$
        \mathbf{E}_{21} \mathbf{A}
    =
        \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
                      -4 & 1 & 0 \\
            \phantom{-}0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            \phantom{-}1 & 1 & 0 \\
            \phantom{-}4 & 6 & 1 \\
                      -2 & 2 & 0 \\
        \end{bmatrix}
    =
        \begin{bmatrix}
            \phantom{-}1 & 1 & 0 \\
            \phantom{-}0 & 2 & 1 \\
                      -2 & 2 & 0 \\
        \end{bmatrix}
    =
        \mathbf{A}^\prime
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        \mathbf{E}_{21} \mathbf{A}
    & = &
        \begin{bmatrix}
            \phantom{-}1 & 0 & 0 \\
                      -4 & 1 & 0 \\
            \phantom{-}0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            \phantom{-}1 & 1 & 0 \\
            \phantom{-}4 & 6 & 1 \\
                      -2 & 2 & 0
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            \phantom{-}1 & 1 & 0 \\
            \phantom{-}0 & 2 & 1 \\
                      -2 & 2 & 0
        \end{bmatrix}
    \\[0.5em] & = &
        \mathbf{A}^\prime
    \end{array}
$$
</div>

Adding first row to third twice brings the $-2$ to zero. This
equates to matrix

$$
    \mathbf{E}_{31} = \begin{bmatrix}
        1 & 0 & 0 \\ 
        0 & 1 & 0 \\ 
        2 & 0 & 1
    \end{bmatrix}
$$

so

<div class = "widescreen">
$$
        \mathbf{E}_{31} \mathbf{A}^\prime
    =
        \begin{bmatrix}
            1 & 0 & 0 \\        
            0 & 1 & 0 \\
            2 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            \phantom{-}1 & 1 & 0 \\
            \phantom{-}0 & 2 & 1 \\
                      -2 & 2 & 0
        \end{bmatrix}
    =
        \begin{bmatrix}
            1 & 1 & 0 \\
            0 & 2 & 1 \\
            0 & 4 & 0
        \end{bmatrix}
    =
        \mathbf{A}^{\prime\prime}.
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
            \mathbf{E}_{31} \mathbf{A}^\prime
        & = &
            \begin{bmatrix}
                1 & 0 & 0 \\        
                0 & 1 & 0 \\
                2 & 0 & 1
            \end{bmatrix}
            \begin{bmatrix}
                \phantom{-}1 & 1 & 0 \\
                \phantom{-}0 & 2 & 1 \\
                          -2 & 2 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1 & 1 & 0 \\
                0 & 2 & 1 \\
                0 & 4 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \mathbf{A}^{\prime\prime}.
    \end{array}
$$
</div>

Last matrix should be of the form that subtracts row two from row
three twice. A matrix

$$
    \mathbf{E}_{32}
    =
    \begin{bmatrix}
        1 &  0 & 0 \\
        0 &  1 & 0 \\
        0 & -2 & 1
    \end{bmatrix}
$$

is such a matrix because

<div class = "widescreen">
$$
        \mathbf{E}_{32} \mathbf{A}^{\prime\prime}
    =
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
            0 & -2 & 1
        \end{bmatrix}
        \begin{bmatrix}
            1 & 1 & 0 \\
            0 & 2 & 1 \\
            0 & 4 & 0
        \end{bmatrix}
    =
        \begin{bmatrix}
            1 & 1 & \phantom{-}0 \\
            0 & 2 & \phantom{-}1 \\
            0 & 0 & -2
        \end{bmatrix}
    =
        \mathbf{A}^{\prime\prime\prime}
    =
        \mathbf{E}_{21} \mathbf{E}_{31} \mathbf{E}_{32} \mathbf{A}
    =
        \mathbf{U}.
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
            \mathbf{E}_{32} \mathbf{A}^{\prime\prime}
        & = &
            \begin{bmatrix}
                1 & 0 & 0 \\
                0 & 1 & 0 \\
                0 & 2 & 1
            \end{bmatrix}
            \begin{bmatrix}
                1 & 1 & 0 \\
                0 & 2 & 1 \\
                0 & 4 & 0
            \end{bmatrix}
        \\[0.5em] & = &
            \begin{bmatrix}
                1 & 1 & \phantom{-}0 \\
                0 & 2 & \phantom{-}1 \\
                0 & 0 & -2
            \end{bmatrix}
        \\[0.5em] & = &
            \mathbf{A}^{\prime\prime\prime}
        \\[0.5em] & = &
            \mathbf{E}_{21} \mathbf{E}_{31} \mathbf{E}_{32} \mathbf{A}
        \\[0.5em] & = &
            \mathbf{U}.
    \end{array}
$$
</div>

By itself,

$$
    \mathbf{E}_{21} \mathbf{E}_{31} \mathbf{E}_32 = \begin{bmatrix}
         1 &  0 & 0 \\
        -4 &  1 & 0 \\
        10 & -2 & 1
    \end{bmatrix}.
$$

<span class = "exnum">4</span> Augmenting matrix $\mathbf{A}$ of
<span class = "exnum">3</span>, call it $\mathbf{A}^\prime$, with
$\mathbf{b}$ $=$ $\begin{bmatrix}1 & 0 & 0\end{bmatrix}^\top$ leads
to augmented matrix

$$
    \mathbf{A}^\prime = \left[
        \begin{array}{c c c | c}
            \phantom{-}1 & 1 & 0 & 1 \\
            \phantom{-}4 & 6 & 1 & 0 \\
                      -2 & 2 & 0 & 0 \\
        \end{array}
    \right]
$$

and doing the multiplication $\mathbf{E}_{21} \mathbf{E}_{31}
\mathbf{E}_{32} \mathbf{A}$ leads to

$$
    \begin{bmatrix}
        1 & 1 &  0 &  1 \\
        0 & 2 &  1 & -4 \\
        0 & 0 & -2 & 10
    \end{bmatrix}.
$$

<span class = "exnum">5</span>

...

<span class = "exnum">6</span> A matrix whose every column is
multiple of $\begin{bmatrix} 1 & 1 & 1 \end{bmatrix}^\top$ is
a matrix like

$$
    \mathbf{A} = \begin{bmatrix}
        1 & 3 & 5 \\
        1 & 3 & 5 \\
        1 & 3 & 5
    \end{bmatrix}.
$$

Applying elimination to this matrix leads to matrix
$$
    \mathbf{A} = \begin{bmatrix}
        1 & 3 & 5 \\
        0 & 0 & 0 \\
        1 & 3 & 5
    \end{bmatrix},
$$

and then with one row exchange to matrix

$$
    \mathbf{A} = \begin{bmatrix}
        1 & 3 & 5 \\
        0 & 0 & 0 \\
        0 & 0 & 0
    \end{bmatrix},
$$

so it is possible to only one pivot, though technically it is found
more then once.

<span class = "exnum">7</span> Matrix that subracts $7$ times row
$1$ from row $3$ is matrix

$$
    \mathbf{E} = \begin{bmatrix}
         1 & 0 & 0 \\
         0 & 1 & 0 \\
        -7 & 0 & 1 \\
    \end{bmatrix}.
$$

**(a)** To invert the operation that $\mathbf{E}$ does when it's
left multplying some matrix, a matrix that <i>adds</i> $7$ times
the row $3$ to row $1$ is needed. Such matrix is

$$
    \mathbf{E}^{-1} = \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 1 & 0 \\
        7 & 0 & 1
    \end{bmatrix}.
$$

**(b)** The matrix product

$$
    \mathbf{E}^{-1} \mathbf{E}
    =
    \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 1 & 0 \\
       -7 & 0 & 1 \\
    \end{bmatrix}
    \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 1 & 0 \\
        7 & 0 & 1
    \end{bmatrix},
$$

so the product's first column is

$$
        \begin{bmatrix}
            1(1)  & + & 0(0) & + & 0(0) \\
            1(0)  & + & 0(1) & + & 0(0) \\
            1(-7) & + & 0(0) & + & 7(1) \\
        \end{bmatrix}
    =
        \begin{bmatrix}
            1 \\ 0 \\ 0
        \end{bmatrix}
$$

and the second and third are obviously

$$
    \begin{bmatrix}
        0 \\ 1 \\ 0
    \end{bmatrix}
$$

and

$$
    \begin{bmatrix}
        0 \\ 0 \\ 1
    \end{bmatrix},
$$

respctively, so

$$
    \mathbf{E}^{-1} \mathbf{E}
    =
    \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 1 & 0 \\
        0 & 0 & 1
    \end{bmatrix}
    =
    \mathbf{I}.
$$

**(c)** If the reverse step is applied first, then

$$
        \mathbf{E} \mathbf{E}^{-1}
    =
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
            7 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0 \\
           -7 & 0 & 1 \\
        \end{bmatrix}
$$

the first column of the product is still $\begin{bmatrix} 1 & 0 &
0\end{bmatrix}^\top$, and the second and third row are as above, so
the product $\mathbf{E^{-1}} \mathbf{E}$ $=$ $\mathbf{I}$.

<span class = "exnum">8</span>

...

<span class = "exnum">9</span> **(a)** The

$$
    \mathbf{E}_{21} = \begin{bmatrix}
        1  & 0 & 0 \\
        -1 & 1 & 0 \\
        0  & 0 & 1
    \end{bmatrix}
$$

and

$$
    \mathbf{P}_{23} = \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 0 & 1 \\
        0 & 1 & 0
    \end{bmatrix}
$$

so

$$
    \mathbf{P}_{23} \mathbf{E}_{21} = \begin{bmatrix}
         1 & 0 & 0 \\
         0 & 0 & 1 \\
        -1 & 1 & 0
    \end{bmatrix}.
$$

**(b)** The matrix $\mathbf{P}_{23}$ is as above, but

$$
    \mathbf{E}_{31}
    =
    \begin{bmatrix}
        1 & 0 & 0 \\
        0 & 1 & 0 \\
       -1 & 0 & 1
    \end{bmatrix},
$$

so

$$
    \mathbf{E}_{31} \mathbf{P}_{23}
    =
    \begin{bmatrix}
         1 & 0 & 0 \\
         0 & 0 & 1 \\
        -1 & 1 & 0
    \end{bmatrix}.
$$

<span class = "exnum">10</span>

**(a)** Exchange matrix

$$
    \mathbf{E}_{13}
    =
    \begin{bmatrix}
        1 & 0 & 1 \\
        0 & 1 & 0 \\
        0 & 0 & 1
    \end{bmatrix}
$$

will add row $3$ to row $1$. For example, let matrix $\mathbf{A}$
be a $3 \times 3$ matrix. Then

$$
    \begin{array}{r c l}
        \mathbf{E}_{13} \mathbf{A}
    & = &
        \begin{bmatrix}
            1 & 0 & 1 \\
            0 & 1 & 0 \\
            0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            a_{11} & a_{12} & a_{13} \\
            a_{21} & a_{22} & a_{23} \\
            a_{31} & a_{32} & a_{33}
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            a_{11} + a_{31} & a_{12} + a_{32} & a_{13} + a_{33} \\
            a_{21}          & a_{22}          & a_{23}          \\
            a_{31}          & a_{32}          & a_{33}
        \end{bmatrix}.
    \end{array}
$$

**(b)** A matrix that adds row $1$ to row $3$ and at the same time,
vice versa, is matrix

$$
    \mathbf{E}
    =
    \begin{bmatrix}
        1 & 0 & 1 \\
        0 & 1 & 0 \\
        1 & 0 & 1
    \end{bmatrix}.
$$

because

$$
    \begin{array}{r c l}
        \mathbf{E} \mathbf{A}
    & = &
        \begin{bmatrix}
            1 & 0 & 1 \\
            0 & 1 & 0 \\
            1 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            a_{11} & a_{12} & a_{13} \\
            a_{21} & a_{22} & a_{23} \\
            a_{31} & a_{32} & a_{33}
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            a_{11} + a_{31} & a_{12} + a_{32} & a_{13} + a_{33} \\
            a_{21}          & a_{22}          & a_{23}          \\
            a_{31} + a_{11} & a_{32} + a_{12} & a_{33} + a_{13}
        \end{bmatrix}.
    \end{array}
$$

**(c)** A matrix that adds row $1$ to row $3$ and then vice versa,
is a matrix

...

<span class = "exnum">11</span> Matrix that has $a_{11}$ $=$ $a_{22}$ $=$
$a_{33}$ $=$ $1$ and that produces two negative pivots after elimination
when no row exchange are not allowed is

$$
    \begin{bmatrix}
        1      & a & b \\
        m_{21} & 1 & c \\
        m_{31} & d & 1 \\
    \end{bmatrix}
$$

where $m_{21}$ $<$ $0$ and $m_{31}$ $\leq$ $m_{21}$, because
subtracting first row from the second leads to pivot $m_{21}$ $-$
$\frac{m_{21}}{1}$ $=$ $m_{21}$ $-$ $m_{21}$ $<$ $0$. The same goes
for the row of $m_{31}$ no matter if the first or the second row is
subtracted.

<span class = "exnum">12</span> The first product is

$$
    \begin{bmatrix}
        0 & 0 & 1 \\
        0 & 1 & 0 \\
        1 & 0 & 0
    \end{bmatrix}
    \begin{bmatrix}
        1 & 2 & 3 \\
        4 & 5 & 6 \\
        7 & 8 & 9
    \end{bmatrix}
    =
    \begin{bmatrix}
        7 & 8 & 9 \\
        4 & 5 & 6 \\
        1 & 2 & 3
    \end{bmatrix}
$$

and the second

$$
    \begin{bmatrix}
        7 & 8 & 9 \\
        4 & 5 & 6 \\
        1 & 2 & 3
    \end{bmatrix}
    \begin{bmatrix}
        0 & 0 & 1 \\
        0 & 1 & 0 \\
        1 & 0 & 0
    \end{bmatrix}
    =
    \begin{bmatrix}
        9 & 8 & 7 \\
        6 & 5 & 4 \\
        3 & 2 & 1
    \end{bmatrix}.
$$

The multiplication resulted in a permutation of the middle matrix
where first the top and bottom rows swapped, and then left and
right columns.

The second product is

$$
    \begin{bmatrix}
         1 & 0 & 0 \\
        -1 & 1 & 0 \\
        -1 & 0 & 1
    \end{bmatrix}
    \begin{bmatrix}
        1 & 2 & 3 \\
        1 & 3 & 1 \\
        1 & 4 & 0
    \end{bmatrix}
    =
    \begin{bmatrix}
        1 & 2 & 3  \\
        0 & 1 & -2 \\
        0 & 2 & -3
    \end{bmatrix}.
$$

<span class = "exnum">13</span> If all of the elements of third
column of $\mathbf{B}$ are all zeros, then multiplying $\mathbf{B}$
with $\mathbf{E}$ yields the product $\mathbf{EB}$ which third
column is always zeros because linear combination between the
column and matrix $\mathbf{E}$ always leads to $0$, or in other
words

$$
      b_{31} \mathbf{e}_1
    + b_{32} \mathbf{e}_2
    + b_{33} \mathbf{e}_3
    \cdots
    + b_{n3} \mathbf{e}_n
    =
    \begin{bmatrix}
        0 \\ 0 \\ 0 \\ \vdots \\ 0
    \end{bmatrix}
$$

where $b_{i3}$ is the $i$th zero of $B$ and $\mathbf{e}_i$, is
$i$th column of matrix $\mathbf{E}$.

On the other hand, if the third row of $\mathbf{B}$ are all zero,
the coefficients $b_{i3}$, might not all be zero, so the dor
product leads vector that might have a non-zero component.

<span class = "exnum">15</span>

...

