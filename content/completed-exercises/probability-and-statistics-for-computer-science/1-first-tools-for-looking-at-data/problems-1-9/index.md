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

<span class = "exnum">2</span> Using the definition
\eqref{eq:mean} to show that

$$
    \operatorname{mean}(\{ x + c \}) = \operatorname{mean}(\{x\}) + c
$$

goes as follows:

$$
    \begin{array}{r c l}
        \operatorname{mean}(\{x + c\})
        & = &
            \dfrac{1}{N}\displaystyle\sum_{i=1}^N (x + c)
        \\[0.5em] & = &
            \dfrac{1}{N}\left((x_1 + c) + (x_2 + c) + \cdots + (x_n + c)\right)
        \\[0.5em] & = &
            \dfrac{1}{N}(x_1 + c + x_2 + c + \cdots + x_n + c)
        \\[0.5em] & = &
            \dfrac{1}{N}(x_1 + x_2 + \cdots + x_n + c + c + \cdots + c)
        \\[0.5em] & = &
            \dfrac{1}{N}(x_1 + x_2 + \cdots + x_n + Nc)
        \\[0.5em] & = &
            \dfrac{1}{N}(x_1 + x_2 + \cdots + x_n) + \dfrac{1}{N}Nc
        \\[0.5em] & = &
            \dfrac{1}{N}(x_1 + x_2 + \cdots + x_n) + c
        \\[0.5em] & = &
            \dfrac{1}{N} \displaystyle\sum_{i=1}^N x_i + c
        \\[0.5em] & = &
            \operatorname{mean}(\{x\}) + c.
    \end{array}    
$$
