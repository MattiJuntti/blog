+++
title  = "Problems 11-20"
layout = "solution-single"
+++

<span class = "exnum">11</span>

...

<span class = "exnum">12</span> Given the system of equations

$$
    \left\{ \ \
        \begin{array}{ r c r c r c r }
            2x & + &  3y & + &  z & = &  8 \\
            4x & + &  7y & + & 5z & = & 20 \\
               &   & -2y & + & 2z & = &  0
        \end{array}
    \right. \ \ ,
$$

the system can be reduced into upper triangular form with two operations by
subtracting first row ($R_1$) multiplied by $l_{21} / l_{11}$ $=$ $4 / 2$
$=$ $2$ from the second row ($R_2$). That is

$$
    \begin{array}{c l}
        \xrightarrow{R_2 - 2R_1} &  \left\{ \ \
            \begin{array}{ r c r c r c r }
                2x & + &  3y & + &  z & = &  8 \\
                   &   &   y & + & 3z & = &  4 \\
                   &   & -2y & + & 2z & = &  0
            \end{array}
        \right. \ \ .
    \end{array}
$$

Then subtracting the multiple $l_{32} / l_{22}$ $=$ $-2/1$, i.e. adding the
multiple of $2$ of $R_2$ to the third row $(R_3)$ leads to

$$
    \begin{array}{c l}
        \xrightarrow{R_2 - 2R_1} &  \left\{ \ \
            \begin{array}{ r c r c r c r }
                \mathbf{2}x & + & 3y          & + & z           & = & 8 \\
                            &   & \mathbf{1}y & + & 3z          & = & 4 \\
                            &   &             &   & \mathbf{8}z & = & 8
            \end{array}
        \right. \ \ ,
    \end{array}
$$

where the pivots are boldened.

From $8z = 8$ it can be seen that $z = 1$, so substituing this to $R_2$ and
solving for $y$ shows that it's equal to $1$. Substituting these values to
$R_1$, the row beocmes

$$
    \phantom{,} \ 2x + 3(1) + 1 = 2x + 4 = 8 \ ,
$$

from where it can be seen that $x = 2$. Then the solution vector for this
system is

$$
    \phantom{.} \ \
        \mathbf{b} = \begin{bmatrix}
            x \\ y \\ z
        \end{bmatrix}
        =
        \begin{bmatrix}
            2 \\ 1 \\ 1
        \end{bmatrix}
    \ \ .
$$

<span class = "exnum">13</span> Subtracting first row from the second after
multiplying it by $l_{21}/l_{11}$ leads to system of equations

$$
    \phantom{.} \quad
        \left\{
            \begin{array}{ r r r r r }
                2x & - & 3y &   &    & = & 3 \\
                   &   & y  & + &  z & = & 1 \\
                2x & - &  y & - & 3z & = & 7
            \end{array}
        \right.
    \quad .
$$

Subtracting the first row from the third once leads to

$$
    \phantom{.} \quad
        \left\{
            \begin{array}{ r r r r r r r }
                2x & - & 3y &   &    & = & 3 \\
                   &   &  y & + &  z & = & 1 \\
                   &   & 2y & - & 3z & = & 4
            \end{array}
        \right.
    \quad 
$$

and subtracting the second row from the third twice further leads to

$$
    \phantom{.} \quad
        \left\{
            \begin{array}{ r r r r r r r }
                2x & - & 3y &   &    & = & 3 \\
                   &   &  y & + &  z & = & 1 \\
                   &   &    & - & 5z & = & 2 \end{array}
        \right.
    \quad ,
$$

so $z = -\frac{2}{5}$ and so $y = \frac{7}{5}$. Since the multiplier of $z$
is $0$, only the $y$ needs to be substituted to the first equation which
leads to

$$
    2x - 3 \left( \dfrac{7}{5} \right) = 2x - \dfrac{21}{5} = 3
$$

so

$$
    \phantom{,} \
        2x = 3 + \dfrac{21}{5}
            = \dfrac{15}{5} + \dfrac{21}{5}
            = \dfrac{36}{5}
    \ ,
$$

which shows that

$$
    \phantom{.} \ x = \dfrac{36/5}{2} = \dfrac{36}{10} \ .
$$

So

$$
    \phantom{,} \quad
        \left\{
            \begin{array}{ r r r }
                x & = & \frac{36}{10} \\
                y & = & \frac{7}{5}   \\
                z & = & -\frac{2}{5}
            \end{array}
        \right.
    \quad .
$$

Substituting these values with, say, the third row of the given system, it
can be seen that

$$
    \begin{array}{r c l}
        2x - y - 3z
         & = & 2 \left( \dfrac{36}{10} \right) - \left( \dfrac{7}{5} \right) + 3 \left( \dfrac{2}{5} \right) \\[0.5em]
         & = & \dfrac{72}{10} - \dfrac{14}{10} + \dfrac{12}{10} \\[0.5em]
         & = & \dfrac{70}{10} \\[0.5em]
         & = & 7,
    \end{array}
$$

<span class = "exnum">14</span>

...

<span class = "exnum">15</span> 

...

<span class = "exnum">16</span> **(a)** When $\mathbf{A}$ is a $3 \times 3$
matrix, then a matrix that needs two row exchanges in order to reach a
triangular form and a solution is

$$
    \phantom{.}
        \begin{bmatrix}
                 0 &     0 & \gamma \\
                 0 & \beta & \gamma \\
            \alpha & \beta & \gamma \\
        \end{bmatrix}
        \begin{bmatrix}
            x \\ y \\ z
        \end{bmatrix}
        =
        \mathbf{b}
    ,
$$

because without row exchanges, trying to pivot first row ($R_1$) with the
second row ($R_2$), and then the same between $R_2$ and the third row
($R_3$) leads to multiplication by $0$ which is not allowed, so the
elimination breaks.

However, exchanging $R_3$ with $R_1$, that is the first row exchange, and
then exchanging $R_2$ with $R_1$ leads to a system of equations of the form

$$
    \phantom{.}
        \begin{bmatrix}
            \alpha & \beta & \gamma \\
            0      & \beta & \gamma \\
            0      & 0     & \gamma
        \end{bmatrix}
        \begin{bmatrix}
            z \\ y \\ x
        \end{bmatrix}
    =
        \mathbf{b}
    .
$$

**(b)** Example of a matrix that needs a one row exchange and later breaks
down is

$$
    \phantom{.}
        \begin{bmatrix}
            0 & \beta & \gamma \\
            \alpha & \beta & \gamma \\
            0 & \beta & \gamma \\
        \end{bmatrix}
    =
        \mathbf{b}
    .
$$

<span class = "exnum">17</span> In the example case, if no rows are
exchanged, one can eliminate all $x$'s, $y$'s and $z$'s from the system of
equations. The steps are subtract the first row ($R_1$) from the second
row ($R_2$) once, and $R_1$ from the third row ($R_3$) two times. This
leads to a solution

$$
    \phantom{.} \quad
        \left\{
            \begin{array}{ r r r }
                0 & = & 0 \\
                0 & = & 0 \\
                0 & = & 2 \\
            \end{array}
        \right.
    \quad ,
$$

No row exchanges are needed.

Same goes for the second systems, that is, subtracting $R_1$ two times from
$R_2$ and $R_1$ three times from $R_3$. This results in the same system as
the one above.


<span class = "exnum">18</span> Such a matrix is can be constructed by
arbitrarily a equation with coeffiecents

$$
    \phantom{,} \ \alpha x + \beta y + \delta z = \gamma \ ,
$$

such that $\alpha \neq \beta \neq \delta$, and then multiplying the values
with some, say, integers like $3$ and $5$, so that the system takes the
form

$$
    \phantom{.} \quad
        \left\{
            \begin{array}{ r r r r r r r }
                  \alpha x & + &   \beta y & + &   \gamma z & = &  \delta \\
                3 \alpha x & + & 3 \beta y & + & 3 \gamma z & = & 3\delta \\
                5 \alpha x & + & 5 \beta y & + & 5 \gamma z & = & 5\delta
            \end{array}
        \right.
    \quad .
$$

Now subtracting the first row multiplied by $3$ from the second and the
first row multiplied by $5$ from the scoend leads to

$$
    \left\{
        \begin{array}{ r r r r r r r }
              \alpha x & + &   \beta y & + &   \gamma z & = &  \delta \\
                     0 & + &         0 & + &          0 & = &       0 \\
                     0 & + &         0 & + &          0 & = &       0
        \end{array}
    \right.
$$

after elimination.

When $\mathbf{b} = (1, 10, 100)$, the system becomes

$$
    \left\{
        \begin{array}{ r r r r r r r }
              \alpha x & + &   \beta y & + &   \gamma z & = & 1   \\
            3 \alpha x & + & 3 \beta y & + & 3 \gamma z & = & 10  \\
            5 \alpha x & + & 5 \beta y & + & 5 \gamma z & = & 100 \\
        \end{array}
    \right.
$$

and applying the same elimination steps as above leads to

$$
    \phantom{.} \quad
        \left\{
            \begin{array}{ r r r r r r r }
                  \alpha x & + &   \beta y & + &   \gamma z & = &  1 \\
                           &   &           &   &          0 & = &  7 \\
                           &   &           &   &          0 & = & 95 \\
            \end{array}
        \right.
    \quad .
$$

When $\mathbf{b} = (0, 0, 0)$, the system becomes

$$
    \left\{
        \begin{array}{ r r r r r r r }
              \alpha x & + &   \beta y & + &   \gamma z & = & 0 \\
            3 \alpha x & + & 3 \beta y & + & 3 \gamma z & = & 0 \\
            5 \alpha x & + & 5 \beta y & + & 5 \gamma z & = & 0 \\
        \end{array}
    \right.
$$

and applying the same elimination steps as above leads to

$$
    \phantom{.} \quad
        \left\{
            \begin{array}{ r r r r r r r }
                  \alpha x & + &   \beta y & + &   \gamma z & = & 0 \\
                           &   &           &   &          0 & = & 0 \\
                           &   &           &   &          0 & = & 0 \\
            \end{array}
        \right.
    \quad .
$$

<span class = "exnum">19</span> Subtracting the first row ($R_1$) once from
the second ($R_2$), leads to $R_2$ being equal to $3y$ $-$ $4z$ $=$ $5$.
Subtracting $R_2$ once from the third row ($R_3$) means that $R_3$ becomes
$(q - 6)z$ $=$ $t - 5$. If $q = 5$, the third row becomes $0 = t - 5$, and
so the system becomes singular with infinitely many solutions. If $t$ too
is equal to $5$, then the third row becomes $0 = 0$, so the system remains
singular and has infinitely many solutions. If $q = t = 6$, then $R_3$ is
$z = 1$.

<span class = "exnum">20</span>

...
