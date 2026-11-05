# ECE 2112: Advanced Computer Programming and Algorithms
## Experiment 5: Introduction to Matrix Programming & Linear Systems

### Overview
This repository contains the solution for **Experiment 5** of the ECE 2112 course at the University of Santo Tomas (Faculty of Engineering, Electronics Engineering Department). 

Although originally designed for MATLAB, this implementation uses **Python 3** with **NumPy** in a Jupyter Notebook / JuCode environment to perform matrix operations, analyze real vs. complex matrix transpositions, and solve simultaneous linear systems.

---

### Key Learning Outcomes
1. Creation of real and complex matrices using numerical libraries.
2. Differentiation between transpose and complex-conjugate (Hermitian) transpose operations.
3. Matrix representation of linear systems.
4. Solving linear systems using the Matrix Inverse Method and Cramer's Rule, followed by numerical precision validation.

---

### Implementation Details

#### **Problem A: Transpose Operations**
- **Real Matrix ($R$):** Evaluated standard transpose, conjugate transpose, and non-conjugate transpose. Verified that all three yield identical results due to zero imaginary components.
- **Complex Matrix ($Z$):** Compared non-conjugate transpose (`transpose(Z)` / `Z.T`) against complex-conjugate transpose (`Z.conj().T`). Demonstrated how the apostrophe / conjugate operator negates imaginary components.

#### **Problem B: Linear System Solution**
Solves the linear system $A \mathbf{x} = \mathbf{b}$:
$$
\begin{aligned}
2x_1 - x_2 + 3x_3 + 2x_4 &= 16 \\
x_1 + 4x_2 - 2x_3 + x_4 &= -7 \\
3x_1 + 2x_2 + x_3 - x_4 &= 6 \\
-2x_1 + 3x_2 + 4x_3 + 2x_4 &= 7
\end{aligned}
$$

1. **Inverse Method:** $\mathbf{x}_{\text{inv}} = A^{-1} \mathbf{b}$ using `np.linalg.inv()`.
2. **Cramer's Rule:** Evaluated by iteratively swapping columns of $A$ with $\mathbf{b}$ and computing determinants via `np.linalg.det()`.
3. **Verification Checks:** 
   - `det(A) != 0` check.
   - Norm difference check: $\text{norm}(\mathbf{x}_{\text{inv}} - \mathbf{x}_{\text{cramer}}) \approx 0$
   - Residual norm check: $\text{norm}(A\mathbf{x}_{\text{inv}} - \mathbf{b}) \approx 0$

---

### Requirements & Setup
To run this script locally or in JuCode:
- **Python 3.x**
- **NumPy**

```bash
pip install numpy
```

---

### File Structure
- `Herrera_PA5.py` / `Herrera_PA5.ipynb` — Primary Python script containing Problem A and Problem B implementations.
- `README.md` — Project documentation.
