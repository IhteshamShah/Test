# MOCI Project

This repository contains a small gridworld experiment for a multi-objective constraint inference using inverse reinforcement learning (MOCI IRL) setup.

## Run instructions

1. Open a terminal in the project folder:

```bash
cd /Users/Desktop/MOCI
```

2. Run the main script with Python:

```bash
python Main.py
```

3. The script generates plots and saves outputs in the `Results/` directory.

## Dependencies

Make sure the following Python packages are installed:

- `numpy`
- `matplotlib`
- `scipy`

Install missing packages with:

```bash
pip install numpy matplotlib scipy
```

## Files

- `Main.py`
  - Main execution script.
  - Defines a customizable gridworld MDP, generates expert demonstrations, runs the EM-MOCI inference framework, and creates plots of trajectories, inferred constraints, and preference recovery.
  - Calls `Sensitivity_Scalability_analysis.py` to run additional sensitivity and scalability experiments.

- `gridworld.py`
  - Defines the `CustomizableFeatureMDP` gridworld environment.
  - Sets up terrain features and transition dynamics for a grid-based MDP.
  - Provides visualization helpers to plot the grid, expert trajectories, inferred constraints, and preference recovery charts.

- `MOCI_IRL.py`
  - Implements the core MOCI IRL algorithm components.
  - Includes backward pass computation, trajectory sampling, trajectory probability calculation, EM-step responsibilities, weight updates, and constraint selection.

- `Sensitivity_Scalability_analysis.py`
  - Runs experiments to evaluate false positive rate and runtime performance.
  - Produces plots showing how dataset size and grid size affect inference quality and scalability.


