---
title: "9.2.0: Geometric series Introduction"
description: "This reference sheet covers introductions to geometric series."
weight: 2
---

# Geometric series

> This reference sheet covers introductions to geometric series.

## Introduction

In 9.1.0, we explored finding values of sequences through functions and lists of numbers. In this reference sheet, we will explore finding values of sequences through recursion, where the value of a term is defined by the value of the previous term.

Adding the terms of any sequence produces a series. Previously we explored finite series, and this sheet features infinite series.

## Geometric series in general

Geometric series can be both finite and infinite. An infinite geometric series will not approach a finite value, whereas a finite geometric series will approach a finite value.

Series are a sum of terms, where each term is a function of the previous term. These series will always follow a pattern:

**For a finite geometric series:**

$a+ax+ax^2+\cdots+ax^{n-1}$

**For an infinite geometric series:**

$a+ax+ax^2+\cdots+ax^{n-1}+ax^{n}+\cdots$

## The sum of a finite geometric series

The sum of a finite geometric series can be found by iterating over a series and computing the sum of each term. This works well and is easy to understand, but is not efficient, and is often not feasible for large series.

The sum of a finite geometric series can be found by using the formula:

$S_n=a+ax+ax^2+\cdots+ax^{n-1}=\frac{a(1-x^n)}{1-x}$

So long that $x\neq1$.

## The sum of an infinite geometric series

The sum of an infinite geometric series is simply found by taking the limit of the sum of a finite geometric series as $n\to\infin$:

$\lim\limits\_{n\to\infin}S_n=a+ax+ax^2+\cdots+ax^{n-1}+ax^{n}+\cdots=\frac{a}{1-x}$

This formula only works if $|x|<1$. If $|x|\geq1$, then the series will diverge to $\infin$ if $a>1$, or $-\infin$ if $a<1$.

If $x=1$, then the series will not develop and each term will remain at $a$.

$a+a+a+a+\cdots$

If $x=-1$, the series will oscillate between $a$ and $-a$, and thus will never converge.
