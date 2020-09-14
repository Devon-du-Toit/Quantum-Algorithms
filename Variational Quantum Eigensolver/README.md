<h1>Variational Quantum Eigensolver</h1>

Based on Musty Thoughts Method (https://www.mustythoughts.com/variational-quantum-eigensolver-explained)

__Variational Method__:

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

This leads to the __variational principle__:

![equation](https://latex.codecogs.com/gif.latex?%3C%20%5Cpsi%20%5Clambda%20%7C%20%5C%20H%20%5C%20%7C%20%5Cpsi%20%5Clambda%20%3E%20%5C%20%5Cgeq%20E_%7B0%7D)

Our E<sub>λ</sub> is an upper bound for the ground energy, which doesn't give a lot of information about the system. To find it as close to the real value as possible we use ansatz.

<br>
<br>

__Ansatz__

We would like to investigate the spaces of all the possible states. We can do that using parameterizable circuits. 

Consider an RY gate. It has a single parameter, the rotational angle. This may represent a spectrum of quantum states:

![equation](https://latex.codecogs.com/gif.latex?%5Calpha%20%7C0%3E%20&plus;%20%281-%20%5Calpha%29%7C1%3E)

Visualization of these states using a bloch-sphere:

![bloch](https://user-images.githubusercontent.com/68278907/93074789-27616900-f685-11ea-8a5d-e3efb5b8c73c.png)

However, it cant represent all states, such as:

![equation](https://latex.codecogs.com/gif.latex?%5Cfrac%7B1%7D%7B2%7D%28%7C0%3E&plus;i%7C1%3E%29)

In order to represent this phase, we add another RX gate. Therefore we want an ansatz that:

- Covers as many states as possible.
- Uses as few gates as possible.
- Uses as few parameters as possible.

__Circuit__:

The circuit will consist of three parts:

- Ansatz, prepares the state required as to apply variational principle.

- Hamiltonian, constructed using Pauli operators and their tensor products.
- Measurement

For the Hamiltonian, we divide its sum into its terms. And for each term we look at every Pauli operator and append rotations to the circuit:

- RY(-π/2) if it is X.
- RX(π/2) if it is Y.
- Nothing if it is Z.

For the measurement, we consider the equaton:

![equation](https://latex.codecogs.com/gif.latex?%3C%20%5Cpsi%20%7C%20%5C%20H%20%5C%20%7C%20%5Cpsi%3E%20%3D%20%5C%20E_%7B%20%5Cpsi%7D)

where |Ψ> is the state created by the ansatz.Since the Hamiltonian is the sum of the Pauli terms, we may consider each term separately:

![equation](https://latex.codecogs.com/gif.latex?H%20%3D%20H_%7B1%7D%20&plus;%20H_%7B2%7D%20&plus;...&plus;%20H_%7Bn%7D)

Since

![equation](https://latex.codecogs.com/gif.latex?%3C%20%5Cpsi%20%7C%20%5C%20H_%7Bi%7D%20%5C%20%7C%20%5Cpsi%20%3E)

is the expected value of H<sub>i</sub>, aproximated by measuring |Ψ> and averaging the result. (The more times this is done, the more precise the answer).

__Example__:

Given Hamiltonian: H = 2 * Z + X + I, its matrix is:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Bvmatrix%7D%203%20%26%201%20%5C%5C%201%20%26%20-1%20%5Cend%7Bvmatrix%7D)

We would like to find its ground state using VQE.

__Solution__:

First we need to choose our ansatz. For simplicity let the ansatz be RY(θ), which allows the states cos(θ)|0> + sin(θ)|1>.

The Hamiltonian will have three parts:

- H<sub>1</sub> = 2*Z
- H<sub>2</sub> = X
- H<sub>3</sub> = I

For the first part, recalling Z gate requires no rotation, thus the first part consits of just an ansatz. For the second case, the X-gate we add the gate RY(-π/2). For the last case, we only add a constant factor to our calculations and we don't need any measurements. Thus we only need two circuits for our VQE:

![example](https://user-images.githubusercontent.com/68278907/93084201-fccadc80-f693-11ea-95bc-a2869d96f3b3.png)

We then apply different values to θ and summing the Hamilton parts together, e.g for:

- θ = 0, H<sub>1</sub> =2, H<sub>2</sub> = 0, H<sub>3</sub> = 1:

![equation](https://latex.codecogs.com/gif.latex?%3C%20%5Cpsi%280%29%20%7C%20%5C%20H%20%5C%20%7C%20%5Cpsi%280%29%20%3E%20%5C%20%3D%20%5C%203)

- θ = π, H<sub>1</sub> =-2, H<sub>2</sub> = 0, H<sub>3</sub> = 1:

![equation](https://latex.codecogs.com/gif.latex?%3C%20%5Cpsi%28%20%5Cpi%29%20%7C%20%5C%20H%20%5C%20%7C%20%5Cpsi%28%20%5Cpi%29%20%3E%20%5C%20%3D%20%5C%20-1)
