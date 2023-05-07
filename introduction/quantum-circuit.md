# Quantum Circuit

### Description

Quantum circuits are the fundamental building blocks of quantum computing. They are used to describe and implement quantum algorithms, which are a sequence of quantum operations applied to quantum bits (qubits). Quantum circuits provide a way to represent and manipulate quantum information.

### Example Code

{% tabs %}
{% tab title="Qiskit" %}
{% hint style="info" %}
Quantum circuits in Qiskit are represented using the[`QuantumCircuit`](https://qiskit.org/documentation/stubs/qiskit.circuit.QuantumCircuit.html) class.
{% endhint %}

```python
from qiskit import QuantumCircuit

# Create a quantum circuit with 2 qubits
# and name the qubits "q"
q = QuantumRegister(2, 'q')
```
{% endtab %}

{% tab title="Q#" %}
{% hint style="info" %}
Q# represents quantum circuits as operations, which are similar to functions or methods in other programming languages.
{% endhint %}

```csharp
namespace Sample {
    open Microsoft.Quantum.Canon;

    operation SimpleQuantumCircuit() : Unit {
        // Allocate 2 qubits
        use q = Qubit[2];
    }
}
```
{% endtab %}
{% endtabs %}
