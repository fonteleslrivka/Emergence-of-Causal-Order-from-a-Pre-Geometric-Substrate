# Emergence-of-Causal-Order-from-a-Pre-Geometric-Substrate
Informational Condensation in the Rank-1 Limit: Emergence of Causal Order from a Pre-Geometric Substrate
# Informational Condensation in the Rank-1 Limit: Emergence of Causal Order from a Pre-Geometric Substrate

[![DOI](https://zenodo.org/badge/DOI_PENDING_2025.svg)](https://github.com/YourGitHubProfile/causal-condensation)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

## 📄 Abstract & Overview

This repository contains the source code for the numerical **toy model** demonstrating **Informational Causal Condensation** in pre-geometric regimes. The model investigates the spectral dynamics of high-dimensional correlation systems and confirms the emergence of a stable dominant mode ($H \ge 0$) characterized by the collapse of spectral entropy ($S \approx 0$)

The core finding is that a single informational ordering axis emerges prior to any geometric structure, suggesting that **temporal order precedes spacetime** in fundamental physics.

## 🧪 Model Core & Key Equations

The model operates on a purely informational substrate defined by the pre-metric $g$, derived from the correlation matrix $\rho$:

$$\rho_{ij} = e^{-D_{ij} / \beta} \qquad \text{and} \qquad g = -\log(\rho + \epsilon)$$

The central operational definition of the pre-geometric phase is:
**Rank-1 Condensation:** The system’s spectral weight concentrates entirely onto the leading eigenvalue ($w_0 \approx 1.0$)[cite: 3753].
**Stability:** The projected Hessian is non-negative ($H_{\text{proj}} \ge 0$)

## 📈 Numerical Results & Evidence

The following figures demonstrate the structural integrity and parameter dependence of the condensation phenomenon (simulated on $N=512$ to $N=1024$ scales):

### 1. Suggestion of Phase Crossover (The $\beta$ Sweep)

This figure is suggestive of, showing the phenomenon is **parameter-dependent**.

| ![Phase Behavior: Effect of Correlation Range](fig_gap_hist.png) |
|:---:| 
| **Figure 10: Phase Behavior ($\lambda_1 / \lambda_2$ vs $\beta$).** The dominance ratio exhibits a sharp, exponential growth as $\beta$ increases, Suggestive of a clear transition from a disordered phase to the Rank-1 condensed phase. |
| ![Spectral weight distribution showing perfect Rank-1](fig_softmax_weights.png) |
The plot of softmax-stabilized weights reveals that the dominant eigenmode (index 0) absorbs the entirety of the informational weight (w ≈ 1.0), while all secondary modes are suppressed to zero. This distribution mathematically corresponds to a vanishing spectral entropy (S = 0),suggesting that the system has stabilized into a single causal axis with no emergent spatial geometry.
| ![Spectral entropy](fig_entropy_zero.png) |
All seeds and system sizes (N = 512, 1024) yield S ≈ 0 within numerical precision. This demonstrates complete condensation of the spectrum into a single mode, marking the system as entering a pre-geometric ordered phase. 

### 2. Spectral Collapse and Robustness

These figures confirm the mathematical signature of the pre-geometric state:

| Figure | Description | Proof Point |
| :--- | :--- | :--- |
| **Log-scale Spectrum** | Shows the steep drop-off of the leading mode ($|\lambda_1|$) followed by a continuous tail[cite: 3232]. | **Suggestive of Rank-1.** No secondary spectral plateau/cluster indicating emergent spatial dimensions. |
| **Seed Variability (Boxplot)** | Suggestive of the eigenvalue magnitude and the spectral gaps are highly stable across multiple random initial conditions. | **Suggestive of Robustness.** Not an artifact of a single seed. |
| **Entropy Collapse** |Shows the system's entropy $S$ is at the numerical floor ($\approx 0$) for all runs. | **Suggestive of Maximal Order.** The mathematical signature of complete informational collapse. |
| **Gap Histogram ($\lambda_4/\lambda_5$)** |Shows that the ratio of secondary eigenvalues clusters tightly around $1.03$. | **Rules out $1+3$ Geometry.** No evidence of 3 distinct spatial modes emerging in the spectrum. |


This repository contains code, figures and reproducibility material for the paper:

**Causal Condensation as a Stable Informational Phase Transition: Spectral Collapse and the Emergence of Rank-1 Order in Pre-Geometric Systems.**

## What is here
- Python scripts that reproduce all figures used in the paper.
- A lightweight, robust spectral pipeline safe for typical laptops (8 GB RAM).
- A methodological appendix with algorithms for projected Hessian, stable softmax, and spectral truncation.
- LaTeX files (`/paper`) ready for Overleaf (place figures in `/figures`).

## Quickstart (Google Colab)
1. Open a new Colab notebook.
2. Mount your GitHub or upload this repository.
3. For each provided script, **paste it into a new cell and execute only that cell** (do not delete previous cells).
4. Example:
   ```python
   # in a single new cell
   !python code/generate_spectrum.py

If running interactive functions in notebooks, call them from new cells (see the script docstrings).

Memory note: For N <= 1024 and k <= 150 the code was designed to run on 8 GB RAM machines. Careful: increasing N or computing full eigen-decompositions will increase memory/time dramatically.

Files

requirements.txt, environment.yml

/code — python scripts to generate each figure

/figures — saved outputs (png)

/paper — LaTeX files

README.md, LICENSE

Reproducibility

All scripts use fixed seeds by default; change seeds in the command line if you want ensembles.

Implementation uses scipy.sparse.linalg.eigsh for spectral extraction and fallbacks if ARPACK fails.

Contact

Author: Rebeca Lemos — (fonteleslrebecca@proton.me)

---


**##environment.yml**

name:causal-condensation channels
  - conda-forge
dependencies:
  - python=3.10
  - numpy>=1.26
  - scipy>=1.11
  - matplotlib>=3.8
  - networkx>=3.2

## 💻 Reproducibility

This repository includes:

fixed random seeds,

deterministic spectral solvers,

detailed appendix with algorithms,

exported figures used in the paper,

and all scripts required for full reproducibility.

The computational pipeline is suitable for:

Google Colab

Standard Linux/MacOS

Zenodo archived environments

Conda-based reproducibility

**##The model is built in Python and relies on standard scientific libraries.
**
### Prerequisites

You need Python 3.x and the following libraries installed:
```bash
pip install numpy scipy matplotlib scikit-learn
