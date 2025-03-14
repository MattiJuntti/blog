+++
title  = "1.2 Events"
layout = "solution-single"
+++

<span class = "exnum">1</span>
**(a)** The probability of $P(b)$ $=$ $1$ $-$ $P(a)$ $-$ $P(c)$ $-$ $P(d)$
$-$ $P(e)$ $=$ $1$ $-$ $0.13$ $-$ $0.48$ $-$ $0.02$ $-$ $0.22$, and **(b)**
the probaiblity of event $P(A)$ $=$ $p(c)$ $+$ $p(d)$ $=$ $0.48$ $+$ $0.02$
$=$ $0.5$. Now that $P(A)$ is known and the equation for computing the
complement of $A$ is given in the book, then it can be said that **(c)**
$P(A^\prime)$ $=$ $1 - P(A)$ $=$ $1 - 0.5$ $=$ $0.5$.

<span class = "exnum">2</span>
**(a)** If $P(A) = 0.27$, then $P(b)$ $=$ $P(A)$ $-$ $p(c)$ $-$ $p(e)$ $=$
$0.27$ $-$ $0.11$ $-$ $0.06$ $=$ $0.22$. Now that $P(b)$ is know, it
becomes possible to see that **(b)** $P(A^\prime)$ $=$ $1 - P(A)$ $=$ $1$
$-$ $(P(b)$ $+$ $P(c)$ $+$ $P(e))$ $=$ $1$ $-$ $(0.22$ $+$ $0.11$ $+$
$0.06)$ $=$ $1$ $-$ $0.39$ $=$ $0.61$. Therefore **(c)** $P(d)$ $=$ $1$ $-$
$p(a)$ $-$ $p(b)$ $-$ $p(c)$ $-$ $p(e)$ $-$ $p(f)$ $=$ $1$ $-$ $0.09$ $-$
$0.22$ $-$ $0.11$ $-$ $0.06$ $-$ $0.29$ $=$ $0.23$.

<span class = "exnum">3</span>
If birthdays are equally likely to fall on any day, then the probability of
one birthday to fall on one day out of the possible 365, excluding the leap
years, is $\frac{1}{365}$. The probability of birthday falling to a
specific month is $\prod_{n \ = \ 1}^{d}\frac{1}{365}$ $=$
$\frac{31}{365}$, where $d$ is the number of days in a month. For January
$d$ $=$ $31$, and for February $d$ $=$ $28$, again, excluding the leap
years, so the probability of having a birthday in January is
$\frac{31}{365}$ and in February it's $\frac{28}{365}$.

<span class = "exnum">4</span>
The costs will decrease when they are not staying the same or increasing.
Since the given probabilities for the latter two are $0.018$ and $0.03$,
subtracting them from the total probability $1$ is the probability of costs
decreasing, i.e. $0.79$. Costs won't increase when they stay the same or
are decreaseng is $0.03$ $+$ $0.18$ $=$ $0.21$.

<span class = "exnum">5</span>
The situation can be modeled in the following way: Let the proposition $A$
be equal to that the Company A's stock will increase, and proposition $B$
mean that the Company B's stock will increase. Then there are four
probabilities to consider which are given in the following Table 1,

$$
    \begin{array}{ c c c }
                           &              & p          \\[0.5em] \hline
        \quad A \uparrow   & B \uparrow   & 0.38 \quad \\[0.5em]
        \quad A \uparrow   & B \downarrow &    x \quad \\[0.5em]
        \quad A \downarrow & B \uparrow   & 0.16 \quad \\[0.5em]
        \quad A \downarrow & B \downarrow & 0.11 \quad \\[0.5em]
    \end{array}    
$$

<br>

<div align = "center">
    Table 1: Possible probabilities for the stocks.
</div>

where $X\uparrow$ means that $X$'s stock will rise, and $X\downarrow$ the
opposite. The $p$ indicates the probability of events in a give row
happening simultaneously.

Since the probabilities of all of these events must add to $1$, the

$$
    x = 1 - 0.38 - 0.16 - 0.11 = 0.35,
$$

that is the event $A\uparrow$ and $B\downarrow$ has the probability of
$0.35$.

The probability that at least one company's stock will rise is the
probability is the cumulative probability of those probabilities where it
is true that at least one company is in state $\uparrow$. Adding those
probabilities are

<widescreen>
$$
    p(A\uparrow \text{ and } B\uparrow) + p(A\uparrow \text{ and } B\downarrow) + p(A\downarrow \text{ and } B\uparrow) \ = \ 0.38 + 0.35 + 0.16 = 0.89.
$$
</widescreen>

<smallscreen>
$$
    \begin{array}{ r c }
          & p(A\uparrow \text{ and } B\uparrow)   \\[0.5em]
        + & p(A\uparrow \text{ and } B\downarrow) \\[0.5em]
        + & p(A\downarrow \text{ and } B\uparrow) \\[0.5em]
        = & 0.38 + 0.35 + 0.16                    \\[0.5em]
        = & 0.89.
    \end{array}
$$
</smallscreen>

<span class = "exnum">6</span> Writing out explicitly all the combinations
of outcomes when rolling two fair six sided dices are given in the Table 2:

$$
    \small {
        \begin{array}{ c c c c c c }
            (1,1)          & (1,2)          & (1,3)          & (1,4)          & (1,5)          & (1,6) \\[0.5em]
            \textbf{(2,1)} & (2,2)          & (2,3)          & (2,4)          & (2,5)          & (2,6) \\[0.5em]
            \textbf{(3,1)} & \textbf{(3,2)} & (3,3)          & (3,4)          & (3,5)          & (3,6) \\[0.5em]
            \textbf{(4,1)} & \textbf{(4,2)} & \textbf{(4,3)} & (4,4)          & (4,5)          & (4,6) \\[0.5em]
            \textbf{(5,1)} & \textbf{(5,2)} & \textbf{(5,3)} & \textbf{(5,4)} & (5,5)          & (5,6) \\[0.5em]
            \textbf{(6,1)} & \textbf{(6,2)} & \textbf{(6,3)} & \textbf{(6,4)} & \textbf{(6,5)} & (6,6) \\[0.5em]
        \end{array}
    }
$$

<br>

<div align = "center">
    Table 2: All possible permutations of rolling two dices.
</div>

In the Table 2 all outcomes where all the strictly greater values of the
red dice, i.e. the first value of a tuple $(x,y)$, are boldened. The number
of these outcomes is $15$ out of all $36$ possible values, i.e. the
probability of outcome where the red die is strictly less $0.5$ is

$$
    \dfrac{15}{16} = 0.4167.
$$

Complement of the event is $1 - 0.4167 = 0.5833$.

<span class = "exnum">7</span> In a deck of cards there are commonly $52$
cards. There are two possible colors in these kind of decks, so each color
has $1 / 2$ $=$ $0.5$ proability being one of the either color.

<span class = "exnum">8</span> From a deck of $52$ cards there are four
possible aces, so the probability of card being a ace of one suit is
$\frac{4}{52}$ $=$ $0.076923$.

<span class = "exnum">9</span> **(a)** The probability that Terica is the
winner is $\frac{1}{4} = 0.25$ and **(b)** the probability that Terica is
winner or a runner up is $\frac{1}{4}$ $+$ $\frac{1}{4}$ $=$ $\frac{2}{4}$
$=$ $\frac{1}{2}$ $=$ $0.5$.

<span class = "exnum">10</span> **(a)** The probability that the battery
$\text{I}$ lasts longest is the sum of all of the outcomes where $\text{I}$
is at the third index. These are the outcomes at center right and bottom
right of the Figure 1.24, so summing their probabilities are $0.39$ $+$
$0.03$ $=$ $0.42$.

**(b)** Similarily the outcomes where the battery $\text{I}$ is at the
first index of the tuple are the probabilites that the battery $\text{I}$
last shortest, that is, the probabilities of top left and top right.
Summing these probabilities are $0.11$ $+$ $0.07$ $=$ $0.18$, which is the
the probability of the event that battery $\text{I}$ lasts the shortest.

**(c)** The event that battery $\text{I}$ does not last longest is the
complement of the probability of battery $\text{I}$ lasting the longest,
i.e.

$$
    1 - 0.42 = 0.58.
$$

**(d)** The probabilities of the event where the battery $\text{I}$ does
lasts longer than battery $\text{II}$ are the sum of probabilities where
$\text{I}$ lies on the right hand-side of $\text{II}$. These are center
left and right, and the one on the bottom right, so the sum is $0.24$ $+$
$0.39$ $+$ $0.03$ $=$ $0.66$.

<span class = "exnum">11</span> **(a)** The probability that both assembly
lines are <i>shut down</i> $(S)$ are $p(S,S)$ $=$ $0.02$. **(b)** When
neither of the assembly lines is down, a assembly line is running in
<i>full capacity</i> ($F$) or in <i>partial capacity</i> $(P)$. These are
the events where the value of the tuples in Figure 1.25 are either $F$ or
$P$, so the sum $(P,P)$ $+$ $(P,F)$ $+$ $(F,P)$ $+$ $(F,F)$ $=$ $0.14$ $+$
$0.20$ $+$ $0.21$ $+$ $0.21$ $+$ $0.19$ $=$ $0.74$.

<span class = "exnum">12</span> When a fair coin is thrown three times, the
number of possible combinations of having heads ($\text{H}$) or tails
($\text{T}$) are

$$
    \begin{array}{ c c c }
        \text{1}          & \text{2}          & \text{3}          \\[0.5em] \hline
        \text{\textbf{H}} & \text{\textbf{H}} & \text{\textbf{H}} \\
        \text{\textbf{H}} & \text{\textbf{H}} & \text{\textbf{T}} \\
        \text{H}          & \text{T}          & \text{H}          \\
        \text{H}          & \text{T}          & \text{T}          \\
        \text{T}          & \text{\textbf{H}} & \text{\textbf{H}} \\
        \text{T}          & \text{H}          & \text{T}          \\
        \text{T}          & \text{T}          & \text{H}          \\
        \text{T}          & \text{T}          & \text{T}          \\
    \end{array}
$$

where all the toss-sequences that have two consequantial $\text{H}$ are
boldened. There are three such rows. Also, as it can be seen from the
table, in total there are eight possible combinations one can have from
tossing a coin three times, so the probability of having two consecutive
$\text{H}$ is

$$
    \frac{3}{8} = 0.3750.
$$

<span class = "exnum">13</span> The companys expectation that revenue is
not below expectation is with probability $0.26$ $+$ $0.36$ $+$ $0.11$ $=$
$0.73$.

<span class = "exnum">14</span> The probability that the advertising
campaign is launched is the sum of the all probabilities that are above
&ldquo;canceled before launch&rdquo;, i.e. the probability that the
advertising campaign is launced but canceled ($0.18$), launched and runs
its targeted length ($0.43$), and launched and is extended beyond its
targeted length ($0.29$), which is $0.9$.
