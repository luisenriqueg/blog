---
layout: post
title: "Introduction to Genetic Algorithms with C++ to solve TSP"
author: "Luis Enrique"
categories: journal
tags: [documentation,sample]
image: Biology.jpg
---

### Objective of the post

This post attempts to explain briefly what genetic algorithms are and how and why they help us solve some problems particularly in the field of optimization problems. We will be solving in C++ the classical TSP (Traveling Salesman Problem) using GA (Genetic Algorithms).

### A Genetic Algorithms perspective

Genetic algorithms for optimization can be seen as set of guidelines for designing a heuristic optimization solver in which we trade accuracy in finding the global maxima/minima in return for a faster execution time. 

This means that it works as a blueprint algorithm in which every concept or step must be adapted to the problem that is being solved.

### An heuristic approach to a simple optimization Problem

This problem will allow us to grasp the main idea in Genetic Algorithms.

Let $f(x) : \mathbb{R} \rightarrow \mathbb{R}$ be a continuous function, we want to find the global maxima of that function in an interval $\[a,b\]$ with an absolute error of $\epsilon$.

One deterministic way to solve this problem is evaluating for each $x_i = a + i\cdot\epsilon$ the function and update the maximum value found so far, since we do not know future values during the iteration the number of operations required to solve this would be $\frac{b-a}{\epsilon}+1$ considering $\epsilon = 10^{-r}$ this means the number of operations is in the order of $10^r$ leading to a complexity of $O((b-a)\cdot 10^r)$ which can be slow.


Now we will explore a non-deterministic solution, Let $X$ be a set of values $x \in \[a,b\]$ with cardinal $N$ these values could follow a specific pattern (e.g equally spaced) or could be chosen at random, now  evaluate $y_i=f(x_i)$ and keep the $x$(s) that gives the highest value(s), to take advantage of the other points select a point $x'=x_i + (1-\lambda)\cdot (x_{i+1}-x_i) \quad \lambda \in \[0,1\]$ where $x_i < x_{i+1}$ and evaluate $f(x')$ update $x_i$ or $x_{i+1}$ according to which gives a higher value. If we iterate this many times and since the $\max_i f(x_i)$ kept is non-decreasing we may end up with a local maxima, global maxima or for some interval $\[x_i,x_{i+1}\]$ the highest value within a subinterval, to mitigate the possibility of staying at the highest point within an subinterval we could increase the value of $N$ to mitigate the problem of local maxima we could take a random value and repeat the process, since at every step every operation is $O(1)$ and assuming we perform $I$ iterations the total complexity would be $O(IN)$ we can test this algorithm and realize that even for small values of these constants we get a good result, and increasing one or the other yields in a higher accuracy we can increase it until it fullfill our needs "good answer in short time".

### Defining the Genetic Algorithms concepts

The definition of the GA concepts will be described as an analogy to previuos heuristic solution.

1. Objective Function: Function we want to optmize. In the previous problem this would be $f(x)$

2. Chromosome: A generic variable that our objective function receives. In the previous problem this would be any $x_i$

3. Population: A set of chromosomes. In the previuos example this would be $X$ with size $N$.

4. Crossover: How we combine 2 chromosomes in hope for better chromosomes. In previuos example this would be $x'=x_i + (1-\lambda)\cdot (x_{i+1}-x_i)$

5. Mutation: A way to avoid staying in a local maxima. In previuos exmaple this would be choosing a random $x$ in hope to move the maximum value found so far.




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
