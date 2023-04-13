---
title: "9.5.1: Interval of convergence"
description: "This reference sheet covers calculating intervals of convergence on power series."
---

# Finding the interval of convergence

All power series have a radius of convergence, denoted by $R$. This radius helps us determine the intervals of convergence.

| $R$        | Conditions of convergence           |
| ---------- | ----------------------------------- |
| $R=0$      | The series converges only for $x=a$ |
| $R=\infty$ | The series converges for all $x$    |

There is a positive radius of convergence such that the series converges for $|x-a|<R$ and diverges for $|x-a|>R$

This leads us to the definition of the interval of convergence:

The interval of convergence is the interval between $a-R$ and $a+R$ and it includes any endpoint where the series converges.

There are certain series whose radii of convergence are known:

| Series                                 | Converges for | Diverges for | Radius of convergence |
| -------------------------------------- | ------------- | ------------ | --------------------- |
| $1+x+x^2+\cdots$                       | $\|x\|<1$     | $\|x\|>1$    | $1$                   |
| $1+\frac{x}{3}+(\frac{x}{3})^2+\cdots$ | $\|x/3\|<1$   | $\|x/3\|>1$  | $3$                   |

We can use `theorem 9.10` to calculate the radius of convergence for a power series. We can use the ratio test to find the values of $x$ for which a power series converges. If we use the series

$\sum\limits_{n=0}^\infin C_n(x-a)^n$

which can be re-written as

$a_n=C_n(x-a)^n$

If we assume $C_n\neq0$ and $x\neq a$, we can use limits:

$\lim\limits_{n\to\infin}\frac{|a_{n+1}|}{|a_n|} = \lim\limits_{n\to\infin}\frac{|C_{n+1}(x-a)^{n+1}|}{|C_n(x-a)^n|}=\lim\limits_{n\to\infin}\frac{|C_{n+1}||x-a|}{|C_n|}=|x-a|\lim\limits_{n\to\infin}\frac{|C_{n+1}|}{C_n}$

<!-- prettier-ignore -->
| Case | Limit | Meaning |
|------|-------|---------|
| 1 | $\lim\limits_{n\to\infin}\frac{\|a\_{n+1}\|}{\|a\_n\|}=\infin$ | The power series converges for only $x=a$, with a radius of $0$ |
| 2 | $\lim\limits_{n\to\infin}\frac{\|a\_{n+1}\|}{\|a\_n\|}=0$ | The power series converges for all $x$, with a radius of $\infin$ |

## Method for computing the radius of convergence `Theorem 9.10`

To calculate the radius of convergence, $R$, for a power series

$\sum\limits_{n=0}^\infin C_n(x-a)^n$

we can use the ratio test by setting $a_n=C_n(x-a)^n$ the applying the following rules

- If $\lim\limits_{n\to\infin}|a_{n+1}|/|a_n|$ is infinite, then the radius is $0$.
- If $\lim\limits_{n\to\infin}|a_{n+1}|/|a_n|$ is $0$, then the radius is $\infin$.
- If $\lim\limits_{n\to\infin}|a_{n+1}|/|a_n| = K|x-a|$, where K is finite and not $0$, then the radius is $1/K$.

---

If $\lim\limits_{n\to\infin}|a_{n+1}|/|a_n|$ fails to exist, the ratio test is inconclusive and does not tell us anything about the convergence of the series. This can occur when some of the $C_n$ terms are $0$.

If we are asked to prove that the power series converges for all $x$

$1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\cdots+\frac{x^n}{n!}$

Our first step is to verify that the ratio test will actually work by verifying none of our terms will evaluate to $0$, or in this case $C_n=1/n!$. Because none of our terms are in this form, we can use the ratio test.

$\lim\limits_{n\to\infin}\frac{|a_{n+1}|}{|a_n|}=|x|\lim\limits_{n\to\infin}\frac{|C_{n+1}|}{|C_n|}=|x|\lim\limits_{n\to\infin}\frac{1/(n+1)!}{1/n!}=|x|\lim\limits_{n\to\infin}\frac{n!}{(n+1)!}=|x|\lim\limits_{n\to\infin}\frac{1}{n+1}=0$

This will result in $R=\infin$, meaning that the series will converge for all x.

And if we are asked to determine the radius of convergence for a series

$\frac{x-1}{3}-\frac{(x-1)^2}{2\times3^2}+\frac{(x-1)^3}{3\times3^3}-\frac{(x-1)^4}{4\times3^4}+\cdots+(-1)^{n-1}\frac{(x-1)^n}{n\times3^n}+\cdots$

Because $C_n=(-1)^{n-1}/(n\times3^n)$ can never be $0$, we can use the ratio test

<!-- prettier-ignore -->
$
\lim\limits_{n\to\infin}\frac{|a_{n+1}|}{|a_n|}=
|x-1|\lim\limits_{n\to\infin}\frac{|C_{n+1}|}{|C_n|}=
|x-1|\lim\limits_{n\to\infin}\frac{|\frac{(-1)^n}{(n+1)3^{n+1}}|}{|\frac{(-1)^{n-1}}{n3^n}|}=
|x-1|\lim\limits_{n\to\infin}\frac{n}{3(n+1)}=
\frac{|x-1|}{3}
$

Thus, the $K$ is $1/3$ by `theorem 9.10`, leading us to compute the radius as $\frac{R=1}{K=3}$, so we can say that the series converges for $|x-1|<3$ and diverges for $|x-1|>3$. After evaluating the inequalities, we can say that the series converges for $-2\lt x\lt 4$

## Endpoints of Interval of Convergence

The ratio test tells us the interval of convergence, but tells us nothing about the behavior of the endpoints of the interval. Unfortunately, there is not a theorem that can answer this question, but we can use some of the tests in sections 9.3 and 9.4 to learn more about the endpoints.

If we are asked to determine the interval of convergence for a series

$\frac{(x-1)}{3}-
\frac{(x-1)^2}{2\times^2}+
\frac{(x-1)^3}{3\times^3}-
\frac{(x-1)^2}{4\times^4}+
\cdots+
(-1)^{n-1}\frac{(x-1)^n}{n\times^n}+\cdots$

This should not look familiar as we have already examined this series.

We have already determined that this series has a radius of 3 and converges from $-2\lt x\lt 4$. and diverges for $x\lt -2$ and $x\gt 4$. However, we do not know what happens at $x=-2$ and $x=4$.

We can use a harmonic series to examine the behavior of the endpoints

$1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}-\cdots$

This is an alternating series, so by the alternating series test, we know that it converges. We can apply this to our series by centering it at $x=-2$ we get the series

$-1-\frac{1}{2}-\frac{1}{3}-\frac{1}{4}-\frac{1}{5}-\cdots$

Because this is a negative harmonic series, it diverges. Therefore, we can say that the series diverges at $x=-2$. By doing the same thing centered at $x=4$, we can say that the series converges at $x=4$, meaning the right endpoint is included and the left endpoint is not included.

## All odd or all even terms

The ratio test requires $\lim\limits_{n\to\infin}\frac{|a_{n+1}|}{|a_n|}$ to be defined for $a_n=C_n(x-a)^n$ but if the power series has only even or odd powers, some coefficients of $C_n$ will be $0$ and the ratio test cannot work. To solve this, we can take advantage of the flexibility of series and rewrite the series in a way that the ratio test can work (where the terms are not 0).

For example, if we are instructed to find the radius and interval of convergence for the series

$1+2^2x^2+2^4x^4+2^6x^6+\cdots$

By saying that the series cannot exist when odd, we mean that the series does not exist as written when $n$ is odd, or that the term $2^3x^3$ does not exist. To defeat this, we can rewrite it as a series that _can_ accept odd terms

We can make every $n$ term even by multiplying it by $2$, so we can rewrite our general terms as

$a_n=2^{2n}x^{2n}$

Then finally by applying our formula, we will replace $n$ with $n+1$ to get

$a_{n+1}=2^{2(n+1)}x^{2(n+1)}$

We can now use the ratio test to determine the radius and interval of convergence

$\frac{|a\_{n+1}|}{|a_n|}=
\frac{2^{2(n+2)}x^{2(n+2)}}{2^{2n}x^{2n}}=
|{2^2x^2}|=4x^2$

The ratio test shows that the series converges if $|x|<\frac{1}{2}$ ($4x^2\lt 1$). This means the radius of convergence is $\frac{1}{2}$ and the interval of convergence is $-1/2\lt x\lt 1.2$. We can use theorem 9.2 to test the convergence at endpoints, and can see that both endpoints are 1, so the series diverges.
