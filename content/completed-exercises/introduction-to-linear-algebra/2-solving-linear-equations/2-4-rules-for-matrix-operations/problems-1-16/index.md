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
