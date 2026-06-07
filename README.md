# Graphene Nanoribbon Field-Effect Transistor (GNRFET) Modeling

Analytical modeling and simulation of Graphene-Based Field-Effect Transistor structures using **MATLAB**. This repository contains the source code and documentation from my Bachelor's thesis, focusing on the electrical characteristics and charge carrier mobility in nanoribbon structures under strong electric fields.

---

## 🔬 Project Overview

As silicon-based CMOS scaling approaches its physical limits, Graphene Nanoribbons (GNRs) offer a promising alternative due to their tunable bandgap and exceptional carrier mobility. This project develops an improved analytical model for GNRFETs that accurately accounts for the non-linear dependence of drift velocity on the electric field.

### Key Objectives:
* Approximate electron drift velocity using 5 different mathematical models and benchmark them against Full-Band Monte Carlo data.
* Implement an adaptive mobility model $\mu(E)$ to capture velocity saturation effects in strong electric fields.
* Simulate and plot the Current-Voltage (I-V) output characteristics ($I_D$ vs. $V_{DS}$) for various geometries and gate voltages.

---

## 🛠️ Tech Stack & Methodology

* **Environment:** MATLAB
* **Modeling Approach:** * Replaced the standard constant mobility assumption with a field-dependent mobility model.
  * Extracted quantum capacitance and oxide capacitance effects near the Dirac point using Maclaurin series expansions.
  * Solved pseudo-quadratic equations to derive the surface potential and output drain current.

---

## 📂 Repository Structure

* `/docs` - Contains the full Bachelor's Thesis (in Ukrainian) detailing the physics, analytical derivations, and structural analysis of GNRFETs.
* `/src/drift_velocity_approx.m` - MATLAB script that computes and plots the approximation of carrier drift velocity using non-linear models.
* `/src/iv_characteristics_model.m` - MATLAB script that generates the $I_D$-$V_{DS}$ output characteristics based on the selected Monte Carlo data sets.

---

## 📈 Sample Results

### Drift Velocity Approximation
The model successfully approximates velocity saturation behavior under high electric fields, matching multi-particle Monte Carlo simulation data.
<img width="1280" height="737" alt="image" src="https://github.com/user-attachments/assets/586317d9-711b-4417-98bc-844c01df0b48" />

### I-V Characteristics ($L=100$ nm, $W=5$ nm)
By introducing field-dependent mobility, the model provides a much more physically accurate representation of the current saturation regime compared to quasi-ballistic models.
<img width="1280" height="691" alt="image" src="https://github.com/user-attachments/assets/7d7a59f7-efe8-46f3-915a-5b51cd598b7d" />


---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/D0nKarLe0n/Graphene-Nanoribbon-Field-Effect-Transistor-GNRFET-Modeling.git
   ```
2. Open MATLAB and navigate to the /src directory.

3. Run drift_velocity_approx.m to view the mobility approximations.

4. Run iv_characteristics_model.m to generate the I-V curves.
