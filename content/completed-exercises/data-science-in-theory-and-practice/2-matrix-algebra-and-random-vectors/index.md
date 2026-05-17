+++
title  = "2. Matrix Algebra and Random Vectors"
date   = 2026-05-11T12:52:23+03:00
layout = "solution-single"
+++

<span class = "exnum">1</span> **(a)** [Trace][01]
($\operatorname{tr}$) means the sum of the values at main diagonal
of square matrix $\mathbf{A}$, that is,

[01]: https://en.wikipedia.org/wiki/Trace_(linear_algebra)

$$
    \operatorname{tr}(\mathbf{A}) = \sum_{i=1}^{n} a_{ii}. \tag{1}
$$

Then, to show that $\operatorname{tr}(\mathbf{AB})$ $=$
$\operatorname{tr}(\mathbf{BA})$, it is sufficient to show that

$$
    \begin{array}{r c l}
        \operatorname{tr}(\mathbf{AB})
            & = & \displaystyle \sum_{i=1}^{n} ab_{ii} \\[0.5em]
            & = & ab_{11} + ab_{22} + \cdots + ab_{nn} \\[0.5em]
            & = & ba_{11} + ba_{22} + \cdots + ba_{nn} \\[0.5em]
            & = & \displaystyle \sum_{i=1}^{n} ba_{ii} \\[0.5em]
            & = & \operatorname{tr}(\mathbf{BA}).
    \end{array}
$$

**(b)** To see that $\operatorname{tr}(\mathbf{A} + \mathbf{B})$
$=$ $\operatorname{tr}(\mathbf{A})$ $+$
$\operatorname{tr}(\mathbf{B})$, it can be shown that

<div class = "widescreen">
$$
    \begin{array}{r c l}
        \operatorname{tr}(\mathbf{AB})
            & = & \displaystyle \sum_{i=1}^{n} a_{ii} + b_{ii}                                \\[0.5em]
            & = & (a_{11} + b_{11}) + (a_{22} + b_{22}) + \cdots + (a_{ii} + b_{ii})          \\[0.5em]
            & = &  a_{11} + b_{11}  + a_{22}  + b_{22}  + \cdots + a_{ii}  + b_{ii}           \\[0.5em]
            & = &  a_{11} + a_{22}  + \cdots  + a_{ii}  + b_{11} + b_{22}  + \cdots  + b_{ii} \\[0.5em]
            & = & \displaystyle \sum_{i=1}^{n} a_{ii} + \displaystyle \sum_{i=1}^{n} b_{ii}   \\[0.5em]
            & = & \operatorname{tr}(\mathbf{A}) + \operatorname{tr}(\mathbf{B}).
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        \operatorname{tr}(\mathbf{A+B})
            & = & \displaystyle \sum_{i=1}^{n} a_{ii} + b_{ii}   \\[0.5em]
            & = & (a_{11} + b_{11}) + (a_{22} + b_{22}) +        \\[0.5em]
            &   & \cdots  + (a_{nn} + b_{nn})                   \\[0.5em]
            & = & a_{11} + b_{11} + a_{22} + b_{22} +            \\[0.5em]
            &   & \cdots + a_{nn} + b_{nn}                     \\[0.5em]
            & = & a_{11} + a_{22} + \cdots + a_{ii} +            \\[0.5em]
            &   & \cdots + b_{11} + b_{22} + \cdots + b_{ii}   \\[0.5em]
            & = & \displaystyle \sum_{i=1}^{n} a_{ii} + \displaystyle \sum_{i=1}^{n} b_{ii} \\[0.5em]
            & = & \operatorname{tr}(\mathbf{A}) + \operatorname{tr}(\mathbf{B}).
    \end{array}
$$
</div>

**(c)** To show that $\operatorname{tr}(c\mathbf{A})$ $=$
$c\operatorname{t}(\mathbf{A})$, for any constant $c$, it can be
shown that $\operatorname{tr}(c\mathbf{A})$ $=$ $\sum_{i=1}^n
ca_{ii}$ $=$ $ca_{11}$ $+$ $ca_{22}$ $+$ $\cdots$ $+$ $ca_{ii}$ $=$
$c(a_{11}$ $+$ $a_{22}$ $+$ $\cdots$ $+$ $a_{ii})$ $=$ $c
\sum_{i=1}^n a_{ii}$ $=$ $c\operatorname{tr}(\mathbf{A})$.

<span class = "exnum">2</span> Definition of the [determinant][02]
is

$$
    \operatorname{det} \mathbf{A}
        = a_{i1}\mathbf{C}_{i1}
        + a_{i2}\mathbf{C}_{i2}
          \cdots
        + a_{in}\mathbf{C}_{in},
        \tag{2}
$$

[02]: https://en.wikipedia.org/wiki/Determinant

where the &ldquo;cofactors&rdquo;

$$
    \mathbf{C}_{ij} = (-1)^{i+j} \operatorname{det} \mathbf{M}_{i,j}
$$

where $\mathbf{M}$ is known as &ldquo;minor matrix&rdquo; that is
given when row $i$ and column $j$ is deleted from the original
matrix$\mathbf{A}$.

**(a)** Then in order to show that $\operatorname{det}\mathbf{A}$
$=$ $\operatorname{det}\mathbf{A}^\top$, is enough know that no
matter if the $\operatorname{det}$ is taken from $\mathbf{A}$ or
$\mathbf{A}^\top$, the operations ends up in same expression of
summations and multiplications that are equal due to the
associativity and commutativity properties of these operations.  In
other words, the proof is then just to show compute the determinant
for both $\mathbf{A}$ and $\mathbf{A}^\top$ to find the (possibly
very) long expression that contain all summations and
multiplications of the determinant, and then make them equal by
rearranging terms.

**(b)**

...

<span class = "exnum">3</span> When

$$
    \mathbf{A} = \begin{bmatrix}
        1 & 4 & 8 \\
        0 & 4 & 9 \\
    \end{bmatrix}
    \ , \qquad
    \mathbf{B} = \begin{bmatrix}
         2 & 4 \\
         1 & 8 \\
        -3 & 9 \\
    \end{bmatrix}
    \ ,
$$

**(a)** then

$$
    \mathbf{A} + \mathbf{B} = \begin{bmatrix}
        1 + 2 & 4 + 4 & 8 - 3 \\
        0 + 1 & 4 + 8 & 9 + 9 \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        3 &  8 &  5 \\
        1 & 12 & 19 \\
    \end{bmatrix}
    ,
$$

**(b)**

$$
    \mathbf{A} + \mathbf{B} = \begin{bmatrix}
        1 - 2 & 4 - 4 & 8 - 3 \\
        0 - 1 & 4 - 8 & 9 - 9 \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        -1 &  0 & 5 \\
        -1 & -4 & 0 \\
    \end{bmatrix}
    ,
$$

**(c)**

<div class = "widescreen">
$$
    \begin{array}{r c l}
        \mathbf{AA}^\top & = & \begin{bmatrix}
            1 & 4 & 8 \\
            0 & 4 & 9 \\
        \end{bmatrix} \begin{bmatrix}
            1 & 0 \\
            4 & 4 \\
            8 & 9 \\
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            1(1) + 4(4) + 8(8) & 0(1) + 4(4) + 9(8) \\
            1(0) + 4(4) + 8(9) & 0(0) + 4(4) + 9(9) \\
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            81 & 88 \\
            88 & 97 \\
        \end{bmatrix},
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c c}
        \mathbf{AA}^\top & = & \begin{bmatrix}
            1 & 4 & 8 \\
            0 & 4 & 9 \\
        \end{bmatrix} \begin{bmatrix}
            1 & 0 \\
            4 & 4 \\
            8 & 9 \\
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            \begin{array}{c c}
               1(1) \\   
             + 4(4) \\
             + 8(8) 
            \end{array} &
            \begin{array}{c}
               0(1) \\   
             + 4(4) \\
             + 9(8) 
            \end{array} \\[0.5em]
            \begin{array}{c}
               1(0) \\   
             + 4(4) \\
             + 8(9) 
            \end{array} &
            \begin{array}{c}
               0(0) \\   
             + 4(4) \\
             + 9(9) 
            \end{array}
        \end{bmatrix}
    \\[0.5em] & = &
        \begin{bmatrix}
            81 & 88 \\
            88 & 97 \\
        \end{bmatrix},
    \end{array}
$$
</div>

and

**(d)** 

...

<span class = "exnum">4</span> If

$$
    \mathbf{A} = \begin{bmatrix}
        1 & 4 & 8 \\
        0 & 4 & 9 \\
    \end{bmatrix}
$$

and

$$
    \mathbf{B} = \begin{bmatrix}
         2 & 4 \\
         1 & 3 \\
        -3 & 9 \\
    \end{bmatrix},
$$

**(a)** then

<div class = "widescreen">
$$
    \mathbf{AB}
    =
    \begin{bmatrix}
        2(1) + 1(4) - 3(8) & 4(1) + 3(4) + 9(8) \\
        2(0) + 1(4) - 3(9) & 4(0) + 3(4) + 9(9) \\
    \end{bmatrix}
    =
    \begin{bmatrix}
        -18 & 88 \\
        -23 & 93 \\
    \end{bmatrix}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c c}
        \mathbf{AB}
        & = &
        \begin{bmatrix}
            \begin{array}{c c}
                2(1) \\ + 1(4) \\ - 3(8)    
            \end{array}
            &
            \begin{array}{c c}
                4(1) \\ + 3(4) \\ + 9(8) 
            \end{array}
            \\[1em]
            \begin{array}{c c}
                2(0) \\ + 1(4) \\ - 3(9)    
            \end{array}
            &
            \begin{array}{c c}
                4(0) \\ + 3(4) \\ + 9(9) 
            \end{array}
        \end{bmatrix}
        \\[1em] & = &
        \begin{bmatrix}
            -18 & 88 \\
            -23 & 93 \\
        \end{bmatrix}
        ,
    \end{array}
$$
</div>

and **(b)**

$$
\begin{array}{r c l}
    \mathbf{BA}
        & = & \begin{bmatrix}
            \mathbf{Ba}_1 & \mathbf{Ba}_2 & \mathbf{Ba}_3
        \end{bmatrix}
        \\[0.5em] & = & \begin{bmatrix}
            1( 2) + 0(4) & 4( 2) + 4(4) & 8( 2) + 9(4) \\
            1( 1) + 0(3) & 4( 1) + 4(3) & 8( 1) + 9(3) \\
            1(-3) + 0(9) & 4(-3) + 4(9) & 8(-9) + 9(9) \\
        \end{bmatrix}
        \\[0.5em] & = & \begin{bmatrix}
            2 & 24 & 52 \\
            1 & 16 & 35 \\
           -3 & 24 & 57 \\
        \end{bmatrix}.
\end{array}
$$

**(c)** The

$$
    \operatorname{tr}(\mathbf{AB})
        = -18 + 93
        = 75
        = 2 + 16 + 57
        = \operatorname{tr}(\mathbf{BA}).
$$
