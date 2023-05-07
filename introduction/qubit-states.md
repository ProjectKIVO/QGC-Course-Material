# Qubit States

### Common Qubit States

As we have seen the the [qubit-representation.md](qubit-representation.md "mention") section, qubits can exist in multiple states beyond 0s and 1s. The **6** commonly found qubit states are:

* Basis states:&#x20;
  * |0⟩: The computational basis state representing 0.
  * |1⟩: The computational basis state representing 1.
* Superposition states:
  * |+⟩: The equal superposition state.
  * \|-⟩: The equal superposition state with a relative phase of π.
* Circular states:
  * |i+⟩: The equal superposition state with a relative phase of π/2.&#x20;
  * |i-⟩: The equal superposition state with a relative phase of -π/2.

{% hint style="info" %}
The two circular states can be referred to as  "right-circular" and "left-circular" states. In this context, the states can be denoted as:

* |i+⟩: Right-circular or clockwise-circular state, also written as |R⟩ or |C⟩.
* |i-⟩: Left-circular or counter-clockwise circular state, also written as |L⟩ or |CC⟩.
{% endhint %}

### Matrix Repersentation

#### Basis States:

$$
|0\rangle = \begin{bmatrix}
1 \\
0
\end{bmatrix}\;\;\;\;\; |1\rangle = \begin{bmatrix}
0 \\
1
\end{bmatrix}
$$

#### Superposition States:

$$
|+\rangle = \begin{bmatrix}
\frac{1}{\sqrt{2}} \\
\frac{1}{\sqrt{2}}
\end{bmatrix}
\;\;\;\;\; 
|-\rangle = \begin{bmatrix}
\frac{1}{\sqrt{2}} \\
-\frac{1}{\sqrt{2}}
\end{bmatrix}
$$

#### Circular States:

$$
|i+\rangle = \begin{bmatrix}
\frac{1}{\sqrt{2}} \\
\frac{i}{\sqrt{2}}
\end{bmatrix}

\;\;\;\;\; 
|i-\rangle = \begin{bmatrix}
\frac{1}{\sqrt{2}} \\
-\frac{i}{\sqrt{2}}
\end{bmatrix}
$$

### Example Code

{% tabs %}
{% tab title="Qiskit" %}
{% hint style="info" %}
You can find information on quantum circuits over at [quantum-circuit.md](quantum-circuit.md "mention").
{% endhint %}

```python
# Import dependency
from qiskit import QuantumRegister
from qiskit import QuantumCircuit

# Initialize 6 qubits
qubits = QuantumRegister(6)

# Initialize a quantum circuit
circuit = QuantumCircuit(qubits)

# |0⟩ state
circuit.initialize('0', qubits[0])

# |1⟩ state
circuit.initialize('1', qubits[1])

# |+⟩ state
circuit.initialize('+', qubits[2])

# |-⟩ state
circuit.initialize('-', qubits[3])

# |i⟩ state
circuit.initialize('r', qubits[4])

# |-i⟩ state
circuit.initialize('l', qubits[5])
```
{% endtab %}

{% tab title="Q#" %}
{% hint style="info" %}
In Q#, there isn't a direct built-in function to initialize the qubits into the six states, and therefore needs to be done manually.
{% endhint %}

```csharp
namespace Sample {
    // Import dependencies
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Measurement;

    @EntryPoint()
    operation InitializeQubits() : Unit {
        // Allocate 6 qubits
        use q = Qubit[6];

        // Initialize qubits

        // Qubit 0 is already in state |0⟩ by default

        // Qubit 1: |1⟩
        X(q[1]);

        // Qubit 2: |+⟩
        H(q[2]);

        // Qubit 3: |-⟩
        H(q[3]);
        Z(q[3]);

        // Qubit 4: |i+⟩ (|R⟩ or |C⟩)
        H(q[4]);
        S(q[4]);

        // Qubit 5: |i-⟩ (|L⟩ or |CC⟩)
        H(q[5]);
        Adjoint S(q[5]);

        // Release qubits back to |0⟩ state
        ResetAll(q);
    }
}
```
{% endtab %}
{% endtabs %}
