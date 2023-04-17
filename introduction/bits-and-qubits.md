# Bits and Qubits

## Bit

A **bit**, short for "binary digit," is the most basic unit of information in digital computing and communication systems. It represents data in a binary system consisting of only two possible values: 0 (zero) or 1 (one). Depending on the context, these two values can symbolize various concepts, such as on/off, true/false, or yes/no.

For the purposes of quantum computing, we will be representing the bits as matrices. Here are the bits 0 and 1 in matrix form:

$$
\ket{0} =
\begin{bmatrix}
1 \\
0
\end{bmatrix}
\\
-----
\\
\ket{1} =
\begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

## Qubit

**A qubit**, short for "quantum bit," is the fundamental unit of quantum information. It is the quantum analog of a classical bit in the context of quantum computing. While classical bits represent information as 0 or 1, qubits take advantage of the principles of quantum mechanics, such as superposition and entanglement, to represent information in more complex ways.

A qubit can exist in a linear combination of the basis states |0⟩ and |1⟩, also known as a superposition. Mathematically, a qubit's state can be represented as:

$$
\ket{\psi} = \alpha\ket{0} + \beta\ket{1}
$$

Here, α and β are complex numbers, and the probabilities of measuring the qubit in the |0⟩ or | the squared magnitudes of the respective coefficients give 1⟩ states. Notably, the probabilities must sum to 1

$$
|\alpha|^2 + |\beta|^2 = 1
$$

The ability of qubits to exist in superpositions allows quantum computers to perform certain calculations and simulations much more efficiently than classical computers. Additionally, quantum entanglement between qubits enables powerful quantum algorithms and protocols, such as quantum teleportation and quantum key distribution.&#x20;
