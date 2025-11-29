# Parameter Estimation of Lithium-Based Battery

This repository contains scripts and data used to estimate key parameters of a lithium-based battery using HPPC (Hybrid Pulse Power Characterization) tests. The goal is to extract a full Three-RC equivalent circuit model by analyzing voltage and current responses under controlled pulse conditions.

---

## Overview

The project focuses on three main tasks:

### Parameter Estimation
- Extract ohmic resistance  
- Estimate polarization resistances  
- Compute time constants  
- Generate OCV–SOC curve  

### Three-RC Battery Modeling
- Implements a full 3-RC equivalent circuit  
- Captures fast and slow dynamic responses  
- Validates model using measured HPPC data  

### Data Processing and Visualization
- Clean and preprocess HPPC signals  
- Segment pulse events  
- Plot voltage, current, SOC, and model fit  
- Export final parameters and figures  

---
root/
│
├── our hppc data/ # Raw HPPC dataset
├── recent model/ # Latest scripts for processing & estimation
│ ├── preprocessing/ # Data cleaning, filtering, SOC calculation
│ ├── estimation/ # Parameter fitting + RC extraction
│ ├── plots/ # All generated plots
│
├── results/ # Optional final outputs
├── README.md


---

## How to Use

### 1. Clone the repository
```bash
git clone https://github.com/dreambigbibek/Parameter_Estimation_of_Lithium_based_battery.git
cd Parameter_Estimation_of_Lithium_based_battery

2. Run the scripts

For MATLAB:

run("main_estimation.m")


For Python (if applicable):

python estimate_parameters.py

3. View results

All plots and extracted model parameters will appear inside:

recent model/plots/
results/

HPPC Data Summary

Hybrid Pulse Power Characterization tests provide:

voltage drop during high-current pulses

recovery voltage profile

SOC-dependent behavior

basis for identifying R0, R1, R2 and C1, C2, C3

These values are used to construct the complete Three-RC model.

Example Visuals (add once you push your images)
![HPPC Pulse](plots/pulse_example.png)
![Model Fit](plots/model_fit.png)

Why This Model Matters

Accurate parameter estimation helps improve:

State of Charge (SOC) prediction

State of Health (SOH) modeling

BMS control logic

Remaining useful life (RUL) estimation

Battery performance simulation

Roadmap

Add EKF-based SOC estimation

Add cycle aging analysis

Compare 1-RC, 2-RC, and 3-RC model accuracy

Add neural-network-based SOH prediction

## Repository Structure

