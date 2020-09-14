<h1>Variational Quantum Eigensolver</h1>

Based on Musty Thoughts Method (https://www.mustythoughts.com/variational-quantum-eigensolver-explained)

Consider the Eigenvalue of a matrix:

![equation](https://latex.codecogs.com/gif.latex?A%5Coverrightarrow%7Bx%7D%3D%20%5Clambda%20%5Coverrightarrow%7Bx%7D)

If we imagine that the matrix A is actually a Hamiltonian and vector x is the eigenstate Ψλ:

![equation](https://latex.codecogs.com/gif.latex?H%20%7C%20%5Cpsi%20%5Clambda%20%3E%20%5C%20%3D%20%5C%20%5Clambda%20%7C%20%5Cpsi%20%5Clambda%20%3E)

which may be viewed as the eigenequation of H. To find the energy value of state |Ψ> we use the expectation value H equation:

![equation](https://latex.codecogs.com/gif.latex?%3C%20%5Cpsi%20%7C%20H%20%7C%20%5Cpsi%20%3E%20%5C%20%3D%20%5C%20E%20%28%20%5Cpsi%20%29)

but if we use an eigenstate we get:

![equation](https://latex.codecogs.com/gif.latex?%3C%20%5Cpsi%20%5Clambda%20%7C%20H%20%7C%20%5Cpsi%20%5Clambda%20%3E%20%5C%20%3D%20%5C%20E%20%5Clambda)

The smallest eigenvalue found would equal the ground state of the system (E<sub>0</sub>). If we were to take an arbitrary state of the system |Ψ> with an associated energy E<sub>Ψ</sub>, we would know:

![equation](https://latex.codecogs.com/gif.latex?E_%7B%20%5Cpsi%7D%20%5Cgeq%20E_%7B0%7D)
