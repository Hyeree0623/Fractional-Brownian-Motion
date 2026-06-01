# FBM Characterization

A collection of Python tools for characterizing **fractional Brownian motion (FBM)**, **Gaussian transport behavior**, and **heterogeneous dynamics** from particle trajectory data.

The codes are designed primarily for **LAMMPS dump files** and provide a workflow for extracting trajectories, handling periodic boundary conditions, and performing statistical analyses of particle motion.

---

## Methods

### 1. P-Variation Test

Estimates scaling behavior of particle trajectories using p-variation analysis. This method can be used to distinguish FBM-like dynamics and infer trajectory roughness properties.

### 2. Gaussianity Test

Evaluates whether particle displacement increments follow Gaussian statistics using:

* Jarque–Bera (JB) test
* Kolmogorov–Smirnov (KS) test

Particles can be classified as Gaussian or non-Gaussian based on user-defined significance criteria.

### 3. Quantile Evolution Analysis

Computes and visualizes the temporal evolution of displacement increment quantiles. This method provides insight into:

* Distribution broadening
* Dynamic heterogeneity
* Rare-event fluctuations
* Time-dependent transport properties

---

## Workflow

```text
LAMMPS Dump File
        ↓
Trajectory Extraction
        ↓
PBC Unwrapping
        ↓
Displacement Calculation
        ↓
 ┌──────────────┬──────────────┐
 │              │              │
 ↓              ↓              ↓
P-Variation   Gaussian Test   Quantile Evolution
   Test                          Analysis
 │              │              │
 ↓              ↓              ↓
Hurst Index   JB/KS Analysis  Quantile Dynamics
 │              │              │
 └──────────────┴──────────────┘
                ↓
      FBM Characterization
```

---

## Features

* Read and process LAMMPS trajectory files
* Support for both 2D and 3D simulations
* Automatic handling of wrapped and unwrapped coordinates
* Periodic boundary condition (PBC) reconstruction
* Selection of arbitrary particle ID ranges
* Single-particle and ensemble-level analyses
* Publication-quality visualization
* Statistical classification of transport behavior

---

## Applications

* Fractional Brownian motion (FBM)
* Active Brownian particles (ABP)
* Molecular dynamics simulations
* Single-particle tracking
* Anomalous diffusion
* Heterogeneous transport
* Non-Gaussian dynamics
* Dynamic phase separation
* Statistical characterization of particle trajectories

---

## Repository Structure

```text
FBM-Characterization/

├── p_variation/
│   └── p_variation_test.py
│
├── gaussian_test/
│   └── gaussian_test.py
│
├── quantile_evolution/
│   └── quantile_evolution.py
│
├── example_data/
│
├── example_results/
│
└── README.md
```

---

## Requirements

* Python 3.9+
* NumPy
* SciPy
* Matplotlib

Install dependencies using:

```bash
pip install numpy scipy matplotlib
```

---

## Citation

If you use these codes in published work directly, please cite the associated publication or repository.

```
Hyeree Hyun et al.,
FBM Characterization Toolkit,
GitHub Repository.
```
