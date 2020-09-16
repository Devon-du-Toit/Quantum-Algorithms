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

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7B*align%7D%20%26%7B%7D%20c_%7B1%7D%3D%5Cfrac%7BH_%7B2%7D&plus;H_%7B3%7D%7D%7B2%7D%5C%5C%20%5C%5C%20%26%7B%7D%20c_%7B2%7D%3D%5Cfrac%7BH_%7B1%7D&plus;H_%7B4%7D%7D%7B2%7D-H_%7B4%7D%5C%5C%20%5C%5C%20%26%7B%7D%20c_%7B3%7D%3D%5Cfrac%7BH_%7B3%7D%20-%20%5Cfrac%7BH_%7B2%7D&plus;H_%7B3%7D%7D%7B2%7D%7D%7Bi%7D%5C%5C%20%5C%5C%20%26%7B%7D%20c_%7B4%7D%3D%5Cfrac%7BH_%7B1%7D&plus;H_%7B4%7D%7D%7B2%7D%20%5Cend%7B*align%7D)