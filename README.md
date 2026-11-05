# ECE 2112: Advanced Computer Programming and Algorithms
## Experiment 5: Introduction to MATLAB Programming (Python / NumPy Implementation)

<div align="center">

| Field | Details |
| :--- | :--- |
| **Author** | Adrian Joseph R. Herrera |
| **Student ID** | 2025000458 |
| **Section** | 2ECE-D |
| **Department** | Electronics Engineering Department |
| **Institution** | University of Santo Tomas - Faculty of Engineering |
| **Platform** | JuCode (Python 3 / NumPy) |

</div>

---

## 📌 Overview
This repository contains the programming implementation for **Experiment 5: Introduction to MATLAB Programming**, adapted for execution in **JuCode** using **Python 3** and the **NumPy** library. 

The lab focuses on matrix creation, transpose operations, analyzing complex vs. real matrix behavior, expressing simultaneous linear systems in matrix form, and solving linear systems using both the **Inverse Method** and **Cramer's Rule** alongside numerical precision checks.

---

## 📂 Repository Contents
* `Herrera_PA5.py` — Complete Python script containing both Problem A and Problem B with labeled outputs, analysis comments, and precision checks.

---

## 🛠️ Intended Learning Outcomes & Implementation
1. **Real & Complex Matrices:** Creating and inspecting multi-dimensional arrays and complex number matrices using `numpy.array`.
2. **Transpose Operations:** Distinguishing between standard non-conjugate transposes (`transpose` / `.T`) and complex-conjugate transposes (`.conj().T`) for both real matrix $R$ and complex matrix $Z$.
3. **Simultaneous Linear Systems:** Setting up coefficient matrix $A$ and right-hand side vector $b$ for a 4-variable linear system.
4. **Alternative Solvers:** Solving the system via:
   * **Inverse Method:** $x_{\text{inv}} = A^{-1}b$
   * **Cramer's Rule:** Replacing individual columns of $A$ with $b$ and computing ratios of determinants.
5. **Numerical Verification:** Validating results using matrix norms (`np.linalg.norm`) and non-zero determinant checks (`np.linalg.det`).

---

## 🚀 How to Run
1. Open your JuCode workspace.
2. Ensure NumPy is available (`import numpy as np`).
3. Run the script `Herrera_PA5.py` from beginning to end without errors.

---

## 📝 Analysis Summary (Problem A)
* **Real Matrix $R$:** All transpose operations (`transpose(R)`, conjugate transpose, and non-conjugate transpose) yield identical results because imaginary components are zero.
* **Complex Matrix $Z$:** `transpose(Z)` and non-conjugate transpose (`Z.T`) yield identical results by swapping indices without altering imaginary signs.
* **Apostrophe Operator (`'`) Equivalent (`Z.conj().T`):** Performs the complex-conjugate (Hermitian) transpose, which both swaps rows/columns and negates the imaginary components of complex entries.
