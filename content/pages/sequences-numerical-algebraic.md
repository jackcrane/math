---
title: "9.1.0: Sequences through numerical and algebraic methods"
description: "This reference sheet covers infinite sequences of numbers through numerical and algebraic methods"
---

# Sequences

> This reference sheet covers using infinite sequences of numbers through numerical and algebraic methods.

## Introduction

Sequences are infinite lists of numbers that are defined by functions or numerical sets. The first term of a sequence is the first number in the sequence, the second term is the second number in the sequence, and so on. The first term of a sequence is always $a_1$ the second term is always $a_2$ and the general term is always $a_n$.

There are multiple ways to express a sequence of numbers. The sequence could be expressed as a list of numbers, a function, or a graph.

## The Functional Method

This method is the most common way to express a sequence of numbers, and is used whenever a sequence is defined by a function.

### Functional example

If we are given a function

$s_n=\frac{n(n+1)}{2}$

We can find the first 6 terms of the sequence by simply plugging in the values of $n$ from 1 to 6.

$s_1=\frac{1(1+1)}{2}=1$

$s_2=\frac{2(2+1)}{2}=3$

$s_{[3,4,5]}=[6, 10, 15]$

$s_6=\frac{6(6+1)}{2}=21$

## Another functional example

If we are given a function

$s_n=\frac{n+(-1)^n}{n}$

Even though the function is different, the process of finding the first 6 terms is exactly the same.

$s_1=\frac{1+(-1)^1}{1}=0$

$s_2=\frac{2+(-1)^2}{2}=3/2$

$s_{[3,4,5]}=[\frac{2}{3}, \frac{5}{4}, \frac{4}{5}]$

$s_6=\frac{6+(-1)^6}{6}=7/6$

Finding terms in a sequence is an extremely simple task that was originally introduced in early algebra classes, just applied with different terminology.

## The Numerical Method

This method is used when a sequence is defined by a list of numbers.

### Sequential example

Finding sequential examples is something of an inverse of the functional example, where instead of plugging in values of $n$ into a function, we are given a list of numbers and are asked to find additional terms in the sequence.

The first step is to find a function that represents the pattern of the sequence.

If we have a sequence

$1,2,4,8,16,32,\dots$

The first 6 terms of a sequence may not perfectly help define the function, but we are able to make a good guess as to the general formula.

$s_n=2^{n-1}$

We can verify the formula by plugging in the first 6 values of $n$ and comparing the results to the first 6 terms of the sequence.

### Another sequential example

If we have a sequence

$\frac{7}{2},\frac{7}{5},\frac{7}{8},\frac{7}{11},\frac{1}{2},\frac{7}{17},\dots$

In this sequence, each numerator is 7 and each denominator is the previous term plus 3. The denominators can be defined by a function

$y=3n+k$

for some $k$. By entering one of the terms into the function, we can find the value of $k$.

$2=3(1)+k=-1$

Now that we know the function defined by the denominators, we can elaborate to the function defining the entire sequence.

$s_n=\frac{7}{3n-1}$

Finally, we can check the formula by plugging in the first 6 values of $n$ and comparing the results to the first 6 terms of the sequence.

## Conclusion

Calculating sequences is a very simple task that can be done with a simple formula or a list of numbers. The functional method is the most common way to calculate sequences, but the numerical method is also very useful.
