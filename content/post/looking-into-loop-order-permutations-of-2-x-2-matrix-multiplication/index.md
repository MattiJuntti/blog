+++
title = 'Looking into loop order permutations of matrix multiplication'
date  = 2026-04-29T12:57:11+03:00
+++

The second problem of the first section of the first chapter in
Golub & van Loan (2013) asks reader to show in a table-manner fashion
the order of operations of operands of a $2 \times 2$ matrix via
the familiar matrix multiplication algorithm:

<!--more-->

<p class = "pseudocode">
$\text{\textbf{Algorithm 1}: Matrix multiplication}$<br>
$1. \ \text{\textbf{for}} \ i = 1:m $<br>
$2. \ \qquad \text{\textbf{for}} \ j = 1:n $<br>
$3. \ \qquad \qquad \text{\textbf{for}} \ k = 1:r $<br>
$4. \ \qquad \qquad \qquad \textbf{C}(i,j) = \textbf{C}(i,j) + \textbf{A}(i,k)\textbf{B}(k,j)$<br>
$5. \ \qquad \qquad \text{\textbf{end}}$<br>
$6. \ \qquad \text{\textbf{end}}$<br>
$7. \ \text{\textbf{end}}$<br>
</p>

As the convention goes, the notation $\mathbf{X}(i,j)$ means the
$(i,j)$th element of some matrix $\mathbf{X}$.

The problem then asks to show the order of the operations on
operands $a_{11}b_{11}$, $a_{11}b_{12}$, $a_{21}b_{11}$,
$a_{21}b_{12}$, $a_{12}b_{21}$, $a_{12}b_{22}$, $a_{22}b_{21}$, and
$a_{22}b_{22}$ of the matrices $\mathbf{A}$ and $\mathbf{B}$, when
the loop order of $\text{\textbf{Algorithm 1}}$ is either $ijk$,
$jik$, $ikj$, $jki$, $kij$ or $kji$. For example, in the matrix
multiplication algorithm above, the loop order is $ijk$, so $i$ is
the index-variable of the outer loop, $j$ the middle loop's and $k$
the inner loop's.

When speaking in terms of $2 \times 2$ matrix, each of these
index-variables are iterating just between two integer values. So
as an example, the values index-variables take in the loop order
permutation $ijk$ take can be expressed as table,

$$
    \begin{array}{ c c l }
        i & j & k \\ \hline
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2 \ ,
    \end{array}
$$

that explicitly displays all possible values the index-variables
take during the computation of $\text{\textbf{Algorithm 1}}$ for
matrices $\mathbf{A}$, $\mathbf{B}$ and $\mathbf{C}$ of
$\mathbb{R}^{2\times2}$. The leftmost column shows values the above
mentioned algorithm's outer loop, center column the middle loop's
values and rightmost the inner loop's values.


This setup is nice, because only the column header labels can be
permuted in order the see the order of computation. For example, if
the loop order is $jik$, that is, $j$ is now the outer loop, $i$
the middle loop and $k$ the inner loop, the table values in the
columns remain the same while the label order changes:

$$
    \begin{array}{ c c l }
        j & i & k \\ \hline
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2
    \end{array}
$$

Using this fact, this tabling setup can then be used for looking up
all of the index values when figuring out the order of the
different order of operations with respect to the operands
mentioned in the first paragraph. Before looking up to these
&ldquo;computation tables&rdquo;, it's useful to have a reminder on
how the matrix multiplication $\mathbf{AB}$ is carried out
arithmetically:

<div class = "widescreen">
$$
    % Define new colors for color coding variables.
    \definecolor{rm}{RGB}{255,  0,  0}
    \definecolor{gm}{RGB}{  0,255,  0}
    \definecolor{bm}{RGB}{  0,  0,255}
    \definecolor{pm}{RGB}{255,  0,255}
    \definecolor{rl}{RGB}{255,127,127}
    \definecolor{gl}{RGB}{127,255,127}
    \definecolor{bl}{RGB}{127,127,255}
    \definecolor{pl}{RGB}{255,127,255}
    %
    \mathbf{AB}
    =
    \begin{bmatrix}
        a_{11} & a_{12} \\
        a_{21} & a_{22}
    \end{bmatrix}
    \begin{bmatrix}
        b_{11} & b_{12} \\
        b_{21} & b_{22}
    \end{bmatrix}
    =
    \begin{bmatrix}
        {\color{rm}a_{11}b_{11}} + {\color{gm}a_{12}b_{21}} & {\color{rl}a_{11}b_{12}} + {\color{gl}a_{12}b_{22}} \\
        {\color{bm}a_{21}b_{11}} + {\color{pm}a_{22}b_{21}} & {\color{bl}a_{21}b_{12}} + {\color{pl}a_{22}b_{22}}
    \end{bmatrix}
    =
    \begin{bmatrix}
        c_{11} & c_{12} \\
        c_{21} & c_{22}
    \end{bmatrix}
    =
    \mathbf{C}.
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c}
              &
            \mathbf{A}\mathbf{B}
    \\[1em] = &
        \begin{bmatrix}
            a_{11} & a_{12} \\
            a_{21} & a_{22}
        \end{bmatrix}
        \begin{bmatrix}
            b_{11} & b_{12} \\
            b_{21} & b_{22}
        \end{bmatrix}
    \\[1em] = &
        \begin{bmatrix}
            {\color{rm}a_{11}b_{11}} + {\color{gm}a_{12}b_{21}} & {\color{rl}a_{11}b_{12}} + {\color{gl}a_{12}b_{22}} \\
            {\color{bm}a_{21}b_{11}} + {\color{pm}a_{22}b_{21}} & {\color{bl}a_{21}b_{12}} + {\color{pl}a_{22}b_{22}}
        \end{bmatrix}
    \\[1em] = &
        \begin{bmatrix}
            c_{11} & c_{12} \\
            c_{21} & c_{22}
        \end{bmatrix}
    \\[1em] = &
        \mathbf{C}.
    \end{array}
$$
</div>

The products $a_{ij}b_{ij}$ are color coded so that it's easier to
read the computation tables for the loop orders $ijk$, $jik$,
$ikj$, $jki$, $kij$ and $kji$

<div class = "widescreen">
$$
    \begin{array}{ c c c }
        i & j & k \\ \hline % Loop order: ijk
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2 
    \end{array}
    \quad
    \begin{array}{ c }
                    \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow
    \end{array}
    \quad
    \begin{array}{ l }
                     \\
        {\color{rm}a_{11}b_{11}} & = & c_{11} \\
        {\color{gm}a_{12}b_{21}} & = & c_{11} \\
        {\color{rl}a_{11}b_{12}} & = & c_{12} \\
        {\color{gl}a_{12}b_{22}} & = & c_{12} \\
        {\color{bm}a_{21}b_{11}} & = & c_{21} \\
        {\color{pm}a_{22}b_{21}} & = & c_{21} \\
        {\color{bl}a_{21}b_{12}} & = & c_{22} \\
        {\color{pl}a_{22}b_{22}} & = & c_{22}
    \end{array}
    \ , \qquad
    \begin{array}{ c c c }
        j & i & k \\ \hline % Loop order: jik
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2 
    \end{array}
    \quad
    \begin{array}{ c }
                    \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow
    \end{array}
    \quad
    \begin{array}{ l }
                     \\
        {\color{rm}a_{11}b_{11}} & = & c_{11} \\
        {\color{gm}a_{12}b_{21}} & = & c_{11} \\
        {\color{bm}a_{21}b_{11}} & = & c_{21} \\
        {\color{pm}a_{22}b_{21}} & = & c_{21} \\
        {\color{rl}a_{11}b_{12}} & = & c_{12} \\
        {\color{gl}a_{12}b_{22}} & = & c_{12} \\
        {\color{bl}a_{21}b_{12}} & = & c_{22} \\
        {\color{pl}a_{22}b_{22}} & = & c_{22}
    \end{array}
    \ ,
$$
</div>

<div class = "widescreen">
$$
    \begin{array}{ c c c }
        i & k & j \\ \hline % Loop order: ikj
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2 
    \end{array}
    \quad
    \begin{array}{ c }
                    \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow
    \end{array}
    \quad
    \begin{array}{ l }
                     \\
        {\color{rm}a_{11}b_{11}} & = & c_{11} \\
        {\color{rl}a_{11}b_{12}} & = & c_{12} \\
        {\color{gm}a_{12}b_{21}} & = & c_{11} \\
        {\color{gl}a_{12}b_{22}} & = & c_{12} \\
        {\color{bm}a_{21}b_{11}} & = & c_{21} \\
        {\color{bl}a_{21}b_{12}} & = & c_{22} \\
        {\color{pm}a_{22}b_{21}} & = & c_{21} \\
        {\color{pl}a_{22}b_{22}} & = & c_{22}
    \end{array}
    \ , \qquad
    \begin{array}{ c c c }
        j & k & i \\ \hline % Loop order: jki
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2 
    \end{array}
    \quad
    \begin{array}{ c }
                    \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow
    \end{array}
    \quad
    \begin{array}{ l }
                     \\
        {\color{rm}a_{11}b_{11}} & = & c_{11} \\
        {\color{bm}a_{21}b_{11}} & = & c_{21} \\
        {\color{gm}a_{12}b_{21}} & = & c_{11} \\
        {\color{pm}a_{22}b_{21}} & = & c_{21} \\
        {\color{rl}a_{11}b_{12}} & = & c_{12} \\
        {\color{bl}a_{21}b_{12}} & = & c_{22} \\
        {\color{gl}a_{12}b_{22}} & = & c_{12} \\
        {\color{pl}a_{22}b_{22}} & = & c_{22}
    \end{array}
    \ ,
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
    &
        \begin{array}{ c c c }
            i & j & k \\ \hline % Loop order: ijk
            1 & 1 & 1 \\
            1 & 1 & 2 \\
            1 & 2 & 1 \\
            1 & 2 & 2 \\
            2 & 1 & 1 \\
            2 & 1 & 2 \\
            2 & 2 & 1 \\
            2 & 2 & 2 
        \end{array}
        \quad
        \begin{array}{ c }
                        \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow
        \end{array}
        \quad
        \begin{array}{ l }
                         \\
            {\color{rm}a_{11}b_{11}} & = & c_{11} \\
            {\color{gm}a_{12}b_{21}} & = & c_{11} \\
            {\color{rl}a_{11}b_{12}} & = & c_{12} \\
            {\color{gl}a_{12}b_{22}} & = & c_{12} \\
            {\color{bm}a_{21}b_{11}} & = & c_{21} \\
            {\color{pm}a_{22}b_{21}} & = & c_{21} \\
            {\color{bl}a_{21}b_{12}} & = & c_{22} \\
            {\color{pl}a_{22}b_{22}} & = & c_{22}
        \end{array}
    \ , \\[1em] &
        \begin{array}{ c c c }
            j & i & k \\ \hline % Loop order: jik
            1 & 1 & 1 \\
            1 & 1 & 2 \\
            1 & 2 & 1 \\
            1 & 2 & 2 \\
            2 & 1 & 1 \\
            2 & 1 & 2 \\
            2 & 2 & 1 \\
            2 & 2 & 2 
        \end{array}
        \quad
        \begin{array}{ c }
                        \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow
        \end{array}
        \quad
        \begin{array}{ l }
                         \\
            {\color{rm}a_{11}b_{11}} & = & c_{11} \\
            {\color{gm}a_{12}b_{21}} & = & c_{11} \\
            {\color{bm}a_{21}b_{11}} & = & c_{21} \\
            {\color{pm}a_{22}b_{21}} & = & c_{21} \\
            {\color{rl}a_{11}b_{12}} & = & c_{12} \\
            {\color{gl}a_{12}b_{22}} & = & c_{12} \\
            {\color{bl}a_{21}b_{12}} & = & c_{22} \\
            {\color{pl}a_{22}b_{22}} & = & c_{22}
        \end{array}
    \ , \\[1em] &
        \begin{array}{ c c c }
            i & k & j \\ \hline % Loop order: ikj
            1 & 1 & 1 \\
            1 & 1 & 2 \\
            1 & 2 & 1 \\
            1 & 2 & 2 \\
            2 & 1 & 1 \\
            2 & 1 & 2 \\
            2 & 2 & 1 \\
            2 & 2 & 2 
        \end{array}
        \quad
        \begin{array}{ c }
                        \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow
        \end{array}
        \quad
        \begin{array}{ l }
                         \\
            {\color{rm}a_{11}b_{11}} & = & c_{11} \\
            {\color{rl}a_{11}b_{12}} & = & c_{12} \\
            {\color{gm}a_{12}b_{21}} & = & c_{11} \\
            {\color{gl}a_{12}b_{22}} & = & c_{12} \\
            {\color{bm}a_{21}b_{11}} & = & c_{21} \\
            {\color{bl}a_{21}b_{12}} & = & c_{22} \\
            {\color{pm}a_{22}b_{21}} & = & c_{21} \\
            {\color{pl}a_{22}b_{22}} & = & c_{22}
        \end{array}
    \ ,
    \end{array}
$$
</div>

<div class = "widescreen">
$$
    \begin{array}{ c c c }
        k & i & j \\ \hline % Loop order: kij
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2 
    \end{array}
    \quad
    \begin{array}{ c }
                    \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow
    \end{array}
    \quad
    \begin{array}{ l }
                     \\
        {\color{rm}a_{11}b_{11}} & = & c_{11} \\
        {\color{rl}a_{11}b_{12}} & = & c_{12} \\
        {\color{bm}a_{21}b_{11}} & = & c_{21} \\
        {\color{bl}a_{21}b_{12}} & = & c_{22} \\
        {\color{gm}a_{12}b_{21}} & = & c_{11} \\
        {\color{gl}a_{12}b_{22}} & = & c_{12} \\
        {\color{pm}a_{22}b_{21}} & = & c_{21} \\
        {\color{pl}a_{22}b_{22}} & = & c_{22}
    \end{array}
    \ , \qquad
    \begin{array}{ c c c }
        k & j & i \\ \hline % Loop order: kji
        1 & 1 & 1 \\
        1 & 1 & 2 \\
        1 & 2 & 1 \\
        1 & 2 & 2 \\
        2 & 1 & 1 \\
        2 & 1 & 2 \\
        2 & 2 & 1 \\
        2 & 2 & 2 
    \end{array}
    \quad
    \begin{array}{ c }
                    \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow \\
        \rightarrow
    \end{array}
    \quad
    \begin{array}{ l }
                     \\
        {\color{rm}a_{11}b_{11}} & = & c_{11} \\
        {\color{bm}a_{21}b_{11}} & = & c_{21} \\
        {\color{rl}a_{11}b_{12}} & = & c_{12} \\
        {\color{bl}a_{21}b_{12}} & = & c_{22} \\
        {\color{gm}a_{12}b_{21}} & = & c_{11} \\
        {\color{pm}a_{22}b_{21}} & = & c_{21} \\
        {\color{gl}a_{12}b_{22}} & = & c_{12} \\
        {\color{pl}a_{22}b_{22}} & = & c_{22}
    \end{array}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
        &
        \begin{array}{ c c c }
            j & k & i \\ \hline % Loop order: jki
            1 & 1 & 1 \\
            1 & 1 & 2 \\
            1 & 2 & 1 \\
            1 & 2 & 2 \\
            2 & 1 & 1 \\
            2 & 1 & 2 \\
            2 & 2 & 1 \\
            2 & 2 & 2 
        \end{array}
        \quad
        \begin{array}{ c }
                        \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow
        \end{array}
        \quad
        \begin{array}{ l }
                         \\
            {\color{rm}a_{11}b_{11}} & = & c_{11} \\
            {\color{bm}a_{21}b_{11}} & = & c_{21} \\
            {\color{gm}a_{12}b_{21}} & = & c_{11} \\
            {\color{pm}a_{22}b_{21}} & = & c_{21} \\
            {\color{rl}a_{11}b_{12}} & = & c_{12} \\
            {\color{bl}a_{21}b_{12}} & = & c_{22} \\
            {\color{gl}a_{12}b_{22}} & = & c_{12} \\
            {\color{pl}a_{22}b_{22}} & = & c_{22}
        \end{array}
        \ , \\[1em] &
        \begin{array}{ c c c }
            k & i & j \\ \hline % Loop order: kij
            1 & 1 & 1 \\
            1 & 1 & 2 \\
            1 & 2 & 1 \\
            1 & 2 & 2 \\
            2 & 1 & 1 \\
            2 & 1 & 2 \\
            2 & 2 & 1 \\
            2 & 2 & 2 
        \end{array}
        \quad
        \begin{array}{ c }
                        \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow
        \end{array}
        \quad
        \begin{array}{ l }
                         \\
            {\color{rm}a_{11}b_{11}} & = & c_{11} \\
            {\color{rl}a_{11}b_{12}} & = & c_{12} \\
            {\color{bm}a_{21}b_{11}} & = & c_{21} \\
            {\color{bl}a_{21}b_{12}} & = & c_{22} \\
            {\color{gl}a_{12}b_{21}} & = & c_{11} \\
            {\color{gm}a_{12}b_{22}} & = & c_{12} \\
            {\color{pl}a_{22}b_{21}} & = & c_{21} \\
            {\color{pm}a_{22}b_{22}} & = & c_{22}
        \end{array}
        \ , \\[1em] &
        \begin{array}{ c c c }
            k & j & i \\ \hline % Loop order: kji
            1 & 1 & 1 \\
            1 & 1 & 2 \\
            1 & 2 & 1 \\
            1 & 2 & 2 \\
            2 & 1 & 1 \\
            2 & 1 & 2 \\
            2 & 2 & 1 \\
            2 & 2 & 2 
        \end{array}
        \quad
        \begin{array}{ c }
                        \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow \\
            \rightarrow
        \end{array}
        \quad
        \begin{array}{ l }
                         \\
            {\color{rm}a_{11}b_{11}} & = & c_{11} \\
            {\color{bm}a_{21}b_{11}} & = & c_{21} \\
            {\color{rl}a_{11}b_{12}} & = & c_{12} \\
            {\color{bl}a_{21}b_{12}} & = & c_{22} \\
            {\color{gm}a_{12}b_{21}} & = & c_{11} \\
            {\color{pm}a_{22}b_{21}} & = & c_{21} \\
            {\color{gl}a_{12}b_{22}} & = & c_{12} \\
            {\color{pl}a_{22}b_{22}} & = & c_{22} \ .
        \end{array}
    \end{array}
$$
</div>

Reading the $c_{ij}$ column from top to bottom shows how the loop
orders compute the components of $\mathbf{C}$. For example, when
the loop order is $ikj$, the results of the third table reveal that
the order of operations with respect to operands in
$\textbf{Algorithm 1}$ computes values at first row in $\textbf{C}$
and then the values of $\textbf{C}$ second row. That is, first
$c_{11}$ is updated with value $c_{11}$ $+$ $a_{11}b_{11}$, then
$c_{12}$ is updated with $c_{12}$ $+$ $a_{11}b_{12}$. Then $c_{11}$
$+$ $a_{11}b_{11}$ is updated with $c_{11}$ $+$ $a_{11}b_{11}$ $+$
$a_{12}b_{21}$, $c_{12}$ with $c_{12}$ $+$ $a_{11}b_{12}$ $+$
$a_{12}b_{22}$ and so on until the algorithm has computed all
values, when the loop termination condition $i$ $=$ $m$, $k$ $=$
$n$ and $j$ $=$ $r$ is reached.

### References

Golub, G. H., & van Loan, C. F. (2013). Matrix computations. JHU press.
