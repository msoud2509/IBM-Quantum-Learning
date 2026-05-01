# IBM Quantum Learning
This repository contains Jupyter notebooks that follow my understanding of the material of the courses from [**IBM Quantum Learning**](https://quantum.cloud.ibm.com/learning/en)

This repo covers the following courses:
1. [**Quantum Information & Computation**](./quantum-info-and-comp) by John Watrous


**NOTE**: Each course may have its own README to explain the specifics of the course structure.

**NOTE**: Notes and Qiskit code are provided in the notebooks, some material from the IBM courses may be left out (for example, much of the classical information sections will not be included), and there may be some extra python code not in the courses, to see the original course material, check out the above link.

### Remarks on the code in the notebooks
- While we generally order qubits in big-endian order, qiskit does little-endian order, so for example in $|01\rangle$, the first qubit is $|1\rangle$ and the second qubit is $|0\rangle$. This is important for example when demonstrating [controlled-unitary operations](quantum-info-and-comp/course-1/2-multiple-systems/5-unitary-operations.ipynb), and in some other places.

## Setup to run the notebooks
1. Run the below from the root of this repo (only tested for WSL):
```bash
python3 -m venv .venv && source .venv/bin/activate && pip install -r requirements.txt
```

2. Select the venv kernel in Jupyter to run the notebooks, then you are good to go!


To get the latest versions of all dependencies, you can also run the below while in the virtual environment:
```bash
pip install -U -r requirements.txt
```

To exit the virtual environment, simply run:
```bash
deactivate
```

