+++
title = 'Comparison of running times table'
date  = 2026-02-15T10:26:44+02:00
+++

### References

Iacono, R., & Boyd, J. P. (2017). New approximations to the principal
real-valued branch of the Lambert W-function. _Advances in Computational
Mathematics_, 43(6), 1403-1436. [https://doi.org/10.1007/s10444-017-9530-3][iacono17]

[iacono17]:https://doi.org/10.1007/s10444-017-9530-3

The first problem of the book by Cormen et al. (2022) is to
determine the largest input size ($n$) that can be solved in time
($t$), when the time complexity measured in milliseconds ($ms$), of
a function $t = f(n)$ is $\lg n$, $\sqrt{n}$, $n$, $n \lg n$,
$n^2$, $n^3$, $2^n$ or $n!$. In order to do this, the equation $t =
f(n)$ needs to be solved for each $n$ of the given time
complexities.

Starting from the first one: If $t$ $=$ $\lg n$, then re-writing
the equation in exponential form leads to $n$ $=$ $2^t$. When $t$
$=$ $\sqrt{n}$ squaring both sides leads to $n$ $=$ $t^2$. In $t$
$=$ $n$, it's obvious that $n$ $=$ $t$. The equation $t$ $=$ $n \lg
n$, does not seem to have a closed form solution, but a numerical
method for computing $n$ $=$ $f(t)$ exists (Iacono & Boyd, 2017).
The method is explained in [this][01] blog page. Solving $t$ $=$
$n^2$ for $n$, means taking the square root from both sides of the
equation and so $n$ $=$ $\sqrt{t}$. Similarly, taking the cube root
of both sides of the equation $t$ $=$ $n^3$ shows that $n$ $=$
$\sqrt[3]{t}$. Taking the base-2 logarithm from $t$ $=$ $2^n$,
leads to $\lg 2^n$ $=$ $n$ $=$ $\lg t$. The equation $t$ $=$ $n!$
.................

[01]:{{< ref "lambert-w-function/index.md">}}

$$
    \lg n = t
$$

<div class = "widescreen">
    <div id = "resulttable_ws"></div>
</div>

<div class = "smallscreen">
    <div id = "resulttable_ss"></div>
</div>

<div align = "center">
    Table 1: Maximum input size approximations.
</div>

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
    '2^n' : (n) => Math.pow(2, n),
    'n^2' : (n) => Math.pow(n, 2),
    'n'   : (n) => n,
    'W(n)' : (n) => e(n),
    '\\sqrt{n}' : (n) => Math.sqrt(n),
    '\\sqrt[3]{n}' : (n) => Math.cbrt(n)
};

const indnt = '    '; // Row indentation level

tbl.innerHTML = 
    '\\begin{array}{ | c | c | c | c | c | c | c | c | } \\hline' + '\n'
        + indnt // Row indentation
        + 'f(n) &'
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

    tbl.innerHTML += ' \\\\ ' + '\\hline' + ' ' + '\n';
}

tbl.innerHTML += '\\end{array}'

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
