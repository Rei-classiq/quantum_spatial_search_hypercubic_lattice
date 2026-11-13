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
