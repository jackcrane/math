---
title: "9.1.2: Convergence of sequences"
description: "This reference sheet covers finding the convergence of sequences of numbers"
---

# Convergence of sequences

> This reference sheet covers finding the convergence of sequences of numbers.

## Introduction

In 9.1.0, we explored finding values of sequences through functions and lists of numbers. In 9.1.1, we explored finding values of sequences through recursion, where the value of a term is defined by the value of the previous term. In this reference sheet, we will explore finding the convergence of sequences, or the value that a sequence approaches as the number of terms increases.

> The sequence $s_1,s_2,s_3,\dots,s_n$ has a limit $L$, written $\lim\limits_{n\to\infin}s_n=L$ if $s_n$ is as close to $L$ as we please whenever $n$ is sufficiently large. If a limit, $L$, exists, we say the sequence converges to its limit $L$. If no limit exists, we say the sequence diverges.

To calculate the limit of sequences, we will use the following rules:

- The sequence $s_n=x^n$ converges to $0$ if $|x|<1$ and diverges if $|x|>1$.
- The sequence $s_n=\frac{1}{n^p}$ converges to $0$ if $p>10$.

## Examples

### Example 1

Does the following sequence converge or diverge?

$s_n=0.8^n$

Since $|0.8|<1$, the sequence converges to $0$.

### Example 2

Does the following sequence converge or diverge?

$s_n=\frac{1-e^{-n}}{1+e^{-1}}$

Since $e^{-1}<1$, we have $\lim\limits_{n\to\infin}e^{-n}=\lim\limits_{n\to\infin}(e^{-1})^n=0$ by the first fact. Thus, the sequence converges to $1$.

### Example 3

Does the following sequence converge or diverge?

$s_n=\frac{n^2+1}{n}$

Since $(n^2+1)/n$ grows without bound, the sequence diverges.

### Example 4

Does the following sequence converge or diverge?

$s_n=1+(-1)^n$

Since $(-1)^n$ alternates in sign, the function will never approach a limit, and thus diverges.

## Conclusion

In this reference sheet, we explored finding the convergence of sequences, or the value that a sequence approaches as the number of terms increases. We found that sequences can converge to a limit, or diverge to infinity. We also found that sequences can converge to $0$ if $|x|<1$ and diverge if $|x|>1$.
