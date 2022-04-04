---
layout: page
title: Worksheet 6
permalink: /worksheets/ws6
---

## Directions

This is a self-guided **group worksheet**.  Work with your group members to follow the instructions below and explore!  Note that some of the results will be assessed later, so make sure you do it right!

## Interpolation

Oftentimes when we are dealing with a very complicated function $$f(x)$$, typical tasks such as differentiating $$f(x)$$, integrating $$f(x)$$ or even evaluating $$f(x)$$ at a point can become challening.
One tactic that is often used is to **approximate** $$f(x)$$ by a nicer function, such as a polynomial $$p(x)$$, on a specific interval.
Then all the difficult things that we wanted to do with $$f(x)$$ can simply be done with $$p(x)$$, and the calculations will all be approximations of the original calculations we wished to perform.

There are many ways to approximate a function $$f(x)$$ by a polynomial $$p(x)$$, some of which (like Taylor series expansions) you may have already seen.
In this worksheet, we will explore a very powerful approximation method called **interpolation**.

**Definition:** Let $$f(x)$$ be a function defined on the $$\mathbb R$$ and fix $$d+1$$ distinct points $$x_0, x_1, \dots, x_d$$ on $$\mathbb R$$.
The **polynomial interpolation** of $$f(x)$$ at these points is the unique polynomial of degree $$d$$

$$p_d(x) = c_0 + c_1x + c_2x^2 + \dots + c_dx_d$$

satisfying the condition that $$p_d(x_j) = f(x_j)$$ for all $$0\leq j \leq d$$.  Here $$c_0,\dots, c_d$$ are just some constants which define the polynomial $$p(x)$$.  The points $$x_0, x_1,\dots, x_d$$ are called the **interpolation points**.  Clearly the degree of the polynomial, and therefore the accuracy of the interpolation, depends on the number of interpolation points.

**Example:**  For example, lets consider the function $$f(x) = e^x+x$$.
The polynomial interpolation of $$f(x)$$ with interpolation points $$x_0 = 0$$ and $$x_1 = 1$$ is the unique polynomial

$$p_1(x) = c_0 + c_1x$$

satisfying $$p_1(0) = e^0+0 = 1$$ and $$p_1(1) = e^1+1= e+1$$.  Inserting this into our expression for $$p_1(x)$$ gives us a system of two equations and two unknowns

$$\left\lbrace\begin{array}{cc}
c_0 + c_1(0) &= 1\\
c_0 + c_1(1) &= e+1\\
\end{array}\right.$$
Solving this system, we find $$c_0 = 1$$ and $$c_1 = e$$ so that our polynomial interpolation is

$$p_1(x) = 1 + ex.$$


### Part 1
Let's practice the example that we described above, but this time with three interpolation points so that our polynomial interpolation will have degree $$2$$.

* (A) Set up a linear system for the coefficients of the polynomial interpolation

$$p_2(x) = c_0 + c_1x + c_2x^2$$

of $$f(x) = e^x +x$$ using the three interpolation points $$x_0 = 0$$, $$x_1 = 1$$, and $$x_2 = -1$$.  Your system should have three equations and three unknowns.

* (B) Solve the system that you found in (A) by hand using row reduction.
* (C) Use MATLAB to create a plot of $$p_2(x)$$ and $$f(x)$$ on the same graph on the interval $$[-1,1]$$.
* (D) As you should see from the graph, $$f(x)$$ has a single $$x$$-intercept in the interval $$[-1,1]$$.  Since $$p_2(x)$$ approximates $$f(x)$$ in this same interval, the root of $$p_2(x)$$ in this interval should approximate the root of $$e^x+x$$!  Use the quadratic formula on $$p_2(x)$$ to get an approximate value for the $$x$$-intercept of $$f(x)$$.
* (D) The actual value of the $$x$$-intercept of $$f(x)$$ is $$x=-0.5671432904$$.  How far away was the approximate value you found in (D)?  Make sure to remember this for the self-assessment later.

### Part 2
We can solve much larger linear systems of equations using MATLAB!  In this way, we can obtain very large polynomial interpolations of a function that we are interested in.  In this part, we will use this to obtain a very accurate polynomial interpolation of $$f(x)$$.

* (A) Set up a linear system for the coefficints of the polynomial interpolation

$$p_4(x) = c_0 + c_1x + c_2x^2 + c_3x^3 + c_4x^4$$

using the five interpolation points $$x_0 = 0$$, $$x_1 = 1$$, $$x_2 = -1$$, $$x_3 = 0.5$$, and $$x_4 = -0.5$$.

* (B) Form the augmented matrix $$A$$ for this linear system and enter it into MATLAB.  Then use the MATLAB function *rref(A)* to calculate the row reduced echelon form of $$A$$ and solve the linear system of equations.  Make sure to remember the solutiono for the self-assessment later.

* (D) Use MATLAB to create a plot of $$p_2(x)$$, $$p_4(x)$$ and $$f(x)$$ all on the same graph on the interval $$[-1,1]$$.  Add a legend indicating which curve is which.

We can use MATLAB to find the roots of a specified polynomial.  To do this we use the command *roots()* which takes in the coefficients of the polynomial from highest to lowest.  For example, to find the roots of the polynomial $$x^2+2x + 3$$, we use the command

```MATLAB
roots([1 2 3])
```

Likewise, to find the roots of the polynomial $$x^6 + x^2 + 2$$, we use the command

```MATLAB
roots([6 0 0 0 1 2])
```

* (E) Use MATLAB to find the roots of the polynomial $$p_4(x)$$ defined above.  The root inside the interval $$[-1,1]$$ should closely approximate the actual value of the $$x$$-intercept of $$f(x)$$.  How far away is your approximation?  Make sure to remember this for the self-assessement later.





