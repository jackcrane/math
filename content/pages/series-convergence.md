---
title: "9.3.0: Convergence of series"
description: "This reference sheet covers more methods to predict and compute the convergence of series."
weight: 2
---

# Convergence of series

> This reference sheet covers more methods to predict and compute the convergence of series.

## Introduction

In 9.2.0, we explored geometric series in general. In 9.2.1, we explored using geometric series to analyze savings and investments. In this reference sheet, we will explore more methods to predict and compute the convergence of series.

If we have a series in which each term is a number defined by $a_n$, the series of sums can be written as

$a_1+a_2+a_3+\cdots+a_n+\cdots$

This works great for small sequences but we can use more advanced notation to better understand and depict the behavior of the series same series

$\sum\limits_{n=1}^\infin a_n$

## Partial sums and convergence of series

The partial sum of a sequence is denoted by $S_n$ and is defined as the sum of the first $n$ terms of the sequence

$\sum\limits_{n=1}^n a_n$

We can use a sequence of partial sums to determine the convergence of the series. If $S_n$ has a limit as $n\to\infin$, then we can define the sum of the series to be that limit. If the limit does not exist, the series is said to diverge.

If we are asked to investigate the convergence of a series with $a_n=1/(n(n+1))$, the first step is to write out the summation and and broken sums to help visualize the task at hand.

$\sum\limits_{n=1}^\infin \frac{1}{n(n+1)}=\frac{1}{2}+\frac{1}{6}+\frac{1}{12}+\frac{1}{20}+\cdots$

The next step is to build partial sums. We do this by adding the previous terms (or partial sum) to the current:

$S_1=1/2$

$S_2=\frac{1}{2}+\frac{1}{6}=\frac{2}{3}$

$S_3=\frac{1}{2}+\frac{1}{6}+\frac{1}{12}=\frac{3}{4}$

$S_4=\frac{1}{2}+\frac{1}{6}+\frac{1}{12}+\frac{1}{20}=\frac{4}{5}$

If we take a step back from the math and just try and recognize patterns, we can tell that the numerators seem to be evaluating to $n$, and the denominators seem to be evaluating to $n+1$. Thus the sequence of partial sums has the formula $S_n=\frac{n}{n+1}$, which we can see converges to 1, meaning that the series also converges to 1.

## Series and Integrals

Just like how in previous units we have been able to convert summations to integrals, we can also use the integral to investigate the convergence of some series. If we use the harmonic series as an example, we can write the series as

$\sum\limits_{n=1}^\infin \frac{1}{n}=1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\cdots$

We can convert this to an integral by using the substitution $x=n$ and $dx=1$ to get

$\int\limits_1^\infin \frac{dx}{x}=1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\cdots$

Using integrals to evaluate series allows us to use the _integral test_ to determine if a series converges or diverges.

## Integral test

Suppose $a_n=f(x)$, where $f(x)$ is decreasing and positive.

- If $\int\limits_1^\infin f(x)dx$ converges, then the series $\sum\limits_{n=1}^\infin a_n$ converges.
- If $\int\limits_1^\infin f(x)dx$ diverges, then the series $\sum\limits_{n=1}^\infin a_n$ diverges.

## The P-series test

We are often asked to determine the values of $p$ that will allow a series to converge. We can use the P-series test to determine this.

The p-series $\sum\limits_{n=1}^\infin \frac{1}{n^p}$ converges if $p>1$ and diverges if $p\leq1$.
