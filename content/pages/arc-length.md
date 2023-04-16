---
title: "8.2.3: Arc Length"
description: "This reference sheet covers using integrals to find the length of an arc on a curve."
weight: 2
---

# Finding the length of an arc

> This reference sheet covers using integrals to find the length of an arc on a curve.

## Introduction

Integrals can also be used to find the length of an arc on a curve.

## Arc length on a standard curve

We have a curve $f(x)=x^3$ and want to find the length of the arc between $x=0$ and $x=5$.

The first step is to find the derivative of the curve. The derivative of $f(x)=x^3$ is $f'(x)=3x^2$. We will be using the non-parametric formula for arc length:

$\int\limits_a^b\sqrt{1+(f'(x))^2}dx$

After substituting in the values for $a$, $b$, and $f'(x)$, we get:

$\int\limits_0^5\sqrt{1+(3x^2)^2}dx=125.68$

## Arc length on a parametric curve

If a particle is described as moving in a path defined by parametric equations with respect to a time value, we can use the parametric formula for arc length:

$\int\limits_a^b\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2}dx$

We have an ellipse given by a parametric equations $x=2cos(t)$, $y=sin(t)$, and we want to find the length of the arc between $t=0$ and $t=2\pi$.

The first step is to find the derivatives of the parametric equations. The derivative of $x=2cos(t)$ is $x'=-2sin(t)$, and the derivative of $y=sin(t)$ is $y'=cos(t)$ Plugging those values into the parametric formula for arc length:

$\int\limits_{0}^{2\pi}\sqrt{(-2sin(t))^2+(cos(t))^2}dt$

After simplifying, we get:

$\int\limits_{0}^{2\pi}\sqrt{4sin^2(t)+cos^2(t)}dt=9.69$

## Conclusion

Integrals can be used to find the length of an arc on a curve. The formula for arc length depends on whether the curve is parametric or non-parametric.
