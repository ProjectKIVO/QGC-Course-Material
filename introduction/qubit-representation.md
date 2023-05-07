# Qubit Representation

### Representation Conversion

Classical computers use multiple bits (0s and 1s), while quantum systems employ several qubits. A classical bit sequence may appear as follows:

$$0101$$

If we want to describe the preceding sequence, we can also express them as

$$
\begin{bmatrix}0\\ 1\end{bmatrix},
\begin{bmatrix}1\\ 0\end{bmatrix},
\begin{bmatrix}0\\ 1\end{bmatrix},
\begin{bmatrix}1\\ 0\end{bmatrix}
$$

Of course, to combine quantum systems, we should apply tensor product to the sequence by doing the following:

$$
\ket{0} \otimes \ket{1} \otimes \ket{0} \otimes \ket{1}
$$

For any 4-qubit system, you can also express the quantum system as:&#x20;

$$
\ket{\mathbb{C}^2} \otimes \ket{\mathbb{C}^2} \otimes \ket{\mathbb{C}^2} \otimes \ket{\mathbb{C}^2}
$$

This vector space can be denoted as $$\left(\mathbb{C}^2\right)^{\otimes 4}$$ which is a complex vector space of dimension $$2^4=16$$. We can also describe the sequence with row vectors as the following:

$$\begin{bmatrix} 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 1 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \end{bmatrix} =$$ $$\begin{array}{c|c}   \textrm{Bit Sequence} & \textrm{Amplitude} \\ \hline   0000 & 0 \\ \hline   0001 & 0 \\ \hline   0010 & 0 \\ \hline   0011 & 0 \\ \hline   0100 & 0 \\ \hline   0101 & 1 \\ \hline   0110 & 0 \\ \hline   0111 & 0 \\ \hline   1000 & 0 \\ \hline   1001 & 0 \\ \hline   1010 & 0 \\ \hline   1011 & 0 \\ \hline   1100 & 0 \\ \hline   1101 & 0 \\ \hline   1110 & 0 \\ \hline   1111 & 0 \end{array}$$