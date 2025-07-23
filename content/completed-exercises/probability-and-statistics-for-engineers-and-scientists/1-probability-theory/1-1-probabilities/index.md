+++
title  = "1.1 Probabilities"
layout = "solution-single"
+++

<span class = "exercise-tag">01</span>

When head is denoted as $\text{H}$ and $\text{T}$, the sample space for three
coin tosses is

<div class = "widescreen">
$$
    \phantom{.} \
    \left\{ \
        \begin{array}{ c c c c }
            (\text{T,T,T}) & (\text{T,T,H}) & (\text{T,H,T}) & (\text{T,H,H}) \\[1em]
            (\text{H,T,T}) & (\text{H,T,H}) & (\text{H,H,T}) & (\text{H,H,H})
        \end{array}
    \ \right\}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \phantom{.} \
    \left\{ \
        \begin{array}{ c c c c }
            (\text{T,T,T}) & (\text{T,T,H}) \\[1em]
            (\text{T,H,T}) & (\text{T,H,H}) \\[1em]
            (\text{H,T,T}) & (\text{H,T,H}) \\[1em]
            (\text{H,H,T}) & (\text{H,H,H})
        \end{array}
    \ \right\}
    \ .
$$
</div>

<span class = "exercise-tag">02</span>

Assuming only two genders, male (M) and female (F), then the sample space
for counting in a group is

$$
     \phantom{.} \ \{ \ (0 \cdot \text{F}), (1 \cdot \text{F}), (2 \cdot \text{F}),  \cdot \cdots (n \cdot \text{F}) \ \} \ ,
$$

i.e. the sample space is

$$
    \phantom{.} \ \{ \ n \in \mathbb{N} \ | \ 1 \leq n \leq k \ \} \ ,
$$

for some $k \in \mathbb{N}$.

<span class = "exercise-tag">03</span>

There are four aces in a deck of cards. Then there's a change of having
zero, one, two, three, or four cards in a hand. That is the sample space of
having four cards in a hand of $13$ cards is $\{0,1,2,3,4\}$.

<span class = "exercise-tag">04</span>

A person can have a birthday in any of the $365$ days of the year. So the
sample space for person's birthday is $\{ 1, 2, 3, \ldots, 365 \}$. If
it's a leap year, the sample space is $\{ 1, 2, 3, \ldots, 365, 366 \}$ due
to the leap day.

<span class = "exercise-tag">05</span>

The sample space is

$$
    \phantom{.} \
        \left\{ \
            \begin{array}{c c c c}
                ( & \text{on time} & , & \text{satisfactorily}   &) \\
                ( & \text{late   } & , & \text{satisfactorily}   &) \\
                ( & \text{on time} & , & \text{unsatisfactorily} &) \\
                ( & \text{late   } & , & \text{unsatisfactorily} &)
            \end{array}
        \ \right\}
    \ .
$$

<span class = "exercise-tag">06</span>

The sample space is

$$
    \phantom{.} \
        \left\{ \
            \begin{array}{c}
                \text{(red,shiny)}  \\
                \text{(red,dull)}   \\
                \text{(blue,shiny)} \\
                \text{(blue,dull)}
            \end{array}
        \ \right\}
    \ .
$$

<span class = "exercise-tag">07</span>

**(a)**

If the odds ratio is $1$, then

$$
    \phantom{,} \ \dfrac{p}{(1 - p)} = 1 \ ,
$$

so

$$
    \phantom{,} \ p = (1 - p) \ ,
$$

from where it follows that

$$
    \phantom{.} \ 2p = 1 \ ,
$$

so

$$
    p = \dfrac{1}{2}.
$$

Substituting $p$ back to the *odds ratio* means that

$$
    \phantom{.} \ \dfrac{(1/2)}{(1 - (1/2))} = \dfrac{(1/2)}{(1/2)} = 1 \ .
$$

**(b)**

Similarily, if the odds ratio is $2$, then

$$
    \phantom{,} \ \dfrac{p}{(1 - p)} = 2 \ .
$$

Then

$$
    \phantom{.} \ p = 2(1 - p) = 2 - 2p \ ,
$$

so

$$
    \phantom{.} \ 2p + p = 3p = 2 \ ,
$$

i.e.

$$
    \phantom{.} \ p = \dfrac{2}{3} \ .
$$

Substituting $p$ back, shows that

$$
    \phantom{.} \ \dfrac{(2/3)}{1 - (2/3)} = \dfrac{(2/3)}{(1/3)} = \dfrac{2}{3}\left( \dfrac{3}{1} \right) = 2 \ .
$$

**(c)**

Now,

$$
    \phantom{.} \ \dfrac{p}{(1 - p)} = 0.25 = \dfrac{1}{4} \ ,
$$

so

$$
    \phantom{,} \ \dfrac{p}{(1 - p)} = \dfrac{1}{4} \ ,
$$

so

$$
    \phantom{.} \ p = \dfrac{1}{4}(1 - p) = \dfrac{1}{4} - \dfrac{1}{4}p \ ,
$$

and therefore

$$
    \phantom{.} \ p - \dfrac{1}{4}p = \dfrac{3}{4}p = \dfrac{1}{4} \ .
$$

Dividing both sides with the $p$'s coefficient shows that

$$
    \phantom{.} \ p = \dfrac{(1/4)}{3/4} = \dfrac{1}{4} \left( \dfrac{4}{3} \right) = \dfrac{1}{4} \ .
$$

Substitution leads to

$$
    \phantom{.} \
        \dfrac{(1/4)}{(1 - (1/4))}
            = \dfrac{(1/4)}{(3/4)}
            = \dfrac{1}{4} \left( \dfrac{4}{3} \right)
            = \dfrac{1}{4}
    \ .
$$

<span class = "exercise-tag">08</span>

<div class = "widescreen">
$$
    \begin{array}{r c l}
        P(V) & = & 1 - P(I) - P(II) - P(III) - P(IV) \\[1em]
             & = & 1 - 0.13 - 0.24 - 0.07 - 0.38 \\[1em]
             & = & 0.18 \ .
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        P(V) & = & 1 - P(I) - P(II) - P(III) \\[1em] & & \quad - \ P(IV) \\[1em]
             & = & 1 - 0.13 - 0.24 - 0.07 - 0.38 \\[1em]
             & = & 0.18 \ .
    \end{array}
$$
</div>

<span class = "exercise-tag">09</span>

If $P(IV)$ and $P(V)$ are equally likely and mean

<div class = "widescreen">
$$
    \begin{array}{r c l}
        P(IV) + P(V) & = & 1 - P(I) - P(II) - P(III) \\[1em]
            & = & 1 - 0.08 - 0.2 - 0.33 \\[1em]
            & = & 0.38 \ ,
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
        &   & P(IV) + P(V) \\[1em]
        & = & 1 - P(I) - P(II) - P(III) \\[1em]
        & = & 1 - 0.08 - 0.2 - 0.33 \\[1em]
        & = & 0.38 \ ,
    \end{array}
$$
</div>

then the probability for both $P(IV)$ and $P(V)$ is their sum divided by
$2$, i.e. $0.19$.

<span class = "exercise-tag">10</span>

Since the $P(\text{I}) = 2P(\text{II})$, $P(\text{II}) = 3P(\text{III})$,
and $P(\text{III})$ is the unknown, i.e. $P(\text{III}) = x$, and

$$
    P(\text{I}) + P(\text{II}) + P(\text{III}) = 1 \ ,
$$

then

<div class = "widescreen">
$$
    \begin{array}{c l}
          P(\text{I}) + P(\text{II}) + P(\text{III})
        & = & 2P(\text{II}) + 3P(\text{III}) + P(\text{III}) \\[1em]
        & = & 2 \cdot 3P(\text{III}) + 3P(\text{III}) + P(\text{III}) \\[1em]
        & = & 6x + 3x + x \\[1em]
        & = & 10x \\[1em]
        & = & 1 \ ,
    \end{array} 
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
        &   & P(\text{I}) + P(\text{II}) + P(\text{III}) \\[1em]
        & = & 2P(\text{II}) + 3P(\text{III}) + P(\text{III}) \\[1em]
        & = & 2 \cdot 3P(\text{III}) + 3P(\text{III}) + P(\text{III}) \\[1em]
        & = & 6x + 3x + x \\[1em]
        & = & 10x \\[1em]
        & = & 1 \ ,
    \end{array} 
$$
</div>

from where it can be seen that $x = \frac{1}{10}$. Substituting $x$ back to
$6x + 3x + x = 1$, shows that the probabilities of the outcomes are
$P(\text{I}) = 0.6$, $P(\text{II}) = 0.3$, and $P(\text{III}) = 0.1$.

<span class = "exercise-tag">11</span>

If

$$
    P(\text{low}) = 0.28
$$

and

$$
    \phantom{.} \ P(\text{average}) = 0.55 \ ,
$$

then

$$
    \begin{array}{r c l}
        P(\text{high})
            & = & p \\[1em]
            & = & 1 - P(\text{low}) - P(\text{average}) \\[1em]
            & = & 1 - 0.28 - 0.55 \\[1em]
            & = & 0.17 \ .
    \end{array}
$$
