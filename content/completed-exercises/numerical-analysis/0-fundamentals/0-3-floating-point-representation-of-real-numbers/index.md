+++
title  = "0.3: Floating point representation of real numbers"
date   = 2025-01-01T00:00:00+03:00
layout = "solution-single"
+++

<span class = "exnum">1</span> **(a)** Because $\left( \frac{1}{4}
\right)_{10} = (0.25)_{10}$, the fractional part can converted to
binary as follows;

$$
    \begin{array}{r c l}
        0.25 & \times & 2 & = & 0.5 & + & 0 \\
        0.5  & \times & 2 & = & 1.0 & + & 1 \\
        0.0  & \times & 2 & = & 0.0 & + & 0 \\
    \end{array}
$$

Reading the ones and zeros at right from top to bottom, it can be
seen that $(0.25)_{10}$ $=$ $(0.10)_2$. Verifying the result can be
done by evaluating the binary fraction by summing the values

$$
    \phantom{.} \ 0 \cdot 2^{-1} + 1 \cdot 2^{-2} = \frac{1}{2^2} = \frac{1}{4} \ ,
$$

so indeed $\left( \frac{1}{4} \right)_{10}$ $=$ $(0.01)_2$.

Expressing the binary value means to moving the decimal, i.e. the
[**radix**][01] point to the right $2$ times, that the number becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \times 2^{-2} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \times \hspace{2pt} 2^{-2} \ .
\end{array}
$$
</div>

[01]:https://simple.wikipedia.org/wiki/Radix_point

**(b)** As above, $\frac{1}{3}$ can be written in decimal form as
$0.\overline{3}$, so the value's binary representation is then

$$
    \begin{array}{r c l}
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        & & & \vdots & & &
    \end{array}
$$

that is, $(0.\overline{0}\overline{1})_2$. Moving radix to the left
by two indices leads to exponent of $2^{-2}$, so the double
precision IEEE-754 binary representation of $\frac{1}{3}$ is

<div class = "widescreen">
$$
    \phantom{.} \ +1.0101 \ 0101 \ 0101 \ 0101 \ 0101 \
                     0101 \ 0101 \ 0101 \ 0101 \ 0101 \
                     0101 \ 0101 \ 0101 \times 2^{-2} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.0101 \ 0101 \ 0101 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0101 \ 0101 \ 0101 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0101 \times \hspace{2pt} 2^{-2} \ .
\end{array}
$$
</div>

**(c)** The logic is the same for as it was for **(a)** and
**(b)**: Convert to decimal, normalize radix, repeat the pattern
and see if the $53$the binary value is $0$ or $1$. In the case of
$0$ do nothing and in the case of $1$, add $1$ to the $52$th bit,
unless all bits after the $53$rd are zero. Thus

$$
    \frac{2}{3} = 0.\overline{6}
$$

has the binary representation

$$
    \begin{array}{r c l}
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        & & & \vdots & & &
    \end{array}
$$

Reading from top to bottom tells that $(\frac{2}{3})_{10} =
(0.\overline{1}\overline{0})_2$, so the floating point
representation is

<div class = "widescreen">
$$
    \phantom{.} \ +1.1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1010 \times 2^{-2} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1010 \ 1010 \ 0010 \ 0010 \ 0010 \ 0010 \\
    \phantom{+1.}1010 \ 1010 \ 0010 \ 0010 \ 0010 \ 0010 \\
    \phantom{+1.}1010 \times \hspace{2pt} 2^{-2} \ .
\end{array}
$$
</div>

but in this case the $53$th bit is $1$, so one bit is needed to be added to
$52$th bit, which means that the floating point representation becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1011 \times 2^{-2} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1010 \ 1010 \ 0010 \ 0010 \ 0010 \ 0010 \\
    \phantom{+1.}1010 \ 1010 \ 0010 \ 0010 \ 0010 \ 0010 \\
    \phantom{+1.}1011 \times \hspace{2pt} 2^{-2} \ .
\end{array}
$$
</div>

**(d)** Steps for the value $0.9$ are the same. Converting the
value to binary

$$
    \begin{array}{r c l}
        0.9 & \times & 2 & = & 0.8 & + & 1 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        & & & \vdots & & &
    \end{array}
$$

so the binary representation of $(0.9)_{10}$ is
$0.1\overline{1}\overline{1}\overline{0}\overline{0}$, and the
floating point is then

<div class = "widescreen">
$$
    \phantom{.} \ +1.1110 \ 0110 \ 0110 \ 0110 \ 0110 \
                     0110 \ 0110 \ 0110 \ 0110 \ 0110 \
                     0110 \ 0110 \ 0110 \times 2^{-2} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1110 \ 0110 \ 0110 \ 0110 \ 0110 \ 0110 \\
    \phantom{+1.}0110 \ 0110 \ 0110 \ 0110 \ 0110 \ 0110 \\
    \phantom{+1.}0110 \times \hspace{2pt} 2^{-1} \ .
\end{array}
$$
</div>

<span class = "exnum">2</span> **(a)** Converting $9.5$ to binary
means applying the binarization routine to the whole and fractional
parts of the number:

$$
    \begin{array}{r c c c c c c}
        9 & \div & 2 & = & 4 & \text{R} & 1 \\
        4 & \div & 2 & = & 2 & \text{R} & 0 \\
        2 & \div & 2 & = & 1 & \text{R} & 0 \\
        1 & \div & 2 & = & 0 & \text{R} & 1 \\
    \end{array}
$$

$$
    \begin{array}{r c c c c c c}
        0.5 & \times & 2 & =      & 0.0 & + & 1 \\
        0.0 & \times & 2 & =      & 0.0 & + & 0 \\
        0.0 & \times & 2 & =      & 0.0 & + & 0 \\
            &        &   & \vdots &     &   &
    \end{array}
$$

So $(9.5)_{10} = (1001.1\overline{0})_2$. Normalizing the radix
means that the binary becomes $1.0011\overline{0}$, making the
exponent to be $2^{3}$, and so, the floating point representation
is

<div class = "widescreen">
$$
    \phantom{.} \ +1.0011 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \times 2^{3}  \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.0011 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \times \hspace{2pt} 2^{3} \ .
\end{array}
$$
</div>

**(b)** The steps for the number $9.6$ are the same: The decimal
part of the number is $(1001)_2$ and the fractional part is

$$
    \begin{array}{r c c c c c c}
        0.6 & \times & 2 & =      & 0.2 & + & 1 \\
        0.2 & \times & 2 & =      & 0.4 & + & 0 \\
        0.8 & \times & 2 & =      & 0.6 & + & 1 \\
        0.6 & \times & 2 & =      & 0.2 & + & 1 \\
        0.2 & \times & 2 & =      & 0.4 & + & 0 \\
        0.8 & \times & 2 & =      & 0.6 & + & 1 \\
            &        &   & \vdots &     &   &
    \end{array}
$$

so $(9.6)_{10} = (1001.\overline{1}\overline{0}\overline{1})_2$. The
exponent is the same as in **(a)**, that is, $2^{3}$. The IEEE 754 floating
representation of $9.6$ is

<div class = "widescreen">
$$
    \phantom{.} \ +1.0011 \ 0110 \ 1101 \ 1011 \ 0110 \
                     1101 \ 1011 \ 0110 \ 1101 \ 1011 \
                     0110 \ 1101 \ 1011 \times 2^{3}  \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.0011 \ 0110 \ 1101 \ 1011 \ 0110 \ 1101 \\
    \phantom{+1.}1011 \ 0110 \ 1101 \ 1011 \ 0110 \ 1101 \\
    \phantom{+1.}1011 \times \hspace{2pt} 2^{3} \ .
\end{array}
$$
</div>

The $53$rd bit is $1$, so $52$nd bit gets incremented by one, and the bit
get carried over and the binary number becomes

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.0011 \ 0110 \ 1101 \ 1011 \ 0110 \ 1101 \\
    \phantom{+1.}1011 \ 0110 \ 1101 \ 1011 \ 0110 \ 1101 \\
    \phantom{+1.}1100 \times \hspace{2pt} 2^{3} \ .
\end{array}
$$
</div>

**(c)** The steps are, convert the decimal number $(100.2)_2$to binary:

$$
    \begin{array}{r c c c c c c}
        100 & \div & 2 & = & 50 & \text{R} & 0 \\
         50 & \div & 2 & = & 25 & \text{R} & 0 \\
         25 & \div & 2 & = & 12 & \text{R} & 1 \\
         12 & \div & 2 & = &  6 & \text{R} & 0 \\
          6 & \div & 2 & = &  3 & \text{R} & 0 \\
          3 & \div & 2 & = &  1 & \text{R} & 1 \\
          1 & \div & 2 & = &  0 & \text{R} & 1 \\
    \end{array}
$$

and

$$
    \phantom{,} \quad
        \begin{array}{r c c c c c c}
            0.2 & \times & 2 & = & 0.4 & + & 0 \\
            0.4 & \times & 2 & = & 0.8 & + & 0 \\
            0.8 & \times & 2 & = & 0.6 & + & 1 \\
            0.6 & \times & 2 & = & 0.2 & + & 1 \\
            0.2 & \times & 2 & = & 0.4 & + & 0 \\
            0.4 & \times & 2 & = & 0.8 & + & 0 \\
            0.8 & \times & 2 & = & 0.6 & + & 1 \\
            0.6 & \times & 2 & = & 0.2 & + & 1 \\
            & & & \vdots & & &
    \end{array}
$$

so the value in binary is $(1100100.\overline{0011})_2$. Moving the
radix to the left by six indices leads to exponent of $2^{-6}$, so
the double precision IEEE-754 binary representation of
$\frac{1}{3}$ is

<div class = "widescreen">
$$
    \phantom{.} \ +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \times 2^{-6} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \times \hspace{2pt} 2^{-6} \ .
\end{array}
$$
</div>

**(c)** The logic is the same for as it was for **(a)** and
**(b)**: Convert to decimal, normalize the radix, repeat the
pattern and see if the $53$the binary value is $0$ or $1$. In the
case of $0$ do nothing and in the case of $1$, add $1$ to the
$52$th bit. Therefore, when

$$
    \frac{2}{3} = 0.\overline{6},
$$

the binary representation is

$$
    \begin{array}{r c l}
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        0.\overline{6} & \times & 2 & = & 0.\overline{3} & + & 1 \\
        0.\overline{3} & \times & 2 & = & 0.\overline{6} & + & 0 \\
        & & & \vdots & & &
    \end{array}
$$

Reading from top to bottom, the $(\frac{2}{3})_{10} =
(0.\overline{1}\overline{0})_2$, so the floating point
representation is

<div class = "widescreen">
$$
    \phantom{.} \ +1.1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1010 \times 2^{-2} \ ,
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1010 \ 1010 \ 1010 \ 1010 \ 1010 \ 1010 \\
    \phantom{+1.}1010 \ 1010 \ 1010 \ 1010 \ 1010 \ 1010 \\
    \phantom{+1.}1010 \times \hspace{2pt} 2^{-2} \ .
\end{array}
$$
</div>

but in this case the $53$th bit is $1$, so one bit is needed to be
added to $52$th bit, which means that the floating point
representation becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1010 \ 1010 \ 1010 \
                     1010 \ 1010 \ 1011 \times 2^{-2} \ ,
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1010 \ 1010 \ 1010 \ 1010 \ 1010 \ 1010 \\
    \phantom{+1.}1010 \ 1010 \ 1010 \ 1010 \ 1010 \ 1010 \\
    \phantom{+1.}1011 \times \hspace{2pt} 2^{-2} \ .
\end{array}
$$
</div>

**(d)** Steps for the value $0.9$ are the same. Converting the
value to binary

$$
    \begin{array}{r c l}
        0.9 & \times & 2 & = & 0.8 & + & 1 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        & & & \vdots & & &
    \end{array}
$$

so the binary representation of $0.9$ is
$0.1\overline{1}\overline{1}\overline{0}\overline{0}$, and the
floating point is then

<div class = "widescreen">
$$
    \phantom{.} \ +1.1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \times 2^{-1} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \times \hspace{2pt} 2^{-1} \ .
\end{array}
$$
</div>

The $53$th bit is $1$, so $1$ can be added to $52$nd bit, meaning
that the binary becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \times 2^{-1} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1101 \times \hspace{2pt} 2^{-1} \ .
\end{array}
$$
</div>

<span class = "exnum">2</span> **(a)** Converting $9.5$ to binary means
applying the binarization routine to the whole and fractional parts of the
number:

$$
    \begin{array}{r c c c c c c}
        9 & \div & 2 & = & 4 & \text{R} & 1 \\
        4 & \div & 2 & = & 2 & \text{R} & 0 \\
        2 & \div & 2 & = & 1 & \text{R} & 0 \\
        1 & \div & 2 & = & 0 & \text{R} & 1 \\
    \end{array}
$$

$$
    \begin{array}{r c c c c c c}
        0.5 & \times & 2 & =      & 0.0 & + & 1 \\
        0.0 & \times & 2 & =      & 0.0 & + & 0 \\
        0.0 & \times & 2 & =      & 0.0 & + & 0 \\
            &        &   & \vdots &     &   &
    \end{array}
$$

So $(9.5)_{10} = (1001.1\overline{0})_2$. Normalizing the radix means that
the binary becomes $1.0011\overline{0}$, making the exponent to be $2^{3}$,
and so, the floating point representation is

<div class = "widescreen">
$$
    \phantom{.} \ +1.0011 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \times 2^{3}  \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{r l l}
    +1.0011000000000 & \\
       0000000000000 & \\
       0000000000000 & \\
       0000000000000 & \hspace{-9pt} \times \hspace{2pt} 2^{3} \ .
\end{array}
$$
</div>

**(b)** The steps for the number $9.6$ are the same: The decimal
part of the number is $(1001)_2$ and the fractional part is

$$
    \begin{array}{r c c c c c c}
        0.6 & \times & 2 & =      & 0.2 & + & 1 \\
        0.2 & \times & 2 & =      & 0.4 & + & 0 \\
        0.4 & \times & 2 & =      & 0.8 & + & 0 \\
        0.8 & \times & 2 & =      & 0.6 & + & 1 \\
        0.6 & \times & 2 & =      & 0.2 & + & 1 \\
        0.2 & \times & 2 & =      & 0.4 & + & 0 \\
        0.4 & \times & 2 & =      & 0.8 & + & 0 \\
        0.6 & \times & 2 & =      & 0.2 & + & 1 \\
            &        &   & \vdots &     &   &
    \end{array}
$$

so $(9.6)_{10} = (1001.\overline{1}\overline{0}\overline{1})_2$.
The exponent is the same as in **(a)**, that is, $2^{3}$. The IEEE
754 floating representation of $9.6$ is

<div class = "widescreen">
$$
    \phantom{.} \ +1.1001 \ 1001 \ 1001 \ 1001 \ 1001 \
                     1001 \ 1001 \ 1001 \ 1001 \ 1001 \
                     1001 \ 1001 \ 1001 \times 2^{3}  \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1001 \ 1001 \ 1001 \ 1001 \ 1001 \ 1001 \\
    \phantom{+1.}1001 \ 1001 \ 1001 \ 1001 \ 1001 \ 1001 \\
    \phantom{+1.}1001 \times \hspace{2pt} 2^{3} \ .
\end{array}
$$
</div>

**(c)** The steps are, convert the decimal number $(100.2)_2$to binary:

$$
    \begin{array}{r c c c c c c}
        100 & \div & 2 & = & 50 & \text{R} & 0 \\
         50 & \div & 2 & = & 25 & \text{R} & 0 \\
         25 & \div & 2 & = & 12 & \text{R} & 1 \\
         12 & \div & 2 & = &  6 & \text{R} & 0 \\
          6 & \div & 2 & = &  3 & \text{R} & 0 \\
          3 & \div & 2 & = &  1 & \text{R} & 1 \\
          1 & \div & 2 & = &  0 & \text{R} & 1 \\
    \end{array}
$$

and

$$
    \phantom{,} \quad
        \begin{array}{r c c c c c c}
            0.2 & \times & 2 & = & 0.4 & + & 0 \\
            0.4 & \times & 2 & = & 0.8 & + & 0 \\
            0.8 & \times & 2 & = & 0.6 & + & 1 \\
            0.6 & \times & 2 & = & 0.2 & + & 1 \\
            0.2 & \times & 2 & = & 0.4 & + & 0 \\
            0.4 & \times & 2 & = & 0.8 & + & 0 \\
            0.8 & \times & 2 & = & 0.6 & + & 1 \\
            0.6 & \times & 2 & = & 0.2 & + & 1 \\
                &        &   & \vdots  &     &   &
        \end{array}
    \quad ,
$$

so $(100.2)_{10}$ $=$ $(1100100.\overline{0}\overline{0}\overline{1}\overline{1})_2$.
Then normalize the radix by moving it to the right of the leftmost binary
equal to $1$, keep count of how many times the radix was moved and set that
number to be a power of the multiplier of $2$ of the binary value, i.e. the
value becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \times 2^{7} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \times \hspace{2pt} 2^{7} \ .
\end{array}
$$
</div>

The $53$rd bit is $1$, so the least significant bit is set to $1$, so the
binary value becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1101 \times 2^{7} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1101 \times \hspace{2pt} 2^{7} \ .
\end{array}
$$
</div>

**(d)** Just as in **(c)**, the steps are the same: Because $44/7$ $=$
$6.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4}$,
the decimal part is $(110)_2$ and the fractional part is

$$
    \phantom{,} \quad
        \begin{array}{r c c c l c c}
            0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & \times & 2
            & = & 0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & + & 0 \\
            0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & \times & 2
            & = & 0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & + & 1 \\
            0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & \times & 2
            & = & 0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & + & 0 \\
            0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & \times & 2
            & = & 0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & + & 0 \\
            0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & \times & 2
            & = & 0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & + & 1 \\
            0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & \times & 2
            & = & 0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & + & 0 \\
        \end{array}
    \quad .
$$

so $(100.2)_{10}$ $=$ $(1100100.\overline{0}\overline{0}\overline{1}\overline{1})_2$.
Then normalize the radix by moving it to the right of the leftmost binary
equal to $1$, keep count of how many times the radix was moved and set that
number to be a power of the multiplier of $2$ of the binary value, i.e. the
value becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \times 2^{7}  \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \times \hspace{2pt} 2^{7} \ .
\end{array}
$$
</div>

The $53$rd bit is $1$, so the least significant bit is set to $1$, so the
binary value becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1100 \ 1100 \ 1100 \
                     1100 \ 1100 \ 1101 \times 2^{7}  \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1001 \ 0000 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1100 \ 1100 \ 1100 \ 1100 \ 1100 \ 1100 \\
    \phantom{+1.}1101 \times \hspace{2pt} 2^{7} \ .
\end{array}
$$
</div>

**(d)** Just as in **(c)**, the steps are the same: Because $44/7$ $=$
$6.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4}$,
the decimal part is $(110)_2$ and the fractional part is

$$
    \phantom{,} \quad
        \begin{array}{r c c c l c c}
            0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & \times & 2
            & = & 0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & + & 0 \\
            0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & \times & 2
            & = & 0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & + & 1 \\
            0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & \times & 2
            & = & 0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & + & 0 \\
            0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & \times & 2
            & = & 0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & + & 0 \\
            0.\overline{5}\overline{7}\overline{1}\overline{4}\overline{2}\overline{8} & \times & 2
            & = & 0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & + & 1 \\
            0.\overline{1}\overline{4}\overline{2}\overline{8}\overline{5}\overline{7} & \times & 2
            & = & 0.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4} & + & 0 \\
            & & & \vdots & & & \\
        \end{array}
    \quad ,
$$

that is $(0.\overline{0}\overline{1}\overline{0})_2$, so
$(6.\overline{2}\overline{8}\overline{5}\overline{7}\overline{1}\overline{4})_{10}$
$=$ $(110.\overline{0}\overline{1}\overline{0})_2$. Normalising the
value means moving the radix to the left two steps, making the
exponent (multiplier) $2^2$, so the floating point binary
representation of $(0.\overline{0}\overline{1}\overline{0})_2$ is

<div class = "widescreen">
$$
    \phantom{.} \ +1.1001 \ 0010 \ 0100 \ 1001 \ 0010 \
                     0100 \ 1001 \ 0010 \ 0100 \ 1001 \
                     0010 \ 0100 \ 1001 \times 2^{2}  \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.1001 \ 0010 \ 0100 \ 1001 \ 0010 \ 0100 \\
    \phantom{+1.}1001 \ 0010 \ 0100 \ 1001 \ 0010 \ 0100 \\
    \phantom{+1.}1001 \times \hspace{2pt} 2^{2} \ .
\end{array}
$$
</div>

<span class = "exnum">3</span>
The IEEE double precision floating point value of $5_{10}$ is
exactly $101_{2}$ $=$ $(1.01 \times 2^{-2})_2$, which means that
storing the fractional part into mantissa of a IEEE double
precision floating point number reserves the most and second most
significant bits. In other words, the number becomes

<div class = "widescreen">
$$
    \phantom{.} \ +1.0100 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \times 2^{-2} \ ,
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +1.0100 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \times \hspace{2pt} 2^{-2} \ ,
\end{array}
$$
</div>

so there are at most $52$ $-$ $2$ $=$ $50$ bits available to store
the fraction of the value $5 \times 2^{-k}$ without loss of
precision. In other words, for $k$ $=$ $1,2,\ldots,50$, i.e., $k
\leq 50$ the number $5 \times 2^{-k}$ can be stored without losing
precision and if $k$ $>$ $50$, the number &ldquo;underflows&rdquo;
to $5 \times 2^{-2}$ because the least significant bit goes outside
of the bits that are taken into account.

<span class = "exnum">4</span>

...

<span class = "exnum">5</span> **(a)** The $1$ and $-1$ cancels on
both sides, so to get the result, just the summation $2^{-51}$ $+$
$2^{-53}$ needs to be evaluated, so because $2^{51}$ $+$ $2^{-53}$
$=$ $2 \times 2 \times 2^{-53}$ $+$ $2^{-53}$ $=$ $4 \times
2^{-53}$ $+$ $2^{-53}$ $=$ $5 \times 2^{-53}$ and since
$\operatorname{fl}(2^{-53})$ is equal to

<div class = "widescreen">
$$
    \phantom{.} \ +0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 1 \times 2^{-53} \ ,
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \ 1 \times \hspace{2pt} 2^{-53} \ ,
\end{array}
$$
</div>

finding out the summation means computing $\sum_{i = 1}^5
\operatorname{fl}_i(2^{-51})$ which means adding $0000 \ 1$ five
times and prepending the leading zeros plus the radix point. The
result is

<div class = "widescreen">
$$
    \begin{array}{c l}
          & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 1\times 2^{-53} \\
        + & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 1\times 2^{-53} \\[0.5em] \hline
          & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0001 \ 0\times 2^{-53} \\
        + & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 1\times 2^{-53} \\[0.5em] \hline
          & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0001 \ 1\times 2^{-53} \\
        + & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 1\times 2^{-53} \\[0.5em] \hline
          & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0010 \ 0\times 2^{-53} \\
        + & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 1\times 2^{-53} \\[0.5em] \hline
          & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0010 \ 1\times 2^{-53} \\
        + & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 1\times 2^{-53} \\[0.5em] \hline
          & + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                         0000 \ 0000 \ 0011 \ 0\times 2^{-53}
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{c l}
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 1 \times \hspace{2pt} 2^{-53} \  \\
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    + & \phantom{+ \ 1.}0000 \ 1 \times \hspace{2pt} 2^{-53} \  \\[0.5em] \hline % # -----
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0001 \ 0 \times \hspace{2pt} 2^{-53} \  \\
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    + & \phantom{+ \ 1.}0000 \ 1 \times \hspace{2pt} 2^{-53} \  \\[0.5em] \hline % # -----
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0001 \ 1 \times \hspace{2pt} 2^{-53} \  \\
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    + & \phantom{+ \ 1.}0000 \ 1 \times \hspace{2pt} 2^{-53} \  \\[0.5em] \hline % # -----
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0010 \ 0 \times \hspace{2pt} 2^{-53} \  \\
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    + & \phantom{+ \ 1.}0000 \ 1 \times \hspace{2pt} 2^{-53} \  \\[0.5em] \hline % # -----
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0010 \ 1 \times \hspace{2pt} 2^{-53} \  \\
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    + & \phantom{+ \ 1.}0000 \ 1 \times \hspace{2pt} 2^{-53} \  \\[0.5em] \hline % # -----
      &           + \ 0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
      & \phantom{+ \ 1.}0011 \ 0 \times \hspace{2pt} 2^{-53}
\end{array}
$$
</div>

and applying the Nearest Rule means that the result is rounded
down, i.e., the $53$rd zero can be discarded, so the result can be
re-written as

<div class = "widescreen">
$$
    \phantom{.} \ +0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0011 \ \times 2^{-52} \ .
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0011 \ \times \hspace{2pt} 2^{-52} \ .
\end{array}
$$
</div>

When doing the same computation in Octave by setting `format` to
`bit` and typing

```octave
>> (1 + (4 * 2^(-53) + 2^(-53))) + 1
```

the result is

<div class = "widescreen">
$$
    \phantom{.} \ +0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0000 \ 0000 \ 0000 \
                     0000 \ 0000 \ 0001 \ \times 2^{-52} \ ,
$$
</div>

<div class = "smallscreen">
$$
\begin{array}{l}
              +0.0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0000 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000 \\
    \phantom{+1.}0001 \ \times \hspace{2pt} 2^{-52} \ ,
\end{array}
$$
</div>

**(b)**

...

<span class = "exnum">6</span>

...


<span class = "exnum">7</span>

...

<span class = "exnum">8</span>

...

<span class = "exnum">9</span>

...

<span class = "exnum">10</span>

...

<span class = "exnum">11</span>

...

<span class = "exnum">12</span>

...

<span class = "exnum">13</span>

...

<span class = "exnum">14</span>

...

<span class = "exnum">15</span>

...

<span class = "exnum">16</span>

...
