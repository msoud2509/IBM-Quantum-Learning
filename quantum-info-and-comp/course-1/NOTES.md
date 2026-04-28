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
    - if a quantum state is not a producrt state, it is an entangled state (cannot be written as a tensor product of two quantum states), quick way to check for entangled with 2 qubits is if ad != bc
    - bell basis: 4 entanled states of two qubits, basis for entire two qubit state space
    - measuring a combination of systems is the same as measuring each system separately,
    - when you measure just one system, the other system is somewhat collapsed (collapses into a single vector)
    combined action of two or more unitary operations is the tensor product of the two or more unitary operations, which is also a unitary operation

## Quantum Circuits
- circuits are essentially just models of computation
- sequence of operations (time goes left to right, acyclic) applied to a quantum state
- wires carry information, gates represent ops
    - in quantum circuits specifically, wires represent qubits, and gates represent unitary operations and measurements
- ops in circuit are opposite in order to how you multiply the matrices (remember matrix mult rules)
- ket+ and ket- are an orthonormal basis for the 2-dim space corresponding to a single qubit
    - bell basis is an orthonormal basis for the 4 dimensional space corresponding to 2 qubits
- a square matrix is called a 'projection' if both are true:
    1. it equals its conjugate transpose
    2. it equals its square (A = AA)
- every projective measurement can be implemented using unitary ops and standard basis measurements
- Global Phase: if two quantum state vectors differ by complex number multiple, then they differ by a 'global phase'
    - since quantum state vectors have euclidean norm of 1, that meanst that this complex number has abs of 1
    - this means taht tow quantum state vectors that differ by a global phase are completely indistinguishable and are considered equivalent
- Relative phase: if you just change the sign of one of the components of the ket0 or ket1, these are distinguishable
- non-cloning thrm: there is no unitary operation to get a copy of an arbritrary quantum state vector
- Discriminating: it is only possible to perfectly discrimate phi and psi if they are orthogonal quantum state

## Entanglement in Action
- an entangled state can be viewed as one e-bit
- **Quantum Teleportation**
    - protocol to send quantum information (only uses entanglement and classical communication to send info)
    - no cloning theorem: once qubit has been sent, sender no longer has it
    - important that no information about the qubit info being sent can be measured (ie in the example prob is 1/4 for every possibility of 2 qubits)

- **Superdense Coding**
    - holevo's thrm: two classical bits cannot be transmitted by a single qubit alone (need to use e-bits)
    - a gate seemingly acting on a single qubit that makes up an entangled state will actually modify the entire e-bit
        - remember that entangled qubits don't have individual identities
    - in superdense coding, the reciever can derive the two classical bits that are being sent based on the resulting bell state

- **The CHSH Game**
    - nonlocal game, two cooperative players that cannot communicate with each other
    - how game is defined = how referee is defined
    - in CHSH game, referee sends out questions
        - a question is 2 bits, and are chosen uniformly at random
        - players respond with their own bits, and the players win if the exclusive or of their answer bits equals the logical AND of the question bits
    - with the nature of the rules here, the players cannot simply use a function of the inputs (deterministic strategy) to guarantee a win (think about why)
    - probabilistic strategy doesn't do any better, as probabilistic strategies are essentially just randomly choosing deterministic strategies




    

