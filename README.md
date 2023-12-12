# Solving QUBO Problems on the DWave Leap API

### Contributors: James Saslow
### 12/11/2023

<b> Return to [Full Project Portfolio](https://github.com/jamessaslow/portfolio) </b>

A tutorial series of solving classic QUBO problems on DWave's quantum annealer systems in DWave Leap &amp; Ocean SDK

<h2> QUBO Problems </h2>

Quadratic Unconstrained Binary Optimization problems, or QUBO problems, are a special class of math problems that can be solved with quantum computing schemes. QUBO problems include the knapsack problem, the traveling salesman problem, max-cut, and more! So why do we need quantum? The time complexity for QUBO's are often exponential or factorial for classical computing implementations. Although QUBO problems are relatively easy to solve classically with small problem sizes, the bottlenecks become quickly apparent as we scale up the problem size. Quantum computing devices utilize 'qubits' instead of classical bits to provide inherent scalability and parallelization that can provide guaranteed speed-ups in the QUBO's time complexity. Currently, quantum computing is in its NISQ (Noisy intermediate-scale quantum) phase, which means that quantum platforms are functioning, but there are connectivity issues and noise issues with scaling up the qubit size drastically. This project aims to guide aspiring quantum engineers to map and solve QUBO problems on DWave's quantum annealers.


<h2> System Requirements </h2>

We access DWave's quantum annealer remotely using the DWave Leap API & Ocean SDK in a Python3 Jupyter Notebook environment. I am using DWave's free access trial plan to interact with their systems. 
This tutorial utilizes **dwave.system** and **dimod** packages from DWave, **networkx** for node-network embedding, as well as standard Python packages i.e. **numpy**, **matplotlib**, & **pandas**.

<h2> DWave's Quantum Annealer </h2>

Unlike many other quantum computing platforms, DWave's quantum annealer **does not** use quantum gates -- They use a different method called **quantum annealing**. Quantum annealers can embed an Ising Hamiltonian and solve for the ground state solution. QUBO problem that can be directly mapped to an Ising Hamiltonian with a simple linear transformation. Finding the ground state of the Ising Hamiltonian means finding the optimal solution(s) to the QUBO! A quantum annealing approach can be thought of as doing a gradient descent on some potential function in search of the absolute minimum. However, the problem with gradient descent is that there is a chance you could get stuck in a relative minima instead. Quantum annealing provides an interesting feature of quantum tunneling which allows an escape from these relative minima wells with some probability. Because of this, quantum annealing uses quantum tunneling to extend the search space in hopes of landing in the absolute minimum well.

![image](https://github.com/jamessaslow/dwave-leap-qubos/assets/22723891/a389535f-5c80-4726-9afe-5f3bdc5f8277)
*Adapted from DWave's Solver Docs*


<h2> Table of Contents</h2>

This project contains several Jupyter Notebook (.ipynb) files containing worked-out examples of how to use DWave's API in solving a variety of QUBO problems

<h3>1) Simple LUBO Example.ipynb <\h3>
   
   - An Introduction to Solving Linear Unconstrained Binary Optimization Problems
   - A simple LUBO is formulated as an arbitrary math problem & solved both analytically and with DWave solvers
2) Subset Sum Problem Example.ipynb
   - The Subset Sum Problem (SSP) is formally introduced as a practical application of a LUBO problem
   - SSP is modified from its usual form to find the subset that extremizes the target sum amount
   - Solved with brute-force search & QUBO implementation in DWave's hybrid solver
3) Knapsack Problem Example.ipynb
   - An extension of the modified SSP problem, but with a carrying capacity inequality constraint
   - Solved with brute-force search & QUBO implementation in DWave's hybrid solver
5) Simple Qubo Example.ipynb
   - A simple QUBO is formulated as an arbitrary math problem, introducing the quadratic nature of the QUBO
   - Solved analytically and with DWave's hybrid solver
6) Max Cut Problem Example.ipynb
   - Node-Network problems are introduced and casted into QUBO formalism
   - Max Cut is solved with DWave's hybrid solver
7) Weighted Max Cut Social Networks.ipynb
   - Weighted Max cut is introduced as an extension of the Max-Cut Problem, adding 'weights' into the graphs
   - DWave hybrid solver is used to partition a social networks into binary groups
