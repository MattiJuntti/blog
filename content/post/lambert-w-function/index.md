+++
title = 'Lambert W-function'
date  = 2026-02-15T10:23:28+02:00
+++

The first problem of chapter 1 in Cormen et al. (2022) is to find
numbers to empty cells of _algorithmic time complexity / time
budget table_. Columns of the table represent different durations of
time ($t$) ranging from one second ($\text{s}$) to one minute
($\text{min}$) to all the way up to one century ($\text{c}$). Rows
of the table are suggested running times of algorithms for inputs
of size $n$. The problem is then to figure out what is the largest
size of $n$ for each algorithm's running time $t$. In other words,
this means solving equations of type $t = f(n)$ for $n$, where $f$
represents some of the given algorithmic time complexities.

<!--more-->

However, it turns out that one of equations, $t = n \lg n$, is not
that obvious to solve for $n$. This is because solving the equation
leads to the use of a function called the [Lambert $W$][lam] which
doesn't have neat closed mathematical form one could translate to
code in order to compute the values of $n$ for different durations
$t$. Some approximation method is needed instead, and since this is
a blog about computer science and we are interested in geeking out
with numerical values, we specifically want to have a numerical
approximation to Lambert $W$. Thanks research a neat numerical
approximation is known (Iacono & Boyd, 2022).

[lam]: mathworld.wolfram.com/LambertW-Function.html

Therefore, the solution to this problem is twofold:

1. Solve $t = n \lg n$ for $n$ with the help of Lambert $W$ and
2. use the numerical approximation to get estimates for the
   different values of $t$.

Here's how the solution goes. Solving

$$
    t = n \ln n
$$

can be started by first noticing that via the [change of basis][01]
(e.g. see Prime Newtons, 2023),

[01]:https://www.youtube.com/watch?v=mJwfpcXwYRU
[02]:https://www.youtube.com/watch?v=mJwfpcXwYRU

$$
    n \lg n = n \dfrac{\ln n}{\ln 2},
$$

so the original equation can then be expressed as

$$
    t = n \dfrac{\ln n}{\ln 2}.
$$

Multiplying both sides of the equation with $\ln 2$ leads to

$$
    n \ln n = t \ln 2.
$$

Because

$$
    \phantom{,} \ n = e^{\ln n} \ ,
$$

then

$$
    \begin{array}{r c l}
        \phantom{,} \ e^{\ln n} \ln e^{\ln n} = e^{\ln n} \ln n = \ln n e^{\ln n} \ ,
    \end{array}
$$

so

$$
    \ln n e^{\ln n} = t \ln 2.
$$

Applying the Lambert W for both sides means that

$$
    W(\ln n e^{\ln n}) = \ln n = W(t \ln 2)
$$

and [taking the exponent][02] (e.g., see Intellecta, 2021) from
both sides leads to solution

[02]:https://www.youtube.com/watch?v=hu8oXMFDNQk

$$
    \phantom{.} \ n = e^{W(t \ln 2)} \ . \tag{1}
$$

As stated in the beginning of this text, (Lambert) $W$ has a
compact numerical approximation (Iacono & Boyd, 2017) that can be
written in C++ as

```c++ {class = listing}
auto W(const double& t) -> double
// Compute the Lambert W approximation for t in [-exp(-1), +inf].
// For more info, see Iacono & Boyd (2017).
{
    if (t < -1.0 * std::exp(-1.0))
    {
        throw std::invalid_argument (
            "Computing only the upper primary branch of Lambert's W"
        );
    }

    double const y = std::sqrt(1.0 + std::exp(1.0) * t);
    double       w = -1.0 + 2.036 * std::log (
        (1.0 + 1.14956131 * y) / 1.0 + 0.45495740
    ) * log(1.0 + y);

    // Compute first three terms of the approximation.
    w = (w / (1.0 + w)) * (1.0 + std::log(t / w));
    w = (w / (1.0 + w)) * (1.0 + std::log(t / w));
    w = (w / (1.0 + w)) * (1.0 + std::log(t / w));

    return w;
}
```

which in turn can be used to model $(1)$ by writing

```c++ {class = listing}
auto e(const double& t) -> double
{
    return std::exp(W(t * std::log(2)));
}
```

Now, given this newly defined function `e`, the maximum input size
of $n$ can be evaluated for the different time durations and the
results are shown in the following table:

<div class = "widescreen">
    <div id = "resulttable_ws"></div>
</div>

<div id = "resulttable_ws"></div>

<div class = "smallscreen">
    <div id = "resulttable_ss"></div>
</div>

<div align = "center">
    Table 1: Maximum input size approximations.
</div>

<script>
evaluatetable();

function evaluatetable(str)
{
    const durations = {
        /* second  */ s   : 1000,
        /* minute  */ min : 60 * 1000,
        /* hour    */ h   : 60 * (60 * 1000),
        /* day     */ d   : 24 * (60 * (60 * 1000)),
        /* month   */ m   : 30 * (24 * (60 * (60 * 1000))),
        /* year    */ y   : 12 * (30 * (24 * (60 * (60 * 1000)))),
        /* century */ c   : 100 * (12 * (30 * (24 * (60 * (60 * 1000)))))
    };

    // Compute for widescreen.
    let res = `$$ \\small`
        + `\n` + `   \\begin{array}{ | l | c | c | c | c | c | c | c | } \\hline`
        + `\n` + `       ` + `\\text{Dur.}`;

    for (const i in durations)
    {
        res += ` & \\text{${i}}`;
    }

    res += ` \\\\` + ` ` + `\\hline` + `\n` + `       ` + `\\text{Result}`;

    for (const i in durations)
    {
        res += ` ` + `&` + ` ` + e(parseFloat(`${durations[i]}`)).toExponential(2);
    }

    res +=  ` ` + `\\\\ \\hline` + `\n` + `   \\end{array}`
         + `\n` + `$$`;

    document.getElementById("resulttable_ws").innerHTML = res;

    // Compute for smallscreen.
    res = `$$ \\small`
        + `\n` + `   \\begin{array}{ | c | r | } \\hline`
        + `\n` + `       \\text{Dur.} & \\text{Result}` + ` \\\\ \\hline`;

    for (const i in durations)
    {
        res += `\n` + `        ` + `\\text{${i}}` + ` & ` + e(parseFloat(`${durations[i]}`)).toExponential(2) + ` \\\\ \\hline`
    }

    res += ` ` + `\\hline` + `\n` + `   \\end{array}`
         + `\n` + `$$`;

    document.getElementById("resulttable_ss").innerHTML = res;
}

function e(t)
{
    return Math.exp(W(t * Math.log(2)));
}

function W(t)
{
    const y = Math.sqrt(1.0 + Math.exp(1.0) * t);
    let   w = -1.0 + 2.036 * Math.log (
        (1.0 + 1.14956131 * y) / 1.0 + 0.45495740
    ) * Math.log(1.0 + y);

    w = (w / (1.0 + w)) * (1.0 + Math.log(t / w));
    w = (w / (1.0 + w)) * (1.0 + Math.log(t / w));
    w = (w / (1.0 + w)) * (1.0 + Math.log(t / w));

    return w;
}
</script>

It can be seen from Table 1, that for example, in one second or in
one day, an algorithm with algorithmic complexity of $n \lg n$, the
possible maximum size of $n$ is around $140$ or $3.9$ million,
respectively.

### References

Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2022).
[_Introduction to algorithms_][press22]. MIT press.

[press22]:https://mitpress.mit.edu/9780262046305/introduction-to-algorithms/

Iacono, R., & Boyd, J. P. (2017). New approximations to the principal
real-valued branch of the Lambert W-function. _Advances in Computational
Mathematics_, 43(6), 1403-1436. [https://doi.org/10.1007/s10444-017-9530-3][iacono17]

[iacono17]:https://doi.org/10.1007/s10444-017-9530-3

Intellecta. (2021, April 17). _Using the LAMBERT W FUNCTION find ALL
solutions! / ( W_0 and W_-1)_ [Video]. YouTube.
[https://www.youtube.com/watch?v=hu8oXMFDNQk](https://www.youtube.com/watch?v=hu8oXMFDNQk)

Prime Newtons. (2023, October 11). _Lambert W Function_ [Video].
YouTube. [https://www.youtube.com/watch?v=mJwfpcXwYRU](https://www.youtube.com/watch?v=mJwfpcXwYRU)
