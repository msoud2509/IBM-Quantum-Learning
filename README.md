# IBM Quantum Learning
This repository contains Jupyter notebooks that follow my understanding of the material of the courses from [**IBM Quantum Learning**](https://quantum.cloud.ibm.com/learning/en)

This repo covers the following courses:
1. [**Quantum Information & Computation**](./quantum-info-and-comp)


**NOTE**: Notes and Qiskit code are provided in the notebooks, some material from the IBM courses may be left out, and there may be some extra python code not in the courses, to see the original course material, check out the above link.

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

