+++
title  = "0.1: Evaluating a Polynomial"
date   = "2025-01-01T00:00:00+03:00"
layout = "solution-single"
+++

#### Problems

<span class = "exnum">1</span>

**(a)**

$$
    \begin{array}{r c l}
        P(x) & = & 6x^4 + x^3 + 5x^2 + x + 1 \\[0.5em]
             & = & 1 + x + 5x^2 + x^3 + 6x^4 \\[0.5em]
             & = & 1 + (1 + x \cdot (5x + x^2 + 6x^3)) \\[0.5em]
             & = & 1 + (1 + x \cdot (x \cdot (5 + x + 6x^2)) \\[0.5em]
             & = & 1 + (1 + x \cdot (x \cdot (5 + (x \cdot (1 + 6x)))) \\[0.5em]
             & = & 1 + (1 + x \cdot (x \cdot (5 + (x \cdot (1 + (x \cdot 6))))))
    \end{array}
$$

**(b)**

$$
    \begin{array}{r c l}
        P(x) & = & -3x^4 + 4x^3 + 5x^2 + x - 1                             \\[0.5em]
             & = & - 1 + x + 5x^2 + 4x^3 - 3x^4                            \\[0.5em]
             & = & - 1 + (x \cdot(1 + 5x + 4x^2 - 3x^3))                   \\[0.5em]
             & = & - 1 + (x \cdot(1 + (x \cdot (5 + 4x^2 - 3x^2))))        \\[0.5em]
             & = & - 1 + (x \cdot(1 + (x \cdot (5 + (x \cdot (4 - 3x)))))) \\[0.5em]
             & = & - 1 + (x \cdot(1 + (x \cdot (5 + (x \cdot (4 - (x \cdot 3)))))))
    \end{array}
$$

**(c)**

$$
    \begin{array}{r c l}
        P(x) & = & 2x^4 + x^3 - x^2 + 1 \\[0.5em]
             & = & 1 - x^2 + x^3 + 2x^4 \\[0.5em]
             & = & 1 + (x \cdot (-x + x^2 + 2x^3)) \\[0.5em]
             & = & 1 + (x \cdot (x \cdot (-1 + x + 2x^2))) \\[0.5em]
             & = & 1 + (x \cdot (x \cdot (-1 + (x \cdot (1 + 2x))))) \\[0.5em]
             & = & 1 + (x \cdot (x \cdot (-1 + (x \cdot (1 + (x \cdot 2))))))
    \end{array}
$$

<span class = "exnum">2</span>

**(a)** Doing [the Horner's factorization][1] for $P$, means that

[1]: https://en.wikipedia.org/wiki/Horner%27s_method

$$
    \begin{array}{r c l}
        P(x) & = & 6x^3 - 2x^2 - 3x + 7 \\[0.5em]
             & = & 7 - 3x - 2x^2 + 6x^3 \\[0.5em]
             & = & 7 + (x \cdot (-3 - x^2 + 6x^2)) \\[0.5em]
             & = & 7 + (x \cdot (-3 + (x \cdot (-2 + 6x)))) \\[0.5em]
             & = & 7 + (x \cdot (-3 + (x \cdot (-2 + (x \cdot 6))))) \\[0.5em]
    \end{array}
$$

so

$$
    \begin{array}{r c l}
        P(-\frac{1}{2})
            & = & 7 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (-2 + (-\frac{1}{2} \cdot 6))))) \\[0.5em]
            & = & 7 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (-5) ))) \\[0.5em]
            & = & 7 + (-\frac{1}{2} \cdot (-3 + \frac{5}{2})) \\[0.5em]
            & = & 7 + (-\frac{1}{2} \cdot (-\frac{1}{2})) \\[0.5em]
            & = & 7 + \frac{1}{4} \ .
    \end{array}
$$

**(b)** Because

$$
    \begin{array}{r c l}
        P(x) & = & 8x^5 - x^4 - 3x^3 + x^2 - 3x + 1                                                       \\[0.5em]
             & = & 1 - 3x + x^2 - 3x^3 - x^4 + 8x^5                                                       \\[0.5em]
             & = & 1 + (x \cdot (-3 + x - 3x^2 - x^3 + 8x^4))                                             \\[0.5em]
             & = & 1 + (x \cdot (-3 + (x \cdot (1 - 3x - x^2 + 8x^3))))                                   \\[0.5em]
             & = & 1 + (x \cdot (-3 + (x \cdot (1 + (x \cdot (-3 - x + 8x^2))))))                         \\[0.5em]
             & = & 1 + (x \cdot (-3 + (x \cdot (1 + (x \cdot (-3 + (x \cdot (-1 + 8x))))))))              \\[0.5em]
             & = & 1 + (x \cdot (-3 + (x \cdot (1 + (x \cdot (-3 + (x \cdot (-1 + (x \cdot 8))))))))) \ , \\[0.5em]
    \end{array}
$$

$$
    \begin{array}{r c l}
        P(-\frac{1}{2}) 
        & = & 1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (-1 + (-\frac{1}{2} \cdot 8))))))))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (-1 - 4)))))))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (-5)))))))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (1 + (-\frac{1}{2} \cdot (-3 + \frac{5}{2})))))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (1 + (-\frac{1}{2} \cdot (-\frac{1}{2})))))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (1 + (\frac{1}{4}))))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-3 + (-\frac{1}{2} \cdot (\frac{5}{4})))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-3 -\frac{5}{8})) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot (-\frac{29}{8})) \\[0.5em]
        & = & 1 + (\frac{29}{16}) \\[0.5em]
        & = & \frac{45}{16} \ .
    \end{array}
$$

**(c)**

If

$$
    \begin{array}{ r c l }
        P(x) & = & 2x^4 + x^3 - x^2 + 1                                      \\[0.5em]
             & = & 1 - x^2 + x^3 + 2x^4                                      \\[0.5em]
             & = & 1 + (x \cdot (-x + x^2 + 2x^3))                           \\[0.5em]
             & = & 1 + (x \cdot ( x \cdot (-1 + x + 2x^2))                   \\[0.5em]
             & = & 1 + (x \cdot ( x \cdot (-1 + (x \cdot 1 + 2x))))          \\[0.5em]
             & = & 1 + (x \cdot ( x \cdot (-1 + (x \cdot 1 + (x \cdot 2))))) \ ,
    \end{array}
$$

then

$$
    \begin{array}{ r c l }
        P(-\frac{1}{2})
        & = & 1 + (-\frac{1}{2} \cdot ( -\frac{1}{2} \cdot (-1 + (-\frac{1}{2} \cdot 1 + (-\frac{1}{2} \cdot 2))))) \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot ( -\frac{1}{2} \cdot (-1 + (-\frac{1}{2} \cdot 1 - 1))))                      \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot ( -\frac{1}{2} \cdot (-1 + (-\frac{3}{2}))))                                  \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot ( -\frac{1}{2} \cdot (-1 - \frac{3}{2})))                                     \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot ( -\frac{1}{2} \cdot (-\frac{5}{2})))                                         \\[0.5em]
        & = & 1 + (-\frac{1}{2} \cdot \frac{5}{4})                                                                  \\[0.5em]
        & = & 1 - \frac{5}{8} \\[0.5em]
        & = & \frac{3}{5} \ .
    \end{array}
$$

<span class = "exnum">3</span>

--

<span class = "exnum">4</span>

**(a)** Polynomial

$$
    \phantom{.} \ P(x) = 1 + x(\frac{1}{2} + (x - 2)(\frac{1}{2} + (x - 3)(-\frac{1}{2}))) \ ,
$$

evaluated at $x = 5$ means that

$$
    \begin{array}{r c l}
        P(5) & = & 1 + 5(\frac{1}{2} + (5 - 2)(\frac{1}{2} + (5 - 3)(-\frac{1}{2}))) \\[0.5em]
             & = & 1 + 5(\frac{1}{2} + 3(\frac{1}{2} + 2(-\frac{1}{2}))) \\[0.5em]
             & = & 1 + 5(\frac{1}{2} + 3(\frac{1}{2} - 1)) \\[0.5em]
             & = & 1 + 5(\frac{1}{2} - \frac{3}{2}) \\[0.5em]
             & = & 1 - 5 \\[0.5em]
             & = & -4 \ .
    \end{array}
$$

**(b)** When $x = -1$,

$$
    \begin{array}{ r c l }
    P(-1) & = & 1 - (\frac{1}{2} + (-1 - 2)(\frac{1}{2} + (-1 - 3)(-\frac{1}{2}))) \\[0.5em]
          & = & 1 - (\frac{1}{2} - 3(\frac{1}{2} - 4(-\frac{1}{2}))) \\[0.5em]
          & = & 1 - (\frac{1}{2} - 3(\frac{1}{2} + 2)) \\[0.5em]
          & = & 1 - (\frac{1}{2} - \frac{15}{2}) \\[0.5em]
          & = & 1 - \frac{1}{2} + \frac{15}{2} \\[0.5em]
          & = & 8 \ .
    \end{array}
$$

<span class = "exnum">5</span>

When **(a)** $x = \frac{1}{2}$ and **(b)** $x = - \frac{1}{2}$ and

$$
    \phantom{.} \ P(x) = 4 + x(4 + (x - 1)(1 + (x - 2)(3 + (x - 3)(2)))) \ ,
$$

$$
    \begin{array}{ r c l }
        P(\frac{1}{2})
        & = & 4 + \frac{1}{2}(4 + (\frac{1}{2} - 1)(1 + (\frac{1}{2} - 2)(3 + (\frac{1}{2} - 3)(2)))) \\[0.5em]
        & = & 4 + \frac{1}{2}(4 + (\frac{1}{2} - 1)(1 + (\frac{1}{2} - 2)(3 - \frac{5}{2}(2))))       \\[0.5em]
        & = & 4 + \frac{1}{2}(4 + (\frac{1}{2} - 1)(1 + (\frac{1}{2} - 2)(-2)))                       \\[0.5em]
        & = & 4 + \frac{1}{2}(4 + (\frac{1}{2} - 1)(1 - \frac{3}{2})(-2))                             \\[0.5em]
        & = & 4 + \frac{1}{2}(4 + (\frac{1}{2} - 1)(-\frac{1}{2})(-2))                                \\[0.5em]
        & = & 4 + \frac{1}{2}(4 + (-\frac{1}{2})(-\frac{1}{2})(-2))                                   \\[0.5em]
        & = & 4 + \frac{1}{2}(4 - 2)                                                                  \\[0.5em]
        & = & 5 \ ,
    \end{array}
$$

and

$$
    \begin{array}{ r c l }
    P(-\frac{1}{2})
    & = & 4 -\frac{1}{2}(4 + (-\frac{1}{2} - 1)(1 + (-\frac{1}{2} - 2)(3 + (-\frac{1}{2} - 3)(2)))) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 + (-\frac{1}{2} - 1)(1 + (-\frac{1}{2} - 2)(3 + (-\frac{7}{2})(2)))) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 + (-\frac{1}{2} - 1)(1 + (-\frac{1}{2} - 2)(3 - 7))) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 + (-\frac{1}{2} - 1)(1 + (-\frac{1}{2} - 2)(-4))) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 + (-\frac{1}{2} - 1)(1 + (-\frac{5}{2})(-4))) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 + (-\frac{1}{2} - 1)(1 + 10)) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 + (-\frac{1}{2} - 1)(11)) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 + (-\frac{3}{2})(11)) \\[0.5em]
    & = & 4 -\frac{1}{2}(4 - \frac{66}{4}) \\[0.5em]
    & = & 4 -\frac{1}{2}(- \frac{50}{4}) \\[0.5em]
    & = & 4 + \frac{50}{8} \\[0.5em]
    & = & \frac{82}{8} \\[0.5em]
    & = & \frac{41}{4} \ .
    \end{array}
$$

<span class = "exnum">6</span> - <span class = "exnum">7</span>

See the blog post &ldquo;[Nested multiplication]({{< ref "post/nested-multiplication/index.md">}})&rdquo;.

#### Computer problems

<span class = "exnum">1</span> The code for the [Octave][oct] /
[MATLAB][mat] `nest` function is

[oct]: https://octave.org/
[mat]: https://www.mathworks.com/products/matlab.html

```octave { class = listing }
function y = nest(d, c, x, b)
    if nargin < 4 b = zeros(d, 1); end

    y = c(d + 1);

    for i = d : -1 : 1
        y = y .* (x - b(i)) + c(i);
    end
end
```

where `d` is the degree of polynomial, `c` is array of `d + 1` coefficients
`c`, `x` the coordinate where to evalute the polynomial, and `b` is athe
array of base points.

Now using the function to evaluate $P(x) = 1 + x + \cdots + x^50$ at $x =
1.00001$ can be done by calling

```octave
>> nest(50, ones(50), 1.00001)
```

and the call results in

```octave
ans = 51.013
```

at Octave command line.

The error of the computation by comparing with the equivalent expression
$Q(x) = (x^{51} - 1)/(x - 1)$ can be computed by running a command

```octave
>> (1.0001 .^ 51 - 1)/(1.0001 - 1)
```

that yields the answer

```octave
ans = 51.128
```

so the error of computation is then

```octave
>> abs(51.128 - 51.013)
```

i.e.

```octave
ans = 0.1150
```

which is $11,5 \%$.

<span class = "exnum">2</span>

Evaluating

$$
    P(x) = 1 - x + x^2 - x^2 + \cdots + x^{98} - x^{99}
$$

when $x = 1.00001$ with the `nest` function can be done by calling the
`nest` function as

```octave
nest(99, (-1) .^ (0:100 - 1), 1.00001)
```

Result of the call is

```octave
ans = -5.0025e-04
```

that is, $P(1.0001) = -0.0005$. It's good to notice that in the previous
call the `(-1) .^ (0:100 - 1)` results is a sequence on numbers from $0, 1,
2, \cdots, 99$, and each of these values are used as a exponent to $-1$ in
order to get the coefficients $1, -1, 1, -1, \ldots, -1$ of $P$.


