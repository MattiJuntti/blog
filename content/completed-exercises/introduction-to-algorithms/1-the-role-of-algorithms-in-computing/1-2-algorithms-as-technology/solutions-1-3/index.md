+++
title  = "Problems 1-3"
date   = 2025-09-06T15:37:52+03:00
layout = "solution-single"
+++

<span class = "exnum">1</span> At the end of the day, all software
applications are &ldquo;algorithmic&rdquo; or &ldquo;require
algorithmic content&rdquo; because all information processing done
at computer is ran by more or less well defined algorithms, i.e. by
a routine that terminates with a correct output.

<span class = "exnum">2</span> Given an algorithm $A$ that executes
in $8n^2$ steps and an algorithm $B$ that executes in $64 n \lg n$
steps, the value on $n$ for which algorithm $B$ executes faster
than $A$ can be modeled by the inequality

$$
    8n^2 < 64n \lg n.
$$

Before trying to solve the inequality, it's good to notice that the
inequality can be factored by dividing both sides by $8n$, so the
inequality becomes

$$
    n < 8 \lg n. \tag{1}
$$

One way to figure out a proper value for $n$, for which the
inequality $(1)$ no longer holds, that is, when $B$ becomes faster
than $A$, is to solve the problem numerically and write a computer
program that outputs the value of $n$, when $(1)$ is no longer
true. Such a program is one that executes the following function,

```c++ {class = listing}
void f() {
    for (double n = 2.0; n > 0.0; n += 1.0) {
        if (n >= 8.0 * std::log2(n)) {
            std::println("n = {}", n);
            n = -1.0;
        }
    }
}
```

Since input of size $n = 1$ is already sorted, no sorting is
needed, so solving the inequality $(1)$ starts assuming with $n =
2$ &mdash; See line `2` of the above code. [Running][1] the
function $f$ as part of a program shows that when $n = 44$, the
algorithm $B$ outperforms algorithm $A$, because then

[1]:https://godbolt.org/z/csqzaY55M

$$
    44 < 8 \lg 44 = 43.675 \ldots ,
$$

that is the inequality no longer holds. If $n = 43$, the inequality
$(1)$ becomes

$$
    43 < 8 \lg 43 = 43.410\cdots ,
$$

which is the last value of $n$, when algorithm $A$ performs better
than $B$.

<span class = "exnum">3</span> Similarly as in the previous
solution, the running time relation of the two algorithms $A$ and
$B$ can be modeled by the inequality

$$
    2^n < 100n^2, \tag{2}
$$

where $n$ is the input size. The inequality can be solved
numerically by modifying the code of <span class =
"exnum">2</span>, by changing the line `3` from

```c++
if (n >= 8.0 * std::log2(n)) {
```

to

```c++
if (std::pow(2,n) >= 100.0 * std::pow(n,2)) {
```

which leads to function

```c++ {class = listing}
void f() {
    for (double n = 2.0; n > 0.0; n += 1.0)) {
        if (std::pow(2,n) >= 100.0 * std::pow(n,2) {
            std::println("n = {}", n);
            n = -1.0;
        }
    }
}
```

[Running][2] a program that calls `f` shows that when $n = 15$ in
$(2)$, the inequality no longer holds. Substituting this value of
$n$ to the inequality shows that,

[2]:https://godbolt.org/z/8oz9MdcbP

$$
    2^{15} = 32768 < 100 (15^2) = 22500
$$

which is false, but when $n = 14$ in $(2)$

$$
    2^{14} = 16384 < 100 (14^2) = 19600
$$

the inequality $(2)$ is true, so $n = 14$ is the smallest for which
the a algorithm $A$ executes faster than $B$. When $n > 15$,
algorithm $B$ performs faster.
