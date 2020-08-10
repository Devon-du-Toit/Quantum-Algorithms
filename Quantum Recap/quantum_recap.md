<h1>Quantum recap</h1>
<br>
<br>

__Complex Conjugate__: Let __z__ be a complex number such that __z__ = a + __i__ b for some scalars a, b and imaginary number __i__. The complex conjugate of __z__ will be __z*__ = a -__i__ b.
<br>
<br>

__Dirac Notation__: Let a, b ∈ ℂ<sup>2</sup>. 

![equation](https://latex.codecogs.com/gif.latex?Ket%3A%20%5C%20%7Ca%3E%20%3D%20%5Cbegin%7Bbmatrix%7D%20a_%7B1%7D%5C%5Ca_%7B2%7D%20%5Cend%7Bbmatrix%7D)

![equation](https://latex.codecogs.com/gif.latex?Bra%3A%20%5C%20%3Cb%7C%3D%7Cb%3E%5E%7B%5Cdagger%7D%3D%5Cbegin%7Bbmatrix%7D%20b_%7B1%7D%5E%7B*%7D%20%26%20b_%7B2%7D%5E%7B*%7D%20%5Cend%7Bbmatrix%7D)

![equation](https://latex.codecogs.com/gif.latex?Bra-Ket%20%3A%20%5C%20%3Cb%7Ca%3E%3D%3Ca%7Cb%3E%5E%7B*%7D%3Da_%7B1%7Db_%7B1%7D%5E%7B*%7D&plus;a_%7B2%7Db_%7B2%7D%5E%7B*%7D)

![equation](https://latex.codecogs.com/gif.latex?Ket-Bra%20%3A%20%5C%20%7Ca%3E%3Cb%7C%3D%3Ca%7Cb%3E%5E%7B*%7D%3D%5Cbegin%7Bbmatrix%7D%20a_%7B1%7Db_%7B1%7D%5E%7B*%7D%20%26%20a_%7B1%7Db_%7B2%7D%5E%7B*%7D%5C%5C%20a_%7B2%7Db_%7B1%7D%5E%7B*%7D%20%26%20a_%7B2%7Db_%7B2%7D%5E%7B*%7D%20%5Cend%7Bbmatrix%7D)

<br>
<br>

__Qubit States__:

![equation](https://latex.codecogs.com/gif.latex?%7C0%3E%20%3D%20%5Cbegin%7Bbmatrix%7D%201%5C%5C0%20%5Cend%7Bbmatrix%7D)

![equation](https://latex.codecogs.com/gif.latex?%7C1%3E%20%3D%20%5Cbegin%7Bbmatrix%7D%200%5C%5C1%20%5Cend%7Bbmatrix%7D)

Note that states |0> and |1> are orthogonal:

![equation](https://latex.codecogs.com/gif.latex?%3C0%7C1%3E%20%3D%201%5Ctimes%200%20&plus;%200%20%5Ctimes%201%20%3D%200)


![equation](https://latex.codecogs.com/gif.latex?%7C&plus;%3E%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%28%7C0%3E&plus;%7C1%3E%29%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%5Cbegin%7Bbmatrix%7D%201%5C%5C%201%20%5Cend%7Bbmatrix%7D)

![equation](https://latex.codecogs.com/gif.latex?%7C-%3E%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%28%7C0%3E-%7C1%3E%29%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%5Cbegin%7Bbmatrix%7D%201%5C%5C%20-1%20%5Cend%7Bbmatrix%7D)

All quantum states are normalized:

![equation](https://latex.codecogs.com/gif.latex?%3C%5Cpsi%7C%5Cpsi%3E%20%3D%201)

e.g:

![equation](https://latex.codecogs.com/gif.latex?%7C%5Cpsi%3E%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%28%20%7C0%3E&plus;%7C1%3E%20%29%20%3D%20%5Cbegin%7Bbmatrix%7D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%5C%5C%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%20%5Cend%7Bbmatrix%7D)

![equation](https://latex.codecogs.com/gif.latex?%3C%5Cpsi%7C%5Cpsi%3E%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%20%5Ctimes%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%20&plus;%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%20%5Ctimes%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%20%3D%201)


<br>
<br>

__Born Rule__: The probability that a state |Ψ> collapse during a measurement onto the basis {|x>,|x<sup>⊥</sup>} to the state |x> is:

![equation](https://latex.codecogs.com/gif.latex?P%28x%29%3D%5Cleft%20%7C%20%3Cx%7C%5Cpsi%3E%20%5Cright%20%7C%5E%7B2%7D)

where the sum of all probabilities adds up to 1:

![equation](https://latex.codecogs.com/gif.latex?%5Csum_%7Bi%7DP%28x_%7Bi%7D%29%3D1)

example:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%7C%5Cpsi%3E%20%3D%5Cfrac%7B1%7D%7B%5Csqrt%7B3%7D%7D%28%7C0%3E&plus;%5Csqrt%7B2%7D%20%5C%20%7C1%3E%29%2C%20%5C%20measured%20%5C%20in%20%5C%20basis%20%5C%20%5C%7B%20%7C0%3E%2C%7C1%3E%20%5C%7D.%20%5C%20Determine%20%5C%20P%280%29.%20%5Cend%7Balign*%7D)

solution:

![equation](https://latex.codecogs.com/gif.latex?%7C%3C0%7C%5Cpsi%3E%7C%5E%7B2%7D%20%3D%20%7C%3C0%20%5C%20%7C%20%5C%20%5Cfrac%7B1%7D%7B%5Csqrt%7B3%7D%7D%28%7C0%3E&plus;%5Csqrt%7B2%7D%7C1%3E%29%3E%7C%5E%7B2%7D)

![equation](https://latex.codecogs.com/gif.latex?%3D%7C%5Cfrac%7B1%7D%7B%5Csqrt%7B3%7D%7D%3C0%7C0%3E&plus;%5Cfrac%7B%5Csqrt%7B2%7D%7D%7B%5Csqrt%7B3%7D%7D%3C0%7C1%3E%7C%5E%7B2%7D)

![equation](https://latex.codecogs.com/gif.latex?%3D%7C%5Cfrac%7B1%7D%7B%5Csqrt%7B3%7D%7D&plus;0%7C%5E%7B2%7D%3D%5Cfrac%7B1%7D%7B3%7D)

example 2:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20What%5C%20is%5C%20the%5C%20probability%5C%20to%5C%20measure%5C%20state%5C%20%7C&plus;%3E%20%5C%20for%20%5C%5C%20%7C%5Cpsi%3E%3D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%28%7C0%3E-%7C1%3E%29%5Cend%7Balign*%7D)

solution:

![equation](https://latex.codecogs.com/gif.latex?%7C%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%3C0%7C0%3E%20-%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%3C0%7C1%3E%20&plus;%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%3C1%7C0%3E%20-%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%3C1%7C1%3E%20%7C%5E%7B2%7D)

![equation](https://latex.codecogs.com/gif.latex?%3D%7C%5Cfrac%7B1%7D%7B2%7D%3C0%7C0%3E-%5Cfrac%7B1%7D%7B2%7D%3C1%7C1%3E%7C%5E%7B2%7D)

![equation](https://latex.codecogs.com/gif.latex?%3D%20%5Cfrac%7B1%7D%7B4%7D%7C1-1%7C%5E%7B2%7D%3D0)

<br>
<br>

__Bloch Sphere__: we can write any normalized (pure) state as:

![equation](https://latex.codecogs.com/gif.latex?%7C%5Cpsi%3E%3Dcos%5Cfrac%7B%5CTheta%20%7D%7B2%7D%7C0%3E&plus;e%5E%7Bi%5Cvarphi%20%7Dsin%5Cfrac%7B%5CTheta%20%7D%7B2%7D%7C1%3E)

where:

![equation](https://latex.codecogs.com/gif.latex?%5Cvarphi%20%5C%20%5Cepsilon%20%5C%20%5B0%2C%20%5C%202%5Cpi%5D)

describes the relative phase, and:

![equation](https://latex.codecogs.com/gif.latex?%5Ctheta%20%5C%20%5Cepsilon%20%5C%20%5B0%2C%20%5C%20%5Cpi%5D)

determines the probability to measure |0> or |1>. All the normalized (pure) states may be illustrated on the surface of a sphere with radius __1__. The coordinates of such a state is given by:

![equation](https://latex.codecogs.com/gif.latex?%5Coverrightarrow%7Br%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%20sin%5Ctheta%20cos%5Ctheta%20%5C%5C%20sin%5Ctheta%20sin%5Cvarphi%20%5C%5C%20cos%5Ctheta%20%5Cend%7Bbmatrix%7D)

![bloch](https://user-images.githubusercontent.com/68278907/89809711-4166d380-db3c-11ea-829f-57add953ca15.png)

for |0>:

![equation](https://latex.codecogs.com/gif.latex?%7C0%3E%20%3A%20%5Ctheta%3D0%20%5C%20%2C%20%5Cvarphi%20%3D%20arbitrary.%20%5Coverrightarrow%7Br%7D%3D%5Cbegin%7Bbmatrix%7D%20sin0%20cos%5Cvarphi%5C%5C%20sin0%20sin%5Cvarphi%5C%5C%20cos0%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%200%5C%5C%200%5C%5C%201%20%5Cend%7Bbmatrix%7D)

for |1>:

![equation](https://latex.codecogs.com/gif.latex?%7C1%3E%20%3A%20%5Ctheta%3D%5Cpi%20%5C%20%2C%20%5Cvarphi%20%3D%20arbitrary.%20%5Coverrightarrow%7Br%7D%3D%5Cbegin%7Bbmatrix%7D%20sin%5Cpi%20cos%5Cvarphi%5C%5C%20sin%5Cpi%20sin%5Cvarphi%5C%5C%20cos%5Cpi%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%200%5C%5C%200%5C%5C%20-1%20%5Cend%7Bbmatrix%7D)

for |+>:

![equation](https://latex.codecogs.com/gif.latex?%7C&plus;%3E%20%3A%20%5Ctheta%3D%5Cfrac%7B%5Cpi%7D%7B2%7D%20%5C%20%2C%20%5Cvarphi%20%3D%200.%20%5Coverrightarrow%7Br%7D%3D%5Cbegin%7Bbmatrix%7D%20sin%5Cfrac%7B%5Cpi%7D%7B2%7D%20cos%5C0%5C%5C%20sin%5Cfrac%7B%5Cpi%7D%7B2%7D%20sin0%5C%5C%20cos%5Cfrac%7B%5Cpi%7D%7B2%7D%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%201%5C%5C%200%5C%5C%200%20%5Cend%7Bbmatrix%7D)

for |->:

![equation](https://latex.codecogs.com/gif.latex?%7C-%3E%20%3A%20%5Ctheta%3D%5Cfrac%7B%5Cpi%7D%7B2%7D%20%5C%20%2C%20%5Cvarphi%20%3D%20%5Cpi.%20%5Coverrightarrow%7Br%7D%3D%5Cbegin%7Bbmatrix%7D%20sin%5Cfrac%7B%5Cpi%7D%7B2%7D%20cos%5Cpi%5C%5C%20sin%5Cfrac%7B%5Cpi%7D%7B2%7D%20sin%5Cpi%20%5C%5C%20cos%5Cfrac%7B%5Cpi%7D%7B2%7D%20%5Cend%7Bbmatrix%7D%20%3D%20%5Cbegin%7Bbmatrix%7D%20-1%5C%5C%200%5C%5C%200%20%5Cend%7Bbmatrix%7D)
