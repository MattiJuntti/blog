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

<span class = "exnum">5</span> When

$$
    \mathbf{A} = \begin{bmatrix}
        5 & 4 & 8 \\
        0 & 4 & 3 \\
    \end{bmatrix}
$$

and

$$
    \mathbf{B} = \begin{bmatrix}
        0 & 4 \\
        1 & 3 \\
       -3 & 2 \\
    \end{bmatrix}
$$

**(a)** and ignoring the possible possibility of using
Moore-Penrose pseudoinverse, matrix $\mathbf{A}^{-1}$ does not
exist because $\mathbf{A}$ is not a square matrix. However, **(b)**
the $(\mathbf{BA})^{-1}$ could exist. This can be checked by first
observing that

$$
    \mathbf{BA}
    =
    \begin{bmatrix}
        0 & 4 \\
        1 & 3 \\
       -3 & 2 \\
    \end{bmatrix}
    \begin{bmatrix}
        5 & 4 & 8 \\
        0 & 4 & 3 \\
    \end{bmatrix}
    =
    \begin{bmatrix}
          0  & 16 & 32 \\
          5  & 16 & 32 \\
        -15  & -4 & -8 \\
    \end{bmatrix}.
$$

Exchanging the first row ($R_1$) with third ($R_3$) leads to

$$
    \begin{bmatrix}
        -15  & -4 & -8 \\
          5  & 16 & 32 \\
          0  & 16 & 32 \\
    \end{bmatrix}.
$$

Then the steps for reducing the matrix into upper triangular form
start by subtracting $R_1$ from the second row ($R_2$)
$\frac{5}{-15}$ $=$ $-\frac{1}{3}$ times, that is, adding $R_1$ to
$R_2$ $\frac{1}{3}$ times gives

$$
\begin{array}{c c}
    &
    \begin{bmatrix}
        -15                 & -4                  & -8                  \\
        5 - (\frac{1}{3})15 & 16 - (\frac{1}{3})4 & 32 - (\frac{1}{3})8 \\
        0                   & 16                  & 32                  \\
    \end{bmatrix}
    \\[1em] = &
    \begin{bmatrix}
        -15 & -4           & -8           \\
          0 & \frac{44}{3} & \frac{88}{3} \\
          0 & 16           & 32           \\
    \end{bmatrix}.
    \\[1em] \xrightarrow{R_3 - \frac{16}{1} \left( \frac{3}{44} \right) R_2} &
    \begin{bmatrix}
        -15 & -4                                                                        & -8                                                           \\
          0 & \frac{44}{3}                                                              & \frac{88}{3}                                                 \\
          0 & 16 - \frac{44}{3} \left( \frac{16}{1} \right) \left( \frac{3}{44} \right) & 32 - \left( \frac{16}{1} \right) \left( \frac{3}{44} \right) \\
    \end{bmatrix}
    \\[1em] = &
    \begin{bmatrix}
        -15 & -4           & -8             \\
          0 & \frac{44}{3} & \frac{88}{3}   \\
          0 & 0            & \frac{340}{11} \\
    \end{bmatrix}.
\end{array}
$$

Since, say, $z$ $=$ $\frac{340}{11}$, then $\frac{44}{3}y$ $+$
$\frac{88}{3}z$ $=$ $\frac{44}{3}y$ $+$ $\frac{88}{3}$ $\left(
\frac{340}{11} \right)$ $=$ $\frac{44}{3}y$ $+$ $\frac{2720}{3}$.
So when $\frac{44}{3}y$ $+$ $\frac{2720}{3}$ $=$ $0$, $y$ $=$
$-\frac{2720}{3}$ $\left( \frac{3}{44} \right)$ $=$
$-\frac{680}{11}$. Substituting $y$ and $z$ back to first equation,
means that $-15x$ $+$ $4 \left( \frac{680}{11} \right)$ $-$ $8
\left( \frac{340}{11} \right)$ $=$ $-15x$ $+$ $\frac{2720}{11}$ $-$
$\frac{2720}{11}$ $=$ $-15x$. So when $-15x$ $=$ $0$, $x$ $=$ $0$.

Now, since $x$, $y$ and $z$ are known, it can be said the the
previous matrix,

$$
    \begin{bmatrix}
        -15 & -4           & -8             \\
          0 & \frac{44}{3} & \frac{88}{3}   \\
          0 & 0            & \frac{340}{11} \\
    \end{bmatrix}
    =
    (\mathbf{BA})^{-1}.
$$

<span class = "exnum">6</span> To show that

$$
    \mathbf{A} = \begin{bmatrix}
         3 & -1 &  0 \\
        -1 &  3 & -1 \\
         0 & -1 &  3 \\
    \end{bmatrix}
$$

is positive definite for any non-zero column vector, it's needed to
be shown that $\mathbf{u^\top A u}$ $>$ $0$, for vector
$\mathbf{u}$ $\in$ $\mathbb{R}^3$ nonidentically zero.

$$
    \mathbf{u} = \begin{bmatrix}
        u_1 \\
        u_2 \\
        u_3 \\
    \end{bmatrix}.
$$

Then

$$
    \begin{array}{r c l}
        \mathbf{u}^\top \mathbf{Au}
        & = & \begin{bmatrix}
            u_1 & u_2 & u_3
        \end{bmatrix}
        \begin{bmatrix}
             3 & -1 &  0 \\
            -1 &  3 & -1 \\
             0 & -1 &  3 \\
        \end{bmatrix}
        \begin{bmatrix}
            u_1 \\ u_2 \\ u_3
        \end{bmatrix}
        \\[1em] & = & \begin{bmatrix}
            u_1 & u_2 & u_3
        \end{bmatrix}
        \begin{bmatrix}
             3u_1 -  u_2        \\
             -u_1 + 3u_2 -  u_3 \\
                  -  u_2 + 3u_3 \\
        \end{bmatrix}
        \\[1em] & = &
            u_1(3u_1 - u_2) + u_2(-u_1 + 3u_2 - u_3) + u_3(-u_2 + 3u_3)
        \\[1em] & = &
            3u_1^2 - u_1u_2 - u_1u_2 + 3u_2^2 - u_2u_3 - u_2u_3 + 3u_3^2
        \\[1em] & = &
            3u_1^2 -2 u_1u_2 + 3u_2^2 - 2u_2u_3 + 3u_3^2
        \\[1em] & = &
            3u_1^2 + 3u_2^2 + 3u_3^2 - 2 u_1u_2 - 2u_2u_3.
    \end{array}
$$

Now splitting the $3u_i^2$ and grouping all terms of the received
expression leads to

$$
    (u_1^2 + u_2^2 - 2u_1u_2) + (u_2^2 + u_3^2 - 2u_2u_3) + 2u_1^2 + u_2^2 + 2u_3^2,
$$

and because

$$
    u_i^2 - 2u_iu_j + u_j^2 = (u_i - u_j)^2, \quad i \neq j,
$$

the previous to last expression becomes

$$
    (u_1 - u_2)^2 + (u_2 - u_3)^2 + 2u_1^2 + u_2^2 + 2u_3^2 = \mathbf{u}^\top \mathbf{A} \mathbf{u}.
$$

Therefore, $\mathbf{u}^\top \mathbf{Au}$ $>$ $0$ and
$\mathbf{A}$ is positive definite for any non-zero column vector.
