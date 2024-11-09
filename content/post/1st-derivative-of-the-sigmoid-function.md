+++
title = '1st Derivative of the Sigmoid Function'
date = 2024-11-09T15:41:54+02:00
+++

In neural networks a **activation function** is a function that
defines a threshold that makes a node of a neural network to
activate. One example of a such activation function is the
**sigmoid function**

$$
    \sigma(x) = \dfrac{1}{1 + e^{-x}}.
$$

<div align = "right">
    (Aggarwal, 2023; Rojas, 1996).
</div>

When training a neural network, activation function's derivative is
needed, but what it is for the sigmoid function?

<!--more-->

Given the derivative

$$
    \dfrac{d}{dx} \sigma(x) = \dfrac{d}{dx} \dfrac{1}{1 + e^{-x}}, \tag{1}.
$$

it can be obvious that applying the **quotient rule** of
derivatives (E.g. see Grossman, 1986), i.e. for a given two
functions $f : \mathbb{R} \rightarrow \mathbb{R}$ and $g :
\mathbb{R} \rightarrow \mathbb{R}$

$$
    \dfrac{d}{dx}\left( \dfrac{f}{g} \right)
        = \dfrac{g(x)(df/dx) - f(x)(dg/dx)}{g^2(x)}
$$

to $(1)$. Letting $f(x) = 1$ and $g(x) = 1 + e^{-x}$ the quotient
rule can be written

<widescreen>
$$
    \dfrac{d}{dx} \sigma(x) = \dfrac{ (1 + e^{-x})\left( \dfrac{d}{dx}1 \right) - (1)\left( \dfrac{d}{dx} 1 + e^{-x} \right) }{(1 + e^{-x})^2}. \tag{2}
$$
</widescreen>

Because

$$
    \dfrac{d}{dx} 1 = 0
$$

and

<widescreen>
$$
    \dfrac{d}{dx} 1 + e^{-x} = \dfrac{d}{dx} 1 + \dfrac{d}{dx} e^{-x} = 0 - e^{-x} = -e^{-x} \ ,
$$
</widescreen>

the nominator of $(2)$ can be written as

<widescreen>
$$
    \dfrac{d}{dx} \sigma(x) = \dfrac{e^{-x}}{(1 + e^{-x})^2}.
$$
</widescreen>

Continuing from the previous expression, next steps are then
applying common algebraic transformations as follows;

<widescreen>
$$
    \begin{array}{r c l}
        \dfrac{d}{dx} \sigma(x)
            & = & \dfrac{0 + e^{-x}}{(1 + e^{-x})^2} \\[1em]
            & = & \dfrac{(1 - 1) + e^{-x}}{(1 + e^{-x})^2} \\[1em]
            & = & \dfrac{1 + e^{-x}}{(1 + e^{-x})^2} - \dfrac{1}{(1 + e^{-x})^2} \\[1em]
            & = & \dfrac{1}{1 + e^{-x}} - \dfrac{1}{(1 + e^{-x})^2} \\[1em]
            & = & \dfrac{1}{(1 + e^{-x})} \left( 1 - \dfrac{1}{1 + e^{-x}} \right) \ ,
    \end{array}
$$
</widescreen>

and because

<widescreen>
$$
    \dfrac{1}{(1 + e^{-x})} = \sigma(x) \ ,
$$
</widescreen>

the next to last step shows that

$$
    \dfrac{d}{dx} \sigma(x) = \dfrac{1}{(1 + e^{-x})} \left( 1 - \dfrac{1}{1 + e^{-x}} \right) = \sigma(x)(1 - \sigma(x))
$$

<div align = "right">
    $\square$
</div>

### References

Aggarwal, C. C. (2023). Neural Networks and Deep Learning - A Textbook. 2nd ed.
<br>
Grossman, S. I. (1986). Calculus of One Variable. 2nd ed.
<br>
Rojas, R. (1996). Neural Networks - A Systematic Introduction. Springer.
