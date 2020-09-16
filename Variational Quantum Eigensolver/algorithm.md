<h1>Variational Quantum Eigensolver</h1>

<h2>Determining a Hamiltonian Matrix:</h2>

Given a Hamiltonian Polynomial in the form:

![equation](https://latex.codecogs.com/gif.latex?H%3Dc_%7B1%7DXYZ&plus;C_%7B2%7DXYZ&plus;C_%7B3%7DXYZ&plus;C_%7B4%7DI)

for C<sub>1-4</sub> constants and X, Y and Z Pauli matrices of:

![equation](https://latex.codecogs.com/gif.latex?X%3D%5Cbegin%7Bbmatrix%7D%200%20%261%20%5C%5C%201%260%20%5Cend%7Bbmatrix%7D%2C%20Y%3D%5Cbegin%7Bbmatrix%7D%200%20%26-i%20%5C%5C%20i%260%20%5Cend%7Bbmatrix%7D%2C%20Z%3D%5Cbegin%7Bbmatrix%7D%201%20%260%20%5C%5C%200%26-1%20%5Cend%7Bbmatrix%7D)

The Hamiltonian matrix is found by simply substituting the Pauli matrices into the Hamiltonian Polynomial.

__Example__:

![equation](https://latex.codecogs.com/gif.latex?Given%20%5C%20Hamiltonian%20%3A%20%5C%20H%3D2Z&plus;X&plus;I)

We substitute the variables X,Y and Z with their Pauli Matrices:

![equation](https://latex.codecogs.com/gif.latex?H%3D2%5Cbegin%7Bbmatrix%7D%201%20%26%200%5C%5C%200%26-1%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%200%20%26%201%5C%5C%201%260%20%5Cend%7Bbmatrix%7D&plus;%5Cbegin%7Bbmatrix%7D%201%20%26%200%5C%5C%200%261%20%5Cend%7Bbmatrix%7D)

Thus the corresponding Hamiltonian matrix will be:

![equation](https://latex.codecogs.com/gif.latex?H%3D2%5Cbegin%7Bbmatrix%7D%203%20%26%201%5C%5C%201%26-1%20%5Cend%7Bbmatrix%7D)


<h2>Determining a Hamiltonian Polynomial</h2>

Given the Hamiltonian Matrix, the corresponding Polynomial may be determined by decomposing the matrix into Pauli terms.
