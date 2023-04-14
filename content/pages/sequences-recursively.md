---
title: "9.1.1: Sequences through recursion"
description: "This reference sheet covers infinite sequences of numbers through recursion"
weight: 1
---

# Sequences through recursion

> This reference sheet covers using infinite sequences of numbers through recursion.

## Introduction

In 9.1.0, we explored finding values of sequences through functions and lists of numbers. In this reference sheet, we will explore finding values of sequences through recursion, where the value of a term is defined by the value of the previous term.

## The Recursive Method

If we are given a sequence defined by

$s_n=s_{n-1}+3$ for $n>1$ and $s_1=4$

When $n=2$, we can find the value of $s_2$ by plugging in the value of $s_1$ into the function.

$s_2=s_{2-1}+3=4+3=7$

When $n=3$, we can find the value of $s_3$ by plugging in the value of $s_2$ into the function.

$s_3=s_{3-1}+3=7+3=10$

Now that we have 2 terms of the sequence, we can find further terms by using the previous values of the sequence.

$4, 7, 10, 13, 16, 19$
