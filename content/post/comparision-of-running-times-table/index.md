+++
title = 'Comparison of running times'
date  = 2026-10-13T15:26:04+03:00
+++

The first problem of the book by Cormen et al. (2022) is to
determine the largest input size ($n$) that can be solved in a
given amount time ($t$) when the time complexity measured in
milliseconds ($ms$) of a function $t = f(n)$, where the given
functions $f$ are $\lg n$, $\sqrt{n}$, $n$, $n \lg n$, $n^2$,
$n^3$, $2^n$ and $n!$. Hence, to solve the problem, all the $n$s
need to be solved with respect to $t$ in each of these functions.

<!--excerpt-->

It can be the case that the functions $t$ $=$ $n \lg n$ and $t$ $=$
$n!$ aren't immediately obvious to solve algebraically.  However,
the solution to the former equation is known as [Lambert's $W$][02]
and it has a numerical approximation (Iacono & Boyd, 2017) that can
be used in solving the given problem. It's explained in another
[page][01] of this blog. The solution for the $n$ in $t$ $=$ $n!$
is left to some future post. Otherwise, solving the functions for
$n$ is pretty trivial:

1. If $t$ $=$ $\lg n$, then re-writing the equation in exponential form leads to $n$ $=$ $2^t$.
2. When $t$ $=$ $\sqrt{n}$, squaring both sides leads to $n$ $=$ $t^2$.
3. In $t$ $=$ $n$, it's obvious that $n$ $=$ $t$.
4. Equation $t$ $=$ $n \lg n$ leads to $n$ $=$ $e^{W(t \ln 2)}$, where $W$ can be [approximated numerically][01].
5. Solving $t$ $=$ $n^2$ for $n$, is solved by taking square root from both values, so $n$ $=$ $\sqrt{t}$.
6. Taking the cube root of both sides of the equation $t$ $=$ $n^3$ shows that $n$ $=$ $\sqrt[3]{t}$.
7. The base-2 logarithm from $t$ $=$ $2^n$, leads to $\lg 2^n$ $=$ $n$ $=$ $\lg t$.

Now given these solutions, it's possible to construct a results
table where a row displays for the approximated input size with
respect to each given time budget laid out as columns of the Table
1.

<div align = "center" style = "margin: 8px 0 -16px 0;">
    Table 1: Maximum input size approximations.
</div>

<div class = "widescreen">
    <div id = "resulttable_ws"></div>
</div>

<div class = "smallscreen">
    <div id = "resulttable_ss"></div>
</div>

So as an example, if some $O(n^2)$ or $O(n^3)$ algorithms are given
a minute worth of computing time, it can be seen from the Table 1,
that the maximum number of input size $n$ that these algorithms can
process are modest $245$ and $39$, respectively. But on the other
hand, if some algorithm has sublinear algorithmic complexity of
$O(\lg n)$ then it can process $3,$$600,$$000,$$000$ inputs, that
is, around thirty and a half billion inputs in one minute.

Though it's a good thing to be mindful that these values are
indicative approximations, not actual measurements.

<!-- Links -->
[01]:{{< ref "lambert-w-function/index.md">}}
[02]:https://mathworld.wolfram.com/LambertW-Function.html

### References

Cormen, T. H., Leiserson, C. E., Rivest, R. L., & Stein, C. (2022).
Introduction to algorithms (4th ed.). MIT Press.

Iacono, R., & Boyd, J. P. (2017). New approximations to the principal
real-valued branch of the Lambert W-function. _Advances in Computational
Mathematics_, 43(6), 1403-1436. [https://doi.org/10.1007/s10444-017-9530-3][iacono17]

### AI tool usage disclaimer

No AI tools were used in writing this text or solving the problem.

<script>
tbl = document.getElementById("resulttable_ws");

const durations = [
    /* second  */ 1000,
    /* minute  */  60 * 1000,
    /* hour    */  60 * (60 * 1000),
    /* day     */  24 * (60 * (60 * 1000)),
    /* month   */  30 * (24 * (60 * (60 * 1000))),
    /* year    */  12 * (30 * (24 * (60 * (60 * 1000)))),
    /* century */ 100 * (12 * (30 * (24 * (60 * (60 * 1000)))))
];

const functions = {
    '2^t'          : (t) => Math.pow(2, t),
    't^2'          : (t) => Math.pow(t, 2),
    't'            : (t) => t,
    'W(t)'         : (t) => e(t),
    '\\sqrt{t}'    : (t) => Math.sqrt(t),
    '\\sqrt[3]{t}' : (t) => Math.cbrt(t)
};

const indnt = '    '; // Row indentation level

tbl.innerHTML = 
    '\\begin{array}{ | l | l | l | l | l | l | l | l | } \\hline' + '\n'
        + indnt // Row indentation
        + 'n &'
        + ' 1 \\ \\text{s} &'
        + ' 1 \\ \\text{min} &'
        + ' 1 \\ \\text{h} &'
        + ' 1 \\ \\text{d} &'
        + ' 1 \\ \\text{m} &'
        + ' 1 \\ \\text{y} &'
        + ' 1 \\ \\text{c}'
        + ' \\\\ ' + '\\hline' + '\n';

for (const [name, f] of Object.entries(functions)) {
    tbl.innerHTML += indnt + name;

    for (const t of durations) {
        let n = Number.parseFloat(f(t)).toExponential(2)
        if (n == 'Infinity') { n = '\\infty'; }
        tbl.innerHTML += ' & ' + '\\small{' + n + '}';
    }

    tbl.innerHTML += ' \\\\ ' + ' ' + '\n';
}

tbl.innerHTML += '\\hline' + '\n' + '\\end{array}'

function e(x)
{
    return Math.exp(W(x * Math.log(2)));
}

function W(x)
{
    const y = Math.sqrt(1.0 + Math.exp(1.0) * x);
    let   w = -1.0 + 2.036 * Math.log (
        (1.0 + 1.14956131 * y) / 1.0 + 0.45495740
    ) * Math.log(1.0 + y);

    w = (w / (1.0 + w)) * (1.0 + Math.log(x / w));
    w = (w / (1.0 + w)) * (1.0 + Math.log(x / w));
    w = (w / (1.0 + w)) * (1.0 + Math.log(x / w));

    return w;
}

function W2(x)
{
    return 1.45869 * Math.log (
        (1.2 * x) / Math.log((2.4 * x) / (Math.log(1.0 + 2.4 * x)))
    ) - 0.45869 * Math.log( 
        (2.0 * x) / (Math.log(1.0 + 2.0 * x))
    );
}

// ---------

tbl = document.getElementById("resulttable_ss");

tbl.innerHTML = 
    '\\begin{array}{ | c | c | c | c | c | c | c | } \\hline' + '\n'
        + indnt // Row indentation
        + 'f(t) &'
        + ' 1 \\ \\text{s} &'
        + ' 1 \\ \\text{min} &'
        + ' 1 \\ \\text{h} &'
        + ' 1 \\ \\text{d} &'
        + ' 1 \\ \\text{m} &'
        + ' 1 \\ \\text{y} &'
        + ' 1 \\ \\text{c}'
        + ' \\\\ ' + '\\hline' + '\n';

for (const [name, f] of Object.entries(functions)) {
    tbl.innerHTML += indnt + name;

    for (const t of durations) {
        tbl.innerHTML += ' & ' + '\\small{'
            + Number.parseFloat(f(t)).toExponential(2)
        + '}';
    }

    tbl.innerHTML += ' \\\\ ' + ' ' + '\n';
}

console.log(tbl.innerHTML)

tbl.innerHTML += '\\hline' + '\n' + '\\end{array}'

function e(x)
{
    return Math.exp(W(x * Math.log(2)));
}

function W(x)
{
    const y = Math.sqrt(1.0 + Math.exp(1.0) * x);
    let   w = -1.0 + 2.036 * Math.log (
        (1.0 + 1.14956131 * y) / 1.0 + 0.45495740
    ) * Math.log(1.0 + y);

    w = (w / (1.0 + w)) * (1.0 + Math.log(x / w));
    w = (w / (1.0 + w)) * (1.0 + Math.log(x / w));
    w = (w / (1.0 + w)) * (1.0 + Math.log(x / w));

    return w;
}

function W2(x)
{
    return 1.45869 * Math.log (
        (1.2 * x) / Math.log((2.4 * x) / (Math.log(1.0 + 2.4 * x)))
    ) - 0.45869 * Math.log( 
        (2.0 * x) / (Math.log(1.0 + 2.0 * x))
    );
}
</script>
