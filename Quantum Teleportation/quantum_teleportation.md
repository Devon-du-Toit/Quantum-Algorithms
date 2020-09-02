<h1>Quantum Teleportation</h1>

<h3>Problem</h3>
We want to send an unkown state:

![equation](https://latex.codecogs.com/gif.latex?%7C%5Cphi%20%3E_%7Bs%7D%3D%20%5Calpha%20%7C0%3E_%7Bs%7D&plus;%5Cbeta%20%7C1%3E_%7Bs%7D)

from person 1 to person 2. But person 1 may only send 2 classical bits. Both persons share the maximally entangled state:

![equation](https://latex.codecogs.com/gif.latex?%7C%5Cpsi%20%5E%7B00%7D%3E_%7BAB%7D%20%3D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%20%5B%5Calpha%20%7C00%3E_%7BAB%7D%20&plus;%20%5Cbeta%20%7C11%3E_%7BAB%7D%5D)

<br>
<br>

<h3>Initial State of System</h3>
  
![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%26%7B%7D%7C%5Cphi%3E_%7Bs%7D%20%5Cotimes%20%5C%20%7C%5Cpsi%20%5E%7B00%7D%3E_%7BAB%7D%20%5C%5C%20%26%7B%7D%3D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%7D%7D%20%5B%5Calpha%20%7C000%3E_%7BSAB%7D%20&plus;%20%5Calpha%20%7C011%3E_%7BSAB%7D&plus;%20%5Cbeta%20%7C100%3E_%7BSAB%7D%20&plus;%20%5Cbeta%20%7C111%3E_%7BSAB%7D%5D%20%5Cend%7Balign*%7D)

We may rewrite this as:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%26%7B%7D%3D%5Cfrac%7B1%7D%7B2%5Csqrt%7B2%7D%7D%5B%28%7C00%3E_%7BSA%7D&plus;%7C11%3E_%7BSA%7D%29%20%5Cotimes%20%28%5Calpha%7C0%3E_%7BB%7D&plus;%5Cbeta%7C1%3E_%7BB%7D%29&plus;%28%7C01%3E_%7BSA%7D&plus;%7C10%3E_%7BSA%7D%29%20%5Cotimes%20%28%5Calpha%7C1%3E_%7BB%7D%20&plus;%20%5Cbeta%7C0%3E_%7BB%7D%29%20%5C%5C%20%26%7B%7D&plus;%28%7C00%3E_%7BSA%7D-%7C11%3E_%7BSA%7D%29%20%5Cotimes%20%28%5Calpha%7C0%3E_%7BB%7D-%5Cbeta%7C1%3E_%7BB%7D%29&plus;%28%7C01%3E_%7BSA%7D-%7C10%3E_%7BSA%7D%29%20%5Cotimes%20%28%5Calpha%7C1%3E_%7BB%7D-%5Cbeta%7C0%3E_%7BB%7D%29%5D%20%5Cend%7Balign*%7D)

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%26%7B%7D%3D%5Cfrac%7B1%7D%7B2%7D%5B%7C%5Cpsi%5E%7B00%7D%3E_%7BSA%7D%20%5Cotimes%20%5C%20%7C%5Cphi%3E_%7BB%7D%20&plus;%20%7C%5Cpsi%5E%7B01%7D%3E_%7BSA%7D%20%5Cotimes%20%5C%20%5Csigma_%7Bx%7D%7C%5Cphi%3E_%7BB%7D%20%5C%5C%20%26%7B%7D&plus;%20%7C%5Cpsi%5E%7B10%7D%3E_%7BSA%7D%20%5Cotimes%20%5C%20%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%20&plus;%20%7C%5Cpsi%5E%7B11%7D%3E_%7BSA%7D%20%5Cotimes%20%5C%20%5Csigma_%7Bx%7D%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%5D%20%5Cend%7Balign*%7D)

<br>
<br>

<h3>Protocol</h3>

![trans](https://user-images.githubusercontent.com/68278907/91061231-36c43800-e62c-11ea-8e71-058899a0a5a1.png)

__Steps__:

Person 1 Does a Bell Measurement on S&A:

By refering to the above equation, Person 1 will know that they may measure for themselves and Person 2:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Balign*%7D%20%26%20Person%20%5C%201%20%26%20Person%20%5C%202%5C%5C%20%26%20%7C%5Cpsi%5E%7B00%7D%3E%20%26%20%7C%5Cphi%3E_%7BB%7D%5C%5C%20%26%20%7C%5Cpsi%5E%7B01%7D%3E%20%26%20%5Csigma_%7Bx%7D%7C%5Cphi%3E_%7BB%7D%5C%5C%20%26%20%7C%5Cpsi%5E%7B10%7D%3E%20%26%20%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%5C%5C%20%26%20%7C%5Cpsi%5E%7B11%7D%3E%20%26%20%5Csigma_%7Bx%7D%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%20%5Cend%7Balign*%7D)

Person 1 then send the classical bits *i, j* to Person 2:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Bvmatrix%7D%20%26%20Person%20%5C%201%20%26%20Person%20%5C%202%20%26%20Bits%20%5C%20sent%20%26%20%5C%5C%20%26%20%7C%5Cpsi%5E%7B00%7D%3E%20%26%20%7C%5Cphi%3E_%7BB%7D%20%26%2000%5C%5C%20%26%20%7C%5Cpsi%5E%7B01%7D%3E%20%26%20%5Csigma_%7Bx%7D%7C%5Cphi%3E_%7BB%7D%20%26%2001%5C%5C%20%26%20%7C%5Cpsi%5E%7B10%7D%3E%20%26%20%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%20%26%2010%5C%5C%20%26%20%7C%5Cpsi%5E%7B11%7D%3E%20%26%20%5Csigma_%7Bx%7D%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%20%26%2011%20%5Cend%7Bvmatrix%7D)

Person 2 then applies the Pauli gates on their qubit:

![equation](https://latex.codecogs.com/gif.latex?%5Cbegin%7Bvmatrix%7D%20%26%20Person%20%5C%201%20%26%20Person%20%5C%202%20%26%20Bits%20%5C%20sent%20%26%20Person%20%5C%202%20%5C%20State%5C%5C%20%26%20%7C%5Cpsi%5E%7B00%7D%3E%20%26%20%7C%5Cphi%3E_%7BB%7D%20%26%2000%20%26%20%7C%5Cphi%3E_%7BB%7D%5C%5C%20%26%20%7C%5Cpsi%5E%7B01%7D%3E%20%26%20%5Csigma_%7Bx%7D%7C%5Cphi%3E_%7BB%7D%20%26%2001%20%26%20%7C%5Cphi%3E_%7BB%7D%5C%5C%20%26%20%7C%5Cpsi%5E%7B10%7D%3E%20%26%20%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%20%26%2010%20%26%20%7C%5Cphi%3E_%7BB%7D%5C%5C%20%26%20%7C%5Cpsi%5E%7B11%7D%3E%20%26%20%5Csigma_%7Bx%7D%5Csigma_%7Bz%7D%7C%5Cphi%3E_%7BB%7D%20%26%2011%20%26%20%7C%5Cphi%3E_%7BB%7D%20%5Cend%7Bvmatrix%7D)

Person 1's state has collapsed during measurement and therefore doesn't have the state |ϕ> anymore, but they sent their state to Person 2.

__Circuit:__

![Untitled](https://user-images.githubusercontent.com/68278907/91714550-4f80a080-eb8c-11ea-986a-58bc97addfc0.png)

for initial q0 the initial state to be transported, and q2 final the transported state.


