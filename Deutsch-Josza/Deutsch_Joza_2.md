```python
from qiskit import *
```


```python
qr = QuantumRegister(3)
```


```python
cr = ClassicalRegister(2)
```


```python
circuit = QuantumCircuit(qr, cr)
```


```python
%matplotlib inline
```


```python
circuit.h(qr[0])
circuit.h(qr[1])
circuit.x(qr[2])
```




    <qiskit.circuit.instructionset.InstructionSet at 0x7f3686cbbd50>




```python
circuit.h(qr[2])
circuit.barrier()
circuit.barrier()
```




    <qiskit.circuit.instructionset.InstructionSet at 0x7f367a157810>




```python
circuit.h(qr[0])
circuit.h(qr[1])
```




    <qiskit.circuit.instructionset.InstructionSet at 0x7f367a157290>




```python
circuit.measure(qr[0], cr[0])
circuit.measure(qr[1], cr[1])
```




    <qiskit.circuit.instructionset.InstructionSet at 0x7f367a157c90>




```python
circuit.draw(output='mpl')
```




![png](output_9_0.png)




```python
simulator = Aer.get_backend('qasm_simulator')
result = execute(circuit, backend = simulator, shots=1024).result()
from qiskit.tools.visualization import plot_histogram
```


```python
plot_histogram(result.get_counts(circuit))
```




![png](output_11_0.png)




```python

```
