Cold Genesis Cosmology (CGC) Solver & Metric Validator

[![CGC Pipeline Verification](https://github.com)](https://github.com)
[![DOI](https://zenodo.org)](https://doi.org)
[![License: MIT](https://shields.io)](https://opensource.org)

This repository provides the reproducible core computational framework for **Cold Genesis Cosmology (CGC)**, as presented in the article *"Cold Genesis Cosmology: A Superfluid, Thermodynamic Origin of Cosmic Structure"*. 

It implements symbolic metric tensor derivations for the emergent Painlevé-Gullstrand acoustic metric, validates Parameterized Post-Newtonian (PPN) γ compliance, and numerically computes the phase-shifted acoustic horizon projections for the Cosmic Microwave Background (CMB) multipole peaks.

---

## 🌌 Mathematical Overview

Cold Genesis Cosmology models the early universe as a localized, non-equilibrium thermodynamic bubble nucleating within an infinite, spatially unbounded quantum superfluid background at ultra-low temperature (T → 0 K). 

The pipeline maps the underlying Madelung hydrodynamic equations into a field Lagrangian to verify two primary features:
1. **Emergent Acoustic Metric Geometry**: Low-energy phonon excitations propagate through the background density profiles according to a curved Lorentzian geometry \(g_{\mu \nu}^{\text{eff}}\), bounding internal causality by the fluid sound speed (\(c_s \to c\)).
2. **Phase-Shifted Acoustic Horizons**: The framework evaluates how global phase single-valuedness constraints (\(\oint \nabla \theta \cdot d\mathbf{r} = 2\pi n\)) enforce topological rigidity and global phase-locking, providing a stable explanation for super-horizon CMB coherence without scalar field inflation.

---

## 🛠️ Repository Architecture

* `cgc_solver.py` — The core Python executable pipeline containing the validation and acoustic mode configuration loops.
* `.zenodo.json` — The archive configuration template mapping creator ORCIDs, open-access policies, and metadata schemas directly to Zenodo indexing.
* `.github/workflows/python-test.yml` — Active GitHub Actions integration running continuous runtime cross-verification checks on every commit.

---

## 🚀 Execution & Verification

### Prerequisites
The codebase runs on any platform supporting standard Python 3 environments. The only mathematical requirement is `numpy`.

```bash
pip install numpy
```

### Running the Validation Stack
Execute the primary script to trigger the full diagnostic verification pipeline:

```bash
python cgc_solver.py
```

### Expected Test Output
A successful compilation will validate numerical convergence limits, confirming the following parameters:

```text
[INFO] COLD GENESIS COSMOLOGY PIPELINE INITIALIZED
[INFO] =================================================================
[INFO] MODULE 1: SYMBOLIC METRIC COMPLIANCE (PPN LIMIT)
[INFO] =================================================================
...
[INFO] Evaluated PPN Gamma parameter: 1.000000
[INFO] Target value: 1.000000 (Delta: 0.00e+00)
[INFO] Verification status: PASSED

[INFO] =================================================================
[INFO] MODULE 2: NUMERICAL ACOUSTIC PEAK GENERATOR
[INFO] =================================================================
[INFO] Global configuration: L = 150.0 Mpc, D_A = 14000.0 Mpc, c_s = 0.57735 c
[INFO] Mode n=1 Resolved:
 -> Sound Horizon Scale r_s: 86.60 Mpc
 -> Projected Angular Multipole ℓ_1: 220.2
[INFO] Mode n=2 Resolved:
 -> Sound Horizon Scale r_s: 86.60 Mpc
 -> Projected Angular Multipole ℓ_2: 539.8
...
[INFO] SYSTEM STATUS: ALL MODULES COMPLETED SUCCESSFULLY
[INFO] Max numerical residual: 2.14e-08 (Tolerance: 1.00e-06): PASSED
```

---

## 📜 Citation & Digital Identifiers

If you utilize this framework or analytical architecture in your research, please cite both the preprint and the software asset:

```bibtex
@article{Malcolm_Cgc_Article_2026,
  author  = {Malcolm, Dana R.},
  title   = {Cold {G}enesis {C}osmology: {A} {S}uperfluid, {T}hermodynamic {O}rigis of {C}osmic {S}tructure},
  journal = {arXiv preprint arXiv:2605.xxxxx},
  year    = {2026}
}

@misc{Malcolm_Cgc_Software_2026,
  author       = {Malcolm, D. R.},
  title        = {Cold {G}enesis {C}osmology: {A}nalytical {S}olver and {E}mergent {M}etric {V}alidation {P}ackage},
  month        = mar,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {v1.0.1},
  doi          = {10.5281/zenodo.20564508}
}
```

---

## ⚖️ License
This project is licensed under the terms of the **MIT License**. See the repository file structure for full legal permissions.
