# 5-Qubit Quantum Error-Correcting Code (Perfect Code)

This notebook simulates the **[[5,1,3]] quantum error-correcting code**, also known as the *perfect code*.  
It demonstrates how a single logical qubit can be protected against **any single-qubit error**.

## Contents
- **Logical State Encoding** – prepares logical $|0_L\rangle, |1_L\rangle, |+_L\rangle, |-_L\rangle$ states  
- **Syndrome Extraction** – measures stabilizer generators using 4 ancilla qubits  
- **Error Injection** – applies random Pauli $X, Y, Z$ errors with probability `p`  
- **Syndrome-Based Correction** – decodes the syndrome and applies corrections  
- **Logical Measurement** – checks whether the logical state was successfully recovered  

## References
- The encoding circuit used in this notebook is based on the construction from the paper:
"Natural 5-Qubit Encoding for Robust Single-Qubit Gates" (arXiv:2410.06375).
- The rest of the implementation is based on the 5-qubit code description from the Wikipedia article:
https://en.wikipedia.org/wiki/Five-qubit_error_correcting_code

## Running the Simulation
x1 and x2 select the logical state:  
00 → $|0_L\rangle$  
01 → $|1_L\rangle$  
10 → $|+_L\rangle$  
11 → $|-_L\rangle$  

The main function:
```python
run_5q_code(p, x1, x2, shots)



