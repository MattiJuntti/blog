+++
title  = "Problems 1-9"
layout = "solution-single"
+++

<span class = "exnum">1</span> To show that the
$\operatorname{mean}(\{kx\})$ equals $k\operatorname{mean}(\{x\})$
comes from the definition  of mean,

\begin{equation} \label{eq:mean}
    \operatorname{mean}(\{x\}) = \frac{1}{N} \sum_{i = 1}^{N} x_i,
\end{equation}

because

$$
    \begin{array}{r c l}
        \operatorname{mean}(\{kx\})
        & = &
        \dfrac{1}{N} \displaystyle\sum_{i=1}^N kx_i
        \\ & = &
        \dfrac{1}{N} (kx_1 + kx_2 + \cdots + kx_n)
        \\[0.5em] & = &
        \dfrac{1}{N} k(x_1 + x_2 + \cdots + x_n)
        \\[0.5em] & = &
        k \dfrac{1}{N} (x_1 + x_2 + \cdots + x_n)
        \\[0.5em] & = &
        k \displaystyle\sum_{i=1}^N x_i
        \\[0.5em] & = &
        k\operatorname{mean}(\{x\}).
    \end{array}
$$
