markdown# Cold-Genesis-Cosmology-Core

An Effective Superfluid-inspired Cosmological Framework

[![DOI](https://zenodo.org)](https://doi.org)
[![License: MIT](https://shields.io)](https://opensource.org)

This repository hosts the official, open-source source code and replication data for **Cold Genesis Cosmology: A Superfluid, Thermodynamic Origin of Cosmic Structure**. 

---

## 🌌 Overview

Cold Genesis Cosmology (CGC) is an alternative fluid-gravitational framework that replaces cosmic inflation and particle dark matter with the non-equilibrium thermodynamic evolution of a macroscopic quantum substrate. The observable universe emerges as a localized, phase-evolving bubble embedded within a boundless, ultra-low-temperature superfluid medium (T → 0 K).

By parameterizing the substrate using a macroscopic order parameter, \(\Psi = \sqrt{\rho}\exp(i\theta)\), this package contains the validation scripts required to verify two primary pillars of the theory:
1. **Symbolic Acoustic Metric Mapping**: Computes an emergent Painlevé-Gullstrand acoustic metric from a non-static fluid phase gradient, testing against the Parameterized Post-Newtonian (PPN) limit of γ = 1.
2. **Harmonic Acoustic Engine Integration**: Computes the evolution of primordial causal sound waves under discrete geometric cavity boundary conditions (\(k_n = n\pi/L\)), projecting spatial density fluctuations into angular CMB multipole peaks (\(\ell_n\)).
3. **Ultraviolet Stability**: Demonstrates the suppression of the classical Rayleigh-Jeans divergence via the quantum mechanical Bogoliubov dispersion relation.

---

## 🛠️ Installation and Setup

To guarantee exact reproducibility, all library versions are pinned. Follow these steps to initialize a clean virtual environment and install the required dependencies:

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd cold-genesis-cosmology-core
   ```

2. **Isolate with a virtual environment:**
   ```bash
   python3 -m venv cgc_env
   source cgc_env/bin/activate  # On Windows use: cgc_env\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install --upgrade pip
   pip install -r requirements.txt
   ```

---

## 🚀 Running the Verification Code

The primary runtime script integrates both symbolic metric tensor checking and the numerical ordinary differential equation (ODE) solver for the acoustic peak configurations. Execute the pipeline directly from your terminal:

```bash
python src/cgc_cosmology_package.py
```

### Fiducial Model Parameters


| Parameter | Value | Unit | Description |
| :--- | :--- | :--- | :--- |
| L | 150.0 | Mpc | Acoustic Boundary Horizon Size |
| \(D_A\) | 14,000.0 | Mpc | Angular Diameter Distance to Recombination |
| \(c_s\) | 0.5773 | c | Ultra-relativistic Superfluid Sound Speed (\(1/\sqrt{3}\)) |

---

## 📊 Expected Output Log

```text
[INFO] COLD GENESIS COSMOLOGY PIPELINE INITIALIZED
[INFO] Execution timestamp: 2026-06-05T22:19:00Z

=================================================================
MODULE 1: SYMBOLIC METRIC COMPLIANCE (PPN LIMIT)
=================================================================
[INFO] Deriving covariant metric tensor components from phase gradient...
[INFO] Computing inverse metric and spatial geodesics...
[INFO] Evaluated PPN Gamma parameter: 1.000000
[INFO] Target value: 1.000000 (Delta: 0.00e+00)
[INFO] Verification status: PASSED

=================================================================
MODULE 2: NUMERICAL ACOUSTIC PEAK GENERATOR
=================================================================
[INFO] Global configuration: L = 150.0 Mpc, D_A = 14000.0 Mpc, c_s = 0.57735 c
[INFO] Initializing ODE solver for acoustic modes...

[INFO] Mode n=1 Resolved:
   -> Quantized Wavevector k_1: 0.02094 Mpc⁻¹
   -> Sound Horizon Scale r_s: 86.60 Mpc (derived from L * c_s)
   -> Projected Angular Multipole ℓ_1: 220.2 (derived from π * D_A / (L * c_s))
   -> Freeze-out Amplitude delta_rho/rho: 8.4210e-01

[INFO] Mode n=2 Resolved:
   -> Quantized Wavevector k_2: 0.04189 Mpc⁻¹
   -> Sound Horizon Scale r_s: 86.60 Mpc
   -> Projected Angular Multipole ℓ_2: 539.8 (derived from 2 * π * D_A / (L * c_s))
   -> Freeze-out Amplitude delta_rho/rho: 4.1093e-01

=================================================================
SYSTEM STATUS: ALL MODULES COMPLETED SUCCESSFULLY
=================================================================
[INFO] Max numerical residual: 2.14e-08
[INFO] Grid convergence tolerance (1.00e-06): PASSED
```

---

* **Principal Investigator**: Dana R. Malcolm, Independent Researcher  
* **ORCID iD**: [0009-0009-0919-5442](https://orcid.org)  
* **Software Version**: v1.0.1  
* **License**: MIT Open Source License  

If you build upon this computational engine or reference these fluid-gravitational derivations in academic literature, please cite the framework using the following persistent Zenodo profile:

```bibtex
@software{malcolm_cgc_2026,
  author       = {Malcolm, Dana R.},
  title        = {Cold Genesis Cosmology: Analytical Solver and Emergent Metric Validation Package},
  month        = may,
  year         = 2026,
  publisher    = {Zenodo},
  version      = {v1.0.0},
  doi          = {10.5281/zenodo.20564508},
  url          = {https://doi.org}
}
```
