# IBM Quantum Learning
This repository contains Jupyter notebooks (along with some personal notes) with the Qiskit implementations of the concepts covered in the course series, [Quantum Information & Computation](https://quantum.cloud.ibm.com/learning/en) by John Watrous.

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

