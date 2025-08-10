# Method-wise Comparison

Task 5 of the Quantum Walks and Monte Carlo project, submitted for WISER 2025. This task provides a detailed comparison of classical, quantum, biased, and noisy Galton Board simulations across 5, 10, 15, 20, and 25 layers. Designed to evaluate performance metrics and distribution differences, it includes comprehensive visualizations and an educational component to enhance understanding of simulation techniques.

## Overview

The Method-wise Comparison analyzes the outputs of four simulation approaches—classical Monte Carlo, ideal quantum walks, biased quantum walks, and noisy quantum walks—using dedicated Jupyter notebooks. The `galton_box_comparison_*.ipynb` files (for 5, 10, 15, 20, and 25 layers) compare histograms, accuracy, and efficiency, providing insights into the strengths and limitations of each method. This task builds on previous simulations (Tasks 1-4) and serves as a critical evaluation step, supported by an educational toolkit for deeper learning.

## Applications

- **Method Evaluation**: Compares classical, quantum, biased, and noisy methods to identify optimal use cases.
- **Performance Insights**: Analyzes accuracy, distribution shapes, and computational efficiency across layers.
- **Educational Value**: Offers a practical example for learning comparative analysis, integrated into the `6_Educational_toolkit`.

## Files and Structure

This folder contains the following key files and directories:

- **`galton_box_comparison_5_layers.ipynb`**: Notebook comparing methods for 5 layers.
- **`galton_box_comparison_10_layers.ipynb`**: Notebook for 10 layers.
- **`galton_box_comparison_15_layers.ipynb`**: Notebook for 15 layers.
- **`galton_box_comparison_20_layers.ipynb`**: Notebook for 20 layers.
- **`galton_box_comparison_25_layers.ipynb`**: Notebook for 25 layers.
- **`results/`**: A directory storing the output visualizations, organized by layer depth:
  - `5_layers/`
    - `galton_box_comparison_5_layers.png`: Comparative histogram for 5 layers.
  - `10_layers/`
    - `galton_box_comparison_10_layers.png`: Comparative plot for 10 layers.
  - `15_layers/`
    - `galton_box_comparison_15_layers.png`: Comparative distribution for 15 layers.
  - `20_layers/`
    - `galton_box_comparison_20_layers.png`: Comparative visualization for 20 layers.
  - `25_layers/`
    - `galton_box_comparison_25_layers.png`: Comparative result for 25 layers.
- **`Comparison_README.md`**: This guide to the comparison analysis.

## Setup and Running Instructions

### Prerequisites

To run this comparison, ensure required dependencies are installed from the root `requirements.txt` file:
- **Qiskit (2.0)**: For quantum circuit execution and noise modeling.
- **Qiskit Aer**: For local noise simulation (included with Qiskit installation).
- **NumPy (1.26.4)**: For numerical computations and array handling.
- **Matplotlib (3.9.2)**: For generating high-quality comparative plots.
Install these dependencies using the command:
```bash
pip install -r ../../requirements.txt
```

### Run the Simulation

1. **Launch Jupyter Notebook**:
   Navigate to the `5_Comparison` directory and start Jupyter Notebook by running:
   ```bash
   jupyter notebook galton_box_comparison_5_layers.ipynb
   ```
   (Repeat for 10, 15, 20, and 25 layers by opening the respective notebooks.)
2. **Execute the Notebook**:
   - Open the notebook in your browser.
   - Run all cells sequentially to load data from previous tasks (1_Classical GB, 2_Quantum GB, task_3_Biased GB, 4_Noise) and generate comparative plots.
   - Each simulation uses 10,000 trials/shots by default, consistent with prior tasks.

### Outputs

After running the simulation, explore the `results/` directory to view the generated plots:
- The comparative histograms overlay distributions from classical, quantum, biased, and noisy methods.
- A notable example is `galton_box_comparison_10_layers.png`, which shows how noise and bias deviate from the ideal quantum and classical curves, providing a clear visual of method differences.

## How It Works

### Mechanics

The comparison implements a multi-method analysis approach:
- **Data Collection**: Loads pre-computed results from `classical_galton_box.ipynb`, `quantum_galton_box.ipynb`, `biased_quantum_galton_box.ipynb`, and `noisy_galton_box.ipynb`.
- **Comparison**: Plots overlaid histograms and calculates metrics (e.g., mean, variance, Kolmogorov-Smirnov distance) to quantify differences.
- **Visualization**: Uses Matplotlib to generate side-by-side or overlaid plots for each layer.

### Parameters

- **Layers**: 5, 10, 15, 20, 25 (representing the number of steps or rows).
- **Trials/Shots**: 10,000 (consistent with previous simulations).
- **Methods**: Classical Monte Carlo, Ideal Quantum, Biased Quantum, Noisy Quantum.

### Output

- The output consists of comparative histograms where the x-axis represents the final position (number of right turns), and the y-axis shows the frequency of outcomes.
- Annotations highlight shifts due to bias and noise, with legends distinguishing each method.

### Complexity

- **Time Complexity**: O(layers * trials * methods), as each method’s data is processed for each layer.
- **Space Complexity**: O(layers * trials), as results for all methods are stored for comparison.

## Relevance to WISER 2025

- **Technical Merit**: The comparison delivers rigorous multi-method analysis, validated by high-resolution plots (DPI=300) that clearly demonstrate distribution and performance differences.
- **Communication**: The visualizations and detailed documentation make the comparison accessible and engaging for judges and learners, supported by the educational toolkit.
- **Novelty**: Provides a comprehensive evaluation of simulation techniques, setting the stage for future optimizations and real hardware validation.

## Next Steps

Looking ahead, plans include:
- Refine the comparison by adding statistical tests (e.g., p-values) to quantify method differences.
- Explore the `6_Educational_toolkit/voila quantum_dashboard_simulator.ipynb` for an interactive comparison tool.
- Prepare for Task 7 (real hardware execution) by validating these findings on actual quantum devices.

## Educational Insights

- Teaches how to compare classical and quantum methods, highlighting noise and bias effects.
- Bridges theoretical simulations with practical evaluation, preparing learners for advanced quantum computing challenges.
- Supports the QUCAN QC101 Spring 2025 curriculum with hands-on comparative analysis.

## Team

Quanto Gladiators: A dedicated group of up to 2 members, collaborating via Discord to advance this project.

## Acknowledgments

- Gratitude is extended to WISER 2025 for providing the platform to showcase this work.



