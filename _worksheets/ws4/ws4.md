---
layout: page
title: Worksheet 4
permalink: /worksheets/ws4
---

## Directions

This is a self-guided **group worksheet**.  Work with your group members to follow the instructions below and explore!  Note that some of the results will be assessed later, so make sure you do it right!

You will need the files

* [river.png](river.png)

## Image filters

Suppose that $$A$$ is an $$m\times n$$ grayscale image, so that each entry is an unsigned integer whose value lies between $$0$$ (black) and $$255$$ (white).
A **linear filter** for a black and white image $$A$$ is an $$\ell\times\ell$$ matrix $$F$$, where typically $$\ell$$ is very small in comparison to $$m$$ and $$n$$.
The matrix $$F$$ determines a formula for changing the value of each pixel $$(i,j)$$ in terms of its **neighboring pixels**.
Applying the filter of $$F$$ to the image $$A$$ creates a new image $$B$$ whose pixels are determined by this formula.

For example, if our matrix is

$$F = \frac{1}{12}\left[\begin{array}{ccc}
1 & 1 & 1\\
1 & 4 & 1\\
1 & 1 & 1
\end{array}\right]$$

Then the $(j,k)$'th pixel in the image $$B$$ is determined by

$$
\begin{align}
B(j,k)  = &\frac{1}{12}  ( A(j-1,k-1) + A(j-1,k) + A(j-1,k+1)\\
                      & + A(j,k-1) + 4A(j,k) + A(j,k+1)\\
                      & + A(j+1,k-1) + A(j+1,k) + A(j+1,k+1) )\\
\end{align}
$$

Obviously, the value of the matrix $$F$$ that we choose profoundly influences the resulting "filtered" image.



