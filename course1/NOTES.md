# Basics on Quantum Information

## Single Systems 
- **Classical state**
    - An intuitive but incorrect way to think about measuring a system is that the system already was in a state regardless of the measurement. 
    - However, the correct way to think about it is that the classical (measured) state is chosen at random according to the probabilistic state.
    - Probablistic state = probability of being in the specified classical state.
    - Deterministic functions: converts classical state a into f(a) for each a in $\Sigma$
        - M(row, col) = 1 if row = f(col), 0 otherwise
    - Dirac notation:
        - Ket: ket is column vector, denoted as |x⟩
        - Bra: bra is row vector, denoted as ⟨x|
        - Inner product: ⟨x|y⟩ = 1 if x=y, 0 otherwise
    - Stochistic matrix: each column is a probability vector (sum of each column is 1)
    - NOTE: matrix multiplication is associative, but not commutative
- **Quantum state**
    - A quantum state is a column vector where its indices correspond with the classical state, and the values are complex numbers
        - Sum of the absolute values squared of the entries is 1
    - Euclidean norm is the magnitude of the vector, which is 1 for quantum states (and probabilistic vectors)
    - qubit state vectors means that the classical state of system is 0 or 1
    - bra is the conjugate transpose of the ket
    - there are plus state and minus states (what's the diff?)
    - a matrix is unitary if its inverse is equal to its conjugate transpose
        - another property is that they preserve the euclidean norm of a vector when multiplied by it (i.e. ||Uw|| = ||w||)
        - closed under multiplication: if U and V are unitary, then UV is also unitary
    - hadamard operations (a unitary matrix), transforms |0⟩ into |+⟩ and |1⟩ into |-⟩ and vice versa
        - can be used to tell if the original state was plus or minus state
    - applying unitary operation twice gets you the pauli x gate, which transforms |0⟩ into |1⟩ and |1⟩ into |0⟩

## Multiple Systems
- **Classical state**
    - Classical state set of (X,Y) is the cartesian product, every single combo
        - dictionary ordered (like in python), left is more significant than right
    - statistical independence: the probability of (x,y) is the product of the probabilities of x and y
    - tensor product is representation of statistical indendence in matrix form
        - it is essentially all possible combinations of elements of two vectors multiplied together in one big column vector
        - property: it is bilinear, and scalars float freely
    - measurements of probabilistic states: if you just measure the first system, need to do conditional probability to get the probability of the second system
    - the tensor product of any number of stochastic matrices is also a stochastic matrix
- **Quantum state**
    - tensor product of quantum state vecotrs are also quantum state vectors, the resulting vector representing independence between the original vector systems (tensor product is a quantum state)
    - if a quantum state is not a producrt state, it is an entangled state (cannot be written as a tensor product of two quantum states)
    - bell basis: 4 entanled states of two qubits, basis for entire two qubit state space
    - measuring a combination of systems is the same as measuring each system separately,
    - when you measure just one system, the other system is somewhat collapsed (collapses into a single vector)
    combined action of two or more unitary operations is the tensor product of the two or more unitary operations, which is also a unitary operation

    

