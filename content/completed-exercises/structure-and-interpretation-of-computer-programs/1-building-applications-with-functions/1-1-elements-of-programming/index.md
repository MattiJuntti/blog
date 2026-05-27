+++
title  = "1.1 Elements of programming"
layout = "solution-single"
+++

<span class = "exnum">1</span> **(a)** The given expression `10;`
evaluates to `10;` **(b)** Since Javascript's `+` operator is
[_left associative_][01], the expression `5 + 5 + 4;` is evaluated
as `(5 + 5) + 4` $=$ `10 + 4` $=$ `14`. **(c)** The expression `9`
`-` `1;` evaluates to `8`. **(d)** Expression `6` `/` `2;`
evaluates to `3`. **(e)** Due to the parentheses having greater
priority in the order of eveluations in Javascript, the expression
`2` `*` `4` `+` `(4` `-` `6);` first evaluates to `` `2` `*` `4`
`+` `(-2)`, then to `2` `*` `4` `-` `2`, then to `(2` `*` `4)` `-`
`2`, then to `8` `-` `2` and finally to `6`. **(d)** Expression
`const` `a` `=` `3` evaluates to `undefined`, because this
expression is a [_declaration_][02], but the expression `a;`
evaluates to `3`. **(f)** The expression `const` `b` `=` `a + 1;`
is evaluated as `const` `b` `=` `(a + 1);` and evaluates to
`undefined` too, because this expression is also a declaration, but
the expression `b;` evaluates to `4`, because `b` is equal to `a +
1` `=` `(3 + 1)` that is equal to `4`. **(g)** Expression `a` `+`
`b` `+` `a` `*` `b;` is evaluated as `((a + b)` `+` `(a * b))`,
where the second term `(a * b)` is evaluated first, then the first
term `(a + b)` and then the sum of these two terms. **(h)**
Expression `a` `===` `b` is evaluated as `(a` `===` `b)`. **(i)**
According to [the operator precedence of Javascript expression][03]
`b` `>` `a` `&&` `b` `<` `a` `*` `b` `?` `b` `:` `a` is evaluated
as

```javascsript
    b > a && a < b * b ? b : a
    = ((b > a) && (a < (b * (b ? b : a)))).
```

**(i)** Expression `a` `===` `4;` is evaluated into a error if `a`
is not defined or either to `true` or `false` is `a` is a number.
**(j)** Expression `? 6;` evaluates to error because there is no
unary, binary nor ternary operations `?` in Javascript. **(k)**
Expression `:` `b` `===` `4;` could first evaluated as `:` `(b ===
4)`, but since the left handside of the `?:` operator is missing
and operand, the whole evaluates to an error. **(l)** Same goes for
the expression `?` `6` `+` `7` `+` `a;`, the left hand-side operand
is missing, so the expression leads to an evaluation error. **(m)**
Expression `2` `+` `(b` `>` `a` `?` `b` `:` `a);` is evaluated as

```javascsript
    (2 + (b > (a ? b : a))).
```

**(n)** The expression

```javascsript
    (a > b
     ? a
     : a < b
     ? b
     : -1
    )
    *
    (a + 1);
```

can be written as

```javascsript
    (a > b ? a : a < b ? b : -1) * (a + 1);
```

and is evaluated as

```javascsript
    (((a > b) ? a : ((a < b) ? b : -1)) * (a + 1)).
```

[01]:https://en.wikipedia.org/wiki/Operator_associativity
[02]:developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements#difference_between_statements_and_declarations
[03]:https://www.w3schools.com/js/js_precedence.asp

<span class = "exnum">2</span> The given expression

$$
    \frac{(5 + 4 + (2 - (3 - (6 + \frac{4}{5}))))}{3(6 - 2)(2 - 7)}
$$

can be translated into Javascript by writing:

```javascsript
    (5 + 4 + (2 - (3 - (6 + (4 / 5)))))
        / 3 * (6 - 2) * (2 - 7)
```

<span class = "exnum">3</span>

...

<span class = "exnum">4</span> If

```javascript
function plus(a,b)
{
    return a + b;
}
```

and

```javascript
function minus(a,b)
{
    return a - b;
}
```

then the function

```javascript
function a_plus_abs_b(a,b)
{
    return (b >= 0 ? plus : minus)(a,b);
}
```

is evaluated by first checking the condition `(b >= 0)`. On `true`
or `false`, either `plus` or `minus` is returned, that is, the
grouping `(b` `>=` `0` `?` `plus` `:` `minus)` is resolved. This
results in a function call to `plus` or `minus` to which the set of
arguments group `(a,b)` are used. The first group is grouping
resolution and the second a function call of `plus` or `minus`.
