---
layout: page
title: Worksheet 8
permalink: /worksheets/ws8
---

## Directions

This is a self-guided **group worksheet**.  Work with your group members to follow the instructions below and explore!  Note that some of the results will be assessed later, so make sure you do it right!

## The Cayley Hamilton Theorem

### Evaluating polynomials on matrices

Consider a polynomial

$$p(x) = a_0 + a_1x + a_2x^2 + \dots + a_dx^d.$$

If $$A$$ is an $$n\times n$$ matrix, we can *"plug in"* the matrix $$A$$ into the polynomial, to get a new matrix

$$p(A) = a_0I + a_1A + a_2A^2 + \dots + a_dA^d$$

where here $$I$$ is the identity matrix.

**Example:**
Consider the polynomial $$p(x) = x^2 + 2x + 3$$ and the matrix

$$A = \left[\begin{array}{cc}1 & 2\\ 0 & -1\end{array}\right].$$

Then

$$\begin{align*}
p(A) &= A^2 + 2A + 3I\\
     & \left[\begin{array}{cc}1 & 2\\ 0 & -1\end{array}\right]^2 + 2\left[\begin{array}{cc}1 & 2\\ 0 & -1\end{array}\right] + 3\left[\begin{array}{cc}1 & 0\\ 0 & 1\end{array}\right]\\
     & \left[\begin{array}{cc}1 & 0\\ 0 & 1\end{array}\right] + \left[\begin{array}{cc}2 & 4\\ 0 & -2\end{array}\right] + \left[\begin{array}{cc}3 & 0\\ 0 & 3\end{array}\right]\\
\end{align*}$$

