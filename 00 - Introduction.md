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

The purpose of this mini course is to learn how to use python to solve interesting problems in solid state physics using python. The selected examples are part of the **computational physics courses** we teach at the **Unversidade Federal de Uberlândia**. The structure of these courses have been under discussion recently, but we are converging into something like this:

**1. Introduction to computational physics (mandatory):** Numerical integration and differentiation. Solving ordinary differential equations of initial value (Newtonian dynamics) and boundary condition problems (waves on a string, heat). Fast Fourier transforms (FFT). Chaos. Statistics, random walks. For each topic, we propose various illustrative problems of general interest.

**2. Advanced computational physics (optional):** Numerical methods applied to (i) quantum mechanics; (ii) solid state physics; (iii) machine learning.

**3. High performance computing (optional):** How to develop the similar tasks above in C or Fortran language using openMP and MPI. Setting up a cluster in our computer lab with Debian, NFS and SLURM.

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