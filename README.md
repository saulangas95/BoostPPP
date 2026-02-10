# Analysis and Modeling of a Boost Converter with Power Processing Reduction for PV Applications

**Manuscript ID:** IEEE LATAM Submission ID: 10356  
**Authors:**  
- Iván A. Reyes-Portillo  
- Saúl R. Méndez-Elizondo  
- Jorge A. Morales-Saldaña  
- Jorge U. Muñoz-Minjares  
- Claudia A. Rivera Romero  
- Dora Castro-López  

---

## 📁 Included Files

This repository contains all the files required to reproduce the analytical, numerical, and simulation-based results presented in the manuscript.

### MATLAB

| File | Related Figure(s) / Equation(s) | Description |
|------|----------------------------------|-------------|
| `BoostPPP_IEEE.mlx` | Eq. (13)–(14), Eqs. (1)–(3), Fig. 4, Fig. 8, Fig. 10 | Main evidence script. Builds the small-signal state-space model (Eq. 13), computes numerical transfer functions (e.g., \(G_{vd}(s)\)), derives symbolic poles and transmission zeros using the Rosenbrock system matrix, and provides a symbolic cross-check via the Faddeev–Leverrier method. Computes operating points from Eqs. (1)–(3), performs pole/zero migration sweeps (Fig. 4), generates the k-factor and processed-power surfaces (Fig. 8), and plots the frequency response of \(G_{vd}(s)\) (Fig. 10). |

### PSIM

| File | Related Figure(s) | Description |
|------|-------------------|-------------|
| `BoostPPPGvdAC.psimch` | Fig. 10 | PSIM schematic used to perform an AC sweep of the switched boost converter. The simulation is executed by pressing **Run Simulation**. The resulting frequency response is used to validate the small-signal transfer function \(G_{vd}(s)\). |
| `TFGvdBoostPP3.txt` | Fig. 10 | Text file containing the AC sweep numerical data exported from PSIM. These data are directly compared against the MATLAB frequency response of \(G_{vd}(s)\). |

---

## 📂 Notes on Time-Domain Waveforms (Fig. 9)

The time-domain voltage and current waveforms reported in **Fig. 9** (Voltage/current waveforms obtained from the switched model) are generated using the same PSIM schematic:

- To obtain these waveforms, **comment or disable the AC Sweep block** in `BoostPPPGvdAC.psimch`.
- Run the transient simulation normally.
- The resulting waveforms correspond to the switched-model responses presented in the manuscript.

---

## 💻 Requirements

### MATLAB
- MATLAB R20XXx or later (recommended: R2020a or newer).
- Required toolboxes:
  - **Control System Toolbox** (for `ss2tf`, `tf`, `bode`, `pzmap`).
  - **Symbolic Math Toolbox** (for symbolic derivations, poles, and zeros).

### PSIM
- PSIM (any version supporting AC Sweep analysis).

---

## ▶️ How to Run

### MATLAB Analysis
1. Open MATLAB and set the repository root as the current working directory.
2. Open and run:
   - `BoostPPP_IEEE.mlx`
3. The script executes sequentially and reproduces all analytical and numerical results reported in the paper.

### PSIM Validation
1. Open `BoostPPPGvdAC.psimch` in PSIM.
2. Press **Run Simulation** to perform the AC sweep.
3. Compare the obtained frequency response with the MATLAB results (Fig. 10).
4. To obtain time-domain waveforms (Fig. 9), disable the AC Sweep block and run the transient simulation.

---

## 📌 Notes for Reproducibility

- All analyses are performed in **continuous time (s-plane)**.
- Parameter values correspond to the nominal set reported in **Table I** of the manuscript.
- The MATLAB figures are exported as **true vector PDFs** using the `painters` renderer to ensure publication-quality graphics.

---

## ✉️ Contact

For questions, clarifications, or replication of results:

**Saúl R. Méndez-Elizondo**  
📧 saul_mdz95@hotmail.com
