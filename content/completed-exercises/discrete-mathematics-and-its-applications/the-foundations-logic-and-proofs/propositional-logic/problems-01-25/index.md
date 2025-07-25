+++
title  = "Problems 01-25"
date   = 2025-01-01T00:00:00+03:00
layout = "solution-single"
+++

<span class = "exnum">1</span>
**(a)** A proposition, True ($\text{T}$).
**(b)** A proposition, $\text{T}$.
**(c)** A proposition, $\text{T}$.
**(d)** A proposition, False $\text{F}$.
**(e)** Not a proposition, $\text{T}$ when $x = 2$, $\text{F}$ otherwise.
**(f)** Not a proposition, because not a declarative sentence.

<span class = "exnum">2</span>
**(a)** Not a proposition, because not a declarative sentence.
**(b)** Not a proposition, because is a question, i.e. not a declarative sentence.
**(c)** A proposition, very very likely $\text{T}$
**(d)** Not a proposition, but if $x = 1$, then $\text{T}$.
**(e)** A proposition, $\text{F}$.
**(f)** Not a proposition, because the sentence is mathematical statement with variables.

<span class = "exnum">3</span>
**(a)** If

$$
    \phantom{,} \ p = \text{``Linda is younger than Sanjay''} \ ,
$$

then

$$
    \phantom{,} \ \lnot p = \text{``Linda is not younger than Sanjay''} \ .
$$

**(b)** If

$$
    \phantom{,} \ p = \text{``Mei makes more money than Isabella''} \ ,
$$

then

$$
    \phantom{,} \ \lnot p = \text{``Mei makes less money than Isabella''} \ .
$$

**(c)** If

$$
    \phantom{,} \ p = \text{``Moshe is taller than Monica''} \ ,
$$

then

$$
    \begin{array}{r c l}
        \lnot p & = & \text{``Moshe is not taller than Monicaj} \\
                & = & \text{``Moshe is shorter than Monica''} \ .
    \end{array}
$$

**(d)** If

$$
    \phantom{,} \ p = \text{``Abby is richer than Ricardo''} \ ,
$$

then

$$
    \phantom{,} \ \lnot p = \text{``Abby is poorer than Ricardo''} \ .
$$

<span class = "exnum">4</span>

**(a)** $\lnot p = \text{``Janice has less Facebook friends than Juan.''}$
<br>
**(b)** $\lnot p = \text{``Quincy is not smarter than Venkat.''}$
<br>
**(c)** $\lnot p = \text{``Zelda drives less miles to school than Paola.''}$
<br>
**(d)** $\lnot p = \text{``Briana wakes up earlier than Gloria.''}$

<span class = "exnum">5</span>

**(a)** $\lnot p = \text{``Mei doesn't have a MP3 player.''}$ <br>
**(b)** $\lnot p = \text{``There's pollution in New Jersey.''}$ <br>
**(c)** $\lnot p = \text{``}2 + 1 \neq 3\text{.''}$ <br>
**(d)** $\lnot p = \text{``The summer in Maine is not hot and sunny.''}$

<span class = "exnum">6</span>

**(a)** $\lnot p = \text{``Jennifer and Teja aren't friends.''}$<br>
**(b)** $\lnot p = \text{``There aren't $13$ items in a baker's dozen''}$<br>
**(c)** $\lnot p = \text{``Abby sen less than $100$ text messages yesterday.''}$<br>
**(d)** $\lnot p = \text{``$121$ is not a perfect square.''}$

<span class = "exnum">7</span>

**(a)** $\lnot p = \text{``Steve does not have more than $100$ GB free disk space on his laptop.''}$<br>
**(b)** $\lnot p = \text{``Zach does not block e-mails or texts from Jennifer.''}$<br>
**(c)** $\lnot p = \text{``$7 \cdot 11 \cdot 13 \neq 999$.''}$<br>
**(d)** $\lnot p = \text{``Diane didn't rode her bicycle 100 miles on Sunday.''}$

<span class = "exnum">8</span>

**(a)** Let $\operatorname{N}_{\text{RAM}}(\text{X})$ denote the number of
random access memory in a cell phone. Then the proposition can be expressed
as

$$
    \begin{array}{r c l}
        (\operatorname{N}_{\text{RAM}}(\text{B}) > \operatorname{N}_{\text{RAM}}(\text{A}))
        & \land & (\operatorname{N}_{\text{RAM}}(\text{B}) > \operatorname{N}_{\text{RAM}}(\text{C})) \\[0.5em]
        & \Updownarrow &                                                                              \\[0.5em]
        (288 > 128) & \land & (288 > 256)                                                             \\[0.5em]
        & \Updownarrow &                                                                              \\[0.5em]
        \text{T} & \land & \text{T}                                                                   \\[0.5em]
        & \Updownarrow &                                                                              \\[0.5em]
        & \phantom{.} \text{T} ,
    \end{array}
$$

which means that the proposition is true.

**(b)** The sentence can be broken down into proposition

<div align = "left">
    $\qquad p = \text{``Smartphone C has more ROM than than smartphone B''}$
</div>

and

<div align = "left">
    $\qquad q = \text{``Smartphone C has higher resolution than smartphone B''}$.
</div>

The conjunction of these proposition is therefore

$$
    \phantom{,} \ p \lor q \ . \tag{1}
$$

Since $\text{Smartphone C}$ has more ROM than $\text{Smartphone B}$, i.e.
$p = \text{T}$, and $\text{Smartphone C}$ has lower resolution than
$\text{Smartphone B}$, i.e. $q = \text{F}$, the proposition $(1)$ is
$\text{T} \lor \text{F} = \text{T}$.

**(c)** Similarily as above, the propositions are:

<div align = "left">
    $\qquad p = \text{``Smartphone B has more RAM than smartphone A''}$
    $\qquad q = \text{``Smartphone B has more ROM than smartphone A''}$
    $\qquad r = \text{``Smartphone B has has highger reolution than smartphone A''}$
</div>

Then the main proposition can be written as

$$
    \phantom{.} \ p \land q \land r \ .
$$

Evalutating the truth values means that $p$ is false ($\text{F}$), $q$ is
true ($\text{T}$), and $r$ is false ($\text{F}$), so the main proposition

$$
    \phantom{.} \
    \phantom{.} \ p \land q \land r = \text{F} \land \text{T} \land \text{F}
    \ .
$$

In order for the logical conjunction to be true, all truth values should be
true, so the proposition is $\text{F}$.

**(d)** The propositions are:

<div align = "left">
    $\qquad p = \text{``Smartphone B has more RAM than smartphone C''}$
    $\qquad q = \text{``Smartphone B has more ROM than smartphone C''}$
    $\qquad r = \text{``Smartphone B has higher resolution than smartphone C''}$
</div>

so the proposition ginve by the task can be written as

$$
    \phantom{.} \ (p \land q) \rightarrow r \ .
$$

Writin out the truthtable for the propositions

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        \quad p \quad & \quad q \quad & \quad r \quad & \quad p \land q \quad & \quad (p \land q) \rightarrow r \quad \\[0.5em] \hline
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\[0.5em]
        \text{T} & \text{T} & \text{F} & \text{T} & \text{F} \\[0.5em]
        \text{T} & \text{F} & \text{T} & \text{F} & \text{T} \\[0.5em]
        \text{T} & \text{F} & \text{F} & \text{F} & \text{T} \\[0.5em]
        \text{F} & \text{T} & \text{T} & \text{F} & \text{T} \\[0.5em]
        \text{F} & \text{T} & \text{F} & \text{F} & \text{T} \\[0.5em]
        \text{F} & \text{F} & \text{T} & \text{F} & \text{T} \\[0.5em]
        \text{F} & \text{F} & \text{F} & \text{F} & \text{T} \\[0.5em] \hline
    \end{array}
$$

Since $p$ is $\text{T}$, $q$ is $\text{T}$, and $r$ is $\text{F}$, it can
be seen from the second row of the above truth table that the proposition
of the task is $\text{F}$.

**(e)** The propositions of the declaration are

<div align = "left">
    $\qquad p = \text{``Smartphone A has more RAM than smartphone B''}$
    $\qquad q = \text{``Smartphone B has more RAM than smartphone A''}$
</div>

so the statement can be written as

$$
    p \leftrightarrow q
$$

which is equal to

$$
    \phantom{.} \ (p \rightarrow q) \land (q \rightarrow r)  \ .
$$

The truth table for this expression is

$$
    \begin{array}{ | c | c | c | c | c | } \hline
           \quad  p \quad                                        &
           \quad  q \quad                                        &
           \quad  p \rightarrow q \quad                          &
           \quad  q \rightarrow p \quad                          &
           \quad (p \rightarrow q) \land (q \rightarrow p) \quad \\[0.5em] \hline
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\[0.5em]
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} \\[0.5em]
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F} \\[0.5em]
        \text{F} & \text{F} & \text{T} & \text{T} & \text{T} \\[0.5em] \hline
    \end{array}
$$

Because $p$ is $\text{F}$ and obviously $q$ is $T$, then it can be seen
from the 3rd row of the above truth table that the statment if $\text{F}$.

<span class = "exnum">9</span> **(a)** The proposition is $\text{F}$.
**(b)** True and true, so the proposition is $\text{T}$. **(c)** False and
false, so $\text{F}$. **(d)** The first proposition is $\text{F}$, the
second $\text{T}$, so the proposition is $\text{T}$ by the definition of
implication. **(e)** Because $p \leftrightarrow q = (p \rightarrow q) \land
(q \rightarrow p)$, $p = \text{F}$ and $q = \text{T}$, the proposition is
$\text{T}$.

<span class = "exnum">10</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;I bought a lottery ticket this week&rdquo;.
    <br>
    $\qquad q =$ &ldquo;I won the million dollar jackpot&rdquo;.
</div>

thegiven (compound) propositions are:

**(a)** $\lnot p =$ &ldquo;I didn't buy a lottery ticket this week&rdquo;.

**(b)** $p \lor q =$ &ldquo;I gought a lottery ticket this week of I won the
million dollar jackpot&rdquo;

**(c)** $p \rightarrow q =$ &ldquo;If I bought a lottery ticket this week,
then I won the million dollar jackpot&rdquo;.

**(d)** $p \land q =$ &ldquo;I bought a lottery ticket this week and I won the million dollar jackpot.&rdquo;

**(e)** $p \leftrightarrow q =$ &ldquo;If and only if I bought a lottery
ticket this week, I won the million dollar jackpot&rdquo;.

**(f)** $\lnot p \rightarrow \lnot q =$ &ldquo;If I didn't buy a lottery ticket
this week, then I did not win the million dollar jackpot&rdquo;.

**(g)** $\lnot p \land \lnot q =$ &ldquo;I did not buy a lottery ticket this week
and I did not win the million dollar jackpot&rdquo;.
ticket this week, then I did not win the million dollar&rdquo;.

**(h)** $\lnot p \land (p \land q) =$ &ldquo;I did not buy a lottery ticket
this week or I bought a lottery ticket this week and I won the million
dollar jackpot&rdquo;.

<span class = "exnum">11</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;Swimming at the New Jersey shore is allowed;.
    <br>
    $\qquad q =$ &ldquo;Sharks have been spotted near the shore&rdquo;.
</div>

the given (compound) propositions are:

**(a)** $\lnot q =$ &ldquo;Swimming at the New Jersey shore is not
allowed&rdquo;

**(b)** $p \land q =$ &ldquo;Swimming at the New Jersey shore is allowed
and sharks have been spotted near the shore&rdquo;.

**(c)** $\lnot p \land q =$ &ldquo;Swimming at the New Jersey shore is not
allowed or sharks have been spotted near the shore&rdquo;

**(d)** $p \rightarrow \lnot q =$ &ldquo;If swimming at the New Jersey
shore is allowed, then sharks have not been spotted near the shore&rdquo;.

**(e)** $\lnot q \rightarrow p =$ &ldquo;If sharks have not been spotted
near the shore, then sharks have been spotted near the shore&rdquo;

**(f)** $\lnot p \rightarrow \lnot q =$ &ldquo;If swimming at the New
Jersey shore is not allower, then sharks have not been spotted near the
shore&rdquo;.

**(g)** $p \leftrightarrow \lnot q =$ &ldquo;If and only if swimming at the
New Jersey shore is allowed, sharks have not been spotted near the shore&rdquo;.

**(h)** $\lnot p \land (p \lor \lnot q) =$ &ldquo;If swimming at the New
Jersey shore is not allowed and swimming at the New Jersey shore is
allowed or sharks have not been spotted near the shore&rdquo;.

<span class = "exnum">12</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;The election is decided&rdquo;.
    <br>
    $\qquad q =$ &ldquo;The votes have been counted&rdquo;.
</div>

the given (compound) propositions are:

**(a)** $\lnot p =$ &ldquo;The election is not decided&rdquo;.

**(b)** $p \land q =$ &ldquo;The election is decided and the votes have
been counted&rdquo;.

**(c)** $\lnot p \land q =$ &ldquo;The election is not decided and the
votes have been counted&rdquo;.

**(d)** $q \rightarrow p =$ &ldquo;If the election is decided, then the
votes have been counted&rdquo;.

**(e)** $\lnot q \rightarrow \lnot p =$ &ldquo;If the votes have not been
counted, then the election is not decided&rdquo;.

**(f)** $\lnot p \rightarrow \lnot q =$ &ldquo; If the election is not
decided, then the votes have not been counted&rdquo;.

**(e)** $p \leftrightarrow q =$ &ldquo;If and only if the election is
decided, the votes have not been counted&rdquo;.

**(f)** $\lnot q \land (\lnot p \lor q) =$ &ldquo;The votes have not been
counted or the election is not decided and the votes have been counted&rdquo;.

<span class = "exnum">13</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;It is below freezing&rdquo;.
    <br>
    $\qquad q =$ &ldquo;It is snowing&rdquo;.
</div>

the propositions are:

**(a)** $p \land q$. **(b)** $p \land \lnot q$. **(c)** $\lnot p \land
\lnot q$. **(d)** $q \leftrightarrow p$ **(e)** $p \rightarrow q$. **(f)**
$(p \lor q) \lor (p \rightarrow q)$ **(g)** $p \leftrightarrow q$.

<span class = "exnum">14</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;You have the flu&rdquo;.
    <br>
    $\qquad q =$ &ldquo;You miss the final examination&rdquo;.
    <br>
    $\qquad r =$ &ldquo;You pass the course&rdquo;.
</div>

then

**(a)** $p \rightarrow q =$ &ldquo;If you have the flu, you miss the final
examination&rdquo;.

**(b)** $\lnot q \rightarrow r =$ &ldquo;If you don't have the flu, then
you pass the course&rdquo;.

**(c)** $q \rightarrow \lnot r =$ &ldquo;If you have the flu, then you
don't pass the course&rdquo;.

**(d)** $p \land q \land r =$ &ldquo;You have the flu, (or) you miss the
final examination, or you pass the course&rdquo;.

**(e)** $(p \rightarrow \lnot r) \lor (q \rightarrow \lnot r) =$ &ldquo;If
you have the flu, then you don't pass the course, or if you miss the final
examination, then you don't pass the course&rdquo;.

**(f)** $(p \land q) \lor (\lnot q \land r) =$ &ldquo;You have the flu and you
miss the final examination or you don't miss the final examination anr you pass
the course&rdquo;.

<span class = "exnum">15</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;You drive over $65$ mils per hour&rdquo;.
    <br>
    $\qquad q =$ &ldquo;You get a speeding ticket&rdquo;.
</div>

then

**(a)** $\lnot q$.
**(b)** $p \rightarrow \lnot q$.
**(c)** $q \rightarrow p$.
**(d)** $\lnot p \rightarrow \lnot q$.
**(e)** $p \rightarrow q$.
**(f)** $q \rightarrow \lnot p$.
**(g)** $q \leftrightarrow p$.

<span class = "exnum">16</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;You get an A on the final exam&rdquo;.
    <br>
    $\qquad q =$ &ldquo;You do every exercise in this bookticket&rdquo;.
    <br>
    $\qquad r =$ &ldquo;You get an A in this class&rdquo;.
</div>

then

**(a)** $p \rightarrow \lnot q$.
**(b)** $p \land q \land r$.
**(c)** $r \rightarrow p$.
**(d)** --
**(e)** $(p \land q) \rightarrow r$.
**(f)** $r \rightarrow (q \lor p)$.

<span class = "exnum">17</span> When the propositions of the declaration
are

<div align = "left">
    $\qquad p =$ &ldquo;Grizzly bears have been seen in the area&rdquo;.
    <br>
    $\qquad q =$ &ldquo;Hiking is safe on the trail&rdquo;.
    <br>
    $\qquad r =$ &ldquo;Berries are ripe along the trail&rdquo;.
</div>

then

**(a)** $r \land \lnot p$.
**(b)** $p \land q \land r$.
**(c)** $r \rightarrow (q \leftrightarrow p)$.
**(d)** $\lnot q \land \lnot p \land r$.
**(e)** $(\lnot q \land \lnor) \rightarrow q$.
**(f)** $(p \land r) \rightarrow \lnot q$.

<span class = "exnum">18</span>
The truth table for biconditional, given in the book, is

$$
    \begin{array}{ | c | c | c | } \hline
               p &        q & p \leftrightarrow q \\ \hline
        \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{F} \\
        \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{F} & \text{T} \\ \hline
    \end{array}
$$

**(a)** then &ldquo;$2 + 2 = 4$ if and only if $1 + 1 = 2$&rdquo; is true
($\text{T}$) because both mathematical expressions are true.

**(b)** then &ldquo;1 + 1 = 2 if and only if $2 + 3 = 4$&rdquo; is false
($\text{F}$) because $2 + 3 = 5$, not $4$, so the right hand-side of the
biconditional operator is $\text{F}$ making the whole proposition
$\text{F}$.

**(c)** then &ldquo;$1 + 1 = 3$ if and only if monkeys can fly&rdquo; is
$\text{F}$ because $1 + 1 \neq 3$, but $2$, so the left hand-side of the
biconditional is $\text{F}$ making the whole proposition $\text{F}$.

**(d)** then &ldquo;$0 > 1$ if and only if $2 > 1$&rdquo;, is $\text{T}$
because both sides of the biconditional are $\text{F}$.

<span class = "exnum">19</span> Truth table for the logical implication is

$$
    \begin{array}{ | c | c | c | } \hline
               p &        q & p \rightarrow q \\ \hline
        \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{F} \\
        \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{T} \\ \hline
    \end{array}
$$

so

**(a)** the statement &ldquo;If $1 + 1 = 2$&rdquo;, then $2 + 2 = 5$ is
$\text{F}$, because the $2 + 2 \neq 5$, but $4$, and $1 + 1 = 2$.

**(b)** from the statement &ldquo;If $1 + 1 = 3$&rdquo;, then $2 + 2 = 4$,
it can be seen that $1 + 1 \neq 3$, but $2$, so it's $\text{F}$. The right
hand-side is $\text{T}$. Because of these, the whole statement is $\text{T}$.

**(c)** the statement &ldquo;if $1 + 1 = 3$&rdquo;, then $2 + 2 = 5$, is
$\text{T}$, because both propositions are $\text{F}$.

**(d)** the statement &ldquo;if monkeys can fly, then $1 + 1 = 3$&rdquo; is
$\text{T}$, for the same reason as is **(c)**, that is, both propositions
in the statement are false, assuming that no flying monkeys exist.

<span class = "exnum">20</span> Based on the truth table of implication
given in <span class = "exnum">19</span>,

**(a)** &ldquo;If $1 + 1 = 3$, then unicorns exist&rdquo; is true ($\text{T}$),
because $1 + 1 \neq 3$, since $1 + 1 = 2$.

**(b)** &ldquo;If $1 + 1 = 2$, then $2 + 3 = 4$&rdquo; is false ($\text{F}$),
because it is true that $1 + 1 = 2$, but it's not true that $2 + 3 = 4$,
because $2 + 2 = 4$.

**(c)** &ldquo;If $ 1 + 1 = 2$, then dogs can fly&rdquo; is $\text{F}$,
because even if the first part of the implication is true, the second part
very likely isn't because no flying dogs shouldn't exits.

**(d)** &ldquo;If monkeys can fly, then $1 + 1 = 3$&rdquo;, is $\text{F}$
because $1 + 1 \neq 3$, $1 + 1 = 2$, and no flying monkeys should exist.

<span class = "exnum">21</span>

**(a)** The proposition most likely is the situation of exclusive or
($\text{XOR}$), even though in the proposition &ldquo;Coffee of tea comes
with dinner&rdquo; the part &ldquo;but not both&rdquo; is not implied. In
these kind of situations, it is common that $\text{XOR}$ is assumed.

**(b)** The proposition is a situation of inclusive or ($\text{OR}$),
because digits are characters, so one can choose a situation of both, that
is, one can have a password of eight characters that has three digits.

**(c)** The proposition is a situation of $\text{OR}$, because usually one
could have done a course in number theory or a course in cryptography, but
it is still a possibility that one could have done both courses too.

**(d)** The proposition is a situation of $\text{XOR}$, or should be,
because it's common that a payment for a good or a service is required only
once, so one shouldn't need to pay, say first in euros and then in dollars
or vice versa.

<span class = "exnum">22</span>

**(a)** The proposition seems to imply that either experience with C++ or
Java is needed, but not necessarily both, so the proposition has a
$\text{OR}$.

**(b)** Based on common experience, usually in these kind of situation, one
can pick one or the other, but not both, so the proposition is based on
$\text{XOR}$.

**(c)** One can have both of the document, i.e. either passport or voter
registration card, so $\text{OR}$.

**(d)** Most likely a $\text{XOR}$, because it shouldn't be possible to do
both, &ldquo;publish or perish&rdquo;.

<span class = "exnum">23</span>

**(a)** If the sentence means inclusive or $\text{OR}$ or exclusive or
($\tex{XOR}$), then in the first meaning the sentence means that one needs
needs to have calculus background or computer science course taken, but not
both. In the case of exclusive or ($\text{XORJ}$), one needs both to take
the discrete mathematics course.

**(b)** In the case of $\text{OR}$, it is possible to get both goods, i.e.
the returned money and the loan. In the case of $\text{XOR}$, one can have
on or the other, but not both, when buying a new car.

**(c)** In the case of $\text{OR}$, one can have either two, three or a
total five items. In the case of $\text{XOR}$, one can have either two or
three.

**(d)** Sentence means that if there are either two feet of snow, the wind
chill falls below $\sim 100 ^\circ \text{F}$, or both, the school is closed
($\text{OR}$). On the other hand, it could be that if there are two feet of
snow or the wind chill falls below $\sim 100 ^\circ \text{F}$, the school
is open, but if both happen at the same time, the school is closed
$\text{XOR}$.

<span class = "exnum">24</span>

**(a)** If one washed boss's car, then one gets promoted.

**(b)** If wind blows from the south, then a spring thaw.

**(c)** If you bought the computer less than a year ago, then the warranty
is good.

**(d)** If Willy cheats, then Willy gets caught.

**(e)** If you access the webpage, then you pay a subscription fee.

**(f)** If one knows the right people, then one gets elected.

**(g)** If Carol is on a boat, Caro gets sick.

<span class = "exnum">25</span>

**(a)** If the wind blows from the northeast, then it snows.

**(b)** If it stays warm for a week, then the apple trees will blossom.

**(c)** If the Pistons win the championship, then they beat the Lakers.

**(d)** If one wants to get to the top of Long's Peak, then one needs to
walk eight miles.

**(e)** If one wants to get tenure as a professor, then one needs to be
world famous.

**(f)** If you dirve more than $400$ miles, then you will need to buy
gasoline.

**(g)** If your guarantee is good, then you bought your CD player less than
90 days ago.

**(h)** If you begin your climb when it's not too late, then you will reach
the summit.

**(i)** If people believe in science, then we will have a future.
