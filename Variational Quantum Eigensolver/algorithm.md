<h1>Variational Quantum Eigensolver</h1>

<h2>Determining a Linear Hamiltonian Matrix:</h2>

Given a Hamiltonian Polynomial in the form:

![equation](https://latex.codecogs.com/gif.latex?H%3DC_%7B1%7DX&plus;C_%7B2%7DY&plus;C_%7B3%7DZ&plus;C_%7B4%7DI)

for C<sub>1-4</sub> constants and X, Y and Z Pauli matrices of:

![equation](https://latex.codecogs.com/gif.latex?X%3D%5Cbegin%7Bbmatrix%7D%200%20%261%20%5C%5C%201%260%20%5Cend%7Bbmatrix%7D%2C%20Y%3D%5Cbegin%7Bbmatrix%7D%200%20%26-i%20%5C%5C%20i%260%20%5Cend%7Bbmatrix%7D%2C%20Z%3D%5Cbegin%7Bbmatrix%7D%201%20%260%20%5C%5C%200%26-1%20%5Cend%7Bbmatrix%7D)

The Hamiltonian matrix is found by simply substituting the Pauli matrices into the Hamiltonian Polynomial.

__Example__:

![equation](https://latex.codecogs.com/gif.latex?Given%20%5C%20Hamiltonian%20%3A%20%5C%20H%3D2Z&plus;X&plus;I)

We substitute the variables X,Y and Z with their Pauli Matrices:

![equation](https://latex.codecogs.com/gif.latex?H%3D2%5Cbegin%7Bbmatrix%7D%201%20%26%200%5C%5C%200%26-1%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%200%20%26%201%5C%5C%201%260%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%201%20%26%200%5C%5C%200%261%20%5Cend%7Bbmatrix%7D)

Thus the corresponding Hamiltonian matrix will be:

![equation](https://latex.codecogs.com/gif.latex?H%3D%5Cbegin%7Bbmatrix%7D%203%20%261%20%5C%5C%201%26-1%20%5Cend%7Bbmatrix%7D)


<h2>Determining a Linear Hamiltonian Polynomial</h2>

Given the Linear Hamiltonian Matrix, the corresponding Polynomial may be determined by decomposing the matrix into Pauli terms as a Linear Combination:

![equation](https://latex.codecogs.com/gif.latex?H%3DC_%7B1%7DX&plus;C_%7B2%7DY&plus;C_%7B4%7DZ&plus;C_%7B4%7DI)

![equation](https://latex.codecogs.com/gif.latex?H%3D%5Cbegin%7Bbmatrix%7D%200%20%26C_%7B1%7D%20%5C%5C%20C_%7B1%7D%26%200%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%200%20%26-iC_%7B2%7D%20%5C%5C%20iC_%7B2%7D%260%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%20C_%7B3%7D%20%260%20%5C%5C%200%26-C_%7B3%7D%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%20C_%7B4%7D%20%26%200%5C%5C%200%26%20C_%7B4%7D%20%5Cend%7Bbmatrix%7D)

![equation](https://latex.codecogs.com/gif.latex?H%3D%5Cbegin%7Bbmatrix%7D%20C_%7B2%7D&plus;C_%7B4%7D%20%26C_%7B1%7D-iC_%7B3%7D%20%5C%5C%20C_%7B1%7D&plus;iC_%7B3%7D%26%20C_%7B4%7D-C_%7B2%7D%20%5Cend%7Bbmatrix%7D)

If the Given Hamiltonian Matrix is:

![equation](https://latex.codecogs.com/gif.latex?H%3D%5Cbegin%7Bbmatrix%7D%20H_%7B1%7D%20%26H_%7B2%7D%20%5C%5C%20H_%7B3%7D%26H_%7B4%7D%20%5Cend%7Bbmatrix%7D)

We then have a set of linear equations:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7B*align%7D%20%26%7B%7D%20C_%7B2%7D&plus;C_%7B4%7D%3DH_%7B1%7D%20%5C%5C%20%26%7B%7D%20C_%7B1%7D-iC_%7B3%7D%3DH_%7B2%7D%20%5C%5C%20%26%7B%7D%20C_%7B1%7D&plus;iC_%7B3%7D%3DH_%7B3%7D%20%5C%5C%20%26%7B%7D%20C_%7B4%7D-C_%7B2%7D%3DH_%7B4%7D%20%5Cend%7B*align%7D)

Or in augmented matrix form:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Bbmatrix%7D%200%20%261%20%260%20%261%20%26%7CH_%7B1%7D%20%5C%5C%201%26%200%20%26-i%20%260%20%26%7CH_%7B2%7D%20%5C%5C%201%26%200%20%26i%20%260%20%26%7CH_%7B3%7D%20%5C%5C%200%26-1%20%260%20%261%20%26%7CH_%7B4%7D%20%5Cend%7Bbmatrix%7D)

For which, if solved:

![Untitled](https://user-images.githubusercontent.com/68278907/93494023-d82d6980-f90c-11ea-9a98-570534959669.png)


__Example__:

Given Hamiltonian Matrix:

![equation](https://latex.codecogs.com/gif.latex?H%3D%5Cbegin%7Bbmatrix%7D%203%20%261%20%5C%5C%201%26-1%20%5Cend%7Bbmatrix%7D)

We have:

![Untitled](https://user-images.githubusercontent.com/68278907/93494394-4540ff00-f90d-11ea-8e85-39bcf3449102.png)

Thus, for:

![equation](https://latex.codecogs.com/gif.latex?H%3DC_%7B1%7DX&plus;C_%7B2%7DY&plus;C_%7B3%7DZ&plus;C_%7B4%7DI)


![equation](https://latex.codecogs.com/gif.latex?H%3DX&plus;2Z&plus;I)

<h2>Selecting an Ansatz</h2>

Selecting an Asatz is heuristic, meaning it is something that is to be discovered for each VQE, usually based on intiution or trial-and-error.

That being said, we'll start with the ansatz RY(θ), as it will allow us to view the states cos|θ>+sin(θ)|1>.

<h2>Quantum Circuit</h2>

The Hamiltonian Polynomial is required, as the parts dictate the required gates:

- For X, the gate __RY(−π/2)__ is applied.
- For Y, __RX(π/2)__ is applied.
- For Z, no gate is applied.
- For I, no gate is applied.

__Example:__

For H = X + 2Z + I, calculate the expectatiobn state, __<ψ| H |ψ> = E(ψ)__.

We start by choosing random parameters, say θ = 0 and θ = π.

- For θ = 0: 

__Calculating <H<sub>Z</sub>>__

Prepare the quantum state |ψ> using our ansatz:

![Untitled](https://user-images.githubusercontent.com/68278907/93479814-0c009300-f8fd-11ea-8360-9b068468e2a8.png)

Calculating the expectation value considering the computational basis (Z-Axis):

![Untitled](https://user-images.githubusercontent.com/68278907/93480009-42d6a900-f8fd-11ea-9978-fd43dd3ba60b.png)

__Calculating <H<sub>X</sub>>__

Prepare the quantum state |ψ'> using our ansatz and rotate it −π/2 (90 degrees) around the Y-Axis to align it with the computational basis (Z-Axis).

![Untitled](https://user-images.githubusercontent.com/68278907/93480574-e3c56400-f8fd-11ea-826e-466a412161bf.png)

Calculate the expectation value considering the computational basis (Z-Axis):

![Untitled](https://user-images.githubusercontent.com/68278907/93480744-10797b80-f8fe-11ea-85cb-2ca6c4dfaf97.png)

Sum all components for the whole expectation value <H>. The expectation value of the identity matrix <H<sub>I</sub>> is 1 therefore:

![Untitled](https://user-images.githubusercontent.com/68278907/93480956-52a2bd00-f8fe-11ea-99bc-6e054c82a71b.png)

- For θ = π: 

__Calculating <H<sub>Z</sub>>__

Prepare the quantum state |ψ> using our ansatz:

![Untitled](https://user-images.githubusercontent.com/68278907/93483796-79aebe00-f901-11ea-8fe8-a391a90de416.png)

Calculate the expectation value considering the computational basis (Z-Axis).

![Untitled](https://user-images.githubusercontent.com/68278907/93483947-a367e500-f901-11ea-8743-725a65b7901b.png)

__Calculate <H<sub>X</sub>__

Prepare the quantum state |ψ'> using our ansatz and rotate it −π/2 (90 degrees) around the Y-Axis to align it with the computational basis (Z-Axis).

![Untitled](https://user-images.githubusercontent.com/68278907/93484252-fb9ee700-f901-11ea-897b-f02f23f830a1.png)

Calculate the expectation value considering the computational basis (Z-Axis)

![Untitled](https://user-images.githubusercontent.com/68278907/93484502-4456a000-f902-11ea-8a6c-5a40b88faef5.png)

Sum all components for the whole expectation value <H>. The expectation value of the identity matrix <H<sub>I</sub>> is 1 therefore:

![Untitled](https://user-images.githubusercontent.com/68278907/93484720-8c75c280-f902-11ea-9b7b-d96b60259bd8.png)
