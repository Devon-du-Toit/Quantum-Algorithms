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






```python
circuit.h(qr[2])
circuit.barrier()
```





```python
circuit.cx(qr[0], qr[2])
circuit.cx(qr[1], qr[2])
circuit.barrier()
```





```python
circuit.h(qr[0])
circuit.h(qr[1])
```






```python
circuit.measure(qr[0], cr[0])
circuit.measure(qr[1], cr[1])
```






```python
circuit.draw(output='mpl')
```




![output_10_0](https://user-images.githubusercontent.com/68278907/87566788-c4bf1180-c6c3-11ea-947f-580450baa5e6.png)





```python
simulator = Aer.get_backend('qasm_simulator')
result = execute(circuit, backend = simulator, shots=1024).result()
from qiskit.tools.visualization import plot_histogram
```


```python
plot_histogram(result.get_counts(circuit))
```



![output_12_0](https://user-images.githubusercontent.com/68278907/87566832-d3a5c400-c6c3-11ea-8af5-940957b30e58.png)





```python

```
