
#  Noise Galton Board Simulation

**Task 4** of the *Quantum Walks and Monte Carlo* project, proudly submitted for WISER 2025. This simulation incorporates noise effects using Qiskit Runtime, modeling realistic quantum hardware limitations in a Galton Board framework. It includes detailed visualizations and an educational component to deepen understanding of noisy quantum systems.

##  Overview

The **Noise Galton Board** builds on the quantum and biased models by introducing noise, such as gate errors and decoherence, to simulate the imperfections of real quantum hardware. The `noisy_galton_box.ipynb` Jupyter notebook leverages Qiskit Runtime to apply noise models across 5, 10, 15, 20, and 25 layers with 10,000 shots each. This task explores how noise impacts quantum walk distributions, providing insights into the robustness of quantum algorithms and serving as a practical learning tool.

##  Applications

- **Noise Modeling**: Simulates quantum hardware imperfections like gate errors and decoherence.
- **Robustness Testing**: Evaluates the resilience of quantum walks under noisy conditions.
- **Educational Value**: Offers a hands-on example for learning about noise in quantum computing, integrated into the `6_Educational_toolkit`.

##  Files and Structure

This folder contains the following key files and directories:

- **`noisy_galton_box.ipynb`**: The core Jupyter notebook implementing the noisy quantum simulation. It uses Qiskit Runtime to apply noise models, simulate walks, and generate histograms for 5, 10, 15, 20, and 25 layers with 10,000 shots per layer.
- **`results/noise/`**: A directory storing the output visualizations:
  - `noisy_biased_galton_box_5_layers.png`: A detailed histogram showing the distribution after 5 layers with noise.
  - `noisy_biased_galton_box_10_layers.png`: A plot for 10 layers, reflecting early noise effects.
  - `noisy_biased_galton_box_15_layers.png`: A distribution for 15 layers with noticeable noise impact.
  - `noisy_biased_galton_box_20_layers.png`: A visualization for 20 layers, showing increased noise influence.
  - `noisy_biased_galton_box_25_layers.png`: A result for 25 layers, highlighting the full effect of noise on the distribution.
- **`Noise_README.md`**: This comprehensive guide to the noise simulation.

##  Setup and Running Instructions

### Prerequisites
To run this simulation, ensure you have the required dependencies installed from the root `requirements.txt` file:
- **Qiskit (1.2.0)**: For quantum circuit creation and noise modeling with Qiskit Runtime.
- **NumPy (1.26.4)**: For numerical computations and array handling.
- **Matplotlib (3.9.2)**: For generating high-quality plots and visualizations.
Install these dependencies using the following command:
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
   - Each simulation uses 10,000 shots by default, with configurable noise parameters adjustable within the code.

### Outputs
After running the simulation, explore the `results/noise/` directory to view the generated plots:
- The histograms display the number of outcomes at each final position, distorted by noise effects.
- A notable example is `noisy_biased_galton_box_10_layers.png`, which shows how noise begins to disrupt the smooth distribution, providing a clear visual of quantum hardware limitations.

##  How It Works

### Mechanics
The simulation implements a noisy quantum Monte Carlo approach:
- **Initialization**: 10,000 quantum walks are initiated at the top of the Galton Board.
- **Noise Application**: Qiskit Runtime applies noise models (e.g., depolarizing noise, amplitude damping) to mimic real quantum hardware errors at each of the 5 to 25 layers.
- **Measurement**: The final states are measured with 10,000 shots, and the results are binned to create histograms.

### Parameters
- **Layers**: 5, 10, 15, 20, 25 (representing the number of quantum steps).
- **Shots**: 10,000 (the number of measurement runs per layer configuration).
- **Noise Model**: Configurable (e.g., depolarizing noise with a probability of 0.01 per gate, adjustable in the code).

### Output
- The output consists of histograms plotted using Matplotlib, where the x-axis represents the final position, and the y-axis shows the frequency of outcomes, altered by noise.
- As layers increase, the distribution becomes more irregular, reflecting the cumulative effect of noise.

### Complexity
- **Time Complexity**: O(layers * shots), as each quantum walk is executed with noise applied at each step.
- **Space Complexity**: O(shots), as only the measurement outcomes need to be stored for histogramming.

##  Relevance to WISER 2025

- **Technical Merit**: The simulation delivers realistic noise-affected distributions, validated by high-resolution plots (DPI=300) that clearly demonstrate the impact of quantum hardware imperfections.
- **Communication**: The visualizations and detailed documentation make the noise concept accessible and engaging for judges and learners, supported by the educational toolkit.
- **Novelty**: Introduces noise modeling in quantum simulations, testing the practicality of quantum walks under real-world conditions.

##  Next Steps

Looking ahead, we plan to:
- Compare results with the biased simulation in `task_3_Biased GB/biased_quantum_galton_box.ipynb` to assess noise versus bias effects.
- Analyze method comparisons in `5_Comparison/galton_box_comparison_*.ipynb` for deeper insights.
- Explore the `6_Educational_toolkit/voila quantum_dashboard_simulator.ipynb` for an interactive learning experience based on this noisy simulation.

##  Team

- **Quanto Gladiators**: A dedicated team of up to 3 members, collaborating seamlessly via Discord to advance this project.

##  Acknowledgments

- We extend our gratitude to WISER 2025 for providing the platform to showcase our work.
- Special thanks to Montanaro (arXiv:1504.06987) for inspiring the exploration of quantum techniques that inform this noise analysis.

 
