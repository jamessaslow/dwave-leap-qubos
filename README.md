# Solving QUBO Problems on the DWave Leap API

<b> Return to [Full Project Portfolio](https://github.com/jamessaslow/portfolio) </b>

A tutorial series of solving classic QUBO problems on DWave's quantum annealer systems in DWave Leap &amp; Ocean SDK

<h2> QUBO Problems </h2>

Quadratic Unconstrained Binary Optimization problems, or QUBO problems, are a special class of math problems that can be solved with quantum computing schemes. QUBO problems include the knapsack problem, the traveling salesman problem, max-cut, and more! So why do we need quantum? The time complexity for QUBO's are often exponential or factorial for classical computing implementations. Although QUBO problems are relatively easy to solve classically with small problem sizes, the bottlenecks become quickly apparent as we scale up the problem size. Quantum computing devices utilize 'qubits' instead of classical bits to provide inherent scalability and parallelization that can provide guaranteed speed-ups in the QUBO's time complexity. Currently, quantum computing is in its NISQ (Noisy intermediate-scale quantum) phase, which means that quantum platforms are functioning, but there are connectivity issues and noise issues with scaling up the qubit size drastically. This project aims to guide aspiring quantum engineers to map and solve QUBO problems on DWave's quantum annealers.


<h2> System Requirements </h2>

We access DWave's quantum annealer remotely using the DWave Leap API & Ocean SDK in a Python3 Jupyter Notebook environment. I am using DWave's free access trial plan to interact with their systems. 
This tutorial utilizes **dwave.system** and **dimod** packages from DWave, **networkx** for node-network embedding, as well as standard packages i.e. **numpy**, **matplotlib**, & **pandas**.

<h2> DWave's Quantum Annealer </h2>

Unlike many other quantum computing platforms, DWave's quantum annealer **does not** use quantum gates -- They use a different method called **quantum annealing**. Quantum annealers can embed an Ising Hamiltonian and solve for the ground state solution. QUBO problem that can be directly mapped to an Ising Hamiltonian with a simple linear transformation. Finding the ground state of the Ising Hamiltonian means finding the optimal solution(s) to the QUBO! A quantum annealing approach can be thought of as doing a gradient descent on some potential function in search of the absolute minimum. However, the problem with gradient descent is that there is a chance you could get stuck in a relative minima instead. Quantum annealing provides an interesting feature of quantum tunneling which allows an escape from these relative minima wells with some probability. Because of this, quantum annealing uses quantum tunneling to extend the search-space in hopes of landing in the absolute minimum well.




