# Classical Galton Board Simulation

   This folder contains the Classical Galton Board simulation (Task 1) for the Quantum Walks and Monte Carlo project, part of WISER 2025 in collaboration with the National Nuclear Laboratory (NNL). The simulation uses Monte Carlo methods to model random walks, producing a binomial distribution that mirrors neutron scattering in nuclear reactors, a key application for NNL’s reactor design and safety efforts.
## Overview
The Galton Board is a device where balls fall through rows of pegs, randomly moving left or right, forming a binomial distribution that approximates a Gaussian curve with more layers. This random walk process is similar to Monte Carlo neutron transport, where neutrons scatter through reactor materials. Our simulation in classical_galton_box.ipynb uses Monte Carlo methods to track ball paths, modeling neutron-like behavior in a simplified form.
## Application to Monte Carlo Neutron Transport
Our classical simulation directly relates to neutron transport in nuclear reactors, a critical focus for NNL:

Neutron Scattering: Each ball’s random path in the Galton Board represents a neutron’s trajectory as it collides with atoms in a reactor core or moderator (e.g., graphite, uranium).
Monte Carlo Method: The simulation samples random left/right moves, akin to Monte Carlo tracking of neutron paths to predict flux (neutron flow) or shielding effectiveness.
Relevance to NNL: This model provides a baseline for understanding neutron behavior, which is essential for optimizing reactor designs and ensuring safety (e.g., minimizing radiation leakage).
Connection to Quantum: This classical simulation sets the stage for quantum walk-based simulations (2_Quantum GB), which could offer faster neutron transport computations, as suggested by Montanaro’s work (arXiv:1504.06987).

## Files and Structure

classical_galton_box.ipynb: Jupyter notebook implementing the Monte Carlo simulation for the Galton Board, with varying layers (5, 10, 15, 20, 25).
results/:
galton_box_5_layers.png: Plot for 5 layers.
galton_box_10_layers.png: Plot for 10 layers.
galton_box_15_layers.png: Plot for 15 layers.
galton_box_20_layers.png: Plot for 20 layers.
galton_box_25_layers.png: Plot for 25 layers.


Classical_README.md: This file, detailing the task and its application.

## Setup and Running

### Prerequisites:
Ensure dependencies are installed (see main requirements.txt):
NumPy
Matplotlib


Run:pip install -r ../requirements.txt




### Run the Simulation:
Open the notebook:jupyter notebook classical_galton_box.ipynb


Execute all cells to generate plots for 5, 10, 15, 20, and 25 layers.


### Outputs:
Plots in results/ show binomial distributions, resembling neutron flux patterns in reactors.
Example: galton_box_10_layers.png shows a bell-shaped curve, similar to neutron distribution after scattering.



## How It Works

Simulation: The notebook uses Monte Carlo methods to simulate balls falling through a Galton Board. For each ball, it randomly chooses left (-1) or right (+1) at each layer, tracking the final position.
### Parameters:
Layers: Number of peg rows (5, 10, 15, 20, 25).
Trials: Number of balls (e.g., 10,000).


Output: A histogram of final positions, forming a binomial distribution that approximates a Gaussian curve, mimicking neutron flux in nuclear reactors.
Complexity:
Time: O(layers * trials), as each ball processes multiple steps.
Space: O(trials) for storing positions.



### Relevance to WISER 2025

Technical Merit: The simulation accurately models random walks, validated by plots showing binomial distributions.
Communication: Clear visualizations and documentation explain the neutron transport analogy.
Novelty: Links Monte Carlo neutron transport to NNL’s reactor design, serving as a baseline for quantum speed-ups in later tasks.

### Next Steps

Compare with quantum simulations (2_Quantum GB) to explore computational speed-ups for neutron transport.
See task_5_comparison for method-wise analysis, including neutron transport accuracy.
Explore src/educational_tool.ipynb for an interactive explanation of neutron transport using this simulation.

### Team

Quanto Gladiators: Up to 3 members, collaborating via Discord.
