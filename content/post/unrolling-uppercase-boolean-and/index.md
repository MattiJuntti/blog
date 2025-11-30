+++
title = 'Unrolling uppercase boolean and'
date  = 2025-11-30T20:02:15+02:00
+++

One of the exercises in Rosen (2019), asks that &ldquo;[i]f $p_1$,
$p_2$, $\ldots$, $p_n$ are $n$ propositions, explain why

$$
    \bigwedge\limits_{i \ = \ 1}^{n - 1} \bigwedge\limits_{j \ = \ i + 1}^n (\lnot p_i \lor \lnot p_j) \tag{1}
$$

is true if and only if at most one of $p_1$, $p_2$, $\ldots$, $p_n$
is true &rdquo; Solving this task requires understanding the
notation, so let's unwrap the thing.

<!--more-->

First step of unwinding $(1)$ is just making the order of
operations obvious by explicitly writing out the enclosing
parentheses as

$$
    \bigwedge\limits_{i \ = \ 1}^{n - 1} \left[ \bigwedge\limits_{j \ = \ i + 1}^n (\lnot p_i \lor \lnot p_j) \right] \tag{2}
$$

This makes it easier to see what is happening: In order to unroll
$(1)$, the expression inside the square brackets is to be evaluated
first.

It's possible that the person reading this is familiar with the
[sum notation][01] used throughout mathematics. The idea in the
uppercase boolean ands of $(1)$ or $(2)$ is similar, that is, the
$\bigwedge$ operator translates to multiple sequential applications
of the logical and ($\land$) operations of some logical
propositions.

[01]: https://mathworld.wolfram.com/Sum.html

In other words, if one assumes $k$ long sequence of logical
propositions $q_k$, the sequence of logical operations

$$
    \phantom{.} \
        q_1 \land q_2 \land \ldots \land q_k
        =
        \bigwedge\limits_{l \ = \ 1}^k q_l
    \ .
$$

Now, let $l$ $=$ $j$ $=$ $i + 1$ for some $i$, $k$ $=$ $n$, and
$q_l$ $=$ $(\lnot p_i$ $\land$ $\lnot p_j)$ in this equation.
Then, substituting these values to $(2)$ it can be seen that

<div class = "widescreen">
$$
    \begin{array}{r c l}
        \displaystyle \bigwedge\limits_{l = 1}^k q_l
            & = & \displaystyle \bigwedge\limits_{j = i + 1}^n (\lnot p_i \land \lnot p_j) \\[0.5em]
            & = & (\lnot p_i \lor \lnot p_{i + 1})
                \ \land \ (\lnot p_i \lor \lnot p_{i + 2})
                \ \land \ \cdots
                \ \land \ (\lnot p_i \lor \lnot p_n).
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        \displaystyle \bigwedge\limits_{l = 1}^k q_l
            & = & \bigwedge\limits_{j = i + 1}^n (\lnot p_i \land \lnot p_j) \\[0.5em]
            & = & (\lnot p_i \lor \lnot p_{i + 1})                           \\[0.75em]
            & \land & (\lnot p_{i + 1} \lor \lnot p_{i + 2})                 \\[0.75em]
            &       & \qquad \quad \vdots                                    \\[0.75em]
            & \land & (\lnot p_{i + n} \lor \lnot p_{i + n + 1}) \ ,
    \end{array}
$$
</div>

Substituting the right hand-side back to $(1)$ means that

<div class = "widescreen">
$$
    \begin{array}{r c l}
        & & \displaystyle \ \bigwedge\limits_{i \ = \ 1}^{n - 1} \
            \left[ \bigwedge\limits_{j \ = \ i + 1}^n (\lnot p_i \lor \lnot p_j) \right] \\[0.5em]
        & & \ = \
            \displaystyle \bigwedge\limits_{i \ = \ 1}^{n - 1} \
            \Biggr[ \
                (\lnot p_i \lor \lnot p_{i + 1})
                \land (\lnot p_{i} \lor \lnot p_{i + 2})
                \land \cdots
                \land (\lnot p_{i} \lor \lnot p_{n})
            \ \Biggr].
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ c c c c c c c }
        \displaystyle \ \bigwedge\limits_{i \ = \ 1}^{n - 1} & \hspace{-1.0em}
            \biggr[ & \hspace{-1.0em} \displaystyle \bigwedge\limits_{j \ = \ i + 1}^n & \hspace{-3.0em} (\lnot p_i \lor \lnot p_j)                           & \hspace{-3.0em} \biggr] \\[0.5em]
            = & \displaystyle \ \bigwedge\limits_{i \ = \ 1}^{n - 1} \hspace{-1.0em} & \biggr[ & \hspace{-2.0em} (\lnot p_i \lor \lnot p_{i+1})                                 & \hspace{-1.0em} \\[0.5em]
              &                                                      \hspace{-1.0em} &         & \hspace{-2.0em} \land \ (\lnot p_i \lor \lnot p_{i+2}) \ \phantom{\land}       & \hspace{-1.0em} \\[0.5em]
              &                                                      \hspace{-1.0em} &         & \hspace{-2.0em} \vdots                                                         & \hspace{-1.0em} \\[0.5em]
              &                                                      \hspace{-1.0em} &         & \hspace{-2.0em} \land \ (\lnot p_{i+n} \lor \lnot p_{i+n+1}) \ \phantom{\land} & \hspace{-1.0em} \biggr] \\[0.5em]
    \end{array}
$$
</div>

Unrolling the outer uppercase boolean follows the same idea as the
inner uppercase boolean, but with the outer uppercase boolean there
is only one running variable $i$ spanning from $1$ to $n - 1$ to
consider. That is

<div class = "widescreen">
$$
    \begin{array}{ c c c c c c c c c c }
        \displaystyle \bigwedge\limits_{i \ = \ 1} ^{n - 1}
              & \hspace{0.0em} \biggr[ & \hspace{0.0em} (\lnot p_i \lor \lnot p_{i+1})   & \land   & (\lnot p_{i} \lor \lnot p_{i + 2}) & \land & \cdots & \land   & (\lnot p_{i} \lor \lnot p_{n})   & \hspace{0.0em} \Biggr] \\[0.5em]
        =      & \hspace{0.0em} \biggr[                 & \hspace{0.0em} (\lnot p_1 \lor \lnot p_{2}) & \land         & (\lnot p_{1} \lor \lnot p_{3}) & \land & \cdots & \land         & (\lnot p_{1} \lor \lnot p_{n})   & \hspace{0.0em} \biggr] \\[0.5em]
        \land  & \hspace{0.0em}                         & \hspace{0.0em}                              & \biggr[       & (\lnot p_{2} \lor \lnot p_{3}) & \land & \cdots & \land         & (\lnot p_{2} \lor \lnot p_{n})   & \hspace{0.0em} \biggr] \\[0.5em]
        \vdots & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       & \ddots &               & \vdots                           & \hspace{0.0em}         \\[0.5em]
        \land  & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       &        & \biggr[       & (\lnot p_{n-1} \lor \lnot p_{n}) & \hspace{0.0em} \biggr] \\[0.5em]
        =      & \hspace{0.0em} \biggr[                 & \hspace{0.0em} \lnot(p_1 \land  p_{2})      & \land         & \lnot( p_{1} \land p_{3})      & \land & \cdots & \land         & \lnot(p_{1} \land p_{n})         & \hspace{0.0em} \biggr] \\[0.5em]
        \land  & \hspace{0.0em}                         & \hspace{0.0em}                              & \biggr[       & \lnot(p_{2} \land p_{3})       & \land & \cdots & \land         & \lnot(p_{2} \land p_{n})         & \hspace{0.0em} \biggr] \\[0.5em]
        \vdots & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       & \ddots &               & \vdots                           & \hspace{0.0em}         \\[0.5em]
        \land  & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       &        & \biggr[       & \lnot(p_{n-1} \land p_{n})       & \hspace{0.0em} \biggr] \\[0.5em]
        =      & \hspace{0.0em} \lnot \biggr[           & \hspace{0.0em} (p_1 \land  p_{2})           & \lor          & ( p_{1} \land p_{3})           & \lor  & \cdots & \lor          & (p_{1} \land p_{n})              & \hspace{0.0em} \biggr] \\[0.5em]
        \land  & \hspace{0.0em}                         & \hspace{0.0em}                              & \lnot \biggr[ & (p_{2} \land p_{3})            & \lor  & \cdots & \lor          & (p_{2} \land p_{n})              & \hspace{0.0em} \biggr] \\[0.5em]
        \vdots & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       & \ddots &               & \vdots                           & \hspace{0.0em}         \\[0.5em]
        \land  & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       &        & \lnot \biggr[ & (p_{n-1} \land p_{n})            & \hspace{0.0em} \biggr] \\[0.5em]
        =      & \hspace{0.0em}  \lnot \biggl\{ \biggr[ & \hspace{0.0em} (p_1 \land  p_{2})           & \lor          & ( p_{1} \land p_{3})           & \lor  & \cdots & \lor          & (p_{1} \land p_{n})              & \hspace{0.0em} \biggr] \\[0.5em]
        \lor   & \hspace{0.0em}                         & \hspace{0.0em}                              & \biggr[       & (p_{2} \land p_{3})            & \lor  & \cdots & \lor          & (p_{2} \land p_{n})              & \hspace{0.0em} \biggr] \\[0.5em]
        \vdots & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       & \ddots &               & \vdots                           & \hspace{0.0em}         \\[0.5em]
        \lor   & \hspace{0.0em}                         & \hspace{0.0em}                              &               &                                &       &        & \biggr[       & (p_{n-1} \land p_{n})            & \hspace{0.0em} \biggr]\biggr\} \\[0.5em]
    \end{array}
$$
</div>

<div class = "smallscreen">
    <div align = "center">
        <b>[ Viewable in horizontal mode ]</b>
    </div>
</div>

from where it can be seen that if all propositions $p_k$ are true,
the expression evaluates to $\lnot(\text{T}$ $\lor$ $\text{T}$
$\lor$ $\cdots$ $\lor$ $\text{T})$ $=$ $\lnot \text{T}$ $=$
$\text{F}$, and if all propositions $p_k$ are false, the right
hand-side evaluates to $\text{T}$. Finally, because of the
definition of logical and, if just one of the propositions $p_1$,
$\ldots$, $p_n$ are true and others false, a proposition of the form
$p_{k-1}$ $\land$ $p_k$ always evaluates to false, which then again
leads to $\lnot($ $\text{F}$ $\lor$ $\text{F}$ $\lor$ $\cdots$
$\text{F})$ $=$ $\lnot \text{F}$ $=$ $\text{T}$. So no matter if
just one proposition $p_k$ is true, the expression $(1)$ still
evaluates to $\text{T}$.

### References

Rosen, K. H. (2019). Discrete mathematics & applications. McGraw-Hill.

