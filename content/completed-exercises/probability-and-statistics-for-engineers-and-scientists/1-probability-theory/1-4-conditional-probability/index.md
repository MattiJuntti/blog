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

<div class = "widescreen">
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
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
              & P(B|A \cup B)                                                  \\[0.5em]
            = & \dfrac{P(B \cap (A \cup B))}{P(A \cup B)}                      \\[0.5em]
            = & \dfrac{P((B \cap A) \cup (B \cap B))}{P(A \cup B)}             \\[0.5em]
            = & \dfrac{P((B \cap A) \cup (B))}{P(A \cup B)}                    \\[0.5em]
            = & \dfrac{P(B \cap A) - P(B) - P((B \cap A) \cap B)}{P(A \cup B)} \\[0.5em]
            = & \dfrac{P(B \cap A) - P(B) - P(B \cap A \cap B)}{P(A \cup B)}   \\[0.5em]
            = & \dfrac{P(B \cap A) - P(B) - P(A \cap B \cap B)}{P(A \cup B)}   \\[0.5em]
            = & \dfrac{P(B \cap A) - P(B) - P(A \cap B)}{P(A \cup B)}          \\[0.5em]
            = & \dfrac{P(B \cap A) - P(B) - P(A \cap B)}{P(A \cup B)}          \\[0.5em]
    \end{array}
$$
</div>

and $P(B \cap A)$ $=$ $0.01$ $+$ $0.02$ $+$ $0.05$ $=$ $0.08$,
$P(A)$ $=$ $0.07$ $+$ $0.05$ $+$ $0.01$ $+$ $0.08$ $+$ $0.02$ $+$
$0.04$ $+$ $0.05$ $=$ $0.32$ and $P(B)$ $=$ $0.46$, then

<div class = "widescreen">
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
            & = & 0.6571.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
              & \dfrac{P(B \cap A) + P(B) - P(A \cap B)}{P(A \cup B)} \\[0.5em]
            = & \dfrac{0.08 + 0.46 - 0.08}{
                \begin{array}{l}
                    \phantom{+} 0.07 + 0.05 + 0.01 \\
                    + 0.08 + 0.02 + 0.04 \\
                    + 0.05 + 0.11 + 0.06 \\
                    + 0.08 + 0.13
                \end{array}
            }                       \\[0.5em]
            = & \dfrac{0.46}{0.7} \\[0.5em]
            = & 0.6571.
    \end{array}
$$
</div>

**(e)**

...

**(f)** Because

<div class = "widescreen">
$$
    \begin{array}{r c l}
        P(A \cap B|A \cup B)
            & = & \dfrac{P((A \cap B) \cap (A \cup B))}{P(A \cup B)} \\[0.5em]
            & = & \dfrac{P(A \cup B)}{P(A \cup B)} \\[0.5em]
            & = & 1,
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
          & P(A \cap B|A \cup B) \\[0.5em]
        = & \dfrac{P((A \cap B) \cap (A \cup B))}{P(A \cup B)} \\[0.5em]
        = & \dfrac{P(A \cup B)}{P(A \cup B)} \\[0.5em]
        = & 1,
    \end{array}
$$
</div>

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

<span class = "exnum">4</span> It the complement of $B$ is not
empty and $A$ $\subset$ $B$, then $P(A)$ is smaller and a proper
subset of $B$, or the same size as $P(A|B)$ and equal to $B$, but
not bigger. An intuition why $A$ can't be bigger is that, if it
was, then

$$
    \frac{P(A \cap B)}{P(B)} > 1
$$

which violates the axiom of probability where all events in a event
space must be less than or equal to $1$.

<span class = "exnum">5</span> The probability for ball being blue
is $\frac{54}{150}$, so there are $150 - 54$ $=$ $96$ red balls in
the bag. The probability that chosen red and shiny is then

$$
    \dfrac{36}{96} = \dfrac{3}{8}.
$$

The probability of a chosen ball being dull red is then $1 -
\frac{3}{8}$ $=$ $\frac{5}{8}$, where $1$ is the event of ball
being red.

<span class = "exnum">6</span> Let $P(X)$ stand for the probability
of event that car repair is on time and $P(Y|X)$ stand for the
probability that the repair is satisfactory, given it's on time.
From the problem definition it's known that $P(X)$ $=$ $0.77$ and
$P(Y|X)$ $=$ $0.85$. The probability that repair is on time and is
satisfactory is

$$
    \begin{array}{c r c l}
                            & P(X|Y) & = & \dfrac{P(Y \cap X)}{P(X)} \\[0.5em]
        \Longleftrightarrow & 0.85   & = & \dfrac{P(Y \cap X)}{0.77}.
    \end{array}
$$

Multiplying both sides of the right hand equation shows that

<div class = "widescreen">
$$
    P(Y \cap X) = P(X \cap Y) = 0.85 \cdot 0.77 = 0.6545.
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
          & P(Y \cap X)     \\[0.5em]
        = & P(X \cap Y)     \\[0.5em]
        = & 0.85 \cdot 0.77 \\[0.5em]
        = & 0.6545.
    \end{array}
$$
</div>

<span class = "exnum">7</span> **(a)** If it's raining today, the
probability of raining tomorrow either increases, decreases or
remains unchanged. **(b)** The probability that lottery winner has
black hair, conditioned on that the lottery winner has brown eyes
remains unchanged. **(c)** The probability that lottery winner has
black hair, conditioned on that the lottery winner own a red car
remains unchanged. **(d)** The probability that a lottery winner is
more than $50$, conditioned on that the lottery winner is more than
$30$ years old remains unchanged.

<span class = "exnum">8</span> Since the assumption is that births
are equally like on any day, the probability that a random person
has a birthday on first day $P(A)$ $=$ $\frac{12}{365}$, because
there are $12$ first days in a year, one for each month. When
conditioned on March, i.e. what is the probability that the first
person is born on first day given that day is in March is
$\frac{1}{31}$, because there is only one first day on March. If
the given month is February, the denominator of the previous
fraction becomes $28$, so the probability for person born on first
day given the month is February is $\frac{1}{28}$.

<span class = "exnum">9</span> The events of batteries failing are:

$$
    \begin{array}{| c c |} \hline
        E_1                 & E_2                 \\
        (\text{I, II, III}) & (\text{I, III, II}) \\
        \text{\small 0.11}  & \text{\small 0.07}  \\[1.0em]
        E_3                 & E_4                 \\
        (\text{II, I, III}) & (\text{II, III, I}) \\
        \text{\small 0.24}  & \text{\small 0.39}  \\[1.0em]
        E_5                 & E_6                 \\
        (\text{III, I, II}) & (\text{III, II, I}) \\
        \text{\small 0.16}  & \text{\small 0.03}  \\ \hline
    \end{array}
$$

where a sequence $(A,B,C)$ denotes that battery of type $A$ fails
first, then type $B$ and finally $C$. Given these the probabilities:

**(a)** Let probability of type $\text{I}$ battery lasting longest
is $P(A)$. Then it not failing first is $P(A^\prime)$. Given these,
$A$ conditional on $A^\prime$ is

<div class = "widescreen">
$$
    \begin{array}{r c l}
        P(A|A^\prime)
            & =       & \dfrac{P(A \cap A^\prime)}{P(A^\prime)}                              \\[0.5em]
            & =       & \dfrac{P(A \cap \{1 - P(A)\})}{1 - P(A)}                             \\[0.5em]
            & =       & \dfrac{P(\{E_4,E_6\} \cap \{E_3,E_4,E_5,E_6\})}{\{E_3,E_4,E_5,E_6\}} \\[0.5em]
            & =       & \dfrac{P(\{E_4,E_6\})}{P(\{E_3,E_4,E_5,E_6\})}                       \\[0.5em]
            & \approx & 0.51.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
                & P(A|A^\prime)                                                        \\[0.5em]
        =       & \dfrac{P(A \cap A^\prime)}{P(A^\prime)}                              \\[0.5em]
        =       & \dfrac{P(A \cap \{1 - P(A)\})}{1 - P(A)}                             \\[0.5em]
        =       & \dfrac{P(\{E_4,E_6\} \cap \{E_3,E_4,E_5,E_6\})}{\{E_3,E_4,E_5,E_6\}} \\[0.5em]
        =       & \dfrac{P(\{E_4,E_6\})}{P(\{E_3,E_4,E_5,E_6\})}                       \\[0.5em]
        \approx & 0.51.
    \end{array}
$$
</div>

**(b)** The probability of type $\text{I}$ battery lasting
longest ($A$) conditional on type $\text{II}$ failing first ($B$)
is

$$
    \begin{array}{r c l}
        P(A|B)
            & =       & \dfrac{P(A \cap B)}{P(B)}      \\[0.5em]
            & =       & \dfrac{P(E_4)}{P(\{E_3,E_4\})} \\[0.5em]
            & \approx & 0.93.
    \end{array}
$$

**(c)** The probability of type $\text{I}$ battery lasting longest
($A$) conditional on type $\text{II}$ lasting longest ($B$) is $0$
because $P(A \cap B)$ $=$ $0$ due to $A$ and $B$ being disjoint
events.

**(d)** The probability of type $\text{I}$ battery lasting longest
($A$) is $P(A)$ $=$ $P(\{E_4,E_6\})$ and the probability of type
$\text{II}$ battery not failing first ($B$) is $P(B)$ $=$
$P(\{E_1,E_2,E_5,E_6)$, so $A$ conditional on $B$ is $P(A \cap B)$
$/$ $P(B)$ $=$ $0.03$ $/$ $(0.11 + 0.07 + 0.16 + 0.03)$ $=$ $0.03$
$/$ $0.37$ $\approx$ $0.08$.

<span class = "exnum">10</span> The given probability values for
two assembly lines operations are,

$$
    \begin{array}{ | c c c | } \hline
        (S,S)                & (S,P)                & (S,F)          \\[-0.25em]
        \text{\small 0.02} & \text{\small 0.06} & \text{\small 0.05} \\[1em]
        (P,S)                & (P,P)                & (P,F)          \\[-0.25em]
        \text{\small 0.07} & \text{\small 0.14} & \text{\small 0.20} \\[1em]
        (F,S)                & (F,P)                & (F,F)          \\[-0.25em]
        \text{\small 0.06} & \text{\small 0.21} & \text{\small 0.19} \\[1em]
        \hline
    \end{array}
$$

where $S$ stands for given line being shutdown, $P$ for line
running at partial capacity and $F$ for line running at full
capacity.

**(a)** The event that both lines are at full capacity is $A$ $=$
$\{ (F,F) \}$ and the event that neither of the lines are shutdown
is $B$ $=$ $\{ (P,P), (P,F), (F,P), (F,F) \}$, so $A$ conditional
on $B$ is $P(A|B)$ $=$ $P(A \cap B)$ $/$ $P(B)$ $=$ $0.19$ $/$
$(0.14$ $+$ $0.20$ $+$ $0.21$ $+$ $0.19)$ $\approx$ $0.26$.

**(b)** If event that at least one line is at full capacity $A$
$=$ $\{(S,F),$ $(P,F),$ $(F,S),$ $(F,P),$ $(F,F)\}$ and the event
that neither line being shut is $B$ $=$ $\{(P,P),$ $(P,F),$
$(F,P),$ $(F,F)\}$, then $A$ conditional on $B$ is $P(A|B)$ $=$
$P(A \cap B)$ $/$ $P(B)$ $=$ $(0.20$ $+$ $0.21$ $+$ $0.19)$ $/$
$(0.14$ $+$ $0.20$ $+$ $0.21$ $+$ $0.19)$ $\approx$ $0.81$.

**(c)** When the event that at least one assembly line is running
at full capacity is $A$ $=$ $\{(S,F),$ $(P,F),$ $(F,S),$ $(F,P),$
$(F,F)\}$ and the event where exactly one line is being shut down
$B$ $=$ $\{(S,P),$ $(S,F),$ $(P,S),$ $(F,S)\}$, then $A$
conditional on $B$ is $P(A|B)$ $=$ $P(A \cap B)$ $/$ $P(B)$ $=$
$(0.05$ $+$ $0.06)$ $/$ $(0.06$ $+$ $0.05$ $+$ $0.07$ $+$ $0.06)$
$\approx$ $0.46$.

**(d)** Probability that neither line is at full capacity ($A$)
conditional on at least one line is operating at partial capacity,
that is, one line is either $P$ or $F$, or both, or in other words
is not $(S,S)$ is $P(A|B)$ $=$ $P(A \cap B)$ $/$ $P(B)$ $=$ $(0.02$
$+$ $0.06$ $+$ $0.07$ $+$ $0.14)$ $/$ $(1 - 0.02)$ $\approx$ $0.30$.
