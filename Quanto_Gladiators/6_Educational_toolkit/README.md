
#  Educational Toolkit

**Task 6** of the *Quantum Walks and Monte Carlo* project, proudly submitted for WISER 2025. This educational toolkit provides an interactive learning platform to explore the Galton Board simulations—classical, quantum, biased, noisy, and comparative methods—through a Voila-based quantum dashboard. Designed to enhance understanding and engagement, it includes detailed instructions and visualizations for learners and educators alike.

##  Overview

The **Educational Toolkit** transforms the technical simulations from Tasks 1-5 into an accessible, hands-on learning experience. The `voila quantum_dashboard_simulator.ipynb` Jupyter notebook, powered by Voila, creates an interactive dashboard that allows users to visualize and manipulate Galton Board simulations across 5, 10, 15, 20, and 25 layers. This tool bridges theoretical concepts with practical application, making it ideal for students, researchers, and WISER judges to explore quantum computing and Monte Carlo methods interactively.

##  Applications

- **Interactive Learning**: Enables users to adjust parameters (e.g., layers, trials, noise levels) and see real-time updates in distributions.
- **Educational Outreach**: Serves as a teaching aid for quantum computing concepts, suitable for workshops or classrooms.
- **Project Demonstration**: Offers an engaging way to showcase the project’s depth and versatility to WISER 2025 evaluators.

##  Files and Structure

This folder contains the following key files and directories:

- **`voila quantum_dashboard_simulator.ipynb`**: The core Jupyter notebook that builds an interactive dashboard using Voila. It integrates data from previous tasks (1_Classical GB, 2_Quantum GB, task_3_Biased GB, 4_Noise, 5_Comparison) and provides widgets for parameter adjustment and visualization.
- **`results/`**: A directory storing output visualizations and dashboard snapshots (generated during runtime):
  - Example files may include `dashboard_5_layers.png`, `dashboard_10_layers.png`, etc., depending on user interactions.
- **`education_toolkit_README.md`**: This comprehensive guide to the educational toolkit.
- **`requirements.txt`**: A specific dependency list for the toolkit, including Voila and additional packages (see Prerequisites).

##  Setup and Running Instructions

### Prerequisites
To set up and run the educational toolkit, ensure you have the required dependencies installed. The root `requirements.txt` should include basic packages, but this folder’s `requirements.txt` adds toolkit-specific dependencies:
- **Qiskit (2.0)**: For quantum circuit execution.
- **Qiskit Aer**: For noise simulation (included with Qiskit).
- **NumPy (1.26.4)**: For numerical computations.
- **Matplotlib (3.9.2)**: For plotting.
- **Voila (0.5.5)**: For converting the notebook into an interactive dashboard.
- **ipywidgets (8.1.2)**: For interactive widgets in the dashboard.
Install these dependencies using the following commands:
```bash
pip install -r ../../requirements.txt
pip install -r 6_Educational_toolkit/requirements.txt
```

### Run the Simulation
1. **Launch Jupyter Notebook**:
   Navigate to the `6_Educational_toolkit` directory and start Jupyter Notebook by running:
   ```bash
   jupyter notebook voila quantum_dashboard_simulator.ipynb
   ```
2. **Convert to Voila Dashboard**:
   - Alternatively, launch the interactive dashboard directly with Voila:
     ```bash
     voila voila quantum_dashboard_simulator.ipynb --port=8866
     ```
   - Open your browser at `http://localhost:8866` to access the dashboard.
3. **Interact with the Dashboard**:
   - Use sliders and dropdowns to adjust layers (5-25), trials/shots (up to 10,000), and noise levels (0% to 10%).
   - Click buttons to regenerate plots and compare classical, quantum, biased, and noisy distributions.

### Outputs
After running the dashboard, explore the interactive interface and save any generated plots to the `results/` directory:
- The dashboard displays overlaid histograms comparing all methods, with real-time updates based on user inputs.
- A notable feature is the ability to toggle between layer depths, showing how distributions evolve with increasing complexity.

##  How It Works

### Mechanics
The toolkit implements an interactive quantum dashboard:
- **Data Integration**: Loads pre-computed results or runs simulations on-the-fly from `1_Classical GB`, `2_Quantum GB`, `task_3_Biased GB`, `4_Noise`, and `5_Comparison`.
- **Widgets**: Uses ipywidgets to create sliders for layers, trials, and noise probability, and buttons to trigger plot updates.
- **Visualization**: Matplotlib generates dynamic plots within the Voila interface, with legends and annotations for clarity.

### Parameters
- **Layers**: 5, 10, 15, 20, 25 (adjustable via slider).
- **Trials/Shots**: 1,000 to 10,000 (configurable range).
- **Noise Level**: 0% to 10% depolarizing error (adjustable).
- **Methods**: Classical, Quantum, Biased, Noisy (selectable via dropdown).

### Output
- The output is an interactive plot where the x-axis represents the number of right turns, and the y-axis shows frequency counts.
- Users can save snapshots (e.g., `dashboard_10_layers.png`) to `results/` for documentation.

### Complexity
- **Time Complexity**: O(layers * trials * methods), as simulations are re-run based on user inputs.
- **Space Complexity**: O(trials), as only current plot data is held in memory.

##  Relevance to WISER 2025

- **Technical Merit**: The toolkit delivers a robust, interactive platform with high-resolution plots (DPI=300), showcasing real-time simulation capabilities.
- **Communication**: The user-friendly dashboard and detailed instructions make complex concepts accessible and engaging for judges and learners.
- **Novelty**: Introduces an educational tool that integrates all project tasks, enhancing the project’s outreach and practical utility.

##  Next Steps

Looking ahead, we plan to:
- Add more interactive features, such as statistical metrics (e.g., variance, KS-test) in the dashboard.
- Expand the toolkit to include real hardware data  for comparison.
- Share the dashboard with the `6_Educational_toolkit/requirements.txt` for broader educational use.

##  Educational Insights
-  Teaches the fundamentals of Monte Carlo and quantum simulations through hands-on interaction.
-  Demonstrates the impact of parameters on outcomes, preparing learners for advanced quantum computing.
-  Supports the QUCAN QC101 Spring 2025 curriculum with a practical, project-based learning tool.

##  Team

- **Quanto Gladiators**: A dedicated team of up to 2 members, collaborating seamlessly via Discord to develop this educational resource.

##  Acknowledgments

- We extend our gratitude to WISER 2025 for providing the platform to showcase our work.




