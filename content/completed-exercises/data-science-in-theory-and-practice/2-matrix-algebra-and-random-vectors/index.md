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
    \operatorname{tr}(\mathbf{A}) = \sum_{i=1}^{n} a_{ii}.
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
