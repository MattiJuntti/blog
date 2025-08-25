+++
title  = "1.3 Combination of Events"
layout = "solution-single"
+++

<span class = "exnum">1</span> Speaking in terms of sets, because
$A = \{ 0 \}$ is an event of $\mathcal{S}$, it makes the (event)
set $A$ to contain a single element, namely the element
&ldquo;$0$&rdquo;. This means that the event $A$ has an element
that indicates nothing and the element is itself something, so the
set can not therefore be empty, so $A \neq \emptyset$.

<span class = "exnum">2</span> **(a)** $P(B)$ $=$ $0.01$ $+$ $0.02$
$+$ $0.05$ $+$ $0.11$ $+$ $0.06$ $+$ $0.13$ $+$ $0.08$ $=$ $0.46$,
**(b)** $P(B \cap C)$ $=$ $0.02$ $+$ $0.05$ $+$ $0.11$ $=$ $0.08$
**(c)** $P(A \cup C)$ $=$ $0.07$ $+$ $0.05$ $+$ $0.01$ $+$ $0.08$
$+$ $0.02$ $+$ $0.04$ $+$ $0.05$ $+$ $0.07$ $+$ $0.11$ $=$ $0.5$,
**(d)** $P(A \cap B \cap C)$ $=$ $0.02$ $+$ $0.05$ $+$ $0.11$ $=$
$0.18$, **(e)** $P(A \cup B \cup C)$ $=$ $0.07$ $+$ $0.05$ $+$
$0.01$ $+$ $0.08$ $+$ $0.02$ $+$ $0.04$ $+$ $0.05$ $+$ $0.07$ $+$
$0.06$ $+$ $0.11$ $+$ $0.08$ $+$ $0.011$ $+$ $0.13$ $=$ $0.791$,
**(f)** $P(A^\prime \cap B)$ $=$ $0.04$ $+$ $0.05$ $+$ $0.03$
$0.01$ $+$ $0.02$ $+$ $0.05$ $+$ $0.08$ $+$ $0.06$ $+$ $0.11$ $+$
$0.13$ $=$ $0.58$, **(g)** $P(B^\prime \cup C)$ $=$ $0.08$ $+$
$0.04$ $+$ $0.07$ $+$ $0.11$ $=$ $0.3$, **(h)** $P(A \cup (B \cap
C))$ $=$ $0.07$ $+$ $0.05$ $+$ $0.01$ $+$ $0.08$ $+$ $0.02$ $+$
$0.05$ $+$ $0.11$ $=$ $0.39$, **(i)** $P((A \cup B) \cap C)$ $=$
$0.07$ $+$ $0.05$ $+$ $0.01$ $+$ $0.06$ $+$ $0.08$ $+$ $0.13$ $=$
$0.4$, and **(j)** $P(A^\prime \cup C)^\prime$ $=$ $0.04$ $+$
$0.05$ $+$ $0.07$ $+$ $0.11$ $+$ $0.11$ $+$ $0.03$ $=$ $0.38$

<span class = "exnum">3</span>

...

<span class = "exnum">4</span> Given that the event $A$ means a
person is a female, $B$ that a person has black hair and $C$ that a
person has blue eyes, event **(a)** $A \cap B$ means that person is
a black haired female, **(b)** $A \cup C^\prime$ means that person
is female, has brown eyes or both, **(c)** $A^\prime \cap B \cap C$
means that person is non-female with black hair and brown eyes, and
**(d)** $A \cap (B \cup C)$ means that person is female with either
black hair, blue eyes or both.

<span class = "exnum">5</span> Let the event $A$ be that the card
drawn from a deck of cards is either $\diamondsuit$ or
$\heartsuit$, i.e., a red suit, and the event $B$ be that the card
is either $\clubsuit$ or $\spadesuit$, i.e., a black suit. Then if
a card is drawn from a deck of cards, the card is either from $A$
or from $B$, but the card can not be from both sets at the same
time, so $A \cap B = \emptyset$, making the events mutually
exclusive by definition (given in the book at page $17$).  On the
other hand, if the drawn card is ace, say, for example that $A$ $=$
$\{$ $\mathcal{A}\clubsuit,$ $\mathcal{A}\diamondsuit,$
$\mathcal{A}\heartsuit,$ $\mathcal{A}\spadesuit$ $\}$ and that the
drawn card is $B$ $=$ $\{$ $\mathcal{A}\heartsuit,$ $2\heartsuit,$
$\ldots,$ $\mathcal{K}\heartsuit$ $\}$, then $A \cap B$ $=$ $\{ \
\mathcal{A}\heartsuit \ \}$ $\neq$ $\emptyset$, so these events are
not mutually exclusive.

<span class = "exnum">6</span> The events are not mutually
exclusive since the intersection $A \cap B$ has a probability value
or the intersection is not an empty set. Assuming that $A^\prime
\cup B^\prime$ $=$ $\emptyset$,

$$
    \begin{array}{ r c l }
        1 & = & P(A) + P(B) - P(A \cap B) \\[0.5em]
          & = & 0.4 + P(B) - 0.3
    \end{array}
$$

so

$$
    \phantom{.} \ P(B) = 1 - 0.4 - 0.3 = 0.4 \ ,
$$

which is a possible value for probability $P(B)$.

<span class = "exnum">7</span> Because

$$
    P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

then, given the probabilities of the exercise,

$$
    \phantom{,} \ 0.8 = 0.5 + P(B) - 0.1 \ ,
$$

so solving for $P(B)$ it can be shown that

$$
    \phantom{.} \ P(B) = 0.8 - 0.5 + 0.1 = 0.4 \ .
$$

Substituting the probability $P(B)$ back to origianal equation it
can be seen that $0.8$ $=$ $0.5$ $+$ $0.4$ $-$ $0.1$ $=$ $0.8$,
that is, the probability value of $P(B)$ solves the problem, so
$P(B) = 0.4$.

<span class = "exnum">8</span> Let the event that evaluation
reveals a problem be named as $A$ and the event that evaluation is
accurate, i.e. correct, as $B$. The given probabilities can then be
written as $P(B)$ $=$ $0.85$, $P(A \cap B^\prime)$ $=$ $0.10$ and
$P(A^\prime \cap B)$ $=$ $0.25$ .

...

<span class = "exnum">9</span> In order for two events to be
mutually exclusive, the intersection of the events is an empty set.
In other words, given two events $A$ and $B$, $A \cap B$ $=$
$\emptyset$. Two or more mutually exclusive events do not have common
outcomes. When the events $A$, $B$ ja $C$ are defined as in the
exercise, the task is to find the intersection $A \cap B \cap C$.
Since a card drawn from a deck of cards can only be of one suit,
these events do not have any common outcomes so their intersection
is empty making the events mutually exclusive.

The probability of card drawn from a deck of cards is one of the
four suits is $\frac{1}{4}$, so

<div class = "widescreen">
$$
    \phantom{.} \
        P(A \cup B \cup C) = P(A) + P(B) + P(C)
            = \frac{1}{4} + \frac{1}{4} + \frac{1}{4}
            = \frac{3}{4}
    \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c c c}
          & P(A \cup B \cup C) & \phantom{=}           \\[0.75em]
        = & P(A) + P(B) + P(C)                         \\[0.5em]
        = & \dfrac{1}{4} + \dfrac{1}{4} + \dfrac{1}{4} \\[0.5em]
        = & \phantom{.} \ \dfrac{3}{4} \ .
    \end{array}
$$
</div>

The event $A^\prime$ defines the outcomes of drawing any other card
than a card from the suit $\heartsuit$. Since the $B$ is in this
set, i.e. $B$ is a outcome in $A^\prime$, because $B$ means the
event of obtaining a $\clubsuit$, $B \subset A^\prime$.

<span class = "exnum">10</span> The outcomes of **(a)** $A$ $\cap$
$B$ is the event where a card drawn from a deck of cards is
$\mathcal{A}\heartsuit$ or $\mathcal{A}\diamondsuit$, **(b)** the
event $A$ $\cup$ $B$ is the event that the card is ace or a picture
card, **(c)** the event $B$ $\cap$ $C^\prime$ the event that card
is red suited number card and **(d)** the event $A \cup (B^\prime
\cap C)$ that the card is black pictured card and or ace or not.
Since a card cannot be picture card and a ace at the same time, the
event could be taken to mean event where drawn card is a picture
card of black suit.

<span class = "exnum">11</span> Let $A$ mean that repair is on
time, $B$ that repair is satisfactory and $A \cap B$ that repair is
on time and satisfatory. Then $A^\prime \cap B^\prime$ means that
repair wasn't on time and was unsatisfactory, that is, the event is
the intersection of situations when repair is on time and not
satisfactory. The probability of this event is

<div class = "widescreen">
$$
    \begin{array}{r c l}
        P(A^\prime \cap B^\prime)
            & = & 1 - P(A \cup B)                 \\[0.5em]
            & = & 1 - (P(A) - P(B) + P(A \cap B)) \\[0.5em]
            & = & 1 - 0.74 - 0.41 + 0.26          \\[0.5em]
            & = & 0.11.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
          & \hspace{-2.0em} P(A^\prime \cap B^\prime) \\[0.5em]
        = & 1 - P(A \cup B)                           \\[0.5em]
        = & 1 - P(A) - P(B) + P(A \cap B)             \\[0.5em]
        = & 1 - 0.74 - 0.41 + 0.26                    \\[0.5em]
        = & 0.11.
    \end{array}
$$
</div>

<span class = "exnum">12</span> The probability of the event $A$,
that is, ball is shiny is $P(A)$ $=$ $\frac{91}{200}$ $=$ $0.455$,
the probability of the event $B$, that is, ball is red is $P(B)$
$=$ $\frac{79}{200}$ $=$ $0.395$ and the probability $A \cap B$,
that is, ball is shiny and red is $P(A \cap B)$ $=$
$\frac{55}{200}$ $=$ $0.275$.

The probability of event $(A \cup B)$, that is, a randomly selected
ball is either a shiny ball or a red ball is

<div class = "widescreen">
$$
    \begin{array}{r c l}
        P(A \cup B)
            & = & P(A) + P(B) - P(A \cap B) \\[0.5em]
            & = & 0.455 + 0.395 - 0.275     \\[0.5em]
            & = & 0.575.
    \end{array}
$$
</div>


<div class = "smallscreen">
$$
    \begin{array}{c l}
          & \hspace{-2em} P(A \cup B) \\[0.5em]
        = & P(A) + P(B) - P(A \cap B) \\[0.5em]
        = & 0.455 + 0.395 - 0.275     \\[0.5em]
        = & 0.575.
    \end{array}
$$
</div>

<span class = "exnum">13</span>

...

<span class = "exnum">14</span> The probabilites events can be
declared as $P(E_1) = 0.08$ revenue is below expectation, $P(E_2) =
0.19$ revenue is slightly below expectation, $P(E_3) = 0.26$
revenue meets the expectation, $P(E_5) = 0.36$ revenue is slightly
above expectation, and $P(E_6) = 0.11$ revenue is above
expectation. 

Given the probabilities, the union of them is

<div class = "widescreen">
$$
    \begin{array}{c l}
          & P \left( \displaystyle \bigcup_{i \ = \ 1}^6 E_i \right) \\[0.5em]
        = & P(E_1 \cup E_2 \cup E_3 \cup E_4 \cup E_5 \cup E_6) \\[0.5em]
        = & P(E_1) \cup P(E_2) \cup P(E_3) \cup P(E_4) \cup P(E_5) \cup P(E_6) \\[0.5em]
        = & P(E_1) + P(E_2) + P(E_3) + P(E_4) + P(E_5) + P(E_6) \\[0.5em]
        = & 0.08 + 0.19 + 0.26 + 0.36 + 0.11 \\[0.5em]
        = & 1,
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{c l}
          & P \left( \displaystyle \bigcup_{i \ = \ 1}^6 E_i \right) \\[0.5em]
        = & P(E_1 \cup E_2 \cup E_3 \cup E_4 \cup E_5 \cup E_6) \\[0.5em]
        = & P(E_1) \cup P(E_2) \cup P(E_3) \\[0.5em]
          & \cup P(E_4) \cup P(E_5) \cup P(E_6) \\[0.5em]
        = & P(E_1) + P(E_2) + P(E_3) \\[0.5em]
          & + P(E_4) + P(E_5) + P(E_6) \\[0.5em]
        = & 0.08 + 0.19 + 0.26 + 0.36 + 0.11 \\[0.5em]
        = & 1,
    \end{array}
$$
</div>

so at the intersection of these events is no outcomes, or in other
words, the intersection of these events is empty, so statistically
speaking, the probability of any combination of these events
happening at the same time is zero.

The union of the given events $A$ and $B$, or in other words, $A
\cup B$ is the event that the event is not below and not above
expectation, that is, $A \cup B$ is the event that revenue meets
expectation. The probability of this event is $0.26$.

<span class = "exnum">14</span> In the context of the exercise, and
usually in general, the possible revenue outcomes are mutually
exclusive. This means that in the intersection of events $A$
(revenue is not below expection, i.e. revenue meets expectation or
is above expectation) and $B$ (revenue is not above expectation,
i.e. the revenue meets expectation or is below) is that event meets
expectation. The union of these events mean all possible outcomes:
Revenue is considerably or slightly below expectation, meets the
expectation, or is slightly or considerably above expectation.

<span class = "exnum">15</span>

...
