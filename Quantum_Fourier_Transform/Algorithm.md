<h1>Quantum Fourier Transform</h1>

The Quantum Fourier Transform (QFT) is given by:

![QFT](https://user-images.githubusercontent.com/68278907/88466718-8ac5ea80-cecf-11ea-9929-ae064d0d5a90.jpg)

where  __*N = 2<sup>n</sup>*__, __*n*__ is the number of qubits and __*y*__ may be given by:

![sigma_y](https://user-images.githubusercontent.com/68278907/88466893-4a676c00-ced1-11ea-87d9-8aeaf6af33ea.jpg)

Substituting this into the original QFT we have:

![qft_ex2](https://user-images.githubusercontent.com/68278907/88467074-4b010200-ced3-11ea-8453-df73753ef091.jpg)

which further reduces to our final expression:

![qft_f](https://user-images.githubusercontent.com/68278907/88467208-db8c1200-ced4-11ea-8a0d-e2cf84b9d8cb.jpg)

<h2>The Quantum Circuit</h2>

The QFT may be implimented by using two types of gates, the single-qubit Hadamard __*H*__ and the controlled rotation __*CROT<sub>k</sub>*__ gate. The Hadamard __*H*__ is given by:

![hadamard](https://user-images.githubusercontent.com/68278907/88467338-628dba00-ced6-11ea-961e-b2cc3ec29f60.jpg)

while the controlled rotation __*CROT<sub>k</sub>*__:

![crot](https://user-images.githubusercontent.com/68278907/88467385-dcbe3e80-ced6-11ea-80f8-80d3540a653c.jpg)

The action of CROTk on the two-qubit state |xjxk⟩ where the first qubit is the control and the second is the target is given by
For a two-qubit state __*|x<sub>j</sub>x<sub>k</sub>*__ where __*x<sub>j</sub>*__ is the control, the controlled rotation has the effect __*CROT<sub>k</sub> |0x<sub>j</sub>>=|0*__0x<sub>j</sub>>.

