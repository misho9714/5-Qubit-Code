# 5-Qubit Quantum Error-Correcting Code (Perfect Code)

This notebook simulates the **[[5,1,3]] quantum error-correcting code**, also known as the *perfect code*.  
It demonstrates how a single logical qubit can be protected against **any single-qubit error**.

## Contents
- **Logical State Encoding** – prepares logical $|0_L\rangle, |1_L\rangle, |+_L\rangle, |-_L\rangle$ states  
- **Syndrome Extraction** – measures stabilizer generators using 4 ancilla qubits  
- **Error Injection** – applies random Pauli $X, Y, Z$ errors with probability `p`  
- **Syndrome-Based Correction** – decodes the syndrome and applies corrections  
- **Logical Measurement** – checks whether the logical state was successfully recovered  

## Running the Simulation
x1 and x2 select the logical state:
00 → |0>,  
01 → |1>,  
10 → |+> = (|0> + |1>)/√2,  
11 → |-> = (|0> - |1>)/√2

The main function:
```python
run_5q_code(p, x1, x2, shots)



