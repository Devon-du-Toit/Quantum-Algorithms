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

For a two-qubit state __*|x<sub>j</sub>x<sub>k</sub>>*__ where __*x<sub>j</sub>*__ is the control, the controlled rotation has the effect 

![crot_3](https://user-images.githubusercontent.com/68278907/88467533-586cbb00-ced8-11ea-9a3b-598e8a7772d0.jpg)

and

![crot_2](https://user-images.githubusercontent.com/68278907/88467513-2c513a00-ced8-11ea-909f-97e3f640e81b.jpg)

The circuit is composed as:

![qft_circ](https://user-images.githubusercontent.com/68278907/88478189-60fbda80-cf46-11ea-8218-346bf370ec94.png)


The steps are as follow:

1. A Hadamard is applied to qubit 1:

![had](https://user-images.githubusercontent.com/68278907/88478244-f7300080-cf46-11ea-8dd7-4dfc28a10ee9.png)

2. The Unitary Rotation __*UROT<sub>2</sub>*__ is applied to qubit 1 with qubit 2 as control:

![urot2](https://user-images.githubusercontent.com/68278907/88478315-ac62b880-cf47-11ea-81d9-57dd4785ed84.png)

3. After the application of the last UROTn gate on qubit 1 controlled by qubit n, the state becomes 

The state of qubit 1 after all the applied __*UROT<sub>n</sub>*__ gates:

![urotn](https://user-images.githubusercontent.com/68278907/88478385-13806d00-cf48-11ea-886a-2db543b558e0.png)

if we consider that __*x = [2<sup>n-1</sup>x<sub>1</sub>+2<sup>n-2</sup>x<sub>2</sub>+...+2<sup>1</sup>x<sub>n-1</sub>+2<sup>0</sup>x<sub>n</sub>]*__, the above expression reduces to:

![red_urot](https://user-images.githubusercontent.com/68278907/88478477-f5ffd300-cf48-11ea-9ff4-d62100a93361.png)

4. Applying a similar repition of gte upon qubits 2 to qubits n, we have the final state, or QFT:

![qft_ur](https://user-images.githubusercontent.com/68278907/88478562-cc937700-cf49-11ea-8c7e-ec0450071d38.png)
