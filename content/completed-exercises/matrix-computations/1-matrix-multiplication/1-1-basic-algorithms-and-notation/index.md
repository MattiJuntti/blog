+++
title  = "1.1. Basic algorithms and notation"
layout = "solution-single"
+++

<span class = "exnum">1</span> Given the product $\mathbf{M}$ $=$
$\mathbf{A} - x_n \mathbf{I}$, where $x_n$ runs from $1$ to $r$ and
$\mathbf{A}$ and the identity matrix $\mathbf{I}$ are matrices in
$\mathbb{R}^{n \times n}$, the first column of $\mathbf{M}$ can be
computed by first multiplying the elements of $\mathbf{I}$ by $x_n$
for all $n$, and then performing pointwise subtraction between the
matrices $\mathbf{A}$ and $x_n\mathbf{I}$.

<p class = "pseudocode">
$\text{\textbf{Algorithm 1}}$<br>
$\text{\textbf{for}} \ i \ = \ 1:n$<br>
$\qquad \mathbf{M}_{i} = \mathbf{A}_{i1} - x_i \mathbf{I}_{i1}$<br>
$\text{\textbf{end}}$<br>
</p>

So for example, if

<div class = "widescreen">
$$
    \mathbf{A} = \begin{bmatrix}
        a_{11} \ \ \ \cdots \\
        a_{21} \ \ \ \cdots \\
        a_{31} \ \ \ \cdots \\
        \vdots              \\
        a_{n1} \ \ \ \cdots
    \end{bmatrix},
    \quad
    \mathbf{x} = \begin{bmatrix}
            x_1 \\ \vdots \\ x_n
    \end{bmatrix},
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c c}
        \mathbf{A} & = & \begin{bmatrix}
            a_{11} \ \ \ \cdots \\
            a_{21} \ \ \ \cdots \\
            a_{31} \ \ \ \cdots \\
            \vdots              \\
            a_{n1} \ \ \ \cdots
        \end{bmatrix}
        , \\[1em]
        \mathbf{x} & = & \begin{bmatrix}
            x_1 \\ \vdots \\ x_n
        \end{bmatrix},
    \end{array}
$$
</div>

then the iterating the above algorithm results in the product

$$
    \mathbf{M} = \begin{bmatrix}
        a_{11} - 1x_1 \\
        a_{12} - 0x_2 \\
        \vdots        \\
        a_{1n} - 0x_n
    \end{bmatrix}
    =
    \mathbf{A}_{i1} - x_i\mathbf{I}_{i1}, \qquad i = 1:n.
$$

<span class = "exnum">2</span> See this [post][1].

[1]:{{< ref "post/looking-into-loop-order-permutations-of-2-x-2-matrix-multiplication/index.md"  >}}.

<span class = "exnum">3</span> For the given matrix $\mathbf{C} \in
\mathbb{R}^{n \times n}$ and $n$-vectors $\mathbf{x}$ and
$\mathbf{y}$,

$$
    \mathbf{C}
    = (\mathbf{x} \mathbf{y}^\top)^k
    = (\mathbf{x} \mathbf{y}^\top)
      (\mathbf{x} \mathbf{y}^\top)
      \cdots
      (\mathbf{x} \mathbf{y}^\top)
    = \mathbf{x}
      \underbrace {
          (\mathbf{y}^\top
          \mathbf{x}) (\mathbf{y}^\top
          \mathbf{x})
          \cdots
          (\mathbf{y}^\top \mathbf{x})
      }_{k-1 \ \text{times}}
          \mathbf{y}^\top
    \tag{1}
$$

and since dot product $\mathbf{y}^\top \mathbf{x}$ is a time
complexity $O(n)$ operation show in the following algorithm as
shown in the following algorithm

<p class = "pseudocode">
$\text{\textbf{Algorithm 3}: {\rm D{\small OT}P{\small RODUCT}}}$<br>
$\text{\textbf{for}} \ i = 1 : n$<br>
$\qquad d = d + \mathbf{y}^\top(i) \mathbf{x}(i) \ \color{gray}{// \ \text{or equivalently,} \ d = d + y_ix_i}$<br>
$\text{\textbf{end}}$<br>
</p>

where $d$ $=$ $0$ when $i$ $=$ $1$, the product of $\mathbf{x}$ and
$\mathbf{y}^\top$, can be organized as computation where dot
products $\mathbf{y}^\top_i \mathbf{x}_{i+1}$, from $i = 1$ to
$k-1$, are first computed to get the scalar $a$, and because
$\mathbf{x} a \mathbf{y}^\top$ $=$ $a \textbf{x} \mathbf{y}^\top$,
the product $\mathbf{x} \mathbf{y}^\top$ can be computed using the
algorithm

<p class = "pseudocode">
$\text{\textbf{Algorithm 4}: {\rm S{\small QR}M{\small AT}M{\small UL}}}$<br>
$\text{\textbf{for}} \ i = 1 : n$<br>
$\qquad \text{\textbf{for}} \ j = 1 : n$<br>
$\qquad \qquad \mathbf{C}(i,j) = a \mathbf{x}(i)\mathbf{y}^\top(j) \ \color{gray}{// \ \text{or equivalently,} \ c_{ij} = ax_iy_j}$<br>
$\qquad \text{\textbf{end}}$<br>
$\text{\textbf{end}}$<br>
</p>

that has time complexity $O(n^2)$. As this time complexity is the
most dominant, the product

$$
    \mathbf{C} = (\mathbf{x}\mathbf{y}^\top)^k
$$

can be computed in $O(n^2)$ time with algorithm that first computes
the scalar $d$ using $\text{\rm D{\small OT}P{\small RODUCT}}$ and
uses that scalar when computing $\text{\rm S{\small QR}M{\small AT}M{\small UL}}$
between the leading vector $\mathbf{x}$ and trailing vector
$\mathbf{y}^\top$ of the right hand-side of $\mathbf{C}$ in $(1)$.
