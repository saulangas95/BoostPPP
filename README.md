# Analysis and Modeling  of a Boost Converter with Power Processing Reduction for PV Applications

**Manuscript ID:** IEEE LATAM Submission ID: 10356  
**Authors:**  
- <Iván A. Reyes-Portillo>  
- <Saúl R. Méndez-Elizondo>  
- <Jorge A. Morales-Saldaña>  
- <Jorge U. Muñoz-Minjares>  
- <Claudia. A. Rivera Romero >
- <Dora Castro-López>

---

## 📁 Included Scripts

This repository contains the MATLAB live script required to reproduce the main analytical and numerical results presented in the manuscript (continuous-time, s-plane).

| Script | Related Figure(s) / Equation(s) | Description |
|--------|----------------------------------|-------------|
| `BoostPPP_IEEE.mlx` | Eq. (13), Eqs. (1)–(3), Fig. 4, Fig. 8, Fig. 10 | Single-file evidence script. Builds the small-signal state-space model (Eq. 13), computes numerical transfer functions (e.g., \(G_{vd}(s)\)), derives symbolic poles and transmission zeros (Rosenbrock system matrix) and provides a symbolic cross-check via the Faddeev–Leverrier method. Computes operating points from Eqs. (1)–(3), performs pole/zero migration sweeps for Fig. 4, generates the k-factor and processed-power surfaces for Fig. 8, and plots the frequency response of \(G_{vd}(s)\) for Fig. 10. |


---

## 💻 Requirements

- MATLAB R20XXx or later (recommended: R2020a or newer).  
- Toolboxes:
  - **Control System Toolbox** (required for `ss2tf`, `tf`, `bode`, `pzmap`).
  - **Symbolic Math Toolbox** (required for symbolic poles/zeros and algebraic derivations).

---

## ▶️ How to Run

1. Open MATLAB and set the repository root as the current working directory.
2. Open and run:
   - `BoostPPP_IEEE.mlx`
3. The script runs from top to bottom and reproduces the reported results.

---

## 📌 Notes for Reproducibility



- The analysis is performed in **continuous time** (s-plane).  
- Parameter values correspond to the manuscript nominal set (Table I).  
- No external datasets are required unless explicitly stated in the manuscript.

---

## ✉️ Contact

For questions or replication of results:  
saul_mdz95@hotmail.com
