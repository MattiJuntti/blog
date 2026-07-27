+++
title  = "Problems 1-16"
layout = "solution-single"
+++

<span class = "exnum">1</span> If $A$ is a $3\times5$, $B$ a
$5\times3$, $C$ a $5\times1$ and $D$ a $3\times1$ matrices with all
entries being $1$ and if matrix multiplication is allowed if and
and only if number of columns of the left handside matrix is equal
to the number of rows of the right handside matrix. In other words,
only a matrix multiplication $A_{n \times k}B_{k \times m}$ is
allowed, where $n$, $m$ and $k$ numbers of rows and columns.
Therefore; $BA$ $=$ $B_{5 \times 3}$ $\cdot$ $A_{3 \times 5}$ is
allowed, $AB$ $=$ $A_{3 \times 5}$ $\cdot$ $B_{5 \times 3}$ is
allowed, $ABD$ $=$ $A_{3 \times 5}$ $\cdot$ $B_{5 \times 3}$
$\cdot$ $D_{3 \times 1}$ is allowed, $DC$ $=$ $D_{3 \times 1}$
$\cdot$ $C_{5 \times 1}$ is not allowed because operand dimensions
don't match, and $A(B + C)$ $=$ $A_{3 \times 5}$ $\cdot$ $(B_{5
\times 3}$ $+$ $C_{5 \times 1})$ is not allowed because dimensions
of $B$ and $C$ don't match.
