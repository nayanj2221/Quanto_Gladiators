# Noise Galton Board Simulation

Task 4 of the Quantum Walks and Monte Carlo project, submitted for WISER 2025. This simulation incorporates realistic quantum noise effects using Qiskit Aer, modeling imperfections like depolarizing errors in a Galton Board framework. It includes detailed visualizations and an educational component to deepen understanding of noisy quantum systems.

## Overview

The Noise Galton Board extends the quantum and biased models by introducing noise, such as gate errors and decoherence, to simulate real quantum hardware limitations. The `noisy_galton_box.ipynb` Jupyter notebook leverages Qiskit Runtime and Qiskit Aer to apply a depolarizing noise model across 5, 10, 15, 20, and 25 layers with 10,000 shots each. This task explores how noise impacts quantum walk distributions, bridging theoretical predictions with practical quantum computing challenges, and serves as a practical learning tool.

## Applications

- **Noise Modeling**: Simulates quantum hardware imperfections like gate errors and decoherence using a depolarizing noise model.
- **Robustness Testing**: Evaluates the resilience of quantum walks under noisy conditions.
- **Educational Value**: Offers a hands-on example for learning about noise in quantum computing, integrated into the `6_Educational_toolkit`.

## Files and Structure

This folder contains the following key files and directories:

- **`noisy_galton_box.ipynb`**: The core Jupyter notebook implementing the noisy quantum simulation. It uses Qiskit Aer’s `depolarizing_error` model applied to Hadamard gates, simulating walks for 5, 10, 15, 20, and 25 layers with 10,000 shots per layer.
- **`results/noise/`**: A directory storing the output visualizations:
  - `noisy_biased_galton_box_5_layers.png`: Histogram showing the distribution after 5 layers with noise.
  - `noisy_biased_galton_box_10_layers.png`: Plot for 10 layers, reflecting early noise effects.
  - `noisy_biased_galton_box_15_layers.png`: Distribution for 15 layers with noticeable noise impact.
  - `noisy_biased_galton_box_20_layers.png`: Visualization for 20 layers, showing increased noise influence.
  - `noisy_biased_galton_box_25_layers.png`: Result for 25 layers, highlighting the full effect of noise on the distribution.
- **`Noise_README.md`**: This guide to the noise simulation.

## Setup and Running Instructions

### Prerequisites

To run this simulation, ensure required dependencies are installed from the root `requirements.txt` file:
- **Qiskit (2.0.1)**: For quantum circuit creation and noise modeling with Qiskit Runtime.
- **Qiskit Aer**: For local noise simulation (included with Qiskit installation).
- **NumPy (1.26.4)**: For numerical computations and array handling.
- **Matplotlib (3.9.2)**: For generating high-quality plots and visualizations.
Install these dependencies using the command:
```bash
pip install -r ../../requirements.txt
```

### Run the Simulation

1. **Launch Jupyter Notebook**:
   Navigate to the `4_Noise` directory and start Jupyter Notebook by running:
   ```bash
   jupyter notebook noisy_galton_box.ipynb
   ```
2. **Execute the Notebook**:
   - Open the notebook in your browser.
   - Run all cells sequentially to simulate the noisy Galton Board for 5, 10, 15, 20, and 25 layers.
   - Each simulation uses 10,000 shots by default, with a 5% depolarizing error probability applied to all Hadamard gates, adjustable within the code.

### Outputs

After running the simulation, explore the `results/noise/` directory to view the generated plots:
- The histograms display the number of outcomes at each final position, distorted by noise effects.
- A notable example is `noisy_biased_galton_box_10_layers.png`, which shows how a 5% depolarizing noise begins to disrupt the smooth distribution, providing a clear visual of quantum hardware limitations.

## How It Works

### Mechanics

The simulation implements a noisy quantum Monte Carlo approach using Qiskit Aer:
- **Initialization**: 10,000 quantum walks are initiated at the top of the Galton Board.
- **Noise Application**: A `depolarizing_error` model with a 5% probability is applied to all Hadamard gates using Qiskit Aer’s `NoiseModel`, mimicking random state replacement due to decoherence and gate imperfections.
- **Measurement**: The final states are measured with 10,000 shots, and the results are binned to create histograms.

### Parameters

- **Layers**: 5, 10, 15, 20, 25 (representing the number of quantum steps).
- **Shots**: 10,000 (measurement runs per layer configuration).
- **Noise Model**: Depolarizing noise with a 5% error probability per Hadamard gate (configurable).

### Output

- The output consists of histograms plotted using Matplotlib, where the x-axis represents the number of right turns (1s), and the y-axis shows the frequency of outcomes, altered by noise.
- The curves shift from ideal quantum behavior, comparing with classical and biased results, highlighting noise-induced distortions.

### Complexity

- **Time Complexity**: O(layers * shots), as each quantum walk is executed with noise applied at each step.
- **Space Complexity**: O(shots), as only the measurement outcomes need to be stored for histogramming.

## Relevance to WISER 2025

- **Technical Merit**: The simulation delivers realistic noise-affected distributions, validated by high-resolution plots (DPI=300) that demonstrate the impact of depolarizing noise on quantum walks.
- **Communication**: The visualizations and detailed documentation make the noise concept accessible and engaging for judges and learners, supported by the educational toolkit.
- **Novelty**: Introduces noise modeling with Qiskit Aer, testing the practicality of quantum walks under real-world conditions, preparing for Task 7 (real hardware validation).

## Next Steps

Looking ahead, plans include:
- Compare noisy results with ideal quantum and classical simulations in `5_Comparison/galton_box_comparison_*.ipynb`.
- Adjust noise probabilities (e.g., 0.1 or 0.2) to observe changes.
- Explore `6_Educational_toolkit/voila quantum_dashboard_simulator.ipynb` for an interactive learning experience based on this noisy simulation.

## Educational Insights

- Teaches how quantum noise affects algorithm outputs, using depolarizing noise as a key example.
- Bridges theory and practical quantum computing limitations, preparing learners for real hardware execution.


## Team

Quanto Gladiators: A dedicated group of up to 3 members, collaborating seamlessly via Discord to advance this project.

## Acknowledgments

- Gratitude is extended to WISER 2025 for providing the platform to showcase this work.


