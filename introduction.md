# MINI COURSE: Computational solid state physics in python

**Prof. Dr. Gerson J. Ferreira**

*Instituto de Física - Universidade Federal de Uberlândia - MG, Brasil*

-----------------

XLIV Congresso Paulo Leal Ferreira
IFT / UNESP

25 – 27 de outubro de 2021

-----------------

## Who am I?

You can find me here: https://gjferreira.wordpress.com/

-----------------

## Summary

The purpose of this mini course is to learn how to use python to solve typical problems in physics, while also improving our knowledge of fundamental solid state topics. The selected examples to be presented here allow us to learn: (i) how to represent quantum operators either as explicit matrices or as linear operators that act on wave-functions; (ii) solve eigenproblems and other linear algebra elements; (iii) apply Gram-Schmidt orthogonalizations; (iv) use FFT; (v) how to use python efficiently.

At the Unversidade Federal de Uberlândia we have been teaching these and other related topics:

**1. Introduction to computational physics (mandatory):** Numerical integration and differentiation. Solving ordinary differential equations of initial value (Newtonian dynamics) and boundary condition problems (waves on a string, heat). Fast Fourier transforms (FFT). Statistics. 

**2. Advanced computational physics (optional):** Numerical methods applied to (i) quantum mechanics; (ii) solid state physics; (iii) machine learning.

**3. High performance computing (optional, offered only once):** How to develop the similar tasks above in C or Fortran language using openMP and MPI. How to build and configure a cluster.

-----------------

## Content

### Introduction to python

- IDEs: spyder, jupyter, VS Code, PyCharm, ...
- Python essentials: variables, functions, operations, ...
- **numpy** essentials: arrays, broadcasting, vector/matrix/elementwise operations
- Plotting figures with **matplotlib**
- Linear algebra with **numpy** and/or **scipy**
- Fast Fourier transforms (**FFT**) with **numpy** and/or **scipy**

### Schrödinger's equation

- Finite differences and matrix representation
    - Eigenstates of potential wells
- Inverse power method and $H$ as a linear operator using FFT
    - Gram-Schmidt orthonormalization

### Topological insulators

- The BHZ model
- Bulk band structure and the band inversion
- Berry curvature and the Chern number
- Edge states