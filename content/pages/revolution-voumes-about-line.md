---
title: "8.2.2: Volumes of revolutions around a line"
description: "This reference sheet covers using integrals to find volumes of objects defined by multiple lines that revolve around an axis or a line."
---

# Finding the volume of a region through revolution around a defined line

> This reference sheet elaborates on 8.2.1 and covers using integrals to find volumes of objects defined by multiple lines that revolve around a line that is not an axis.

## Introduction

This sheet covers the exact same process as 8.2.1, but instead of revolving around an axis, we will be revolving around a line that is not an axis. This adds an extra step to the process, but the process and understanding is still the same.

## Things to Know

- The process of finding the volume of a revolution is almost exactly the same to finding the volume of a defined solid revolved around an axis
- The decision of what direction to slice the shape is a more difficult decision to make
- Bounds are rarely given in this type of question and must be found

## Finding the volume of a weird shape

We have a shape bounded by the curves $y=x$ and $y=x^2$ is rotated about the line $y=3$, and we want to find the volume of this shape.

Just like finding the volume of a defined solid, we want to find the way to slice the shape that will result in the easiest 2d shapes to work with. In this type of a shape, there are two possible ways to slice the shape, and they are named "washers" and "shells". Washers are discs with an outer and inner radius (the space between called $\delta r$) and are evaluated as their thickness reduces to 0. Shells are discs with defined thicknesses, but are evaluated as their $\delta r$ approaches 0.

For this problem, we will be using the washer method, finding vertical slices that are perpendicular to the line $y=3$. This will result in circular discs with an outer and inner radius that can be found using the equations of the curves.

The first step is to find the inner and outer radiuses of the discs, based on the equations of the curves.

Inner radius: $r_{in}=3-x$

Outer radius: $r_{out}=3-x^2$

The next step is to find the area of each disc, which is simply found by $\pi(r_{out}^2-r_{in}^2)$ and then multiplying by the thickness of the disc, $\Delta x$, in this case. This gives us the volume of each slice, which we can then add together to find the total volume:

$\pi(3-x^2)^2\Delta x-\pi(3-x)^2\Delta x$

Then we can use a summation to find the total volume:

$\sum(\pi(3-x^2)^2-\pi(3-x)^2)\Delta x$

Then we can integrate to find the volume:

$\int(\pi(3-x^2)^2-\pi(3-x)^2)dx = \int((9-6x^2+x^4)-(9-6x+x^2))dx = \pi\int(6x-7x^2+x^4)dx$

$\pi(3x^2-\frac{7x^3}{3}+\frac{x^5}{5})\Bigg|_a^b$

The next question is what the bounds of the integral are. Computing the bounds is more difficult than in previous problems, but is still simple: we need to find the points where the curves that define the shape intersect themselves. This is done by setting the two equations equal to each other and solving for $x$, which gives us $x=0$ and $x=1$. This means that the bounds of the integral are $0$ and $1$.

$\pi(3x^2-\frac{7x^3}{3}+\frac{x^5}{5})\Bigg|_0^1=2.72$

## Conclusion

This sheet refines the previous sheet in how to find the volume of a solid defined by two curves that revolve around a line and not an axis. The process is the same, but the bounds are more difficult to find.
