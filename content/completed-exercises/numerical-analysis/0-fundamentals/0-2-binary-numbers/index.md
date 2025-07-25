+++
title  = "0.2: Binary numbers"
date   = 2025-01-01T00:00:00+03:00
layout = "solution-single"
+++

<span class = "exnum">1</span> Applying the conversion scheme at pages 6-7
the binary representation of

**(a)** $64$ is

$$
    \begin{array}{ r c r c r c | c }
        \phantom{0}64 & \div & 2 & = & \phantom{0}32 & \text{R} & 0 \\
                   32 & \div & 2 & = &            16 & \text{R} & 0 \\
                   16 & \div & 2 & = &             8 & \text{R} & 0 \\
                    8 & \div & 2 & = &             4 & \text{R} & 0 \\
                    4 & \div & 2 & = &             2 & \text{R} & 0 \\
                    2 & \div & 2 & = &             1 & \text{R} & 0 \\
                    1 & \div & 2 & = &             0 & \text{R} & 1
    \end{array}
$$

and reading from bottom-to-up direction $(64)_{10}$ $=$ $(1000000)_2$.

**(b)** Binary representation of $17$ is

$$
    \begin{array}{ r c r c r c | c }
        \phantom{0}17 & \div & 2 & = & \phantom{00}8 & \text{R} & 1 \\
                    8 & \div & 2 & = &             4 & \text{R} & 0 \\
                    4 & \div & 2 & = &             2 & \text{R} & 0 \\
                    2 & \div & 2 & = &             1 & \text{R} & 0 \\
                    1 & \div & 2 & = &             0 & \text{R} & 1
    \end{array}
$$

so $(17)_{10} = (10001)_2$.

**(c)** Binary representation of $79$ is

$$
    \begin{array}{ r c r c r c | c }
        \phantom{0}79 & \div & 2 & = & \phantom{0}39 & \text{R} & 1 \\
                   39 & \div & 2 & = &            19 & \text{R} & 1 \\
                   19 & \div & 2 & = &             9 & \text{R} & 1 \\
                    9 & \div & 2 & = &             4 & \text{R} & 1 \\
                    4 & \div & 2 & = &             2 & \text{R} & 0 \\
                    2 & \div & 2 & = &             1 & \text{R} & 0 \\
                    1 & \div & 2 & = &             0 & \text{R} & 1
    \end{array}
$$

so $(79)_{10} = (1001111)_2$.

**(d)** Binary representation of $227$ is

$$
    \begin{array}{ r c r c r c | c }
       227 & \div & 2 & = &          113 & \text{R} & 1 \\
       113 & \div & 2 & = &           56 & \text{R} & 1 \\
        56 & \div & 2 & = &           28 & \text{R} & 0 \\
        28 & \div & 2 & = &           14 & \text{R} & 0 \\
        14 & \div & 2 & = &            7 & \text{R} & 0 \\
         7 & \div & 2 & = &            3 & \text{R} & 1 \\
         3 & \div & 2 & = &            1 & \text{R} & 1 \\
         1 & \div & 2 & = &            0 & \text{R} & 1
    \end{array}
$$

so $(227)_{10} = (11100011)_2$.

<span class = "exnum">2</span>

**(a)** If

$$
    \left( \frac{1}{8} \right)_{10} = (0.125)_{10}
$$

then

$$
    \begin{array}{ l c c c l c c }
        0.125 & \times & 2 & = & 0.25 & + & 0 \\
        0.25  & \times & 2 & = & 0.5  & + & 0 \\
        0.5   & \times & 2 & = & 0.0  & + & 1
    \end{array}
$$

so $(0.125)_{10} = (0.001)_2$.

**(b)** Similarily, because

$$
    \frac{7}{8} = 1 - \frac{1}{8} = 1 - 0.125 = 0.875,
$$

then

$$
    \begin{array}{ l c c c l c c }
        0.875 & \times & 2 & = & 0.75 & + & 1 \\
         0.75 & \times & 2 & = & 0.5  & + & 1 \\
          0.5 & \times & 2 & = & 0.0  & + & 1
    \end{array}
$$

thenceworth $(0.875)_{10} = (0.111)_2$.

**(c)** Expressing $35/16$ as a decimal by using the long division
algorithm leads to a real number $2.1875$, so to binarize the number means
binarizing the $2.0$ and $0.1875$ separately,

$$
    \begin{array}{ r c r c r c | c }
         2 & \div & 2 & = & 0 & \text{R} & 0 \\ 
         1 & \div & 2 & = & 0 & \text{R} & 1
    \end{array}
$$

and

$$
    \begin{array}{ l c c c l c c }
        0.1875 & \times & 2 & = & 0.375 & + & 0 \\
         0.375 & \times & 2 & = & 0.75  & + & 0 \\
          0.75 & \times & 2 & = & 0.5   & + & 1 \\
           0.5 & \times & 2 & = & 0.0   & + & 1
    \end{array}
$$

so $(2.1875)_{10} = (10.0011)_2$.

**(d)** Becasue $31/64 = 0.484375$, so

$$
    \begin{array}{ l c c c l c c }
        0.484375 & \times & 2 & = & 0.96875 & + & 0 \\
        0.96875  & \times & 2 & = & 0.9375  & + & 1 \\
        0.9375   & \times & 2 & = & 0.875   & + & 1 \\
        0.975    & \times & 2 & = & 0.75    & + & 1 \\
        0.75     & \times & 2 & = & 0.5     & + & 1 \\
        0.5      & \times & 2 & = & 0.0     & + & 1
    \end{array}
$$

meaning that $(0.484375)_{10} = (0.011111)_2$.

<span class = "exnum">3</span> Next exercises show only the steps and
solutions.

**(a)** $(10.5)_{10} = (1010.1)_2$:

$$
    \begin{array}{ r c r c r c c }
        10 & \div & 2 & = & 5 & \text{R} & 0 \\
         5 & \div & 2 & = & 2 & \text{R} & 1 \\
         2 & \div & 2 & = & 1 & \text{R} & 0 \\
         1 & \div & 2 & = & 0 & \text{R} & 1
    \end{array}
$$

$$
    \begin{array}{ r c r c r c c }
        0.5 & \times & 2 & = & 0.0 & + & 1 \\
        0.0 & \times & 2 & = & 0.0 & + & 0
    \end{array}
$$

**(b)** $(1/3)_{10} = (0.\bar{3})_{10} = (0.\bar{01})_2$:

$$
    \begin{array}{ c c r c c c c }
        0.\bar{3} & \times & 2 & = & 0.\bar{6} & + & 0 \\
        0.\bar{6} & \times & 2 & = & 0.\bar{3} & + & 1 \\
        0.\bar{3} & \times & 2 & = & 0.\bar{6} & + & 0 \\
        0.\bar{6} & \times & 2 & = & 0.\bar{3} & + & 1 \\
        0.\bar{3} & \times & 2 & = & 0.\bar{6} & + & 0 \\
        0.\bar{6} & \times & 2 & = & 0.\bar{3} & + & 1 \\
        \vdots    & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
    \end{array}
$$

**(c)** $(5/7)_{10} = (0.\bar{714285})_{10} = (0.\bar{10})_2$:

$$
    \begin{array}{ l c r c l c c }
        0.\bar{714285} & \times & 2 & = & 0.\bar{42857}  & + & 1 \\
        0.\bar{42857}  & \times & 2 & = & 0.\bar{857142} & + & 0 \\
        0.\bar{714285} & \times & 2 & = & 0.\bar{42857}  & + & 1 \\
        0.\bar{42857}  & \times & 2 & = & 0.\bar{857142} & + & 0 \\
        \vdots & \vdots & \vdots & \vdots & \vdots & \vdots & \vdots
    \end{array}
$$

**(d)** $(12.8)_{10} = (0.\bar{1100})_2$:

$$
    \begin{array}{ r c r c r c c }
        12.0 & \div & 2 & = & 6 & \text{R} & 0 \\
           6 & \div & 2 & = & 3 & \text{R} & 0 \\
           3 & \div & 2 & = & 1 & \text{R} & 1 \\
           1 & \div & 2 & = & 0 & \text{R} & 1
    \end{array}
$$

$$
    \begin{array}{ l c r c l c c }
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0
    \end{array}
$$

**(d)** $(55.4)_{10} = (110010.\overline{0110})_2$:

$$
    \begin{array}{ r c r c r c c }
        55.0 & \div & 2 & = & 25 & \text{R} & 0 \\
          25 & \div & 2 & = & 12 & \text{R} & 1 \\
          12 & \div & 2 & = &  6 & \text{R} & 0 \\
           6 & \div & 2 & = &  3 & \text{R} & 0 \\
           3 & \div & 2 & = &  1 & \text{R} & 1 \\
           1 & \div & 2 & = &  0 & \text{R} & 1
    \end{array}
$$

$$
    \begin{array}{ l c r c l c c }
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0
    \end{array}
$$

**(f)** $(0.1)_{10} = (0.\overline{001})_2$:

$$
    \begin{array}{ l c r c l c c }
        0.1 & \times & 2 & = & 0.2 & + & 0 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.6 & \times & 2 & = & 0.2 & + & 1
    \end{array}
$$

<span class = "exnum">4</span>

**(a)** $(11.25)_{10} = (1111.01)_2$:

$$
    \begin{array}{ r c r c r c c }
        11.0 & \div & 2 & = & 5 & \text{R} & 1 \\
           5 & \div & 2 & = & 2 & \text{R} & 1 \\
           2 & \div & 2 & = & 1 & \text{R} & 1 \\
           1 & \div & 2 & = & 0 & \text{R} & 1
    \end{array}
$$

$$
    \begin{array}{ l c r c l c c }
        0.25 & \times & 2 & = & 0.5 & + & 0 \\
        0.50 & \times & 2 & = & 0.0 & + & 1 \\
    \end{array}
$$

**(b)** $(2/3)_{10} = (0.\bar{6})_{10} = (0.100)_2$:

$$
    \begin{array}{ l c r c l c c }
        0.6  & \times & 2 & = & 0.2 & + & 1 \\
        0.2  & \times & 2 & = & 0.4 & + & 0 \\
        0.4  & \times & 2 & = & 0.8 & + & 0 \\
        0.6  & \times & 2 & = & 0.2 & + & 1 \\
        0.2  & \times & 2 & = & 0.4 & + & 0 \\
        0.4  & \times & 2 & = & 0.8 & + & 0
    \end{array}
$$

**(c)** $(3/5)_{10} = (0.6)_{10} = (0.\bar{100})_2$:

$$
    \begin{array}{ l c r c l c c }
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0
    \end{array}
$$

**(d)** $(3.2)_{10} = (11.001\bar{0011})_2$:

$$
    \begin{array}{ r c r c r c c }
        3.0 & \div & 2 & = & 1 & \text{R} & 1 \\
          1 & \div & 2 & = & 0 & \text{R} & 1
    \end{array}
$$

$$
    \begin{array}{ l c r c l c c }
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
    \end{array}
$$

**(e)** $(30.6)_{10} = (11110.\bar{100})_2$:

$$
    \begin{array}{ r c r c r c c }
        30.0 & \div & 2 & = & 15 & \text{R} & 0 \\
          15 & \div & 2 & = &  7 & \text{R} & 1 \\
           7 & \div & 2 & = &  3 & \text{R} & 1 \\
           3 & \div & 2 & = &  1 & \text{R} & 1 \\
           1 & \div & 2 & = &  0 & \text{R} & 1 \\
    \end{array}
$$

$$
    \begin{array}{ l c r c l c c }
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.2 & \times & 2 & = & 0.4 & + & 0 \\
        0.4 & \times & 2 & = & 0.8 & + & 0
    \end{array}
$$

**(f)** $(99.9)_{10} = (1000010.1\bar{110})_2$:

$$
    \begin{array}{ r c r c r c c }
        99.0 & \div & 2 & = & 33 & \text{R} & 0 \\
          33 & \div & 2 & = & 16 & \text{R} & 1 \\
          16 & \div & 2 & = &  8 & \text{R} & 0 \\
           8 & \div & 2 & = &  4 & \text{R} & 0 \\
           4 & \div & 2 & = &  2 & \text{R} & 0 \\
           2 & \div & 2 & = &  1 & \text{R} & 0 \\
           1 & \div & 2 & = &  0 & \text{R} & 1
    \end{array}
$$

$$
    \begin{array}{ l c r c l c c }
        0.9 & \times & 2 & = & 0.8 & + & 1 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
        0.8 & \times & 2 & = & 0.6 & + & 1 \\
        0.6 & \times & 2 & = & 0.2 & + & 1 \\
        0.4 & \times & 2 & = & 0.8 & + & 0 \\
    \end{array}
$$

<span class = "exnum">5</span> &ndash; <span class = "exnum">6</span>

If

$$
    \pi = 3.141592653589793
$$

then

$$
    \begin{array}{ r c r c r c c }
           3 & \div & 2 & = &  1 & \text{R} & 1 \\
           1 & \div & 2 & = &  0 & \text{R} & 1
    \end{array}
$$

and

<div class = "widescreen">
$$
    \begin{array}{ l c r c l c c }
        0.141592653589793 & \times & 2 & = & 0.283185307179586 & + & 0 \\
        0.283185307179586 & \times & 2 & = & 0.566370614359172 & + & 0 \\
        0.566370614359172 & \times & 2 & = & 0.132741228718344 & + & 1 \\
        0.132741228718344 & \times & 2 & = & 0.265482457436688 & + & 0 \\
        0.265482457436688 & \times & 2 & = & 0.530964914873376 & + & 0 \\
        0.530964914873376 & \times & 2 & = & 0.061929829746752 & + & 1 \\
        0.061929829746752 & \times & 2 & = & 0.123859659493504 & + & 0 \\
        0.123859659493504 & \times & 2 & = & 0.247719318987008 & + & 0 \\
        0.247719318987008 & \times & 2 & = & 0.495438637974016 & + & 0 \\
        0.495438637974016 & \times & 2 & = & 0.990877275948032 & + & 0 \\
        0.990877275948032 & \times & 2 & = & 0.981754551896064 & + & 1 \\
        0.981754551896064 & \times & 2 & = & 0.963509103792128 & + & 1 \\
        0.963509103792128 & \times & 2 & = & 0.927018207584256 & + & 1 \\
        0.927018207584256 & \times & 2 & = & 0.854036415168512 & + & 1 \\
        0.854036415168512 & \times & 2 & = & 0.708072830337024 & + & 1 \\
    \end{array}
$$
</div>
<div class = "smallscreen">
$$
    \begin{array}{ l c r c l c c }
        0.1415\ldots & \times & 2 & = & 0.2831\ldots & + & 0 \\
        0.2831\ldots & \times & 2 & = & 0.5663\ldots & + & 0 \\
        0.5663\ldots & \times & 2 & = & 0.1327\ldots & + & 1 \\
        0.1327\ldots & \times & 2 & = & 0.2654\ldots & + & 0 \\
        0.2654\ldots & \times & 2 & = & 0.5309\ldots & + & 0 \\
        0.5309\ldots & \times & 2 & = & 0.0619\ldots & + & 1 \\
        0.0619\ldots & \times & 2 & = & 0.1238\ldots & + & 0 \\
        0.1238\ldots & \times & 2 & = & 0.2477\ldots & + & 0 \\
        0.2477\ldots & \times & 2 & = & 0.4954\ldots & + & 0 \\
        0.4954\ldots & \times & 2 & = & 0.9908\ldots & + & 0 \\
        0.9908\ldots & \times & 2 & = & 0.9817\ldots & + & 1 \\
        0.9817\ldots & \times & 2 & = & 0.9635\ldots & + & 1 \\
        0.9635\ldots & \times & 2 & = & 0.9270\ldots & + & 1 \\
        0.9270\ldots & \times & 2 & = & 0.8540\ldots & + & 1 \\
        0.8540\ldots & \times & 2 & = & 0.7080\ldots & + & 1 \\
    \end{array}
$$
</div>

so $\pi$ in binary when computing its first fifteen digits are

$$
    \phantom{.} \ (11.00101000011111)_{10} \ .
$$

Similarily, since

$$
    e = 2.718281828459045\cdots
$$

so ignoring numbers after the 15th digit of $e$, it can be seen that for
$(2.0)_{10}$,

$$
    \begin{array}{ r c r c r c c }
           2 & \div & 2 & = &  0 & \text{R} & 1 \\
           0 & \div & 2 & = &  0 & \text{R} & 0
    \end{array}
$$

and for the decimal part

<div class = "widescreen">
$$
    \begin{array}{ l c r c l c c }
        0.718281828459045 & \times & 2 & = & 0.436563656918090 & + & 1 \\
        0.436563656918090 & \times & 2 & = & 0.873127313836180 & + & 0 \\
        0.873127313836180 & \times & 2 & = & 0.746254627672360 & + & 1 \\
        0.746254627672360 & \times & 2 & = & 0.492509255344720 & + & 1 \\
        0.492509255344720 & \times & 2 & = & 0.985018510689440 & + & 0 \\
        0.985018510689440 & \times & 2 & = & 0.970037021378880 & + & 1 \\
        0.970037021378880 & \times & 2 & = & 0.940074042757760 & + & 1 \\
        0.940074042757760 & \times & 2 & = & 0.880148085515520 & + & 1 \\
        0.880148085515520 & \times & 2 & = & 0.760296171031040 & + & 1 \\
        0.760296171031040 & \times & 2 & = & 0.520592342062080 & + & 1 \\
        0.520592342062080 & \times & 2 & = & 0.041184684124160 & + & 1 \\
        0.041184684124160 & \times & 2 & = & 0.082369368248320 & + & 0 \\
        0.082369368248320 & \times & 2 & = & 0.164738736496640 & + & 0 \\
        0.164738736496640 & \times & 2 & = & 0.329477472993280 & + & 0 \\
        0.329477472993280 & \times & 2 & = & 0.658954945986560 & + & 0 \\
        0.658954945986560 & \times & 2 & = & 0.317909891973120 & + & 0
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{ l c r c l c c }
        0.7182\ldots & \times & 2 & = & 0.4365\ldots & + & 1 \\
        0.4365\ldots & \times & 2 & = & 0.8731\ldots & + & 0 \\
        0.8731\ldots & \times & 2 & = & 0.7462\ldots & + & 1 \\
        0.7462\ldots & \times & 2 & = & 0.4925\ldots & + & 1 \\
        0.4925\ldots & \times & 2 & = & 0.9850\ldots & + & 0 \\
        0.9850\ldots & \times & 2 & = & 0.9700\ldots & + & 1 \\
        0.9700\ldots & \times & 2 & = & 0.9400\ldots & + & 1 \\
        0.9400\ldots & \times & 2 & = & 0.8801\ldots & + & 1 \\
        0.8801\ldots & \times & 2 & = & 0.7602\ldots & + & 1 \\
        0.7602\ldots & \times & 2 & = & 0.5205\ldots & + & 1 \\
        0.5205\ldots & \times & 2 & = & 0.0411\ldots & + & 1 \\
        0.0411\ldots & \times & 2 & = & 0.0823\ldots & + & 0 \\
        0.0823\ldots & \times & 2 & = & 0.1647\ldots & + & 0 \\
        0.1647\ldots & \times & 2 & = & 0.3294\ldots & + & 0 \\
        0.3294\ldots & \times & 2 & = & 0.6589\ldots & + & 0 \\
        0.6589\ldots & \times & 2 & = & 0.3179\ldots & + & 0
    \end{array}
$$
</div>

which means that $e$ approximated to first fifteen digits is

$$
    \phantom{.} \ (01.101101111110000)_2 \ .
$$

<span class = "exnum">7</span>

**(a)**

<div class = "widescreen">
$$
    (1010101)_2 =
        1 \cdot 2^6 +
        0 \cdot 2^5 +
        1 \cdot 2^4 +
        0 \cdot 2^3 +
        1 \cdot 2^2 +
        0 \cdot 2^1 +
        1 \cdot 2^0 = 85.
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        (1010101)_2 & = & 1 \cdot 2^6 + 0 \cdot 2^5 + 1 \cdot 2^4 \\[0.2em]
                    &   & + \ 0 \cdot 2^3 + 1 \cdot 2^2 + 0 \cdot 2^1 \\[0.2em]
                    &   & + \ 1 \cdot 2^0 \\[0.2em]
                    & = & 85.
    \end{array}
$$
</div>

**(b)**

<div class = "widescreen">
$$
    \begin{array}{r c l}
        (1011.101)_2 & = & 1 \cdot 2^3
            + 0 \cdot 2^2
            + 1 \cdot 2^1
            + 1 \cdot 2^0
            + 1 \cdot 2^{-2}
            + 0 \cdot 2^{-3}
            + 1 \cdot 2^{-4} \\
            & = & 8 + 2 + 1 + \dfrac{1}{2} + \dfrac{1}{8} \\
            & = & 11.6525.
    \end{array}
$$
</div>

<div class = "smallscreen">
$$
    \begin{array}{r c l}
        (1011.101)_2 & = & 1 \cdot 2^3 + 0 \cdot 2^2           \\[0.2em]
            &   & + 1 \cdot 2^1 + 1 \cdot 2^0 + 1 \cdot 2^{-2} \\[0.2em]
            &   & + 0 \cdot 2^{-3} + 1 \cdot 2^{-4}            \\
            & = & 8 + 2 + 1 + \dfrac{1}{2} + \dfrac{1}{8}      \\
            & = & 11.6525.
    \end{array}
$$
</div>

**(c)**

...

**(d)**

...

**(e)**

...

**(f)**

...

**(g)**

...

**(g)**

...

<span class = "exnum">8</span>

...
