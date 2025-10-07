# Particle Swarm Optimization (PSO) Project

This project implements the **Particle Swarm Optimization (PSO)** algorithm, developed according to the requirements provided by the professor.
The official project specification can be found in the file `Project_Fuzzy.pdf`.

The implementation is built around a custom `ParticleCandidate` class, which
represents individual particles with a position (the candidate solution) and
a velocity vector. The `ParticleSwarmOptimizer` class then manages a population
of such particles, updating them iteratively based on personal best, neighborhood
best, and global best solutions.

Finally, the implementation is tested on different fitness functions
(Sphere, Rastrigin, Rosenbrock) to validate correctness and robustness.

All implementation details, comments, and justifications for design choices are provided within the notebook.
