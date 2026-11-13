# Quantum Circuits for Quantum Spatial Search on d-Dimensional Lattices

This repository contains the source code, numerical simulations, circuit synthesis scripts, and supporting data for the paper "Quantum Circuits for Quantum Spatial Search on d-Dimensional Lattices".  https://arxiv.org/pdf/2607.19151

The repository provides the materials used to generate the results presented in the main text and Supplemental Material.

## Overview

This work constructs explicit quantum circuits for discrete-time quantum-walk spatial search on $d$-dimensional hypercubic lattices and systematically evaluates their quantum resource requirements.

The repository includes implementations and numerical evaluations of:

- Quantum spatial search circuits for $d=2,3,4$, and $5$.
- Circuit resource scaling, including qubit counts, CX-gate counts, and circuit depths.
- Comparisons of shift-operator implementations using QFT-based adders, ripple-carry adders, MCX-gate cascades, and automated synthesis.
- Robustness against quantum-gate noise and initial-state preparation errors.
- Search performance under different marked-vertex locations and boundary conditions.

## Repository Structure 

```text
.
├── README.md
├── requirements.txt
├── notebooks/
│   └── ...
├── data/
    └── ...
```
- `notebooks/`: Numerical experiments supporting the main text and Supplemental Material.
- `data/`: Data used to generate the figures and tables.

## Requirements

The quantum circuits are implemented using the Classiq platform. Numerical simulations and data analysis are performed using Python and the relevant scientific computing libraries.
Additional configuration or authentication may be required for circuit synthesis through the Classiq platform.

## Notebooks and Data

| Topic | Notebook | Data |
|---|---|---|
| Search probability: exact vs. circuit simulation ($d=2$–$5$) | `d=2/spatial_search4.ipynb`, `d=3/spatial_search_cube.ipynb`, `d>3/spatial_search_d4.ipynb`, `d>3/spatial_search_d5.ipynb`, `d>3/exact_sim_d4.ipynb`, `d>3/exact_sim_d5.ipynb`, `d>3/plot_d2_d5.ipynb` (figure) | `d>3/data.csv` |
| Circuit resource scaling (width, depth, CX) | `resource_eval_d2_d5.ipynb` (synthesis), `data_plot_ver3.ipynb` (figure and fits) | `resource_one_iteration_d2_d5.csv`, `resource_topt_d2_d5.csv`, `depth_scaling_fit_table.csv` |
| Shift-operator implementations (QFT adder, ripple-carry adder, MCX cascade, automated synthesis) | `comparison_search_in_motion/shift_implementations_d2.ipynb`, `compare_ours_vs_search_in_motion_d2.ipynb`, `search_probability_{qft,ripple,mcx}.ipynb`, `search_probability_all.ipynb` (figure) | `shift_compare_{default,opt}.csv`, `resource_*_ours_vs_paper.csv`, `search_probability_{qft,ripple,mcx}.csv` |
| Robustness to gate noise | `d=2/spatial_search_fidelity_v2.ipynb` | `d=2/fidelity_{cx_only,pstar,scaling_fit}_v2.csv` |
| Robustness to initial-state errors (Appendix B) | `d>3/initial_state_robustness.ipynb` | `d>3/initial_state_error_overrot_{curves,pmax,time}_d2_d5.csv` |
| Target location and boundary conditions (Appendix C) | `d>3/target_location_robustness.ipynb` | `d>3/target_location_curves_d2.csv` |

Circuit synthesis requires Classiq authentication (`classiq.authenticate()`).
The figures use LaTeX rendering (`text.usetex=True`), so a LaTeX installation is required to regenerate them.
The resource data were synthesized with `classiq==1.33.0`; other versions may give slightly different gate counts.


## Reproducing the Results

The scripts and notebooks are organized according to the numerical experiments presented in the paper.

To reproduce the results:

1. Install the required dependencies.
2. Configure the Classiq environment where necessary.
3. Run the corresponding scripts or notebooks.
4. Generate the figures using the provided data and plotting scripts.

The simulation parameters and configurations are provided alongside the corresponding experiments.

## Citation

If you use this repository in your research, please cite:

R. Sato, "Quantum Circuits for Quantum Spatial Search on d-Dimensional Lattices," submitted to *Physical Review A* (2026).

Preprint: https://arxiv.org/abs/2607.19151
