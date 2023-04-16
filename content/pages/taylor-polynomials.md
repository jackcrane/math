---
title: "10.1.0: Taylor Polynomials"
description: "This reference sheet covers how to approximate a function using polynomials."
weight: 10
---

# Linear Approximations with Taylor Polynomials

We learned how to approximate a function using a 1-degree polynomial last year: we learned how to form a tangent line.

The key to tangent lines is that they hav the same slope and value at a point as the original function, meaning that the tangent line will ever. In general, tangent lines can be summarized to be more accurate as the point of inspection approaches the point of tangency.

Tangent line approximations are also referred to as the first Taylor approximation:

**Taylor polynomial of Degree 1 approximating $f(x)$ for $x$ near $0$**

$f(x)\approx P_1(x)=f(0)+f'(0)x$

If we are asked to find the taylor polynomial of degree 1 for $g(x)=cos(x)$ for $x$ near $0$, the first step is to compute the tangent line. We know the tangent line at $x=0$ is just a horizontal line at $y=1$.

This can be confirmed by computing guesses that are close to, but not equal to, $0$:

$g(0.05) = cos(0.05) \approx 0.998$

$g(-0.1) = cos(-0.1) \approx 0.995$

$g(0.4) = cos(0.4) \approx 0.921$

However, as we get further away from $0$, the tangent line becomes less accurate.

<script type="text/tikz">
  \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
  \begin{tikzpicture}
    \draw[->, gray] (-3, 0) -- (3, 0);
    \draw[->, gray] (0, -3) -- (0, 3);
    \draw[color=theme]   plot (\x,{cos(\x r)});
    \draw[domain=-4:4,smooth,variable=\x,theme_invert] plot ({\x},{1});
  \end{tikzpicture}
</script>

To advance past this limitation, we can use more complex equations to serve as our approximation functions, like

## Quadratic Approximations

Using a quadratic polynomial, we can approximate a function with a much higher degree of accuracy than we could with a line.

If we are instructed to find a quadratic approximation for $g(x)=cos(x)$ for $x$ near $0$, our first step is to understand what will form a better approximation than a line.

The rule we have to follow is that the polynomial must have the same value, slope, and second derivative as the original function at the point of inspection. In mathematical terms, this means that the polynomial must satisfy the following conditions:

- $P_2(0)=g(0)$
- $P_2'(0)=g'(0)$
- $P_2''(0)=g''(0)$

We can start with the general form of a quadratic polynomial:

$P_2(x)=ax^2+bx+c$

We can then substitute in the C-functions:

$P_2(0)=C_0+C_1x+C_2x^2$

The next step is to compute the C cases, which can be done by plugging in values and computing the derivative

| Polynomial form          | Function value   |
| ------------------------ | ---------------- |
| $P_2(x)=C_0+C_1x+C_2x^2$ | $g(x)=cos(x)$    |
| $P_2'(x)=C_1+2C_2x$      | $g'(x)=-sin(x)$  |
| $P_2''(x)=2C_2$          | $g''(x)=-cos(x)$ |

We can then solve for the C values:

| C value | Intermediate                                                                           | Value       |
| ------- | -------------------------------------------------------------------------------------- | ----------- |
| $C_0$   | $P_2(0)=g(0)=cos(0)$                                                                   | $1$         |
| $C_1$   | $P_2'(0)=g'(0)=-sin(0)$                                                                | $0$         |
| $2C_2$  | $P_2''(0)=g''(0)=-cos(0)$ Note the C value is multiplied by 2, so value must be halved | $-1$ $-1/2$ |

And finally, we can plug in the values to get our quadratic approximation:

$cos(x)\approx 1+0x-\frac{1}{2}x^2=1-\frac{x^2}{2}$

By plotting the original function

<script type="text/tikz">
  \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
  \begin{tikzpicture}
    \draw[->, gray] (-3, 0) -- (3, 0);
    \draw[->, gray] (0, -3) -- (0, 3);
    \draw[color=theme]   plot (\x,{cos(\x r)});
    \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{1-\x*\x/2});
  \end{tikzpicture}
</script>

We can see that the quadratic approximation is much more accurate than the linear approximation across the domain of $[-\pi, \pi]$, and by doing the same thing we did to test the accuracy of the linear approximation, we can see that the quadratic approximation provides a much more accurate approximation for values that have a more varied distance from $0$.

We can generalize this to the formula

**Taylor polynomial of Degree 2 approximating $f(x)$ for $x$ near $0$**

$f(x)\approx P_2(x)=f(0)+f'(0)x+\frac{f''(0)}{2}x^2$

The second Taylor approximation is far more accurate than the first, but is still limited in its accuracy and the domain of values it can accurately approximate. To get a more accurate approximation, we can use...

## Higher-degree polynomials

The graph above shows that the second-degree polynomial is far more accurate than the first-degree polynomial, but it is still limited in its accuracy as it can still bend away from the original function for larger values of $x$. To get a more accurate approximation, we can use higher-degree polynomials.

$f(x)\approx P_n(x)=C_0+C_1x+C_2x^2+\cdots +C_{n-1}x^{n-1}+C_nx^n$

To find the values of the constants we need the function and each of its first $n$ derivatives to agree with the polynomial at $x=0$. Generally speaking, the higher a degree of a Taylor polynomial, the larger the interval for which the approximation is valid.

To find the constants, with $n=3$ as an example, we can construct a sum

$f(x)\approx C_0+C_1x+C_2x^2+C_3x^3$

We can substitute $x=0$ to get $C_0$, and we can differentiate and substitute to get further values of $C$

In general, we can use the following formula to find the $C$ values:

$C_n=\frac{f^{(n)}(0)}{n!}$

From there, we can define the nth-degree Taylor polynomial as

$f(x)\approx P_n(x)=f(0)+f'(0)x+\frac{f''(0)}{2}x^2+\frac{f'''(0)}{3!}x^3+\cdots +\frac{f^{(n)}(0)}{n!}x^n$

Where $P_n(x)$ is the Taylor polynomial of the $n$th degree centered at $x=0$.

If we examine the taylor polynomial at each degree, we can see that the higher the degree, the more accurate the approximation is.

We will be approximating the function $f(x)=sin(x)$ for $x$ near $0$.

<blockquote>

**1st degree**

| Polynomial form | Value at 0 |
| --------------- | ---------- |
| $f(x)=sin(x)$   | $f(0)=0$   |
| $f'(x)=cos(x)$  | $f'(0)=1$  |

Leading us to a first-degree Taylor polynomial of $f(x)$ for $x$ near $0$:

$f(x)\approx P_2(x)=0+1x+\frac{1}{2}x^2$

  <script type="text/tikz">
    \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
    \begin{tikzpicture}

      \draw[->, gray] (-3, 0) -- (3, 0);
      \draw[->, gray] (0, -3) -- (0, 3);
      \draw[color=theme]   plot (\x,{sin(\x r)}) node[right] {sin(x)};
      \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{0+\x});

  \end{tikzpicture}
  </script>

We can see that the first-degree Taylor polynomial is already accurate for values of $x$ near $0$, but rapidly becomes inaccurate as $x$ increases.

</blockquote>

<blockquote>

**2nd degree**

| Polynomial form | Value at 0 |
| --------------- | ---------- |
| $f(x)=sin(x)$   | $f(0)=0$   |
| $f'(x)=cos(x)$  | $f'(0)=1$  |

This leads us to a second-degree Taylor polynomial of $f(x)$ for $x$ near $0$:

$f(x)\approx P_2(x)=0+1x+\frac{0}{2!}x^2$

  <script type="text/tikz">
    \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
    \begin{tikzpicture}

      \draw[->, gray] (-3, 0) -- (3, 0);
      \draw[->, gray] (0, -3) -- (0, 3);
      \draw[color=theme]   plot (\x,{sin(\x r)}) node[right] {sin(x)};
      \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{0+\x});

  \end{tikzpicture}
  </script>

</blockquote>

<blockquote>

**3rd degree**

| Polynomial form   | Value at 0   |
| ----------------- | ------------ |
| $f(x)=sin(x)$     | $f(0)=0$     |
| $f'(x)=cos(x)$    | $f'(0)=1$    |
| $f''(x)=-sin(x)$  | $f''(0)=0$   |
| $f'''(x)=-cos(x)$ | $f'''(0)=-1$ |

This leads us to a third-degree Taylor polynomial of $f(x)$ for $x$ near $0$:

$f(x)\approx P_3(x)=0+1x+\frac{0}{2!}x^2-\frac{1}{3!}x^3$

  <script type="text/tikz">
    \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
    \begin{tikzpicture}

      \draw[->, gray] (-3, 0) -- (3, 0);
      \draw[->, gray] (0, -3) -- (0, 3);
      \draw[color=theme]   plot (\x,{sin(\x r)}) node[right] {sin(x)};
      \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{0+\x-\x^3/6});

  \end{tikzpicture}
  </script>

</blockquote>

<blockquote>

**4th degree**

| Polynomial form     | Value at 0     |
| ------------------- | -------------- |
| $f(x)=sin(x)$       | $f(0)=0$       |
| $f'(x)=cos(x)$      | $f'(0)=1$      |
| $f''(x)=-sin(x)$    | $f''(0)=0$     |
| $f'''(x)=-cos(x)$   | $f'''(0)=-1$   |
| $f^{(4)}(x)=sin(x)$ | $f^{(4)}(0)=0$ |

This leads us to a fourth-degree Taylor polynomial of $f(x)$ for $x$ near $0$:

$f(x)\approx P_4(x)=0+1x+\frac{0}{2!}x^2-\frac{1}{3!}x^3+\frac{0}{4!}x^4$

  <script type="text/tikz">
    \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
    \begin{tikzpicture}

      \draw[->, gray] (-3, 0) -- (3, 0);
      \draw[->, gray] (0, -3) -- (0, 3);
      \draw[color=theme]   plot (\x,{sin(\x r)}) node[right] {sin(x)};
      \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{0+\x-\x^3/6});

  \end{tikzpicture}
  </script>

</blockquote>

<blockquote>

**5th degree**

| Polynomial form     | Value at 0     |
| ------------------- | -------------- |
| $f(x)=sin(x)$       | $f(0)=0$       |
| $f'(x)=cos(x)$      | $f'(0)=1$      |
| $f''(x)=-sin(x)$    | $f''(0)=0$     |
| $f'''(x)=-cos(x)$   | $f'''(0)=-1$   |
| $f^{(4)}(x)=sin(x)$ | $f^{(4)}(0)=0$ |
| $f^{(5)}(x)=cos(x)$ | $f^{(5)}(0)=1$ |

This leads us to a fifth-degree Taylor polynomial of $f(x)$ for $x$ near $0$:

$f(x)\approx P_6(x)=0+1x+\frac{0}{2!}x^2-\frac{1}{3!}x^3+\frac{0}{4!}x^4+\frac{1}{5!}x^5$

  <script type="text/tikz">
    \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
    \begin{tikzpicture}

      \draw[->, gray] (-3, 0) -- (3, 0);
      \draw[->, gray] (0, -3) -- (0, 3);
      \draw[color=theme]   plot (\x,{sin(\x r)}) node[right] {sin(x)};
      \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{0+\x-\x^3/6+\x^5/120});

  \end{tikzpicture}
  </script>

</blockquote>

<blockquote>

**6th degree**

| Polynomial form      | Value at 0     |
| -------------------- | -------------- |
| $f(x)=sin(x)$        | $f(0)=0$       |
| $f'(x)=cos(x)$       | $f'(0)=1$      |
| $f''(x)=-sin(x)$     | $f''(0)=0$     |
| $f'''(x)=-cos(x)$    | $f'''(0)=-1$   |
| $f^{(4)}(x)=sin(x)$  | $f^{(4)}(0)=0$ |
| $f^{(5)}(x)=cos(x)$  | $f^{(5)}(0)=1$ |
| $f^{(6)}(x)=-sin(x)$ | $f^{(6)}(0)=0$ |

This leads us to a sixth-degree Taylor polynomial of $f(x)$ for $x$ near $0$:

$f(x)\approx P_6(x)=0+1x+\frac{0}{2!}x^2-\frac{1}{3!}x^3+\frac{0}{4!}x^4+\frac{1}{5!}x^5+0x^6$

  <script type="text/tikz">
    \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
    \begin{tikzpicture}

      \draw[->, gray] (-3, 0) -- (3, 0);
      \draw[->, gray] (0, -3) -- (0, 3);
      \draw[color=theme]   plot (\x,{sin(\x r)}) node[right] {sin(x)};
      \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{0+\x-\x^3/6+\x^5/120});

  \end{tikzpicture}
  </script>

</blockquote>

<blockquote>

**7th degree**

| Polynomial form      | Value at 0      |
| -------------------- | --------------- |
| $f(x)=sin(x)$        | $f(0)=0$        |
| $f'(x)=cos(x)$       | $f'(0)=1$       |
| $f''(x)=-sin(x)$     | $f''(0)=0$      |
| $f'''(x)=-cos(x)$    | $f'''(0)=-1$    |
| $f^{(4)}(x)=sin(x)$  | $f^{(4)}(0)=0$  |
| $f^{(5)}(x)=cos(x)$  | $f^{(5)}(0)=1$  |
| $f^{(6)}(x)=-sin(x)$ | $f^{(6)}(0)=0$  |
| $f^{(7)}(x)=-cos(x)$ | $f^{(7)}(0)=-1$ |

This leads us to a seventh-degree Taylor polynomial of $f(x)$ for $x$ near $0$:

$f(x)\approx P_8(x)=0+1x+\frac{0}{2!}x^2-\frac{1}{3!}x^3+\frac{0}{4!}x^4+\frac{1}{5!}x^5+\frac{0}{6!}x^6-\frac{1}{7!}x^7$

  <script type="text/tikz">
    \definecolor{theme}{HTML}{23b0ff}
  \definecolor{theme_invert}{HTML}{b64b00}
    \begin{tikzpicture}

      \draw[->, gray] (-3, 0) -- (3, 0);
      \draw[->, gray] (0, -3) -- (0, 3);
      \draw[color=theme]   plot (\x,{sin(\x r)}) node[right] {sin(x)};
      \draw[domain=-3:3,smooth,variable=\x,theme_invert] plot ({\x},{0+\x-\x^3/6-\x^7/5040});

  \end{tikzpicture}
  </script>

</blockquote>

We can see how the taylor polynomial is getting closer and closer to the actual function as x is increasing. Generally, the more terms we add to the Taylor polynomial, the closer it will be to the actual function. However, the more terms we add, the more complex the polynomial becomes.

## Taylor polynomials around $x=a$

We can also use Taylor polynomials to approximate functions around a point other than $x=0$ by simply changing the value of $x$ that we plug into each term in the taylor polynomial, thus changing the formula to:

$f(x)\approx P_n(x)=f(a)+f'(a)(x-a)+\frac{f''(a)}{2!}(x-a)^2+\frac{f'''(a)}{3!}(x-a)^3+...+\frac{f^{(n)}(a)}{n!}(x-a)^n$
