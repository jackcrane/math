---
title: "8.1.1: Finding areas by slicing"
description: "This cheat sheet covers using an integral to find the area of a region under a curve."
---

# Using integrals to find the area of 2d region defined by a function.

> This cheat sheet covers using an integral to find the area of a region under a curve.

## Introduction

In previous chapters, we found the area under a curve by cutting it up into increasingly tiny rectangles (or other shapes) and adding their areas:

$\lim_{n \to \infty} \sum\limits_{i=0}^{n} (\frac{b-a}{n})*f(a+\frac{b-a}{n}k)$

This can be a good way to approximate the area under a curve, but it can be time consuming and is inexact. This chapter focuses on using an integral to find the area under a curve instead:

$\int_a^b f(x) dx$

Once we know how to find the area under the curve, however, we can use the same techniques to find the area of any region bounded by one or more curves.

## Things to Know

Before diving into using the integral to find the area under a curve, there are a few important things to keep in mind:

- The integral is a sum of infinitely many rectangles, so it is exact.
- The integral is the opposite of the derivative, so the integral of a derivative is the original function.

## Calculating the Area under a curve

To calculate the area under a curve, we need to find the integral of the function that describes the curve. For example, if we want to find the area under the curve $y = x^2$, we need to find the integral of $x^2$:

$\int x^2 dx = \frac{1}{3}x^3 + C$

where $C$ is a constant of integration. To find the area under the curve, we need to evaluate the integral at the upper and lower bounds of the curve:

$\int_a^b f(x) dx = F(a) - F(b) = \lim_{n \to b-}F(a) - \lim_{n \to b-}F(b)$

where $F(x)$ is the integral of $f(x)$. Recalling that $F(x)=\frac{1}{3}x^3 + C$, we can apply the definition to find the area:

$\int_0^1 x^2 dx = \frac{1}{3} - 0 = \frac{1}{3}$

## Calculating the Area of a triangular region

Finding the area under a curve is all well and good, but the real power comes from using the same techniques to find the area of _any_ region bounded by curves. For example, if we want to find the area of an isosceles triangle with base $10$ and height $5$, we could use the triangle area formula:

$\text{Area} = \frac{1}{2}\text{base} * \text{height}$

But what if we don't know the formula, or a general formula simply does not exist? _We can use an integral!_ To use an integral to find the area of the triangle, we will need to use a reimann sum to find the area of the triangle. We can do this by cutting the triangle up into infinitely many rectangles, and then adding their areas. To do this, we will need a few more bits of data. We know the formula of the rectangle area that we will be using ($\text{Area} = \text{base} * \text{height}$). We will know the height ($\Delta x$) of each rectangle, but we need to be able to find the base in terms of height, where given a height from the bottom of the triangle, we can find the corresponding width.

$[\frac{w_i}{10} = \frac{5-h_i}{5}] = [w_i=2(5-h_i)] = \textcolor{#ff6600}{[w_i=10-2h_i]}$

Once we have a function that gives us the width of the subrectangles, we can construct a summation representing the area of the triangle:

$\sum\limits_{i=0}^{n}w_i\Delta h=\sum\limits_{i=0}^{n}\textcolor{#ff6600}{10-2h_i}\Delta h\text{ cm}^2$

By taking the limit to infinity, we can get the integral for the area of the triangle:

$\sum\limits\_{i=0}^{n}{10-2h_i}\Delta h\ = \int_0^5(10-2h)dh\text{ cm}^2$

And finally, by evaluating the integral at the upper and lower bounds, we can find the area of the triangle:

$(10h-2h)\Bigg|_0^5=25\text{ cm}^2$

And as a final step, checking our work with the traditional formula:

$\frac{1}{2}10*5=25\text{ cm}^2$

## Calculating the Area of a semi-circular region

We can use the same techniques to find the area of any region bounded by curves. For example, if we want to find the area of a semi-circle with radius $7$, we can use the circle area formula:

$\text{Area} = \pi r^2$

But just like triangles, we can use the integral to find this instead!

Just like the triangle, the first step is to find the area of a single rectangle, and to do so, we need to calculate the width of a rectangle at a given height. While it is slightly more complex than on the triangle, it is still pretty easy to determine this function using the pythagorean theorem, where $h$ is $a$, and $w$ is $b$:

$[h_i^2+(\frac{w_i}{2})=7^2] = [w_i=\sqrt{4(7^2-h^2_i)}] = \textcolor{#ff6600}{[w_i=2\sqrt{49-h_i^2}]}$

And a summation:

$\sum\limits_{i=0}^{n}w_i\Delta h=\sum\limits_{i=0}^{n}\textcolor{#ff6600}{2\sqrt{49-h_i^2}}\Delta h\text{ cm}^2$

And taking the limit to infinity to get the integral:

$\sum\limits_{i=0}^{n}{2\sqrt{49-h_i^2}}\Delta h\ = 2\int_0^7(\sqrt{49-h^2})dh\text{ cm}^2$

And finally, evaluating the integral using the table of integrals:

$2*\frac{1}{2}(h\sqrt{49-h^2}+49arcsin(\frac{h}{7}))\Bigg|_0^7=49arcsin(1)=\frac{49}{2}\pi$

And checking our work with the traditional formula:

$\frac12\pi7^2=\frac{49}{2}\pi$

## Conclusion

Using the integral to find the area of any curve is an extremely powerful skill to have because once we are able to determine the area of any 2d shape, we are able to determine the volume of any 3d shape.
