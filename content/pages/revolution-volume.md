---
title: "8.2.1: Volumes of revolutions"
description: "This reference sheet covers using integrals to find volumes of objects that revolve around an axis or a line."
weight: 2
---

# Finding the volume of a region through revolution

> This reference sheet covers using integrals to find volumes of objects that revolve around an axis or a line.

## Introduction

Many shapes do not have names but can be easily defined by specifying a line or curve and an axis that they revolve around. These shapes are called _revolutions_ and can be used to find the volume of many objects with circular cross-sections.

## Things to Know

- The process of finding the volume of a revolution is almost exactly the same to finding the volume of a defined solid

## Finding the volume of a weird shape 1

We have a shape bounded by the curve $y=e^{-x}$ and the $x$-axis between $x=0$ and $x=1$ and is revolved around the $x$-axis. We want to find the volume of this shape.

Just like finding the volume of a defined solid, we want to find the way to slice the shape that will result in the easiest 2d shapes to work with. In this case, we will be using slices that are perpendicular to the $x$-axis, which will result in circular slices.

By using the function, we can easily deduce the radius of the disk across $\Delta x$:$y=e^{-x}$, from which the disc volume can be found.

$\pi y^2\Delta x=\pi(e^{-x})^2\Delta x$

Converting to a summation we can get a representation of the entire shape:

$\sum\limits_{i=0}^{n-1}\pi(e^{-x})^2\Delta x$

From the question, we know that the bounds of the shape are $x=0$ and $x=1$, and we can convert the summation to an integral:

$\int\limits_0^1\pi(e^{-x})^2\,dx=\pi(-\frac{1}{2})e^{-2x}\Bigg|_0^1=1.36$

## Finding the volume of a weird shape 2

We have a shape defined by the curve $r=3+\cos(\frac{\pi y}{25})$, which is revolved around the $y$-axis, and is 100 units tall.

Just like finding the volume of a defined solid, we want to find the way to slice the shape that will result in the easiest 2d shapes to work with. In this case, we will be using slices that are perpendicular to the $y$-axis, which will result in circular discs.

We can slice the shape into small circular discs with thickness $dy$. The radius of each disc is given by the function $r=3+\cos(\frac{\pi y}{25})$, and the area of each disc can be found using the formula for the area of a circle:

$A = \pi r^2$

$A = \pi (3+\cos(\frac{\pi y}{25}))^2$

The volume of each disc is then given by:

$V = A \cdot dy$

$V = \pi (3+\cos(\frac{\pi y}{25}))^2 \cdot dy$

We can integrate over the range of $y$ to find the total volume of the shape:

$\int\limits_{0}^{100} \pi (3+\cos(\frac{\pi y}{25}))^2 \cdot dy = 2984.5\text{ cm}^3$

## Conclusion

In this sheet, we found the volume of a shape that is revolved around an axis. This is a useful technique that can be used to compute the volume of many objects with circular cross-sections.
