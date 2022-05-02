---
layout: page
title: Worksheet 9
permalink: /worksheets/ws9
---

## Directions

This is a self-guided **group worksheet**.  Work with your group members to follow the instructions below and explore!  Note that some of the results will be assessed later, so make sure you do it right!

## Spectral Cluserting for Graphs

### The graph Laplacian

Let $$G$$ be a graph with $$n$$ vertices.
The **adjacency matrix** of the graph is the symmetric matrix $$A$$ whose $$j,k$$'th entry is given by

$$A_{jk} = \left\lbrace\begin{array}{cc}
1 & \text{vertices j and k are connected}\\
0 & \text{vertices j and k are not connected}
\end{array}\right.$$

The **degree matrix** $$D$$ is an $$n\times n$$ diagonal matrix whose diagonal entries are given by

$$D_{jj} = \text{degree of vertex j},$$

where the degree of a vertex is the number of edges touching the vertex.
The **graph Laplacian** is the difference of these two matrices

$$L = D-A.$$

For example, consider the graph

<center>
<img src="ws9/graph1.png" alt="Simple Example Graph" width="200">
</center>

The adjacency matrix of this graph is given by

$$A = \left[\begin{array}{cccc}
0 & 1 & 1 & 1\\
1 & 0 & 0 & 1\\
1 & 0 & 0 & 0\\
1 & 1 & 0 & 0
\end{array}\right]$$

and the degree matrix is

$$D = \left[\begin{array}{cccc}
3 & 0 & 0 & 0\\
0 & 2 & 0 & 0\\
0 & 0 & 1 & 0\\
0 & 0 & 0 & 2\\
\end{array}\right]$$

The graph Laplacian is then

$$L = D-A = \left[\begin{array}{cccc}
3  & -1 & -1 & -1\\
-1 &  2 &  0 & -1\\
-1 &  0 &  1 &  0\\
-1 & -1 &  0 &  2
\end{array}\right]$$

* Problem 1: Find the largest eigenvalue of the Laplacian matrix of the graph

<center>
<img src="ws9/graph2.png" alt="Star Graph" width="200">
</center>

Make sure to save the value to use in the self-assessement later!

A graph is **connected** if you can travel from a fixed vertex to any other vertex via a series of edges.  It turns out that this is characterized by whether or not $$0$$ shows up more than once as an eigenvalue of the graph Laplacian!

* Problem 2: Create a new graph which is not connected by removing the edge between $$1$$ and $$4$$ and the edge between $$2$$ and $$5$$ in the graph from Problem 1.  Show that the new graph Laplacian has $$0$$ occuring as an eigenvalue more than once.

## Clusters in graphs

A **cluster** in a graph is a collection of vertices which are closely connected to each other in comparison to their connections elsewhere.
For example, in the graph below the red vertices are strongly interconnected to each other, but weakly connected to the blue vertices.  Likewise the blue vertices are strongly connected to each other but weakly connected elsewhere.

<center>
<img src="ws9/graph3.png" alt="Simple Cluster Graph" width="200">
</center>

Just like the eigenvalues of the Laplacian can detect whether a graph is connected or not, they can also be used to find clusters!  This process is called **spectral clustering**.

a






