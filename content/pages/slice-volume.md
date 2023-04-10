---
title: "8.1.2: Finding volumes by slicing"
description: "This reference sheet covers using integrals to find volumes of objects defined by functions."
---

# Calculating the area of a region under a curve

> This reference sheet covers using integrals to find volumes of objects defined by functions.

## Introduction

In the previous sheet I defined how to find the area of a region bounded by curves. In this sheet, though, I will be focusing on finding the _volume_ of a region bounded by curves. It is a remarkably similar process, just with a few extra steps.

## Things to Know

Before diving into using the integral to find the area under a curve, there are a few important things to keep in mind:

- This sheet focuses on _regular_ 3d shapes, or shapes that can be defined by a function, either via extrusion or revolution.
- When evaluating these volumes, they will need to be sliced. There are multiple ways to slice objects, but you should pick the method that results in the easiest 2d shapes to work with.

## Finding the volume of a cone

Just like finding the area of a 2d shape, we will need to break the problem into small slices so we can assemble a riemann sum. This problem will focus on the volume of a cone with the point facing up. There are multiple ways we can slice this cone, one method (vertical slices) will leave us with arch-shaped slices, and the other (horizontal slices) will leave us with circular slices. Because circles are much easier to work with than arches, we will be using horizontal slices.

Like in the previous sheet, some problems have defined functions that can be used to find the volume, like cones:

$V = \frac{1}{3} \pi r^2 h$

But again, like on the last page, we will not always have or know the function that defines the volume for the specific shape we are working with.

If we define our cone to be 10 units wide and 5 units tall, we can find the volume by slicing it into infinitely small slices and adding up the areas of each slice.

We will always need to define the height and width of each slice given an elevation of the slice. This can be done 2d line, allowing us to define a slope and a y-intercept. We can then use this line to find the width of the slice at a given height. We know that the width of the slice at the top of the cone ($5$) is $0$, and the width of the slice at the bottom of the cone ($0$) is $10$. We can then use the slope of the line to find the width of the slice at any height in between.

$[w_i=10-2h]=[r_i=5-h_i]$

Now that we know the width of a slice at any height, we are ready to construct our sum

$\sum\limits_{i=0}^{n}\pi(5-h_i)^2\Delta h$

And then we can convert the sum to an integral:

$\int_0^5\pi(5-h)^2\,dh$

Which can finally be solved to find the volume of the cone:

$\int_0^5\pi(5-h)^2\,dh = \frac{-\pi}{3}(5-h)^3\Bigg|_0^5=\frac{125}{3}\pi\text{ cm}^3$

Now that we have found the volume of the cone, we can use the known cone volume function to check our work:

$\frac{1}{3}\pi(5)^2(10)=\frac{125}{3}\pi\text{ cm}^3$

## Finding the volume of a hemisphere

The process for finding the volume of a hemisphere is very similar to finding the volume of a cone. The only difference is that we will have to use a different function to determine the width of the slice at a given height. Just like the cone, slicing in the horizontal direction will make the problem much easier to solve, so we will be using coin-shaped horizontal slices to find the volume of the hemisphere. Just like the cone, we have a recognized function that can be used to find the volume of a hemisphere:

$V = \frac{4}{3} \pi r^3$

Let's define our hemisphere to have a radius of $7$ units.

Again, by multiplying the area of a slice at given height by the height of the slice, we can find the volume of the slice. Although still simple, this task is more complicated than the cone because it is not a linear relationship. Instead, we can use the pythagorean theorem to find the width of a slice at a given height:

$r=\sqrt{7^2-h^2}=\sqrt{49=h^2}$

And thus we can find the volume of the slice by multiplying the area of the slice by the height of the slice:

$\pi r^2\Delta h=\pi(7^2-h^2)\Delta h$

Then the slices can be combined to a summation:

$\sum\limits_{i=0}^{n}\pi(7^2-h_i^2)\Delta h$

And then converted to an integral from $0$ to $7$ (bottom to top of the hemisphere):

$\int_0^7\pi(7^2-h^2)\,dh$

## Conclusion

This sheet covers how to find the volume of any regular 3d shape that can be defined by a function. The process is very similar to finding the area of a region bounded by curves, but with a few extra steps. The most important thing to remember is that the slices need to be as simple as possible, so that the area of the slice can be easily calculated.
