---
title: "9.5.0: Power series"
description: "This reference sheet covers using the power series to calculate the interval of convergence."
weight: 2
---

# Comparison of series

> This reference sheet covers using the power series to calculate the interval of convergence.

## Introduction

A power series about $x=a$ is a sum of constants times powers of $x-a$.

$C_0+C_1(x-a)+C_2(x-a)^2+\cdots+C_n(x-a)^n+\cdots$

This can all be rewritten as a summation

$\sum\limits_{n=0}^\infin C_n(x-a)^n$

To investigate the convergence of a power series, we start with partial sums

$S_n(x), S_1(x), S_2(x), \cdots$

Recall that for a fixed value of $x$, if the partial sums converges to a limit S, then the power series converges to $S$ for this value of $x$.

It is important to note that power series may converge for some values of $x$ and diverge for other values of $x$.

## Example: Finding general terms

If we are asked to find an expression for the general term in summation notation of the power series

$\frac{(x-2)^4}{4}-\frac{(x-2)^6}{9}+\frac{(x-2)^8}{16}-\frac{(x-2)^10}{25}+\cdots$

By the general form introduced in the introduction, we can find out that the series is about $x=2$. We can also recognize that the exponent is increasing by 2 each time and is thus $2n$, and the denominator is doubling each time and is thus $2^n$, allowing us to write the series as a summation:

$\sum\limits_{n=2}^\infin \frac{(x-2)^{2n}}{2^n}$

This is close, but the series we are given alternates between positive and negative terms. We can fix this by multiplying each term by $(-1)^n$.

$\sum\limits_{n=2}^\infin \frac{(-1)^n(x-2)^{2n}}{2^n}$

## Example: Finding convergence or divergence at a point

If we are given a power series defined by the following expression

$\sum\limits_{n=0}^\infin \frac{x^n}{2^n}$

We are asked to determine whether the series converges or diverges at $x=-1$ and $x=3$.

We will start with $x=-1$. The first step is to substitute $x=-1$ into the series. We get

$\sum\limits_{n=0}^\infin \frac{(-1)^n}{2^n}=\sum\limits_{n=0}^\infin (-\frac{1}{2})^n$

By the definition of a geometric series and the formula for the `Sum of an infinite geometric series`, we know the ratio of the series ($-1/2$), and thus it converges to

$\frac{1}{1-(-\frac{1}{2})}=\frac{2}{3}$

The next step is to substitute $x=3$ into the series. We get

$\sum\limits_{n=0}^\infin \frac{3^n}{2^n}=\sum\limits_{n=0}^\infin (\frac{3}{2})^n$

We can see the ratio of the series is $\frac{3}{2}$, and thus it diverges because the absolute value of the ratio is greater than 1.
