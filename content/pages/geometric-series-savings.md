---
title: "9.2.2: Geometric series: Savings"
description: "This reference sheet covers using geometric series to analyze savings and investments."
weight: 1
---

# Geometric series: Savings

> This reference sheet covers using geometric series to analyze savings and investments.

## Introduction

In 9.2.0, we explored geometric series in general. In this reference sheet, we will explore using geometric series to analyze savings and investments.

## Regular deposits into a savings account

Typically, savings are accumulated by setting aside small but regular amounts of money to be deposited into an account. For sake of this example, lets assume we are depositing $1000$ dolalrs into a savings account that will yield an interest rate of $5%$ per year, compounding annually. How much money (balance) will be in the account after the $n$th year?

The first step is to evaluate the first few years by hand to understand the patterns of the function.

$B_1=1000$

$B_2=B_1(1.05)+1000=1000(1.05)+1000$

$B_3=B_2(1.05)+1000=1000(1.05)^2+1000(1.05)+1000$

Now that we can recognize patterns, it is easier to write a function to evaluate the balance after $n$ years.

$B_n=1000(1.05)^{n-1}+1000(1.05)^{n-2}+\cdots+1000(1.05)+1000$

Because we can see that the series is approaching a number and not infinity (practically we can see that this is shrinking, not growing), we can use the sum of a finite geometric series formula to find the balance after $n$ years.

$B_n=\frac{1000(1-(1.05)^n)}{1-1.05}$

Obviously the more we save, the more we will have in the account, and the more we will earn from interest, so if we were to take the limit to infinity, it would evaluate to an infinite balance.
