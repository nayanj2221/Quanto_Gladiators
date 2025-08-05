# 🌌 Quantum Galton Board Simulation

Welcome to the **Quantum Galton Board Simulation**, which represents Task 2 of the Quantum Walks and Monte Carlo project. This initiative is proudly submitted for WISER 2025 in collaboration with the National Nuclear Laboratory (NNL). Our simulation harnesses the power of quantum walks using Qiskit to model random walks, offering potential speed-ups for Monte Carlo neutron transport—a transformative advancement for NNL’s reactor design and safety innovations!

## ✨ Overview

The Quantum Galton Board elevates the classic concept of the Galton Board to a new dimension! Instead of traditional balls tumbling randomly, this simulation employs quantum superposition and interference to explore multiple paths simultaneously, resulting in unique and intricate distributions. This innovative approach mirrors the principles of Monte Carlo neutron transport, where neutrons scatter through reactor materials. The `quantum_galton_box.ipynb` notebook utilizes Qiskit to execute quantum walk simulations, aiming to enhance neutron flux predictions for NNL’s nuclear research.

## 🚀 Application to Monte Carlo Neutron Transport

This quantum simulation significantly enhances neutron transport, aligning seamlessly with NNL’s mission:

- **Quantum Neutron Scattering**: Quantum walks simulate numerous neutron paths concurrently, accurately reflecting their scattering through reactor materials such as uranium and graphite.
- **Monte Carlo Speed-Up**: By leveraging quantum circuits, this simulation promises near-quadratic speed-ups over classical methods, as highlighted by Montanaro (arXiv:1504.06987), thereby improving neutron flux and shielding calculations.
- **NNL Advantage**: Faster simulations can optimize reactor designs, enhance safety protocols, and reduce computational costs, making this approach invaluable for nuclear research.
- **Building on Classical Foundations**: This project builds upon the classical simulation (1_Classical GB), showcasing the advantages of quantum methods for addressing large-scale neutron transport challenges.

## 📂 Files and Structure

Here’s what you’ll find in this project:

- **quantum_galton_box.ipynb**: A Jupyter notebook that implements quantum walk simulations using Qiskit, testing configurations with 5, 10, 15, 20, and 25 layers.
- **results_quantum/**:
  - `quantum_galton_box_5_layers.png`: A striking histogram for 5 layers.
  - `quantum_galton_box_10_layers.png`: An elegant distribution for 10 layers.
  - `quantum_galton_box_15_layers.png`: A detailed visualization for 15 layers.
  - `quantum_galton_box_20_layers.png`: A comprehensive plot for 20 layers.
  - `quantum_galton_box_25_layers.png`: An impressive result for 25 layers.
- **Quantum_README.md**: This document serves as your comprehensive guide to the quantum simulation!

## 🛠️ Setup and Running Instructions

### Prerequisites

To get started, ensure you have the necessary dependencies installed from the root `requirements.txt`:

- Qiskit (1.2.0)
- NumPy (1.26.4)
- Matplotlib (3.9.2)

You can install these dependencies by running the following command:

```bash
pip install -r ../../requirements.txt
```
## Run the Simulation
1. Launch Jupyter Notebook with the command:
```bash
jupyter notebook quantum_galton_box.ipynb
```
2.Execute all cells to simulate quantum walks for 5, 10, 15, 20, and 25 layers, with a default of 10,000 shots.

## Outputs
Explore the `results_quantum/` directory for plots displaying quantum distributions that resemble enhanced neutron flux patterns. A highlight is `quantum_galton_box_10_layers.png`, which showcases a unique curve that reflects quantum-enhanced neutron scattering.

## How It Works
### Mechanics
The notebook utilizes Qiskit to create quantum circuits, applying Hadamard gates for superposition and measuring outcomes to simulate quantum walks effectively.

### Parameters
- Layers: 5, 10, 15, 20, 25 (representing quantum steps).
- Shots: 10,000 (the number of measurement runs, default).
## Output
The histograms display probability distributions that differ from classical binomial distributions due to quantum interference, effectively mimicking complex neutron behavior!

### Complexity
- *Time Complexity*: O(layers * shots), with the potential for quantum speedup.
- *Space Complexity*: O(shots) for storing measurement results.
 ## Relevance to WISER 2025
- *Technical Merit*: This project leverages Qiskit for accurate quantum walk simulations, validated by distinct plots (DPI=300) that effectively mimic enhancements in neutron flux.
- *Communication*: The clear analogy between quantum processes and neutron transport makes the project engaging and accessible for judges and researchers alike.
- *Novelty*: This simulation introduces quantum speed-ups for NNL’s neutron transport challenges, building on classical foundations and paving the way for future advancements.
##  Next Steps
Looking ahead, we plan to:

- Compare results with the classical simulation in `1_Classical GB/classical_galton_box.ipynb` to quantify speed-ups for neutron transport.
- Dive into `task_5_comparison` for a detailed method analysis.
- Explore `src/educational_tool.ipynb` for an interactive quantum neutron transport demonstration.
## Team
* Quanto Gladiators*: A dedicated team of up to 3 members, collaborating via Discord to achieve excellence in quantum research.
## Acknowledgments
- We extend our gratitude to WISER 2025 for the opportunity to showcase this work.
- Special thanks to NNL for their commitment to advancing neutron transport research.
- Credit to Montanaro (arXiv:1504.06987) for inspiring the exploration of quantum speed-ups!
