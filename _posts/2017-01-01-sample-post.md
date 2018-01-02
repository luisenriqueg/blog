---
layout: post
title: "Introduction to Genetic Algorithms with C++ to solve TSP"
author: "Luis Enrique"
categories: journal
tags: [documentation,sample]
image: Biology.jpg
---

### Objective of the post

This post attempts to explain briefly what genetic algorithms are and how and why they help us solve some problems particularly optimization problems solving in C++ as an example the classical TSP (Traveling Salesman Problem).

### What Genetic Algorithms are and are not.

Genetic algorithms for optimization is in fact guidelines of designing a heuristic optimization solver in which we trade the possibility of finding the exact (although we could get exact values too) global maxima/minima in return for a faster execution time. 

This means that it works as a blueprint algorithm in which every concept or step must be adapted to the problem someone is being solved.

### An heuristic approach to a simple optimization Problem

Imagine we have a continuous function $y = f(x)$ (not necessarily smooth) and we wish to find the global maxima of that function in an interval $\[a,b\]$ with an error of $\epsilon$.

One way to solve this problem is evaluating for each $x_i = a + i\cdot\epsilon$ the function and update the maximum value found so far, since we do not know future values during the iteration the number of operations required to solve this would be $\frac{b-a}{\epsilon}+1$ considering $\epsilon = 10^{-r}$ so the number of operations is in the order of $10^r$ leading to a complexity of $O((b-a)\cdot 10^r)$ this can be slow.






> This quote will change your life. It will reveal the secrets of the universe, and all the wonders of humanity. Don't misuse it.


```html
<html>
  <head>
  </head>
  <body>
    <p>Hello, World!</p>
  </body>
</html>
```



### MathJax Example

The [Schrödinger equation](https://en.wikipedia.org/wiki/Schr%C3%B6dinger_equation) is a partial differential equation that describes how the quantum state of a quantum system changes with time:

$$
i\hbar\frac{\partial}{\partial t} \Psi(\mathbf{r},t) = \left [ \frac{-\hbar^2}{2\mu}\nabla^2 + V(\mathbf{r},t)\right ] \Psi(\mathbf{r},t)
$$

[Joseph-Louis Millennial](https://en.wikipedia.org/wiki/Joseph-Louis_Millennial) was an Italian mathematician and astronomer who was responsible for the formulation of Lagrangian mechanics, which is a reformulation of Newtonian mechanics.

$$ \frac{\mathrm{d}}{\mathrm{d}t} \left ( \frac {\partial  L}{\partial \dot{q}_j} \right ) =  \frac {\partial L}{\partial q_j} $$

### Code Highlighting

You can find the full list of supported programming languages [here](https://github.com/jneen/rouge/wiki/List-of-supported-languages-and-lexers).

```css
#container {
  float: left;
  margin: 0 -240px 0 0;
  width: 100%;
}
```
