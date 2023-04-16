---
title: "9.2.1: Geometric series: Medicine"
description: "This reference sheet covers introductions to geometric series through computing the amount of medicine in a patient after n doses."
weight: 2
---

# Geometric series: Medicine

> This reference sheet covers introductions to geometric series through computing the amount of medicine in a patient after n doses.

## Introduction

In the introduction sheet, we defined how series may behave when summed to infinity or to some fininte solution. Here we will be computing the amount of medicine in a patient's bloodstream after a certain number of doses using a finite geometric series.

## Repeated drug dosage

By nature of how drugs release medicine into the body, the amount of medicine in the body is not constant, but rather a function of time. For this example, a patient takes $250\text{ mg}$ doses 4 times a day (every 6 hours). It is known that after the end of 6 hours, 4% of the medicine is still in the body. We want to find the amount of medicine in the body when the patient takes more doses.

The first step is to define the quantity of medicine in the blood after the patient takes their $n^{th}$ dose. Using recursion as covered in 9.1.1, we can study the amount of medicine based on the previous dosage:

$Q_1 = 250\text{ mg}$

$Q_2 = \textcolor{#ff6600}{250}(0.04)+250 = 260\text{ mg}$

Where $Q_1$ is the amount of medicine in the body after the first dose, and $Q_2$ is the amount of medicine in the body immediately after the second dose added to the amount of medicine in the body after the first dose. It is important to understand that the first $\textcolor{#ff6600}{250}$ is the result of $Q_1$ and thus the entire function could be rewritten as:

$Q_2 = Q_1(0.04)+250$

If we further define the function, we get to

$Q_3 = Q_2(0.04)+250$

$= (250(0.04)+250)(0.04)+250$

$= 250(0.04)^2+250(0.04)^1+250$

$= 260.4\text{ mg}$

If we were asked to find the amount of medicine in the body after the $10\text{nth}$ dose, we could surmise:

$Q\_{10} = 250(0.04)^9+250(0.04)^8+250(0.04)^7+\cdots+250(0.04)^3+250(0.04)+250(0.04)^0$

If we subtract $(0.04)Q_{10}$ from both sides and factoring, we can simplify from a string of 10 additions to a concise function:

$Q\_{10} = \frac{250(1-(0.04)^{10})}{1-0.04}$

And by replacing $10$ with $n$, we get the general formula for the amount of medicine in the body after the $n^{th}$ dose:

$Q_n = \frac{250(1-(0.04)^n)}{1-0.04}$

As the patient takes more medicine, we can find out the amount of the medicine in their bloodstream by plugging in values, or if we wanted to see where the medicine level would plateau, we could compute the limit of the function as $n\to\infin$

$\lim\limits\_{n\to\infin}\frac{250(1-(0.04)^n)}{1-0.04}=\frac{250(1-0)}{1-0.04}$

Which evaluates to $260.42\text{ mg}$, which is the highest possible amount of medicine in the patient's body assuming they are taking the medicine as suggested.
