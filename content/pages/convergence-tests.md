---
title: "9.4.0: Convergence Tests"
description: "This reference sheet covers comparing two series to predict convergence."
---

# Comparison of series

> This reference sheet covers comparing two series to predict convergence.

We can use comparison tests to compare two series and predict convergence.

## Comparison test `Theorem 9.4`

Suppose $0\leq a_n\leq b_n$ for all $n$ beyond a certain value.

- If $\sum{b_n}$ converges, then $\sum{a_n}$ converges
- If $\sum{b_n}$ diverges, then $\sum{a_n}$ diverges

We are asked to compute if the series converges

$\sum\limits_{n=1}^\infin \frac{1}{n^3+1}$

When $n\geq 1$, we know that $n^3+1\geq 1$ and $n^3+1\geq n^3$. Thus, we can use the comparison test to determine if the series converges.

$0\leq \frac{1}{n^3+1}\leq \frac{1}{n^3}$

By that statement, we know that every term in the series of $\sum{\frac{1}{n^3+1}}$ is less than or equal to every term in the series of $\sum{\frac{1}{n^3}}$. Since we know that $\sum{\frac{1}{n^3}}$ converges by the p-series test, we can conclude that $\sum{\frac{1}{n^3+1}}$ also converges.

## Limit comparison test `Theorem 9.5`

The comparison test uses the relationship between the terms of two series, $a_n$ and $b_n$, to determine if the series converges. The limit comparison test uses the relationship between the terms of a series and the limit of the series as they approach infinity to determine if the series converges.

If we are asked to predict the convergence of

$\sum{\frac{n^2-5}{n^3+n+2}}$

The first step is to observe how as $n\to\infin$, the highest-power terms in the numerator $n^2$ and denominator $n^3$ dominate the function, and thus the entire function can be rewritten as

$\frac{n^2}{n^3}=\frac{1}{n}$

And since we already know that the harmonic series diverges, we can make a reasonable guess that the series $\sum{\frac{n^2-5}{n^3+n+2}}$ also diverges. However, we are not able to know for 100% certainty because the inequality is not in the right direction

$\frac{n^2-5}{n^3+n+2}\leq \frac{1}{n}$

Thus, we can use the limit comparison test to determine if the series converges.

**Limit comparison test**

Suppose $a_n>0$ and $b_n>0$ for all $n$. If

$\lim\limits_{n\to\infin} \frac{a_n}{b_n} = c$

where $c>0$, then the two series $\sum{a_n}$ and $\sum{b_n}$ either both converge or diverge.

## Series of both positive and negative terms `Theorem 9.6`

If we are asked to predict the convergence of a series with both positive and negative terms, the total area of the rectangles is no longer simply equal to $\sum{a_n}$. That said, it is still true that if the total area of the rectangles is finite, the series converges. Thus, we get

**Convergence of Absolute Values Implies Convergence**

If $\sum{|a_n|}$ converges, then so does $\sum{a_n}$.

## The ratio test `Theorem 9.7`

The idea of a geometric series is the ratio of a term to its next term:

$\frac{a_{n+1}}{a_n}$

Where the ratio is a constant for all $n$. The ratio test uses this idea to determine if a series converges.

**Ratio test**

For a series $\sum{a_n}$, suppose the sequence of ratios $|a_{n+1}/a_n|$ has a limit:

$\lim\limits_{n\to\infin} |a_{n+1}|/|a_n| = L$

- If $L<1$, then $\sum{a_n}$ converges
- If $L>1$ or $L=\infin$, then $\sum{a_n}$ diverges
- If $L=1$, the test does not tell us anything about the convergence of the series

## Alternating series test `Theorem 9.8`

A series is called an alternating series if the terms alternate in sign

$\sum\limits_{n=1}^\infin \frac{(-1)^{n-1}}{n}$

$=1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}-\frac{1}{6}+\cdots$

We can use the alternating series test to determine if the series converges.

**Alternating series test**

An alternating series of the form

$\sum\limits_{n=1}^\infin (-1)^{n-1}a_n=a_1-a_2+a_3-a_4+\cdots$

converges if

$0 \lt a_{n+1} \lt a_n$ for all $n$. and $\lim\limits_{n\to\infin} a_n = 0$

## Absolute and conditional convergence

We say that a series $\sum{a_n}$ is

- Absolutely convergent if $\sum{a_n}$ and $\sum{|a_n|}$ both converge
- Conditionally convergent if $\sum{a_n}$ converges but $\sum{|a_n|}$ diverges
