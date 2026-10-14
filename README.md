# Network Topology & Stochastic Differential Equation (SDE) Simulations

## Overview
This repository contains Python simulation codes designed to analyze topological phase transitions, thermodynamic shielding, and high-dimensional algorithmic interventions within scale-free networks. 

The simulations utilize Stochastic Differential Equations (SDEs) accelerated by Numba to model systemic cascades, behavioral conformity, and topological defects across varying macroscopic scales (up to $N = 100,000$). Each script validates a specific theoretical hypothesis regarding complex network vulnerabilities and resilience mechanisms.

## Hypotheses & Features

### 1. Hypothesis 1: Topological Phase Transition & Irreversible Hysteresis
**File:** `hypothesis1_hysteresis.py` / `Simulation_Results_Hypothesis1`
- **Objective:** Investigates the difference in network collapse when malicious payloads target "Hub" (Super-spreader) nodes versus "Random" nodes.
- **Key Mechanism:** Demonstrates **irreversible hysteresis**—once a systemic topological defect ($D$) is triggered, it persists even after the attack payload is completely removed.
- **Outputs:** KS statistic convergence (Ergodic Self-Organization), Hysteresis comparisons, and Asymptotic Bias across macroscopic scales.

### 2. Hypothesis 2: Thermodynamic Shielding & Systemic Cascade
**File:** `hypothesis2_shielding.py` / `Simulation_Results_Hypothesis2`
- **Objective:** Demonstrates how malicious actors can blind macroscopic detection systems using noise flooding (dummy data injection).
- **Key Mechanism:** As dummy data dilutes the macro-sensor ($X_A$), the actual systemic topological defect ($\beta_1$) cascades and collapses the network while remaining entirely hidden below the sensor's detection threshold ($\theta = 0.18$).
- **Outputs:** Sensor dynamics, detection failure visualization, and hidden cascade metrics.

### 3. Hypothesis 3: High-Dimensional Algorithmic Intervention
**File:** `hypothesis3_intervention.py` / `Simulation_Results_Hypothesis3`
- **Objective:** Compares different algorithmic intervention strategies to repair network topology post-attack.
- **Key Mechanism:** Evaluates the impact of:
  - **No Intervention** (Baseline hysteresis)
  - **1D Intervention (Edge Injection):** Found to inadvertently worsen topological porosity (penalty applied).
  - **2D Intervention (2-Simplex Injection):** Effectively boosts repair capacity and restores network integrity.
- **Outputs:** Intervention comparison graphs and proof of scale-invariant efficacy across different network sizes.

## Requirements
The simulations are highly optimized and require the following Python libraries:
- `numpy`
- `scipy`
- `pandas`
- `matplotlib`
- `numba` (Crucial for JIT compilation and fast SDE integration)

## Usage
These scripts are originally designed to run seamlessly in **Google Colab** or Jupyter Notebook environments.

1. Open the script in a Jupyter Notebook or Google Colab.
2. Run the cells sequentially. 
3. The scripts include a Phase 0 (Burn-in) process to mathematically guarantee ergodic self-organization (confirmed via Kolmogorov-Smirnov statistics) before executing the main attack/intervention phases.
4. Upon completion, the scripts will automatically generate CSV data files and high-resolution PNG graphs, bundle them into a `.zip` file, and trigger a download.

## Output Structure
Each simulation will generate a directory (e.g., `simulation_results_hypothesis1/`) containing:
- `ks_convergence.csv`: Data confirming system stabilization prior to the experiment.
- `*.csv`: Raw simulation dynamics and defect rates.
- `Fig1_KS_Convergence.png`: Plot of KS statistics.
- `Fig2_*.png`: Primary comparative visualization of the hypothesis.
- `Fig3_*.png`: Scaling behavior across $N=1000, 10000, 100000$.

## License
MIT License
