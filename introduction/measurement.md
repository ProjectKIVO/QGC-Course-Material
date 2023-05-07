# Measurement

### Description

Qubit measurement is an important operation in quantum computing, allowing us to extract classical information from a quantum system. A measurement of the qubit in the computational basis collapses the quantum state to either |0⟩ or |1⟩ with their respective probabilities.&#x20;

### Reason For Measurement

In quantum computing, it is not possible to read the information of a qubit directly because of the principles of quantum mechanics. Furthermore, the act of measuring a qubit can introduce noise into the system, which can cause errors in the computation. This is because the measurement process interacts with the qubit and can disturb its state.

{% hint style="info" %}
Remember, measurement is a non-deterministic process.&#x20;
{% endhint %}

In practice, measurements are used to extract classical information from a quantum system, but the measurement result is probabilistic and may not accurately reflect the true quantum state of the system. Instead, quantum algorithms and circuits are designed to manipulate and transform the quantum state of a system in a way that can be used to extract useful information while minimizing the impact of noise and errors.

### Example Code

{% tabs %}
{% tab title="Qiskit" %}
```python
from qiskit import QuantumCircuit

# Create a quantum circuit with one qubit and one classical bit
qc = QuantumCircuit(1, 1)

# Measure the qubit in the computational basis and store the result in the classical bit
qc.measure(0, 0)
```
{% endtab %}

{% tab title="Q#" %}
```qsharp
namespace Sample {
    // Import dependencies
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Measurement;

    @EntryPoint()
    operation Sample() : Result {
        // Allocate a qubit
        use q = Qubit();

        // Return the result of a measurement
        return M(q);
    }
}
```
{% endtab %}
{% endtabs %}
