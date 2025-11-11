# MPS to Matrix Conversion & Reconstruction (Computational Optimization — Week 1, 2023)

**Course:** MSc Computational Optimization  
**Year:** 2023  
**Language:** Python  
**Original Code Comments:** English
This project focuses on understanding how **linear optimization problems are represented** and how to convert between:
- **Standard MPS format** (used in optimization libraries),
- and a **matrix representation** suitable for computational processing.

The goal was not to use existing solvers, but to **manually parse and reconstruct** the problem in order to understand the structure of linear programs internally.

---

## Objectives

1. **Read** a linear optimization problem stored in `.mps` format.
2. **Extract**:
   - The **constraint matrix** `A`
   - The **right-hand side** vector `b`
   - The **objective coefficients** vector `c`
   - The **constraint type vector** `Eqin` (≤, =, ≥)
3. **Store** these in `.txt` form for inspection.
4. **Measure CPU processing time** for problems of different sizes.
5. **Reconstruct the `.mps` file** from the `.txt` matrix representation to verify correctness.

This exercise ensures a **deep understanding** of how linear problems are structured *before* using them in solvers.

---

## Files in This Folder

| File | Purpose |
|------|---------|
| `Iliopoulou_week(1)_A.py` | Reads `.mps` → extracts `(A, b, c, Eqin)` → saves them in `.txt` → prints CPU time. |
| `Iliopoulou_week(1)_B.py` | Reads the `.txt` matrix form → reconstructs a valid `.mps` file. |
| `Iliopoulou_week(1)_A.pdf` | Assignment report including CPU time comparison across datasets. |

---

## Workflow

### 1) Convert MPS → Matrix 
Run:
```bash```
python Iliopoulou_week(1)_A.py

### 2) Convert Matrix → MPS (Reconstruction)

Run the reconstruction script:
```bash```
python Iliopoulou_week(1)_B.py

