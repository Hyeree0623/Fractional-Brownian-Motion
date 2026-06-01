# FBM Characterization

A collection of tools for identifying fractional Brownian motion (FBM)
and Gaussian transport behavior from particle trajectories.

## Methods

1. P-Variation Test
2. Gaussianity Test

## Workflow

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
 ↓              ↓
P-Variation     Gaussian Test
 │              │
 ↓              ↓
Hurst Index     JB/KS Analysis
 │              │
 └───────┬──────┘
         ↓
FBM Characterization


