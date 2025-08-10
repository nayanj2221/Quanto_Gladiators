# Biased Galton Board Simulation

Task 3 of the Quantum Walks and Monte Carlo project, submitted for WISER 2025. This simulation introduces biased quantum walks using Qiskit, modeling non-uniform neutron scattering.

## Overview

The Biased Galton Board adds a twist to the classic and quantum models. Instead of equal left-right probabilities, this simulation incorporates bias (e.g., 70% right, 30% left) using quantum circuits, reflecting real-world neutron scattering with material-dependent probabilities. The `biased_galton_box.ipynb` notebook leverages Qiskit to simulate these biased walks, enhancing neutron transport predictions.

## Application to Monte Carlo Neutron Transport

This biased quantum simulation tackles complex neutron behavior:

- **Biased Neutron Scattering**: Models neutrons scattering unevenly through reactor materials like uranium or graphite, where bias reflects material properties.
- **Monte Carlo Enhancement**: Biased quantum walks offer refined flux predictions, building on classical and unbiased quantum methods.
- **Impact**: Improves reactor shielding and safety by simulating realistic neutron paths, reducing errors in large-scale transport models.
- **Quantum Edge**: Extends `2_Quantum GB`, exploring how bias affects speedup potential (Montanaro, arXiv:1504.06987).

## Files and Structure

- **`biased_galton_box.ipynb`**: Jupyter notebook implementing biased quantum walk simulations with Qiskit, testing 5, 10, 15, 20, and 25 layers.
- **`results_biased/`**:
  - `biased_galton_box_5_layers.png`: Histogram for 5 layers.
  - `biased_galton_box_10_layers.png`: 10-layer distribution.
  - `biased_galton_box_15_layers.png`: 15-layer plot.
  - `biased_galton_box_20_layers.png`: 20-layer visualization.
  - `biased_galton_box_25_layers.png`: 25-layer result.
- **`Biased_README.md`**: This guide to the biased simulation.

## Setup and Running Instructions

### Prerequisites

- Install dependencies from the root `requirements.txt`:
  - Qiskit (1.2.0)
  - NumPy (1.26.4)
  - Matplotlib (3.9.2)
- Command:
  ```bash
  pip install -r ../../requirements.txt
  ```

### Run the Simulation

- Launch Jupyter Notebook:
  ```bash
  jupyter notebook biased_galton_box.ipynb
  ```
- Execute all cells to simulate biased quantum walks for 5, 10, 15, 20, and 25 layers (default: 10,000 shots).

### Outputs

- Check `results_biased/` for plots showing skewed distributions, mimicking biased neutron flux patterns. Highlight: `biased_galton_box_10_layers.png` reflects uneven scattering due to quantum bias.

## How It Works

- **Mechanics**: Qiskit creates biased quantum circuits, adjusting probabilities (e.g., via rotation gates) to simulate non-uniform walks.
- **Parameters**:
  - **Layers**: 5, 10, 15, 20, 25 (quantum steps).
  - **Shots**: 10,000 (default measurement runs).
  - **Bias**: Configurable (e.g., 70% right, 30% left).
- **Output**: Histograms show skewed distributions, modeling complex neutron behavior.
- **Complexity**: O(layers * shots) time, O(shots) space, with bias impacting quantum advantage.

## Relevance to WISER 2025

- **Technical Merit**: Accurate biased quantum simulations, validated by high-res plots (DPI=300) mimicking neutron flux variations.
- **Communication**: Clear link between biased walks and neutron scattering, engaging for judges.
- **Novelty**: Introduces biased quantum methods for neutron transport, advancing beyond classical and unbiased models.

## Next Steps

- Compare with `1_Classical GB` and `2_Quantum GB` for bias impact.
- Analyze `task_5_comparison` for method accuracy.
- Explore `src/educational_tool.ipynb` for biased neutron transport insights.

## Team

Quanto Gladiators: A group of up to 3 members, collaborating via Discord.

## Acknowledgments

- Thanks to WISER 2025 for the platform.
- Credit to Montanaro (arXiv:1504.06987) for quantum speedup ideas.
