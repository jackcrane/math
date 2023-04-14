---
title: Formulas
description: This page contains a list of all the formulas that are used in the reference sheets.
weight: 1000000000000000000
---

# Formulas

This page contains a list of all the formulas that are used in the reference sheets.

## 8.2.3: Arc Length

Arc length of a non-parametric curve $\int_a^b\sqrt{1+(f'(x))^2}dx$

Arc length of a parametric curve $\int_a^b\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2}dx$

## 9.2.0

Sum of a finite geometric series $S_n=a+ax+ax^2+\cdots+ax^{n-1}=\frac{a(1-x^n)}{1-x}$ where $x\neq1$

Sum of an infinite geometric series $\lim\limits\_{n\to\infin}S_n=a+ax+ax^2+\cdots+ax^{n-1}+ax^{n}+\cdots=\frac{a}{1-x}$ where $|x|<1$

## 9.3.0

**Convergence tests**

If $\lim\limits_{n\to\infin}a_n\neq 0$ or $\lim\limits_{n\to\infin}a_n\neq\infin$, does not exist, the series diverges

**Integral test**

If $\lim\limits_{n\to\infin}\int\limits_1^nf(x)dx$, converges, then $\sum{a_n}$ converges

If $\lim\limits_{n\to\infin}\int\limits_1^nf(x)dx$, diverges, then $\sum{a_n}$ diverges

**P-series test**

$\sum\limits_{n=1}^\infin \frac{1}{n^p}$ converges if $p>1$ and diverges if $p\leq1$.

## 9.4.0

**Comparison test**

Suppose $0\leq a_n\leq b_n$ for all $n$ beyond a certain value.

- If $\sum{b_n}$ converges, then $\sum{a_n}$ converges
- If $\sum{b_n}$ diverges, then $\sum{a_n}$ diverges

**Limit comparison test**

Suppose $a_n>0$ and $b_n>0$ for all $n$. If

$\lim\limits_{n\to\infin} \frac{a_n}{b_n} = c$

where $c>0$, then the two series $\sum{a_n}$ and $\sum{b_n}$ either both converge or diverge.

**Absolute convergence test**

If $\sum{|a_n|}$ converges, then so does $\sum{a_n}$.

**Ratio test**

For a series $\sum{a_n}$, suppose the sequence of ratios $|a_{n+1}/a_n|$ has a limit:

$\lim\limits_{n\to\infin} |a_{n+1}|/|a_n| = L$

- If $L<1$, then $\sum{a_n}$ converges
- If $L>1$ or $L=\infin$, then $\sum{a_n}$ diverges
- If $L=1$, the test does not tell us anything about the convergence of the series

**Alternating series test**

An alternating series of the form

$\sum\limits_{n=1}^\infin (-1)^{n-1}a_n=a_1-a_2+a_3-a_4+\cdots$

converges if

$0 \lt a_{n+1} \lt a_n$ for all $n$. and $\lim\limits_{n\to\infin} a_n = 0$

**Error bounds for alternating series**

Let $S_n=\sum\limits_{i=1}^n (-1)^{i-1}a_i$ be the $n^{th}$ partial sum of an alternating series and let $S=\lim\limits_{n\to\infin}S_n$. Suppose that $0 \lt a_{n+1} \lt a_n$ for all $n$ and $\lim\limits_{n\to\infin} a_n = 0$. Then $|S-S_n|\leq a_{n+1}$.

**Absolute or conditional convergence test**

We say that a series $\sum{a_n}$ is

- Absolutely convergent if $\sum{a_n}$ and $\sum{|a_n|}$ both converge
- Conditionally convergent if $\sum{a_n}$ converges but $\sum{|a_n|}$ diverges

## 9.5.0

**Power series**

A power series about $x=a$ is a sum of constants times powers of $x-a$:

$C_0+C_1(x-a)+C_2(x-a)^2+\cdots+C_n(x-a)^n+\cdots=\sum\limits\_{n=0}^\infin C_n(x-a)^n$

**Radius of convergence**

The radius of convergence $R$ of a power series has 3 possible states

- $R=0$: The series converges for only $x=a$
- $R=\infin$: The series converges for all $x$
- $R>0$: The series converges for $|x-a|<R$ and diverges for $|x-a|\gt R$

Calculate with a ratio test

$\sum\limits_{n=0}^\infin C_n(x-a)^n$

we can use the ratio test by setting $a_n=C_n(x-a)^n$ the applying the following rules

- If $\lim\limits_{n\to\infin}|a_{n+1}|/|a_n|$ is infinite, then the radius is $0$.
- If $\lim\limits_{n\to\infin}|a_{n+1}|/|a_n|$ is $0$, then the radius is $\infin$.
- If $\lim\limits_{n\to\infin}|a_{n+1}|/|a_n| = K|x-a|$, where K is finite and not $0$, then the radius is $1/K$.

**Interval of convergence**

The interval of convergence of a power series is the interval between the two points $a-R$ and $a+R$, including endpoints where the series converges.
