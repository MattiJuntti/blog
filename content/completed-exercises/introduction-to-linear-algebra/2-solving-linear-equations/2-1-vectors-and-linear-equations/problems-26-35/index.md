+++
title  = "Problems 26-35"
date   = "2025-01-01T00:00:00+03:00"
layout = "solution-single"
+++

<span class = "exercise-tag">26</span>

--

<span class = "exercise-tag">27</span>

The row picture will show $2$ planes in $3$-dimensional space. The column
picture is in $2$-dimensional space. The solutions normally lie on a line
in **$\mathbf{3}$-D** space.

<span class = "exercise-tag">28</span>

For four linear equations in two unknowns $x$ and $y$, the row picture
shows four **in a lines in 2-D plane**. The column picture is in
$2-dimensional space$. The equations have no solution unless the vector on
the right side is a combination of **of the vectors on the left side**.

<span class = "exercise-tag">29</span>

If

$$
    \phantom{.} \
        \mathbf{u}_1 = \begin{bmatrix}
            0.8 & 0.3 \\
            0.2 & 0.7
        \end{bmatrix}
        \begin{bmatrix}
            1 \\ 0
        \end{bmatrix}
        =
        \begin{bmatrix}
            0.8 \\ 0.2
        \end{bmatrix}
    \ ,
$$

then

$$
    \mathbf{u}_2 = \mathbf{Au}_1 = \begin{bmatrix}
       - \\ - 
    \end{bmatrix}
$$

<span class = "exercise-tag">29</span> &ndash; <span class = "exercise-tag">29</span>

Solved in a blog [post]({{< ref "post/simple-markov-chain/index.md" >}}).

<span class = "exercise-tag">31</span>

Example of such matrix is

Step for finding such a matrix is starting with the given first row

$$
        \begin{array}{c | c}
            \begin{bmatrix}
                8 & 3 & 4 \\
                  &   &   \\
                  &   &
            \end{bmatrix}
            &
                \begin{array}{l}
                    \text{Remaining:} \\
                    \{ 1, 2, 5, 6, 7, 9 \} \ .
                \end{array}
        \end{array}
$$

Then taking $5$ and $2$ from the &ldquo;$\text{Remaining}$&rdquo; numbers
and adding the to diagonal leads to $8 + 5 + 2 = 15$, so the matrix can be
updated into form

$$
        \begin{array}{c | c}
            \begin{bmatrix}
                8 & 3                      & 4 \\
                  & \textcolor{#FF6868}{5} & \\
                  &                        & \textcolor{#FF6868}{2}
            \end{bmatrix}
            &
                \begin{array}{l}
                    \text{Remaining:} \\
                    \{ 1, 6, 7, 9 \} \ .
                \end{array}
        \end{array}
$$

Additionally from the anti-diagonal, it's possible to see a simple eqution
$4 + 5 + x = 15$, and by solving for $x$, we see that $x = 6$, so matrix
can be updated

$$
        \begin{array}{c | c}
            \begin{bmatrix}
                8                      & 3 & 4 \\
                                       & 5 & \\
                \textcolor{#FF6868}{6} &   & 2
            \end{bmatrix}
            &
                \begin{array}{l}
                    \text{Remaining:} \\
                    \{ 1, 7, 9 \} \ .
                \end{array}
        \end{array}
$$

Now because

$$
    \begin{array}{r c l}
        15 & = & 8 + 3 + 4 \\
           & = & 8 + 5 + 2 \\
           & = & 4 + 5 + 6 \ ,
    \end{array}
$$

everything looks okay. Then because $6 + 7 + 2 = 15$ and $3 + 5 + 7 = 15$,
the matrix can be updated as

$$
        \begin{array}{c | c}
            \begin{bmatrix}
                8                      & 3 & 4 \\
                                       & 5 & \\
                6 & \textcolor{#FF6868}{7} & 2
            \end{bmatrix}
            &
                \begin{array}{l}
                    \text{Remaining:} \\
                    \{ 1, 9 \} \ .
                \end{array}
        \end{array}
$$

From the current matrix and the numbers &ldquo;$\text{Remaining}$&rdquo;,
it should be relatively easy to see three new simple arithmetic equations

$$
    \begin{array}{r c l}
        8 + x + 6 = 15 \ , \\[0.5em]
        x + 5 + y = 15 \ , \\[0.5em]
        4 + y + 2 = 15 \ ,
    \end{array}
$$

and by letting $x = 1$, then the equations are

$$
    \begin{array}{r c l}
        8 + 1 + 6 = 15 \ , & \textcolor{green}{\checkmark} \\[0.5em]
        1 + 5 + y = 15 \ , & \\[0.5em]
        4 + y + 2 = 15 \ . &
    \end{array}
$$

and remainig there's only $9$, so letting $y$ to have that value, the
set of equations become

$$
    \begin{array}{r c l}
        8 + 1 + 6 = 15 \ , & \textcolor{green}{\checkmark} \\[0.5em]
        1 + 5 + 9 = 15 \ , & \textcolor{green}{\checkmark} \\[0.5em]
        4 + 0 + 2 = 15 \ , & \textcolor{green}{\checkmark}
    \end{array}
$$

so everything checks. Now updating the matrix with this info, the matrix
becomes

$$
        \begin{array}{c | c}
            \begin{bmatrix}
                8                      & 3 & 4 \\
                \textcolor{#FF6868}{1} & 5 & \textcolor{#FF6868}{9}\\
                6                      & 7 & 2
            \end{bmatrix}
            &
                \begin{array}{l}
                    \text{Remaining:} \\
                    \varnothing \ .
                \end{array}
        \end{array}
$$

Now chcking the values of all rows, columns, and the diagonal and the
anti-diagonal add up to 15, a table can be written such that

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | }
        \begin{array}{r c}
            \ 8 + 3 + 4 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 1 + 5 + 9 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 6 + 7 + 2 = 15 & \textcolor{green}{\checkmark} \
        \end{array}
        &
        \begin{array}{r c}
            \ 8 + 1 + 6 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 3 + 5 + 7 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 4 + 9 + 2 = 15 & \textcolor{green}{\checkmark} \
        \end{array}
        &
        \begin{array}{r c}
            \ 8 + 5 + 2 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 4 + 5 + 6 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ \phantom{8 + 5 + 9 = 15 } &
        \end{array}
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c }
        \begin{array}{r c}
            \ 8 + 3 + 4 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 1 + 5 + 9 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 6 + 7 + 2 = 15 & \textcolor{green}{\checkmark} \
        \end{array}
    \\[1em] \hline
        \begin{array}{r c}
            \ 8 + 1 + 6 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 3 + 5 + 7 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 4 + 9 + 2 = 15 & \textcolor{green}{\checkmark} \
        \end{array}
    \\[1em] \hline
        \begin{array}{r c}
            \ 8 + 5 + 2 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ 4 + 5 + 6 = 15 & \textcolor{green}{\checkmark} \ \\[0.5em]
            \ \phantom{8 + 5 + 9 = 15 } &
        \end{array}
    \end{array}
$$
</div>

from where it can be seen that the matrix the exercise is asking for is

$$
    \phantom{.} \
        \begin{bmatrix}
            8 & 3 & 4 \\
            1 & 5 & 9 \\
            6 & 7 & 2
        \end{bmatrix}
        =
        \mathbf{M}_3
    \ .
$$

The

<div class = "widescreen">
$$
    \phantom{.} \
        \mathbf{M}_3 \begin{bmatrix}
            1 \\ 1 \\ 1
        \end{bmatrix}
        =
        \begin{bmatrix}
            8 & 3 & 4 \\
            1 & 5 & 9 \\
            6 & 7 & 2
        \end{bmatrix}
        \begin{bmatrix}
            1 \\ 1 \\ 1
        \end{bmatrix}
        =
        \begin{bmatrix}
            8 + 3 + 4 \\
            1 + 5 + 9 \\
            6 + 7 + 2
        \end{bmatrix}
        =
        \begin{bmatrix}
            15 \\ 15 \\ 15
        \end{bmatrix}
    \ .
$$
</div>

<div class = "smallscreen">
$$
        \begin{array}{ c c c }
            \phantom{=} &
                \mathbf{M}_3 \begin{bmatrix}
                    1 \\ 1 \\ 1
                \end{bmatrix}
            &\phantom{=} \\[1em] = &
                \begin{bmatrix}
                    8 & 3 & 4 \\
                    1 & 5 & 9 \\
                    6 & 7 & 2
                \end{bmatrix}
                \begin{bmatrix}
                    1 \\ 1 \\ 1
                \end{bmatrix}
            &\phantom{=} \\[1em] = &
                \begin{bmatrix}
                    8 + 3 + 4 \\
                    1 + 5 + 9 \\
                    6 + 7 + 2
                \end{bmatrix}
            &\phantom{=} \\[1em] = &
                \phantom{.} \
                    \begin{bmatrix}
                        15 \\ 15 \\ 15
                    \end{bmatrix}
                \ .
        \end{array}
$$
</div>

<span class = "exercise-tag">32</span>

If the third column is $\mathbf{u} + \mathbf{v}$. Column picture has
$\mathbf{b}$ outside the plane of $\mathbf{u}$, $\mathbf{v}$, and
$\mathbf{w}$. Rowpicture is an intersection of two planes parallel to a
third plane.

<span class = "exercise-tag">33</span>

--

<span class = "exercise-tag">34</span>

The matrix equation form is

$$
    \phantom{.} \
    \mathbf{Ax} = \begin{bmatrix}
        \phantom{-}2 & -1           & \phantom{-}0 & \phantom{-}0 \\
        -1           & \phantom{-}2 & -1           & \phantom{-}0 \\
        \phantom{-}0 & -1           & \phantom{-}2 & -1           \\
        \phantom{-}0 & \phantom{-}0 & -1           & \phantom{-}2
    \end{bmatrix}
    \begin{bmatrix}
        x_1 \\ x_2 \\ x_3 \\ x_4
    \end{bmatrix}
    =
    \begin{bmatrix}
        1 \\ 2 \\ 3 \\ 4
    \end{bmatrix}
    \ .
$$

<span class = "exercise-tag">35</span>

Such a Sudoku-matrixj is

$$
    \phantom{.} \
    \mathbf{S}
    =
    \left[ \
        \begin{array}{ | c c c | c c c | c c c | } \hline
            1 & 5 & 2 & 4 & 8 & 9 & 3 & 7 & 6 \\
            7 & 3 & 9 & 2 & 5 & 6 & 8 & 4 & 1 \\
            4 & 6 & 8 & 3 & 7 & 1 & 2 & 9 & 5 \\ \hline
            3 & 8 & 7 & 1 & 2 & 4 & 6 & 5 & 9 \\
            5 & 9 & 1 & 7 & 6 & 3 & 4 & 2 & 8 \\
            2 & 4 & 6 & 8 & 9 & 5 & 7 & 1 & 3 \\ \hline
            9 & 1 & 4 & 6 & 3 & 7 & 5 & 8 & 2 \\
            6 & 2 & 5 & 9 & 4 & 8 & 1 & 3 & 7 \\
            8 & 7 & 3 & 5 & 1 & 2 & 9 & 6 & 4 \\ \hline
        \end{array} 
    \ \right]
    \ .
$$

The matrix multiplication

$$
    \mathbf{Sx}
$$

when $\mathbf{x} = [ \ 1_1, 1_2, \ldots, 1_9 \ ]^\top$ will produce a
vector, where each $i$th component is sum of $i$th row of $S$, i.e.

$$
    \phantom{.} \ 1 + 2 + \cdots + 9 = 45 \ .
$$

The following is lazy answer, but changing the first and the second row
will not break the requirement for $\mathbf{S}$. So if the row exchanges
are done within the boundaries of a horizontal blocks, then it is possible
to have multiple Sudoku-matrices, but there might be other ways too.
