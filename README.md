# MINI COURSE: Computational solid state physics in python

Prof. Dr. Gerson J. Ferreira 

*Instituto de Física, Universidade Federal de Uberlândia*

---------------------

[XLIV Congresso Paulo Leal Ferreira de Física](http://professores.ift.unesp.br/congressoPauloLealFerreira/), 25, 26 e 27 de outubro de 2021, 1h por dia. Total de 3h

---------------------

## About

The class notes written here are in English, but the mini course will be in Portuguese.

The purpose of this mini course is to learn how to use python to solve interesting problems in solid state physics using python. The selected examples are part of the **computational physics courses** we teach at the **Unversidade Federal de Uberlândia**. The structure of these courses have been under discussion recently, but we are converging into something like this:

**1. Introduction to computational physics (mandatory):** Numerical integration and differentiation. Solving ordinary differential equations of initial value (Newtonian dynamics) and boundary condition problems (waves on a string, heat). Fast Fourier transforms (FFT). Chaos. Statistics, random walks. For each topic, we propose various illustrative problems of general interest.

**2. Advanced computational physics (optional):** Numerical methods applied to (i) quantum mechanics; (ii) solid state physics; (iii) machine learning.

**3. High performance computing (optional):** How to develop the similar tasks above in C or Fortran language using openMP and MPI. Setting up a cluster in our computer lab with Debian, NFS and SLURM.

-----------------

## Resumo / Abstract

**Official abstract in Portuguese**

Neste minicurso abordaremos alguns problemas ilustrativos da física estado sólido usando abordagens numéricas em python. Começaremos com uma rápida introdução ao python: fundamentos da linguagem, matplotlib, numpy (linalg, fft), scipy. Aplicaremos as técnicas numéricas para estudar métodos para solução numérica da equação de Schrödinger. Aplicaremos estes a poços quânticos simples e para o modelo BHZ de isolantes topológicos. Neste último caso, investigaremos a inversão de bandas e transição de fase topológica analisando a hibridização das bandas a medida que o gap inverte de positivo para negativo. Calcularemos a curvatura de Berry e número de Chern para o modelo BHZ. Ao longo do minicurso, apresentaremos os fundamentos teóricos e numéricos de cada exemplo. Exercícios serão propostos como tarefas curtas ou para serem feitas em casa após as aulas. Para se prepararem para o mini-curso, adiantem-se pelos links abaixo:

[1] As aulas referentes a este mini-curso estão disponíveis na minha playlist [Mini-Cursos - Estado Sólido Computacional](https://www.youtube.com/playlist?list=PLdIC0E4zfhQgk9e0zmBwO5LfdZxfH2zhz)

[2] Se não quiserem instalar python nas suas máquinas, podem desenvolver os exercícios via [Google Colab](https://colab.research.google.com/)

[3] [Instalando Python no Windows](https://www.youtube.com/watch?v=dpdWU59XTP8)

[4] [Tutorial Python](https://compphysics.readthedocs.io/)

[5] Veja vídeos de tópicos relacionados no [meu canal youtube](https://www.youtube.com/c/GersonJFerreira/)

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
    - Eigenstates of potential wells and superlattices
- Inverse power method and $H$ as a linear operator using FFT
    - Gram-Schmidt orthonormalization

### Topological insulators

- The BHZ model
- Bulk band structure and the band inversion
- Berry curvature and the Chern number
- Edge states
