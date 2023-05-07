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
