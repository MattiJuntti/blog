+++
title  = "1.4 Conditional probability"
layout = "solution-single"
+++

<span class = "exnum">1</span> **(a)**

$$
    \begin{array}{r c l}
        P(A|B)
            & = & \dfrac{P(A \cap B)}{P(B)}
            \\[0.5em] & = & \dfrac{0.01 + 0.12 + 0.05}{
                0.01 + 0.02 + 0.05 + 0.11 +
                0.06 + 0.08 + 0.13
            }
            \\[0.5em] & = & \dfrac{0.18}{0.46}
            \\[0.5em] & = & 0.3913
    \end{array}
$$

**(b)**

$$
    \begin{array}{r c l}
        P(C|A)
            & = & \dfrac{P(C \cap A)}{P(C)} \\[0.5em]
            & = & \dfrac{
                0.08 + 0.02 + 0.04 + 0.05
            }{
                0.08 + 0.02 + 0.04 + 0.05 +
                0.07 + 0.11 + 0.11
            }                               \\[0.5em]
            & = & \dfrac{0.19}{0.48}        \\[0.5em]
            & = & 0.3958
    \end{array}
$$

**(c)**

$$
    \begin{array}{r c l}
        P(B|A \cap B)
            & = & \dfrac{P(B \cap (A \cap B))}{P(A \cap B)} \\[0.5em]
            & = & \dfrac{P(B \cap A \cap B)}{P(A \cap B)}   \\[0.5em]
            & = & \dfrac{P(B \cap B \cap A)}{P(A \cap B)}   \\[0.5em]
            & = & \dfrac{P(B \cap A)}{P(A \cap B)}          \\[0.5em]
            & = & \dfrac{P(A \cap B)}{P(A \cap B)}          \\[0.5em]
            & = & 1
    \end{array}
$$

**(d)** Because

$$
    \begin{array}{r c l}
        P(B|A \cup B)
            & = & \dfrac{P(B \cap (A \cup B))}{P(A \cup B)}                      \\[0.5em]
            & = & \dfrac{P((B \cap A) \cup (B \cap B))}{P(A \cup B)}             \\[0.5em]
            & = & \dfrac{P((B \cap A) \cup (B))}{P(A \cup B)}                    \\[0.5em]
            & = & \dfrac{P(B \cap A) - P(B) - P((B \cap A) \cap B)}{P(A \cup B)} \\[0.5em]
            & = & \dfrac{P(B \cap A) - P(B) - P(B \cap A \cap B)}{P(A \cup B)}   \\[0.5em]
            & = & \dfrac{P(B \cap A) - P(B) - P(A \cap B \cap B)}{P(A \cup B)}   \\[0.5em]
            & = & \dfrac{P(B \cap A) - P(B) - P(A \cap B)}{P(A \cup B)}          \\[0.5em]
            & = & \dfrac{P(B \cap A) - P(B) - P(A \cap B)}{P(A \cup B)}          \\[0.5em]
    \end{array}
$$

and $P(B \cap A)$ $=$ $0.01$ $+$ $0.02$ $+$ $0.05$ $=$ $0.08$,
$P(A)$ $=$ $0.07$ $+$ $0.05$ $+$ $0.01$ $+$ $0.08$ $+$ $0.02$ $+$
$0.04$ $+$ $0.05$ $=$ $0.32$ and $P(B)$ $=$ $0.46$, then

$$
    \begin{array}{r c l}
        \dfrac{P(B \cap A) + P(B) - P(A \cap B)}{P(A \cup B)}
            & = & \dfrac{0.08 + 0.46 - 0.08}{
                \begin{array}{l}
                    \phantom{+} 0.07 + 0.05 + 0.01 \\
                    + 0.08 + 0.02 + 0.04 \\
                    + 0.05 + 0.11 + 0.06 \\
                    + 0.08 + 0.13
                \end{array}
            }                       \\[0.5em]
            & = & \dfrac{0.46}{0.7} \\[0.5em]
            & = & 0.6571
    \end{array}
$$

**(e)**

...

**(f)** Because

$$
    \begin{array}{r c l}
        P(A \cap B|A \cup B)
            & = & \dfrac{P((A \cap B) \cap (A \cup B))}{P(A \cup B)} \\[0.5em]
            & = & \dfrac{P(A \cup B)}{P(A \cup B)} \\[0.5em]
            & = & 1,
    \end{array}
$$

because $(A \cap B)$ $\in$ $(A \cup B)$.

<span class = "exnum">3</span> **(a)** Let $A$ denote event that
card is ace of hearts and $B$ that the card is of red suit. Then

$$
    \begin{array}{r c l}
        P(A|B)
        & =       & \dfrac{P(A \cap B)}{P(B)} \\[0.5em]
        & =       & \dfrac{1/52}{26/52}       \\[0.5em]
        & =       & \dfrac{1}{26}             \\[0.5em]
        & \approx & 0.04
    \end{array}
$$

**(b)** If card is heart ($A$) and from red suit ($B$), then

$$
    \begin{array}{r c l}
        P(A|B)
        & = & \dfrac{P(A \cap B)}{P(B)} \\[0.5em]
        & = & \dfrac{13/52}{26/52}      \\[0.5em]
        & = & \dfrac{1/4}{1/2}          \\[0.5em]
        & = & \dfrac{1}{8}.
    \end{array}
$$

**(c)** If card is from red suit ($A$) and a heart ($B$), then

$$
    \begin{array}{r c l}
        P(A|B)
        & =       & \dfrac{P(A \cap B)}{P(B)} \\[0.5em]
        & =       & \dfrac{1/26}{13/52}       \\[0.5em]
        & =       & \dfrac{1/26}{1/4}         \\[0.5em]
        & \approx & 0.15
    \end{array}
$$

**(d)** If card is heart ($A$) and from black suit ($B$), then

$$
    \begin{array}{r c l}
        P(A|B)
        & = & \dfrac{P(A \cap B)}{P(B)} \\[0.5em]
        & = & \dfrac{0}{26/52}          \\[0.5em]
        & = & 0.
    \end{array}
$$

Card can't be heart if it's from black suit.

**(e)** If card is king ($A$) and from red suit, then

$$
    \begin{array}{r c l}
        P(A|B)
        & =       & \dfrac{P(A \cap B)}{P(B)} \\[0.5em]
        & =       & \dfrac{2/26}{26/52}       \\[0.5em]
        & =       & \dfrac{2}{13}             \\[0.5em]
        & \approx & 0.15.
    \end{array}
$$

**(f)** If card is king ($A$) and red picture card ($B$), then

$$
    \begin{array}{r c l}
        P(A|B)
        & =       & \dfrac{P(A \cap B)}{P(B)} \\[0.5em]
        & =       & \dfrac{1/12}{12/52}       \\[0.5em]
        & \approx & 0.36.
    \end{array}
$$
