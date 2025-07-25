+++
title  = "Problems 26-54"
date   = 2025-01-01T00:00:00+03:00
layout = "solution-single"
+++

<span class = "exnum">26</span>

**(a)** &ldquo;If I will remember to send you the address, then you send me
an e-mail message.&rdquo;

**(b)** &ldquo;If you were born in the United States, then one is a
citizen.&rdquo;

**(c)** &ldquo;If you keeo your textbook, then ti will be a useful
reference in your future courses.&rdquo;

**(d)** &ldquo;If the goalie plays well, then the Red Wings will win
Stanley Cup.&rdquo;

**(e)** &ldquo;If you get the job, then you had the credentials.&rdquo;

**(f)** &ldquo;If there is a storm, then the beach erodes.&rdquo;

**(g)** &ldquo;If one has a valid password, then it's possible to log on to
the server.&rdquo;

**(h)** &ldquo;If you begin your climb early, you will reach the summit&rdquo;.

**(i)** &ldquo;If you are among the first $100$ customers tomorrow, then
you will get a free ice cream cone&rdquo;.

<span class = "exnum">27</span>

**(a)** &ldquo;You buy an ice cream cone, if and only if it is hot
ouside.&rdquo;

**(b)** &ldquo;You win the contest if and only if you have the only winning
ticket.&rdquo;

**(c)** &ldquo;You get promoted if and only if you have connections&rdquo;.

**(d)** &ldquo;If you watch television if and only if your mind will decay.&rdquo;

**(e)** &ldquo;The trains run late if and only if I take it.&rdquo;

<span class = "exnum">28</span>

**(a)** &ldquo;You get an A in this course if and only if you learn how to
solve discrete mathematics problems.&rdquo;

**(b)** &ldquo;If you read the newspaper every day if and only if you will
be informed.&rdquo;

**(c)** &ldquo;It rains if and only if it is a weekend day&rdquo;.

**(d)** &ldquo;You can see the wizard if and only if the wizard is not in.&rdquo;

**(e)** &ldquo;My airplane flight is late if and only if I have to catch a
connecting flight&rdquo;.

<span class = "exnum">29</span>
Given a conditional statement of the form $p \rightarrow q$, the converse
of the proposition is $q \rightarrow p$, the contrapositive is $\lnot q
\rightarrow \lnot p$, and the inverse is $\lnot p \rightarrow \lnot q$.

**(a)** Then for the proposition $p \rightarrow q =$ &ldquo;If it snows
today, I will ski tomorrow&rdquo;, the converse is &ldquo;If I will ski
tomorrow, then it snows today&rdquo;, the contrapositive is &ldquo;If I
will not ski tomorrow, then it doesn't snow today&rdquo;, and the inverse
is &ldquo;If it doesn't snow today, I will not ski tomorrow.&rdquo;

**(b)** Then for the propoistion $p \rightarrow q =$ &ldquo;I come to class
whenever there is going to be a quiz&rdquo; $=$ &ldquo;If there is going to
be a quiz, then I come to class&rdquo;, then converse is &ldquo;If I come
to class, then there is going to be a quiz&rdquo;, the contrapositive is
&ldquo;If I don't come to class, then there is not going to be a
quiz&rdquo;, and the inverse is &ldquo;If there is not going to be a quiz,
then I will not come to class&rdquo;.

**(c)** Then for the proposition $p \rightarrow q =$ &ldquo;A positive
integer is a prime only if it has no divisors other than $1$ and
itself&rdquo; $=$ &ldquo;If a positive integer is a prime, then it has no
divisors other than $1$ and itself&rdquo;, the converse is &ldquo;If a
positive has no divisors other than $1$ and itself, then it is a
prime&rdquo;, the contrapositive is &ldquo;If a positive integer is not a
prime, then it has other divisors than $1$ and itself&rdquo;, and the
inverse is &ldquo;If a positive integer is not a prime, then it has other
divisors than $1$ and itself&rdquo;.

<span class = "exnum">30</span> Given the proposition

**(a)** &ldquo;If it shows tonight, I will stay home&rdquo; $=$ &ldquo;If it
snows tonight, then I will stay home&rdquo; and noting that the definitions
in <span class = "exnum">29</span>, the converse of the proposition is
&ldquo;If I will stay home, then it snows tonight&rdquo;, the
contrapositive is &ldquo;If I do not stay in home, then it does not snow
tonight&rdquo;, and the inverse is &ldquo;If it does not snow tonight, I
will not stay home&rdquo;.

**(b)** &ldquo;I go to the beach whenever it is a sunny summer day&rdquo;
$=$ &ldquo;If it is a sunny summer, then I go to the beach&rdquo;, the
converse of the proposition is &ldquo;If I go to the beach, then it is a
sunny summer&rdquo;, the contrapositive is &ldquo;If I do not go to the beach,
then it is not a sunny summer&rdquo;, and the inverse is &ldquo;If it is
not a sunny summer, then I won't go to the beach&rdquo;

**(c)** &ldquo;When I stay up late, it is necessary that I sleep until
noon&rdquo;, whhich is the same as saying &ldquo;If I sleep until noon,
then I stay up late&rdquo;, the converse of the proposition is &ldquo;If I
stay up late, then I sleep until noon&rdquo;, the contrapositive is
&ldquo;I won't stay up late, then I won't sleep until noon&rdquo;, and the
inverse is &ldquo;If I don't sleep until noon, then I won't stay up
late&rdquo;.

<span class = "exnum">31</span>
Since the number of rows in a truth table is equal to the number of unique
propositions squared, that is, the number of rows in a truth table is equal
to

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p_1, p_2, \ldots, p_n\})} = 2^n
    \tag{1}
$$

where $\operatorname{ToNum}$ (&ldquo;Total Number&rdquo;) is the function
mapping the number of unique propositions in a compound proposition in $P$
to some positive integer,

**(a)** and when the given proposition

$$
    P = p \rightarrow \lnot p
$$

the proposition has $2^{\operatorname{ToNum}(P)} = 2^1 = 2$ rows.

**(b)** and when the given proposition

$$
    P = (p \lor \lnot r) \land (q \lor \lnot s)
$$

the proposition has

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p,q,r,s\})} = 2^4 = 16
$$

rows.

**(c)** and when the given proposition

$$
    P = q \lor p \lor \lnot s \lor \lnot r \lor \lnot t \lor u
$$

the proposition has

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p,q,r,s,t,u\})} = 2^6 = 64
$$

rows.

**(d)** and when the given proposition

$$
    P = (p \land r \land t) \leftrightarrow (q \land t)
$$

the proposition has

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p,q,r,t\})} = 2^4 = 16
$$

rows.

<span class = "exnum">32</span> Using the counting mechanism defined in
$(1)$ of <span class = "exnum">31</span>,

**(a)** given the proposition

$$
    P = (q \rightarrow \lnot p) \lor (\lnot p \rightarrow \lnot q)
$$

the proposition has

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p,q\})} = 2^2 = 4
$$

rows.

**(b)** given the proposition

$$
    P = (p \land \lnot t) \land (p \lor \lnot s)
$$

the proposition has

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p,q,s,t\})} = 2^4 = 16
$$

rows.

**(c)** given the proposition

$$
    P = (p \rightarrow r) \lor (\lnot s \rightarrow \lnot t) \land (\lnot u \rightarrow v)
$$

the proposition has

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p,r,s,t,u,v\})} = 2^6 = 64
$$

rows.

**(d)** given the proposition

$$
    P = (p \land r \land s) \lor (q \land t) \lor (r \land \lnot t)
$$

the proposition has

$$
    2^{\operatorname{ToNum}(P)} = 2^{\operatorname{ToNum}(\{p,q,r,s,t\})} = 2^5 = 32
$$

rows.

<span class = "exnum">33</span>

**(a)** The truth table for proposition $p \land \lnot p$

<div class = "widescreen">
    <div align = "center">
        <table class = "fixedcol min">
            <tr>
                <th>$p$</th> <th>$\lnot p$</th> <th>$p \land \lnot p$</th>
            </tr>
            <tr>
                <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td>
            </tr>
            <tr>
                <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td>
            </tr>
        </table>
    </div>
</div>

<div class = "smallscreen">
    <div align = "center">
        <table class = "fixedcol max">
            <tr>
                <th>$p$</th> <th>$\lnot p$</th> <th>$p \land \lnot p$</th>
            </tr>
            <tr>
                <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td>
            </tr>
            <tr>
                <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td>
            </tr>
        </table>
    </div>
</div>

**(b)** The truth table for proposition $p \lor \lnot p$

<div class = "widescreen">
    <div align = "center">
        <table class = "fixedcol min">
            <tr>
                <th>$p$</th> <th>$\lnot p$</th> <th>$p \lor \lnot p$</th>
            </tr>
            <tr>
                <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td>
            </tr>
            <tr>
                <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td>
            </tr>
        </table>
    </div>
</div>

<div class = "smallscreen">
    <div align = "center">
        <table class = "fixedcol max">
            <tr>
                <th>$p$</th> <th>$\lnot p$</th> <th>$p \lor \lnot p$</th>
            </tr>
            <tr>
                <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td>
            </tr>
            <tr>
                <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td>
            </tr>
        </table>
    </div>
</div>

**(c)** The truth table for proposition $(p \lor q) \rightarrow q$

<div class = "widescreen">
    <div align = "center">
        <table class = "mid">
            <tr>
                <th>$p$</th>
                <th>$q$</th>
                <th>$\lnot q$</th>
                <th>$(p \lor \lnot q)$</th>
                <th>$(p \lor \lnot q) \rightarrow q$</th>
            </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> </tr>
        </table>
    </div>
</div>

<div class = "smallscreen">
    <div align = "center">
        <table class = "max">
            <tr>
                <th>$p$</th>
                <th>$q$</th>
                <th>$q$</th>
                <th>$(p \lor \lnot q)$</th>
            </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr>
                <th colspan = "4">$(p \lor \lnot q) \rightarrow q$</th>
            </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{F}$</td> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{F}$</td> </tr>
        </table>
    </div>
</div>

**(d)** The truth table for proposition $(p \lor q) \rightarrow (p \land q)$

<div class = "widescreen">
    <div align = "center">
        <table class = "mid">
            <tr>
                <th>$p$</th> <th>$q$</th> <th>$(p \lor q)$</th> <th>$(p \land q)$</th> <th>$(p \lor q) \rightarrow (p \land q)$</th>
            </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> </tr>
        </table>
    </div>
</div>

<div class = "smallscreen">
    <div align = "center">
        <table class = "fixedcol max">
            <tr>
                <th>$p$</th> <th>$q$</th> <th>$(p \lor q)$</th> <th>$(p \land q)$</th> 
            </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> </tr>
            <tr>
                <th colspan = "4">$(p \lor q) \rightarrow (p \land q)$</th>
            </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{F}$</td> </tr>
            <tr> <td colspan = "4">$\text{F}$</td> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
        </table>
    </div>
</div>

**(e)** The truth table for proposition $(p \rightarrow \lnot p)
\leftrightarrow (\lnot q \rightarrow \lnot p)$ is

<div class = "widescreen">
    <div align = "center">
        <table class = "mid">
            <tr>
                <th>$p$</th> <th>$q$</th> <th>$\lnot p$</th> <th>$\lnot q$</th> <th>$p \rightarrow q$</th> <th>$\lnot q \rightarrow \lnot p$</th>             </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr>
                <th colspan = "6">$(p \rightarrow \lnot p) \leftrightarrow (\lnot q \rightarrow \lnot p)$</th>
            </tr>
            <tr> <td colspan = "6">$\text{T}$</td> </tr>
            <tr> <td colspan = "6">$\text{T}$</td> </tr>
            <tr> <td colspan = "6">$\text{T}$</td> </tr>
            <tr> <td colspan = "6">$\text{T}$</td> </tr>
        </table>
    </div>
</div>

<div class = "smallscreen">
    <div align = "center">
        <table class = "max">
            <tr> <th>$p$</th> <th>$q$</th> <th>$\lnot p$</th> <th>$\lnot q$</th> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr>
            <th colspan = "2">$p \rightarrow q$</th> <th colspan = "2">$\lnot q \rightarrow \lnot p$</th>
            </tr>
            <tr> <td colspan = "2">$\text{T}$</td> <td colspan = "2">$\text{T}$</td> </tr>
            <tr> <td colspan = "2">$\text{F}$</td> <td colspan = "2">$\text{F}$</td> </tr>
            <tr> <td colspan = "2">$\text{T}$</td> <td colspan = "2">$\text{T}$</td> </tr>
            <tr> <td colspan = "2">$\text{T}$</td> <td colspan = "2">$\text{T}$</td> </tr>
            <tr>
                <th colspan = "4">$(p \rightarrow \lnot p) \leftrightarrow (\lnot q \rightarrow \lnot p)$</th>
            </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
        </table>
    </div>
</div>

**(f)** The truth table for proposition $(p \rightarrow q) \rightarrow (q \rightarrow p)$ is

<div class = "widescreen">
    <div align = "center">
        <table class = "mid">
            <tr> <th>$p$</th> <th>$q$</th> <th>$p \rightarrow q$</th> <th>$q \rightarrow p$</th> <th>$(p \rightarrow q) \rightarrow (q \rightarrow p)$</th> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
        </table>
    </div>
</div>

<div class = "smallscreen">
    <div align = "center">
        <table class = "max fixedcol">
            <tr> <th>$p$</th> <th>$q$</th> <th>$p \rightarrow q$</th> <th>$q \rightarrow p$</th>  </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{T}$</td> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> <td>$\text{F}$</td> </tr>
            <tr> <td>$\text{F}$</td> <td>$\text{F}$</td> <td>$\text{T}$</td> <td>$\text{T}$</td> </tr>
            <tr> <th colspan = "4">$(p \rightarrow q) \rightarrow (q \rightarrow p)$</th> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
            <tr> <td colspan = "4">$\text{F}$</td> </tr>
            <tr> <td colspan = "4">$\text{T}$</td> </tr>
        </table>
    </div>
</div>

<br>

<div align = "center" style = "margin: 16px 0 16px 0; border: 3px solid var(--accent);">
    <strong>DISCLAIMER</strong>: I'll switch to $\LaTeX$ table output here
    since writing the truth tables in HTML table-format, as is seen above, is
    too laborius.
</div>

<span class = "exnum">34</span>

**(a)**

$$
    \begin{array}{ | c | c | c | } \hline
       p        & \lnot p  & p \land \lnot p \\ \hline
       \text{T} & \text{F} & \text{F}        \\
       \text{F} & \text{T} & \text{F}        \\ \hline
    \end{array}
$$

**(b)**

$$
    \begin{array}{ | c | c | c | } \hline
       p        & \lnot p  & p \leftrightarrow \lnot p \\ \hline
       \text{T} & \text{F} & \text{F}                  \\
       \text{F} & \text{T} & \text{F}                  \\ \hline
    \end{array}
$$

**(c)**

$$
    \begin{array}{ | c | c | c | c | } \hline
        p        & q        & p \lor q & p \oplus (p \lor q) \\ \hline
        \text{T} & \text{T} & \text{T} & \text{F}            \\
        \text{T} & \text{F} & \text{F} & \text{F}            \\
        \text{F} & \text{T} & \text{F} & \text{T}            \\
        \text{F} & \text{F} & \text{F} & \text{F}            \\ \hline
    \end{array}
$$

**(d)**

$$
    \begin{array}{ | c | c | c | c | } \hline
        p        & q        & p \land q & p \lor q & (p \land q) \rightarrow (p \lor q) \\ \hline
        \text{T} & \text{T} & \text{T}  & \text{T} & \text{T}                           \\
        \text{T} & \text{F} & \text{T}  & \text{F} & \text{F}                           \\
        \text{F} & \text{T} & \text{T}  & \text{F} & \text{F}                           \\
        \text{F} & \text{F} & \text{F}  & \text{F} & \text{T}                           \\ \hline
    \end{array}
$$

**(e)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | } \hline
        p        & \lnot p  & q        & q \rightarrow \lnot p & p \leftrightarrow q & (q \rightarrow \lnot p) \oplus (p \leftrightarrow q) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{F}              & \text{T}            & \text{F}                         \\
        \text{T} & \text{F} & \text{F} & \text{T}              & \text{F}            & \text{T}                         \\
        \text{F} & \text{T} & \text{T} & \text{T}              & \text{F}            & \text{T}                         \\
        \text{F} & \text{T} & \text{F} & \text{T}              & \text{T}            & \text{T}                         \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | } \hline
        p        & \lnot p  & q        & q \rightarrow \lnot p & p \leftrightarrow q \\ \hline
        \text{T} & \text{F} & \text{T} & \text{F}              & \text{T}            \\
        \text{T} & \text{F} & \text{F} & \text{T}              & \text{F}            \\
        \text{F} & \text{T} & \text{T} & \text{T}              & \text{F}            \\
        \text{F} & \text{T} & \text{F} & \text{T}              & \text{T}            \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | } \hline
        (q \rightarrow \lnot p) \oplus (p \leftrightarrow q) \\ \hline
        \text{F}                                             \\
        \text{T}                                             \\
        \text{T}                                             \\
        \text{T}                                             \\ \hline
    \end{array}
$$
</div>

**(f)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
        p         & q        & \lnot q  & p \leftrightarrow q & p \leftrightarrow \lnot q & (p \leftrightarrow q) \oplus (p \leftrightarrow \lnot q) \\ \hline
        \text{T} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & \lnot q  & p \leftrightarrow q & p \leftrightarrow \lnot q \\ \hline
        \text{T} & \text{T} & \text{F} & \text{T}            & \text{F}                  \\
        \text{T} & \text{F} & \text{T} & \text{F}            & \text{T}                  \\
        \text{F} & \text{T} & \text{F} & \text{F}            & \text{T}                  \\
        \text{F} & \text{F} & \text{T} & \text{T}            & \text{F}                  \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \leftrightarrow q) \oplus (p \leftrightarrow \lnot q) \\ \hline
        \text{T}                                                 \\
        \text{T}                                                 \\
        \text{T}                                                 \\
        \text{T}                                                 \\ \hline
    \end{array}
$$
</div>

<span class = "exnum">35</span>

**(a)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & p \land q & p \oplus q & (p \land q) \rightarrow (p \oplus q) \\ \hline
        \text{T} & \text{T} & \text{T}  & \text{F}   & \text{F} \\
        \text{T} & \text{F} & \text{F}  & \text{T}   & \text{T} \\
        \text{F} & \text{T} & \text{F}  & \text{T}   & \text{T} \\
        \text{F} & \text{F} & \text{F}  & \text{F}   & \text{T} \\
    \end{array}
$$

**(b)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & p \land q & p \oplus q & (p \land q) \rightarrow (p \oplus q) \\ \hline
        \text{T} & \text{T} & \text{T}  & \text{F}   & \text{F} \\
        \text{T} & \text{F} & \text{F}  & \text{T}   & \text{T} \\
        \text{F} & \text{T} & \text{F}  & \text{T}   & \text{T} \\
        \text{F} & \text{F} & \text{F}  & \text{F}   & \text{T} \\
    \end{array}
$$

**(c)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & p \land q & p \lor q & (p \land q) \oplus (p \lor q) \\ \hline
        \text{T} & \text{T} & \text{T}  & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{F}  & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{F}  & \text{T} & \text{F} \\
        \text{F} & \text{F} & \text{F}  & \text{F} & \text{T} \\
    \end{array}
$$

**(d)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & \lnot p  & q        & p \leftrightarrow q & \lnot p \leftrightarrow q & (p \leftrightarrow q) \oplus (\lnot p \leftrightarrow q) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T}            & \text{F}                  & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{F}            & \text{T}                  & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{F}            & \text{T}                  & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{T}            & \text{F}                  & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & \lnot p  & q        & p \leftrightarrow q & \lnot p \leftrightarrow q \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T}            & \text{F}                  \\
        \text{T} & \text{F} & \text{F} & \text{F}            & \text{T}                  \\
        \text{F} & \text{T} & \text{T} & \text{F}            & \text{T}                  \\
        \text{F} & \text{T} & \text{F} & \text{T}            & \text{F}                  \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \leftrightarrow q) \oplus (\lnot p \leftrightarrow q) \\ \hline
        \text{T}                                                 \\
        \text{T}                                                 \\
        \text{T}                                                 \\
        \text{T}                                                 \\ \hline
    \end{array}
$$
</div>

**(e)**

<div class = "widescreen">
ss
$$
    \begin{array}{ | c | c | c | c | c | c | c | c | } \hline
        p & \lnot p & q & r & \lnot r & p \leftrightarrow q & \lnot p \leftrightarrow \lnot r & (p \leftrightarrow q) \oplus (\lnot p \leftrightarrow \lnot r) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{F} & \text{F} & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c |} \hline
        p        & \lnot p  & q        & r        & \lnot r  & p \leftrightarrow q & \lnot p \leftrightarrow \lnot r \\ \hline
        \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T}            & \text{F}                        \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T}            & \text{T}                        \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F}            & \text{F}                        \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{F}            & \text{T}                        \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{T} & \text{F}            & \text{T}                        \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{F}            & \text{F}                        \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T}            & \text{T}                        \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T}            & \text{F}                        \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \leftrightarrow q) \oplus (\lnot p \leftrightarrow \lnot r) \\ \hline
        \text{T}                                                       \\
        \text{F}                                                       \\
        \text{F}                                                       \\
        \text{T}                                                       \\
        \text{T}                                                       \\
        \text{F}                                                       \\
        \text{F}                                                       \\
        \text{T}                                                       \\ \hline
    \end{array}
$$
</div>

**(f)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & \lnot q  & p \oplus q & p \oplus \lnot q & (p \oplus q) \rightarrow (p \oplus \lnot q) \\ \hline
        \text{T} & \text{T} & \text{F} & \text{F}   & \text{T}         & \text{T}                                    \\
        \text{T} & \text{F} & \text{T} & \text{T}   & \text{F}         & \text{F}                                    \\
        \text{F} & \text{T} & \text{F} & \text{T}   & \text{F}         & \text{F}                                    \\
        \text{F} & \text{F} & \text{T} & \text{F}   & \text{T}         & \text{T}                                    \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & \lnot q  & p \oplus q & p \oplus \lnot q \\ \hline
        \text{T} & \text{T} & \text{F} & \text{F}   & \text{T}         \\
        \text{T} & \text{F} & \text{T} & \text{T}   & \text{F}         \\
        \text{F} & \text{T} & \text{F} & \text{T}   & \text{F}         \\
        \text{F} & \text{F} & \text{T} & \text{F}   & \text{T}         \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        (p \oplus q) \rightarrow (p \oplus \lnot q) \\ \hline
        \text{T}                                    \\
        \text{F}                                    \\
        \text{F}                                    \\
        \text{T}                                    \\ \hline
    \end{array}
$$
</div>

<span class = "exnum">36</span>

**(a)**

$$
    \begin{array}{ | c | c | }    \hline
        p        & p \oplus p  \\ \hline
        \text{T} & \text{F}    \\
        \text{F} & \text{F}    \\ \hline
    \end{array}
$$

**(b)**

$$
    \begin{array}{ | c | c | c | } \hline
        p        & \lnot p  & p \oplus p  \\ \hline
        \text{T} & \text{F} & \text{T}    \\
        \text{F} & \text{T} & \text{T}    \\ \hline
    \end{array}
$$

**(c)**

$$
    \begin{array}{ | c | c | c | c | } \hline
            p        & q        & \lnot q  & p \oplus \lnot q \\ \hline
            \text{T} & \text{T} & \text{F} & \text{T} \\
            \text{T} & \text{F} & \text{T} & \text{F} \\
            \text{F} & \text{T} & \text{F} & \text{F} \\
            \text{F} & \text{F} & \text{T} & \text{T} \\ \hline
    \end{array}
$$

**(d)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
       p        & \lnot p  & q        & \lnot q  & \lnot p \oplus \lnot q \\ \hline
       \text{T} & \text{F} & \text{T} & \text{F} & \text{T} \\
       \text{T} & \text{F} & \text{F} & \text{T} & \text{F} \\
       \text{F} & \text{T} & \text{T} & \text{F} & \text{F} \\
       \text{F} & \text{T} & \text{F} & \text{T} & \text{T} \\ \hline
    \end{array}
$$

**(e)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
       p        & q        & \lnot q  & p \oplus q & p \oplus \lnot q & (p \oplus q) \lor (p \oplus \lnot q) \\ \hline
       \text{T} & \text{T} & \text{F} & \text{T}   & \text{F}         & \text{T}                             \\
       \text{T} & \text{F} & \text{T} & \text{F}   & \text{T}         & \text{T}                             \\
       \text{F} & \text{T} & \text{F} & \text{F}   & \text{T}         & \text{T}                             \\
       \text{F} & \text{F} & \text{T} & \text{T}   & \text{F}         & \text{T}                             \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
       p        & q        & \lnot q  & p \oplus q & p \oplus \lnot q \\ \hline
       \text{T} & \text{T} & \text{F} & \text{T}   & \text{F}         \\
       \text{T} & \text{F} & \text{T} & \text{F}   & \text{T}         \\
       \text{F} & \text{T} & \text{F} & \text{F}   & \text{T}         \\
       \text{F} & \text{F} & \text{T} & \text{T}   & \text{F}         \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \oplus q) \lor (p \oplus \lnot q) \\ \hline
        \text{T}                             \\
        \text{T}                             \\
        \text{T}                             \\
        \text{T}                             \\ \hline
    \end{array}
$$
</div>

**(f)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
       p        & q        & \lnot q  & p \oplus q & p \oplus \lnot q & (p \oplus q) \land (p \oplus \lnot q) \\ \hline
       \text{T} & \text{T} & \text{F} & \text{T}   & \text{F}         & \text{F}                              \\
       \text{T} & \text{F} & \text{T} & \text{F}   & \text{T}         & \text{F}                              \\
       \text{F} & \text{T} & \text{F} & \text{F}   & \text{T}         & \text{F}                              \\
       \text{F} & \text{F} & \text{T} & \text{T}   & \text{F}         & \text{F}                              \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
       p        & q        & \lnot q  & p \oplus q & p \oplus \lnot q \\ \hline
       \text{T} & \text{T} & \text{F} & \text{T}   & \text{F}         \\
       \text{T} & \text{F} & \text{T} & \text{F}   & \text{T}         \\
       \text{F} & \text{T} & \text{F} & \text{F}   & \text{T}         \\
       \text{F} & \text{F} & \text{T} & \text{T}   & \text{F}         \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \oplus q) \lor (p \oplus \lnot q) \\ \hline
        \text{F}                             \\
        \text{F}                             \\
        \text{F}                             \\
        \text{F}                             \\ \hline
    \end{array}
$$
</div>

<span class = "exnum">37</span>

**(a)**

$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
        p        & q        & \lnot q  & p \rightarrow \lnot q \\ \hline
        \text{T} & \text{T} & \text{F} & \text{F}              \\
        \text{T} & \text{F} & \text{T} & \text{F}              \\
        \text{F} & \text{T} & \text{F} & \text{T}              \\
        \text{F} & \text{F} & \text{T} & \text{T}              \\ hline
    \end{array}
$$

**(b)**

$$
    \begin{array}{ | c | c | c | c | } \hline
        p        & \lnot p  & q        & \lnot p \leftrightarrow q \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T}                  \\
        \text{T} & \text{F} & \text{F} & \text{T}                  \\
        \text{F} & \text{T} & \text{T} & \text{T}                  \\
        \text{F} & \text{T} & \text{F} & \text{F}                  \\ hline
    \end{array}
$$

**(c)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
        p        & \lnot p  & q        & p \rightarrow q & \lnot p \rightarrow q & (p \rightarrow q) \lor (\lnot p \rightarrow q) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T}                                                           \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{T} & \text{T}                                                           \\
        \text{F} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T}                                                           \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T}                                                           \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & \lnot p  & q        & p \rightarrow q & \lnot p \rightarrow q \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              \\
        \text{T} & \text{F} & \text{F} & \text{F}        & \text{T}              \\
        \text{F} & \text{T} & \text{T} & \text{T}        & \text{T}              \\
        \text{F} & \text{T} & \text{F} & \text{T}        & \text{F}              \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \rightarrow q) \lor (\lnot p \rightarrow q) \\ \hline
        \text{T}                                       \\
        \text{T}                                       \\
        \text{T}                                       \\
        \text{T}                                       \\ \hline
    \end{array}
$$
</div>

**(d)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
        p & \lnot p  & q & p \rightarrow q & \lnot p \rightarrow q & (p \rightarrow q) \land (\lnot p \rightarrow q) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T}                                              \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{T} & \text{F}                                              \\
        \text{F} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T}                                              \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{F}                                              \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & \lnot p  & q        & p \rightarrow q & \lnot p \rightarrow q \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T}        & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{F}        & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{T}        & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{T}        & \text{F} \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \rightarrow q) \lor (\lnot p \rightarrow q) \\ \hline
        \text{T}                                       \\
        \text{F}                                       \\
        \text{T}                                       \\
        \text{F}                                       \\ \hline
    \end{array}
$$
</div>

**(e)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
        p & \lnot p  & q & p \leftrightarrow q & \lnot p \leftrightarrow q & (p \leftrightarrow q) \lor (\lnot p \leftrightarrow q) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T}                                                             \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{F} & \text{F}                                                             \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{F}                                                             \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T}                                                             \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & \lnot p  & q        & p \rightarrow q & \lnot p \rightarrow q \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              \\
        \text{T} & \text{F} & \text{F} & \text{F}        & \text{T}              \\
        \text{F} & \text{T} & \text{T} & \text{T}        & \text{T}              \\
        \text{F} & \text{T} & \text{F} & \text{T}        & \text{F}              \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \rightarrow q) \lor (\lnot p \rightarrow q) \\ \hline
        \text{T}                                       \\
        \text{F}                                       \\
        \text{F}                                       \\
        \text{T}                                       \\ \hline
    \end{array}
$$
</div>

<span class = "exnum">38</span>

**(a)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & r        & p \lor q  & (p \lor q) \lor r  \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T}  & \text{T}           \\
        \text{T} & \text{T} & \text{F} & \text{T}  & \text{T}           \\
        \text{T} & \text{F} & \text{T} & \text{T}  & \text{T}           \\
        \text{T} & \text{F} & \text{F} & \text{T}  & \text{T}           \\
        \text{F} & \text{T} & \text{T} & \text{T}  & \text{T}           \\
        \text{F} & \text{T} & \text{F} & \text{T}  & \text{T}           \\
        \text{F} & \text{F} & \text{T} & \text{F}  & \text{T}           \\
        \text{F} & \text{F} & \text{F} & \text{F}  & \text{F}           \\ \hline
    \end{array}
$$

**(b)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & r        & p \lor q  & (p \lor q) \land r  \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{T} & \text{F} & \text{T}  & \text{F}            \\
        \text{T} & \text{F} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{F} & \text{F} & \text{T}  & \text{F}            \\
        \text{F} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{F} & \text{T} & \text{F} & \text{T}  & \text{F}            \\
        \text{F} & \text{F} & \text{T} & \text{F}  & \text{F}            \\
        \text{F} & \text{F} & \text{F} & \text{F}  & \text{F}            \\ \hline
    \end{array}
$$

**(c)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & r        & p \land q & (p \land q) \lor r  \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{T} & \text{F} & \text{T}  & \text{T}            \\
        \text{T} & \text{F} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{F} & \text{F} & \text{T}  & \text{T}            \\
        \text{F} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{F} & \text{T} & \text{F} & \text{T}  & \text{T}            \\
        \text{F} & \text{F} & \text{T} & \text{F}  & \text{T}            \\
        \text{F} & \text{F} & \text{F} & \text{F}  & \text{F}            \\ \hline
    \end{array}
$$

**(d)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & r        & p \land q & (p \land q) \land r \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{T} & \text{F} & \text{T}  & \text{F}            \\
        \text{T} & \text{F} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{F} & \text{F} & \text{T}  & \text{F}            \\
        \text{F} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{F} & \text{T} & \text{F} & \text{T}  & \text{F}            \\
        \text{F} & \text{F} & \text{T} & \text{F}  & \text{F}            \\
        \text{F} & \text{F} & \text{F} & \text{F}  & \text{F}            \\ \hline
    \end{array}
$$

**(e)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & \lnot r  & p \lor q  & (p \lor q) \land \lnot r \\ \hline
        \text{T} & \text{T} & \text{F} & \text{T}  & \text{F}            \\
        \text{T} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{F} & \text{F} & \text{T}  & \text{F}            \\
        \text{T} & \text{F} & \text{T} & \text{T}  & \text{T}            \\
        \text{F} & \text{T} & \text{F} & \text{T}  & \text{F}            \\
        \text{F} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{F} & \text{F} & \text{F} & \text{F}  & \text{T}            \\
        \text{F} & \text{F} & \text{T} & \text{F}  & \text{F}            \\ \hline
    \end{array}
$$

**(f)**

$$
    \begin{array}{ | c | c | c | c | c | } \hline
        p        & q        & \lnot r  & p \land q & (p \land q) \lor \lnot r \\ \hline
        \text{T} & \text{T} & \text{F} & \text{T}  & \text{T}            \\
        \text{T} & \text{T} & \text{T} & \text{T}  & \text{T}            \\
        \text{T} & \text{F} & \text{F} & \text{F}  & \text{F}            \\
        \text{T} & \text{F} & \text{T} & \text{F}  & \text{T}            \\
        \text{F} & \text{T} & \text{F} & \text{F}  & \text{F}            \\
        \text{F} & \text{T} & \text{T} & \text{F}  & \text{T}            \\
        \text{F} & \text{F} & \text{F} & \text{F}  & \text{F}            \\
        \text{F} & \text{F} & \text{T} & \text{F}  & \text{T}            \\ \hline
    \end{array}
$$

<span class = "exnum">39</span>

**(a)**

$$
    \begin{array}{ | c | c | c | c | c |  } \hline
        p        & \lnot q  & r        & \lnot q \lor r & p \rightarrow (\lnot q \lor r) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{F} \\
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{F} & \text{F} & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} \\ \hline
    \end{array}
$$

**(b)**

$$
    \begin{array}{ | c | c | c | c | c |  } \hline
         \lnot p & q        & r        & q \rightarrow r & \lnot p \rightarrow (q \rightarrow r) \\ \hline
        \text{F} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{F} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{F} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{F} & \text{F} & \text{F} \\
        \text{T} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{T} \\ \hline
    \end{array}
$$

**(c)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
       p        & \lnot p  & q        & r        & p \rightarrow q & \lnot p \rightarrow r & (p \rightarrow q) \lor (\lnot p \rightarrow r) \\ \hline
       \text{T} & \text{F} & \text{T} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{T} & \text{F} & \text{T} & \text{F} & \text{T}        & \text{T}              & \text{T} \\
       \text{T} & \text{F} & \text{F} & \text{T} & \text{F}        & \text{T}              & \text{T} \\
       \text{T} & \text{F} & \text{F} & \text{F} & \text{F}        & \text{T}              & \text{T} \\
       \text{F} & \text{T} & \text{T} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{F} & \text{T} & \text{T} & \text{F} & \text{T}        & \text{F}              & \text{T} \\
       \text{F} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{F} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{F}              & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
       p        & \lnot p  & q        & r        & p \rightarrow q & \lnot p \rightarrow r \\ \hline
       \text{T} & \text{F} & \text{T} & \text{T} & \text{T}        & \text{T}              \\
       \text{T} & \text{F} & \text{T} & \text{F} & \text{T}        & \text{T}              \\
       \text{T} & \text{F} & \text{F} & \text{T} & \text{F}        & \text{T}              \\
       \text{T} & \text{F} & \text{F} & \text{F} & \text{F}        & \text{T}              \\
       \text{F} & \text{T} & \text{T} & \text{T} & \text{T}        & \text{T}              \\
       \text{F} & \text{T} & \text{T} & \text{F} & \text{T}        & \text{F}              \\
       \text{F} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              \\
       \text{F} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{F}              \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
       (p \rightarrow q) \lor (\lnot p \rightarrow r) \\ \hline
       \text{T} \\
       \text{T} \\
       \text{T} \\
       \text{T} \\
       \text{T} \\
       \text{T} \\
       \text{T} \\
       \text{T} \\ \hline
    \end{array}
$$
</div>

**(d)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
       p        & \lnot p  & q        & r        & p \rightarrow q & \lnot p \rightarrow r & (p \rightarrow q) \land (\lnot p \rightarrow r) \\ \hline
       \text{T} & \text{F} & \text{T} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{T} & \text{F} & \text{T} & \text{F} & \text{T}        & \text{T}              & \text{T} \\
       \text{T} & \text{F} & \text{F} & \text{T} & \text{F}        & \text{T}              & \text{F} \\
       \text{T} & \text{F} & \text{F} & \text{F} & \text{F}        & \text{T}              & \text{F} \\
       \text{F} & \text{T} & \text{T} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{F} & \text{T} & \text{T} & \text{F} & \text{T}        & \text{F}              & \text{F} \\
       \text{F} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{F} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{F}              & \text{F} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
       p        & \lnot p  & q        & r        & p \rightarrow q & \lnot p \rightarrow r \\ \hline
       \text{T} & \text{F} & \text{T} & \text{T} & \text{T}        & \text{T}              \\
       \text{T} & \text{F} & \text{T} & \text{F} & \text{T}        & \text{T}              \\
       \text{T} & \text{F} & \text{F} & \text{T} & \text{F}        & \text{T}              \\
       \text{T} & \text{F} & \text{F} & \text{F} & \text{F}        & \text{T}              \\
       \text{F} & \text{T} & \text{T} & \text{T} & \text{T}        & \text{T}              \\
       \text{F} & \text{T} & \text{T} & \text{F} & \text{T}        & \text{F}              \\
       \text{F} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              \\
       \text{F} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{F}              \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
       (p \rightarrow q) \lor (\lnot p \rightarrow r) \\ \hline
       \text{T} \\
       \text{T} \\
       \text{F} \\
       \text{F} \\
       \text{T} \\
       \text{F} \\
       \text{T} \\
       \text{F} \\ \hline
    \end{array}
$$
</div>

**(e)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
       p        & q        & \lnot q  & r        & p \leftrightarrow q & \lnot q \leftrightarrow r & (p \leftrightarrow q) \lor(\lnot p \leftrightarrow r) \\ \hline
       \text{T} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{T} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{T}              & \text{T} \\
       \text{T} & \text{F} & \text{T} & \text{T} & \text{F}        & \text{T}              & \text{T} \\
       \text{T} & \text{F} & \text{T} & \text{F} & \text{F}        & \text{F}              & \text{F} \\
       \text{F} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{F} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{T}              & \text{T} \\
       \text{F} & \text{F} & \text{T} & \text{T} & \text{T}        & \text{T}              & \text{T} \\
       \text{F} & \text{F} & \text{T} & \text{F} & \text{T}        & \text{F}              & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
       p        & q        & \lnot q  & r        & p \leftrightarrow q & \lnot q \leftrightarrow r \\ \hline
       \text{T} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T} \\
       \text{T} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{T} \\
       \text{T} & \text{F} & \text{T} & \text{T} & \text{F}        & \text{T} \\
       \text{T} & \text{F} & \text{T} & \text{F} & \text{F}        & \text{F} \\
       \text{F} & \text{T} & \text{F} & \text{T} & \text{T}        & \text{T} \\
       \text{F} & \text{T} & \text{F} & \text{F} & \text{T}        & \text{T} \\
       \text{F} & \text{F} & \text{T} & \text{T} & \text{T}        & \text{T} \\
       \text{F} & \text{F} & \text{T} & \text{F} & \text{T}        & \text{F} \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
       (p \leftrightarrow q) \lor(\lnot p \leftrightarrow r) \\ \hline
       \text{T} \\
       \text{T} \\
       \text{T} \\
       \text{F} \\
       \text{T} \\
       \text{T} \\
       \text{T} \\
       \text{T} \\ \hline
    \end{array}
$$
</div>

**(f)**

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | c | } \hline
        p & \lnot p & q & \lnot q & r & \lnot p \leftrightarrow \lnot q & q \leftrightarrow r & (\lnot p \leftrightarrow \lnot q) \leftrightarrow (q \leftrightarrow r) \\ \hline
        \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{F} & \text{F} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} & \text{F} & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
        p & \lnot p & q & \lnot q & r & \lnot p \leftrightarrow \lnot q & q \leftrightarrow r \\ \hline
        \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F} & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{F} & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | c | c | c | c | c | c | c | } \hline
        (\lnot p \leftrightarrow \lnot q) \leftrightarrow (q \leftrightarrow r) \\ \hline
        \text{T} \\
        \text{F} \\
        \text{T} \\
        \text{F} \\
        \text{F} \\
        \text{T} \\
        \text{F} \\
        \text{T} \\ \hline
    \end{array}
$$
</div>

<span class = "exnum">40</span>

<div class = "widescreen">
$$
    \begin{array}{ | c | c | c | c | c | c | c | } \hline
        p & q & r & s & p \rightarrow q & (p \rightarrow q ) \rightarrow  r & ((p \rightarrow q ) \rightarrow  r ) \rightarrow s \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} \\
        \text{T} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} & \text{F} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{T} & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} \\
        \text{F} & \text{F} & \text{F} & \text{F} & \text{T} & \text{F} & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | c | c | c | c | c | } \hline
        p & q & r & s & p \rightarrow q & (p \rightarrow q ) \rightarrow  r \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{T} & \text{F} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{F} & \text{T} & \text{T} & \text{F} \\
        \text{T} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{T} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{F} & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{F} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F} \\
        \text{F} & \text{F} & \text{F} & \text{F} & \text{T} & \text{F} \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        ((p \rightarrow q ) \rightarrow  r ) \rightarrow s \\ \hline
        \text{T} \\
        \text{T} \\
        \text{T} \\
        \text{T} \\
        \text{F} \\
        \text{F} \\
        \text{F} \\
        \text{F} \\
        \text{T} \\
        \text{T} \\
        \text{T} \\
        \text{T} \\
        \text{T} \\
        \text{T} \\
        \text{T} \\
        \text{T} \\ \hline
    \end{array}
$$
</div>

<span class = "exnum">41</span>

<div class = "widescreen">
$$
    \begin{array}{ | c | } \hline
        p & q & r & s & (p \leftrightarrow q) & (r \leftrightarrow s) & (p \leftrightarrow q) \leftrightarrow (r \leftrightarrow s) \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{T} & \text{T} & \text{F} & \text{T} & \text{F} & \text{F} \\
        \text{T} & \text{T} & \text{F} & \text{T} & \text{T} & \text{F} & \text{F} \\
        \text{T} & \text{T} & \text{F} & \text{F} & \text{T} & \text{T} & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{T} & \text{F} & \text{T} & \text{F} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{T} & \text{T} & \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F} & \text{F} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{F} & \text{T} \\
        \text{F} & \text{T} & \text{F} & \text{F} & \text{F} & \text{T} & \text{F} \\
        \text{F} & \text{F} & \text{T} & \text{T} & \text{T} & \text{T} & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{F} & \text{T} & \text{F} & \text{F} \\
        \text{F} & \text{F} & \text{F} & \text{T} & \text{T} & \text{F} & \text{F} \\
        \text{F} & \text{F} & \text{F} & \text{F} & \text{T} & \text{T} & \text{T} \\ \hline
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ | c | } \hline
        p        & q        & r        & s        & (p \leftrightarrow q) & (r \leftrightarrow s)   \\ \hline
        \text{T} & \text{T} & \text{T} & \text{T} & \text{T}              & \text{T} \\
        \text{T} & \text{T} & \text{T} & \text{F} & \text{T}              & \text{F} \\
        \text{T} & \text{T} & \text{F} & \text{T} & \text{T}              & \text{F} \\
        \text{T} & \text{T} & \text{F} & \text{F} & \text{T}              & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{T} & \text{F}              & \text{T} \\
        \text{T} & \text{F} & \text{T} & \text{F} & \text{F}              & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{T} & \text{F}              & \text{F} \\
        \text{T} & \text{F} & \text{F} & \text{F} & \text{F}              & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{T} & \text{F}              & \text{T} \\
        \text{F} & \text{T} & \text{T} & \text{F} & \text{F}              & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{T} & \text{F}              & \text{F} \\
        \text{F} & \text{T} & \text{F} & \text{F} & \text{F}              & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{T} & \text{T}              & \text{T} \\
        \text{F} & \text{F} & \text{T} & \text{F} & \text{T}              & \text{F} \\
        \text{F} & \text{F} & \text{F} & \text{T} & \text{T}              & \text{F} \\
        \text{F} & \text{F} & \text{F} & \text{F} & \text{T}              & \text{T} \\ \hline
    \end{array}
$$
$$
    \begin{array}{ | c | } \hline
        (p \leftrightarrow q) \leftrightarrow (r \leftrightarrow s) \\ \hline
        \text{T} \\
        \text{F} \\
        \text{F} \\
        \text{T} \\
        \text{F} \\
        \text{T} \\
        \text{T} \\
        \text{F} \\
        \text{F} \\
        \text{T} \\
        \text{T} \\
        \text{F} \\
        \text{T} \\
        \text{F} \\
        \text{F} \\
        \text{T} \\ \hline
    \end{array}
$$
</div>

<span class = "exnum">42</span>

When either of the two propositions on the either side of the logical or
($\lor$) is true ($\text{T}$), the whole expression is always $\text{T}$.
Then in the given expression, $(q \lor \lnot r)$ $\land$ $(r \land \lnot p)$
$\land$ $(r \land \lnot p)$, the compound propositions will always be true.
That is if $p$, $q$, and $r$ are all $\text{T}$, then the given proposition
is equal to $\text{T}$ $\land$ $\text{T}$ $\land$ $\text{T}$, from where it
can be seen that the given proposition is always true.

<span class = "exnum">43</span> If either one of the propositions $p$, $q$,
or $r$ is $\text{T}$ and one if $\text{F}$, in $(p$ $\lor$ $q$ $\lor$ $r)$
$\land$ $(\lnot p$ $\lor$ $\lnot$ $q$ $\lor$ $r)$, then the left hand-side
(LHS) of the logical and ($\land$) will always be $T$, no matter what the
truth value of the third proposition is.

And on the other hand, reverse is true for the right hand-side (RHS) of the
$\land$ connecting the LHS and RHS. That is, the RHS will always be
$\text{T}$, one of the propositions, that is, the one being $\text{F}$ will
always be $\text{T}$, because of the logical not ($\lnot$).

This means that whenever one of the propositions $p$, $q$, or $r$ is
$\text{T}$ and one is $\text{F}$, the LHS and RHS of the given proposition
will always be $\T$ and the whole proposition will always be equal to
$\text{T}$ $\land$ $\text{T}$. Because of this, the whole expression is
then always $\text{T}$.

If $p$, $q$, and $r$ are all $\text{T}$ or $\text{F}$ at the same time,
then LHS will be either $\text{T}$ or $\text{F}$ and the RHS the opposite
of that, that is, either $\text{F}$ or $\text{T}$. Therefore the given
experssion will always be either $\text{T}$ $\land$ $\text{F}$ or vice
versa, so the expression will always be $\text{F}$.

<span class = "exnum">44</span>

...

<span class = "exnum">45</span>

...

<span class = "exnum">46</span>

Given that $x = 1$ and assuming that the programming language is
[short-circuiting][1] w.r.t. it's boolean logic, the value of $x$ after the
expression

[1]:https://en.wikipedia.org/wiki/Short-circuit_evaluation

**(a)** $\text{\textbf{if}}$ $x + 2 = 3$ $\text{\textbf{then}}$ $x := x +
1$ means that $x = 2$, because $x + 2$ $=$ $1 + 2$ $=$ $3$ so the
$\text{\textbf{then}}$ is run, and so $x$ gets incremented by $1$, i.e. $x$
becomes $2$.

**(b)** $\text{\textbf{if}}$ $x + 2 = 3$ $\text{\textbf{then}}$ $x := x +
1$ means that $x = 2$, because the left hand-side (LHS) of the
$\\operatorname{OR}$ becomes true ($\text{T}$), so no matter what the right
hand-side (RHS) is, the $\text{\textbf{then}}$ will be run, and so $x$ gets
incremented by $1$, i.e. $x$ becomes $2$.

**(c)** will be $1$ because the LHS will evaluate to false $(\text{F})$,
and in order for the $\operatorname{AND}$ operator to be $\text{T}$, both
LHS and RHS needs to be $\text{T}$. This means that the
$\text{\textbf{then}}$-part will not be evaluated and $x$ won't get
icremented by the $x :=  x + 1$ instruction.

**(d)** $\text{\textbf{if}}$ $(x + 1 = 2)$ $\operatorname{XOR}$ $(x + 2 =
3)$ will evaluate to $\text{T}$ since $x + 1$ $=$ $1 + 1 = 2$ and $x + 2$
$=$ $1 + 3 = 3$, i.e. both propositions of the
$\operatorname{XOR}$-operator will evaluate to $\text{T}$ and the whole
expression becomes $T$, the $\text{\textbf{then}}$ block will be ran and
$x$ gets incremented by one, and will be $x = 2$.

**(e)** $\text{\textbf{if}}$ $<$ $2$ will evaluate to $T$, since $x = 1 <
2$ is true, and so the $x$ gets incremented by $1$ becoming $2$ after this
$\text{\textbf{if}}$-$\text{\textbf{then}}$ instruction is executed.

<span class = "exnum">47</span>

**(a)**

$$
    \begin{array}{ r c c }
                           & 101 & 1110 \\
                           & 010 & 0001 \\ \hline
        \operatorname{OR}  & 111 & 1111 \\
        \operatorname{AND} & 000 & 0000 \\
        \operatorname{XOR} & 111 & 1111 \\
    \end{array}
$$

**(b)**

$$
    \begin{array}{ r c c }
                           & 1111 & 0000 \\
                           & 1010 & 1010 \\ \hline
        \operatorname{OR}  & 1111 & 1010 \\
        \operatorname{AND} & 1010 & 0000 \\
        \operatorname{XOR} & 0101 & 1010 \\
    \end{array}
$$

**(c)**

$$
    \begin{array}{ r c c c }
                           & 00 & 0111 & 0001 \\
                           & 10 & 0100 & 1000 \\ \hline
        \operatorname{OR}  & 10 & 0111 & 1001 \\
        \operatorname{AND} & 00 & 0100 & 0000 \\
        \operatorname{XOR} & 10 & 0011 & 1001 \\
    \end{array}
$$

**(d)**

$$
    \begin{array}{ r c c c }
                           & 11 & 1111 & 1111 \\
                           & 00 & 0000 & 0000 \\ \hline
        \operatorname{OR}  & 11 & 1111 & 1111 \\
        \operatorname{AND} & 00 & 0000 & 0000 \\
        \operatorname{XOR} & 11 & 1111 & 1111 \\
    \end{array}
$$

<span class = "exnum">48</span>

**(a)**

$$
    \begin{array}{ c c c } \\
              & 0 & 1011 \\
        \lor  & 1 & 1011 \\ \hline
              & 1 & 1011 \\
       \land  & 1 & 1000 \\ \hline
              & 1 & 1000
    \end{array}
$$

**(b)**

$$
    \begin{array}{ c c c } \\
              & 0 & 1111 \\
       \land  & 1 & 0101 \\ \hline
              & 0 & 0101 \\
        \lor  & 0 & 1000 \\ \hline
              & 0 & 1101
    \end{array}
$$

**(c)**

$$
    \begin{array}{ c c c } \\
              & 0 & 1010 \\
       \oplus & 1 & 1011 \\ \hline
              & 1 & 0001 \\
       \oplus & 0 & 1000 \\ \hline
              & 1 & 1001
    \end{array}
$$

**(d)**

$$
    \begin{array}{ c c c } \\
              & 1 & 1011 &          &   &      & 1          & 0001           \\
         \lor & 0 & 1010 &          &   &      & 1          & 1011           \\ \hline
              & 1 & 1011 &          &   &      & 1          & 1011           \\
              &   &      & \searrow &   &      &            & \ \downarrow   \\
              &   &      &          & 1 & 1011 &            & \swarrow \quad \\
        \land &   &      &          & 1 & 1011 & \leftarrow &                \\ \hline
              &   &      &          & 1 & 1011 &            &                \\
    \end{array}
$$

<span class = "exnum">49</span>

If the truth value of the proposition

$$
    \text{P} = \text{Fred is happy}
$$

is $0.8$, and the truth value of the proposition

$$
    \text{Q} = \text{John is happy},
$$

and the negation of a proposition ($\lnot \text{Q}$) in <emphasis>fuzzy
logic</emphasis> is

$$
    \phantom{,} \ \lnot \text{Q} = \text{T} - q = 1 - q \ ,
$$

where $\text{T} = 1$ means true, and $q$ is the (probability) truth value
of $\text{Q}$, then

$$
    \phantom{.} \ \lnot \text{P} = 1 - 0.8 = 0.2 \ ,
$$

and

$$
    \phantom{.} \ \lnot \text{Q} = 1 - 0.2 = 0.8 \ ,
$$

<span class = "exnum">50</span>

Since the truth value of the conjunction of two propositions in fuzzy logic
is the minimum ($\min$) of the truth values of the two proposition, and
given the $\text{P}$ and $\text{Q}$ as in the previous exercise <span class
= "exnum">49</span>, then

<div class = "widescreen">
$$
    \phantom{.} \ \text{P} \land \text{Q} = \min(\text{P},\text{Q}) = \min(0.8,0.2) = 0.2 = \text{Q} \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ r c l }
        \text{P} \land \text{Q}
            & = & \min(\text{P},\text{Q}) \\
            & = & \min(0.8,0.2) \\
            & = & 0.2 \\
            & = & \text{Q} \ .
    \end{array}
$$
</div>

Similarly

<div class = "widescreen">
$$
    \phantom{.} \ \lnot \text{P} \land \lnot \text{Q} = \min(\lnot \text{P}, \lnot \text{Q}) = \min(0.2,0.8) = 0.2 = \lnot \text{P} \ .
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ r c l }
        \lnot \text{P} \land \lnot \text{Q}
            & = & \min(\lnot \text{P},\lnot \text{Q}) \\
            & = & \min(0.2,0.8) \\
            & = & 0.2 \\
            & = & \lnot \text{P} \ .
    \end{array}
$$
</div>

<span class = "exnum">52</span>

Yes, the assertion &ldquo;This statement is false&rdquo; is a proposition.
This is because it can be falsified. Let $P$ be the shorthand for the
assertion. Then $P$ is just as it was just given, and $\lnot P$ $=$
&ldquo;This statement is true&rdquo;.
