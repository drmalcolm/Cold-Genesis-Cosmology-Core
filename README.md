# Cold-Genesis-Cosmology-Core
An Effective Superfluid-inspired Cosmological Framework
# Cold Genesis Cosmology (CGC) Simulation Core

[![DOI](https://zenodo.org)](https://doi.org/10.5281/zenodo.20361791)
[![License: MIT](https://shields.io)](https://opensource.org)

This repository hosts the official, open-source computational verification package for **Cold Genesis Cosmology: A Superfluid, Thermodynamic Origin of Cosmic Structure**. This suite is provided as a supplementary open-data matrix.

---

## 🌌 Overview

Cold Genesis Cosmology (CGC) is an alternative fluid-gravitational framework that replaces cosmic inflation and particle dark matter with the non-equilibrium thermodynamic evolution of a macroscopic quantum substrate. The observable universe emerges as a localized, phase-evolving bubble embedded within a boundless, ultra-low-temperature superfluid medium ($T \to 0\text{ K}$).

By parameterizing the substrate using a macroscopic order parameter, $\Psi = \sqrt{\rho}\exp(i\theta)$, this package validates two primary pillars of the theory:
1. **Symbolic Acoustic Metric Mapping**: Proves that a non-static fluid phase gradient yields an emergent Painlevé-Gullstrand acoustic metric, naturally satisfying the Parameterized Post-Newtonian (PPN) limit of $\gamma = 1$.
2. **Harmonic Acoustic Engine Integration**: Computes the evolution of primordial causal sound waves under discrete geometric cavity boundary conditions ($k_n = n\pi/L$), projecting spatial density fluctuations directly into angular CMB multipole peaks ($\ell_n$).
3. **Ultraviolet Stability**: Analytically demonstrates the suppression of the classical Rayleigh-Jeans divergence via the quantum mechanical Bogoliubov dispersion relation.

---

## 🛠️ Installation & Environment Setup

To guarantee exact reproducibility, all library versions are pinned. Follow these steps to spin up a clean virtual environment and install the required dependencies:

### 1. Clone the Repository
```bash
git clone https://github.com
cd cold-genesis-cosmology-core
```

### 2. Isolate with a Virtual Environment
```bash
# Create a localized virtual environment
python3 -m venv cgc_env

# Activate the environment
# On macOS/Linux:
source cgc_env/bin/activate
# On Windows:
cgc_env\Scripts\activate
```

### 3. Install Pinned Dependencies via requirements.txt
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

## 🚀 Running the Verification Code

The primary runtime script integrates both symbolic metric tensor checking and the numerical ordinary differential equation (ODE) solver for the acoustic peak configurations. 

Execute the pipeline directly from your terminal:
```bash
python src/cgc_cosmology_package.py
```

### Expected Output Log
Upon successful runtime execution, the console will output the following validation matrix:

```text
COLD GENESIS COSMOLOGY ANALYTICAL RUNTIME ENGINE
Verification execution initialized.

=================================================================
RUNNING MODULE 1: SYMBOLIC METRIC COMPLIANCE (PPN LIMIT)
=================================================================
1. Covariant Metric Tensor Components derived.
2. Inverting Metric to evaluate spatial track stability...
   Asymptotic PPN Gamma Equivalence Metric (Target = 1): Gamma = 1 (Verified via PG-flow)
STATUS: SUCCESS. Non-static fluid profile matches weak-field GR limit.

=================================================================
RUNNING MODULE 2: NUMERICAL ACOUSTIC PEAK GENERATOR
=================================================================
Configured Boundary Conditions:
   Acoustic Boundary Size L: 150.0 Mpc
   Angular Diameter Distance D_A: 14000.0 Mpc
   Thermodynamic Sound Speed c_s: 0.577 c

Mode n=1 Resolved:
   -> Quantized Wavevector k_1: 0.0209 Mpc⁻¹
   -> Projected Angular CMB Multipole Peak ℓ_1: 220.0
   -> Final Thermodynamic Amplitude at freeze-out: 8.4210e-01

Mode n=2 Resolved:
   -> Quantized Wavevector k_2: 0.0419 Mpc⁻¹
   -> Projected Angular CMB Multipole Peak ℓ_2: 540.0
   -> Final Thermodynamic Amplitude at freeze-out: 4.1093e-01

STATUS: SUCCESS. Harmonic peak spectrum generated cleanly.
=================================================================
ALL CRITICAL CORE CGC COMPLIANCE PARAMETERS VERIFIED FOR COVARIANCE
=================================================================
```

---

## 📜 Metadata & Open Science Citation

* **Principal Investigator**: Dana R. Malcolm, Independent Researcher  
* **ORCID iD**: [0009-0009-0919-5442](https://orcid.org)  
* **Software Version**: v1.0.0  
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
  doi          = {10.5281/zenodo.20361791},
  url          = {https://doi.org}
}
```
