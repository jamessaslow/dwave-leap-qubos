# Solving QUBO Problems on the DWave Leap API

<b> Return to [Full Project Portfolio](https://github.com/jamessaslow/portfolio) </b>

A tutorial series of solving classic QUBO problems on DWave's quantum annealer systems in DWave Leap &amp; Ocean SDK

<h2> QUBO Problems </h2>

Quadratic Unconstrained Binary Optimization problems, or QUBO problems, in short, are a special class of math problems that can be solved with quantum computing schemes. QUBO problems include the knapsack problem, the traveling salesman problem, max-cut, and more! So why do we need quantum? The time complexity for QUBO's are often exponential or factorial for classical computing implementations. Although QUBO problems are relatively easy to solve classically with small problem sizes, the bottlenecks become quickly apparent as we scale up the problem size. Quantum computing devices utilize 'qubits' instead of classical bits to provide inherent scalability and parallelization that can provide guaranteed speed-ups in the QUBO's time complexity. Currently, quantum computing is in its NISQ (Noisy intermediate-scale quantum) phase, which means that quantum platforms are functioning, but there are connectivity issues and noise issues with scaling up the qubit size drastically. This project aims to guide aspiring quantum engineers to map and solve QUBO problems on DWave's quantum annealers.


<h2> DWave's Quantum Annealer </h2>

We access DWave's quantum annealer remotely using the DWave Leap API & Ocean SDK in a Python3 Jupyter Notebook environment. I am using DWave's free access trial plan to interact with their systems.
