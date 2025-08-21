---
title: 'From Classical bits to Quantum Kets'
tags: ["Quantum", "Kevin", "Introduction"]
---

{{< katex >}}

### The Classical Bit:

- In any computer, everything boils down to bits.
- A **"bit"**, or a **"c-bit"**, is the smallest unit of data. It can only have one of two values: \(0\) or \(1\)

- *Do note that a classical bit has only one definite state, either 0 [off] or 1 [on].*
---
### Entering the Quantum World: Dirac Notation

To represent these classical bits in a quantum context, we use a special notation called *Dirac notation*, or bra-ket notation. For now, we'll focus on the **"ket"** part, which looks like this: **\(| \psi \rangle\)**.

You can think of a ket as just a fancy way to write a column vector.

This method of representing our classical bits is called ***Basis State Encoding***. We define our two classical states, \(0\) and \(1\), as two distinct basis vectors.

The classical bit '0' is represented by the ket vector \(|0\rangle\):
$$|0\rangle = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$$

The classical bit '1' is represented by the ket vector \(|1\rangle\):
$$|1\rangle = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$$

These two vectors, \(|0\rangle\) and \(|1\rangle\), are the ***computational basis states***. They are the quantum equivalent of the classical \(0\) and \(1\).

---
### Operations on a Classical Bit

Now that we have our bits represented as vectors, how do we perform operations on them, like flipping a bit from \(0\) to \(1\)? In the quantum world, these operations are represented by *matrices*. To apply an operation to a bit, we simply multiply its matrix by the bit's vector.

Let's look at four fundamental functions that can be applied to a single classical bit.<br>
[1. Identity](#1-identity-the-do-nothing-operation)<br>
[2. Negation](#2-negation-the-flip-operation-not-gate)<br>
[3. Constant Zero](#3-constant-0-the-always-output-0-operation)<br>
[4. Constant One](#4-constant-1-the-always-output-1-operation)

#### 1. Identity: The *"Do Nothing"* Operation

This function, \(f(x) = x\), takes an input bit and returns the same bit.

* *Matrix:* \(I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}\)

* Applying to \(|0\rangle\):
    $$\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \implies I|0\rangle = |0\rangle$$

* Applying to \(|1\rangle\):
    $$\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \implies I|1\rangle = |1\rangle$$

<br>

#### 2. Negation: The *"Flip"* Operation (NOT Gate)

This function, \(f(x) = \neg x\), flips the bit. A \(0\) becomes a \(1\), and a \(1\) becomes a \(0\). This is the equivalent of a classical NOT gate. In quantum computing, it's often called the **Pauli-X** gate.

* *Matrix:* \(X = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\)


* Applying to \(|0\rangle\):
    $$\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \implies X|0\rangle = |1\rangle$$

* Applying to \(|1\rangle\):
    $$\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \implies X|1\rangle = |0\rangle$$


#### 3. Constant-0: The *"Always Output 0"* Operation

This function, \(f(x) = 0\), ignores the input and always returns \(0\).

* *Matrix:* \(C_0 = \begin{pmatrix} 1 & 1 \\ 0 & 0 \end{pmatrix}\)

* Applying to \(|0\rangle\):
    $$\begin{pmatrix} 1 & 1 \\ 0 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \implies C_0|0\rangle = |0\rangle$$
* Applying to \(|1\rangle\):
    $$\begin{pmatrix} 1 & 1 \\ 0 & 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix} \implies C_0|1\rangle = |0\rangle$$


#### 4. Constant-1: The *"Always Output 1"* Operation

This function, \(f(x) = 1\), is the opposite of the one above. It always returns \(1\).

* *Matrix:* \(C_1 = \begin{pmatrix} 0 & 0 \\ 1 & 1 \end{pmatrix}\)


* Applying to \(|0\rangle\):
    $$\begin{pmatrix} 0 & 0 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \implies C_1|0\rangle = |1\rangle$$
* Applying to \(|1\rangle\):
    $$\begin{pmatrix} 0 & 0 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix} \implies C_1|1\rangle = |1\rangle$$
