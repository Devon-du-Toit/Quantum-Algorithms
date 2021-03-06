<h1> Deutsch-Josza Algorithm </h1>

</br></br>

<h2>Problem</h2>
  
Consider being given some hidden Boolean function __*f*__ where __*f(x<sub>1</sub>, x<sub>2</sub>, ..., x<sub>n</sub>)*__ maps onto either __*0*__ or __*1*__. </br></br>
Although hidden, the function is known to be either balanced or constant. This implies that the function __*f*__, if given a binary string of length __*n*__, for all possible inputs either returns a specific value (it could only be __1__ or __0__) or it returns exactly half of all the answers as __0__ and exactly half of the other answers as __1__.
</br>
</br>
We are asked to determine whether __*f*__ is balanced or constant.

</br></br>

<h2>Classical Solution</h2>

The solution may be found in the best case by evaluating __*f*__ with different values twice. If the two answers are not the same we know that __*f*__ is balanced.

In the worst case we wil need to evaluate __*f*__ a total of __*2 <sup>n</sup> + 1*__ times to ensure it is constant.

</br></br>

<h2>Quantum Solution</h2>

The solution to this problem may be found with only __*1*__ iteration using a quantum computer.

</br>

__The Algorithm__

1. Setup __*n + 1*__ qubits, initialised to __|0>__, except for the last qubit, which is initialised to __*|1>*__.
2. Let all the __*|0>*__ qubits be considered the binary input string and the __*|1>*__ qubit be considered the output.
3. Apply a Hadamard Gate over every qubit register.
4. Apply __*f*__ (A.K.A the oracle) over every qubit.
5. Apply a Hadamard to every qubit, except for the last.
6. Measure each qubit, except for the last. If all the measurements are in state __*|1>*__ the function is balanced. If all measured states are __*|0>*__ the function is constant.

</br>

__The Quantum Circuit__

![Deutsch_Josza_Circuit_1](https://user-images.githubusercontent.com/68278907/87480376-7b23e780-c62d-11ea-9c27-9f398ef2e6ee.jpg)

__The unkown function/Oracle__

Although the initial problem is to solve an unkown function setup, we need to paradoxically know what the function is for us to build it's circuit.

For a __constant__ function: The output will be a constant (e.g. f(x) = 1), so we may omit any gate within the oracle, as the output is independent of the input. This is due to the fact that for a constant function, the input qubits and quantum states are not effected.
![Deutsch_Josza_Circuit_2](https://user-images.githubusercontent.com/68278907/87480256-3bf59680-c62d-11ea-807b-09c4244fcf6c.jpg)

For a __*balanced*__ function: A CNOT on input qubits and output qubit as target will simulate a balanced function.
![Deutsch_Josza_Circuit_3](https://user-images.githubusercontent.com/68278907/87480932-a22ee900-c62e-11ea-8ddb-9433101368b7.jpg)
</br>
