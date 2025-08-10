# Monte Carlo Quantum Galton Board
### Project Name
Quantum Walks and Monte Carlo
### Team Name
Quanto_Gladiators
### Team Members
## Team Members
- **Nayan Jadhav**: WISER Enrollment ID: gst-AmKO7kPeqNZy6xI
- **Arham Sabadra**: WISER Enrollment ID: gst-U6ySL3CkHLSbHdy
- **Member2**: WISER Enrollment ID: WP2025-ZZZZ (Placeholder)

*Note: WISER Enrollment IDs are placeholders and will be updated upon receipt.*

#  Quantum Galton Box Analysis

This project explores the potential of **quantum computing** in simulating complex systems using a **Galton Box-style Monte Carlo approach**, also known as a **quantum walk simulation**. Inspired by the concept of the **Universal Statistical Simulator**, the project highlights how quantum circuits can model probabilistic behaviors efficiently, and serves as an educational exploration into both classical and quantum stochastic systems.

---

##  Objective

The main objective of this project is to **simulate, analyze, and compare** different versions of the Galton Box — classical, quantum, noisy quantum, and biased quantum — across multiple layers. The goal is to investigate:

- How quantum superposition and interference affect output distributions,
- The impact of noise on quantum circuits,
- Differences between biased and unbiased systems,
- And how quantum results deviate or converge to classical expectations under various conditions.

---

##  Background

A **Galton Box (Plinko)** is a statistical device where balls drop through several layers of pegs, taking random left or right turns, and accumulate into a distribution that closely resembles a binomial (or normal) curve. This randomness makes it an ideal candidate for **Monte Carlo simulation**. In the quantum version, **Hadamard gates** represent a quantum coin flip, allowing superpositions of left/right states.

The quantum Galton Box is relevant to:

- **Quantum walks** and **quantum Fourier transforms**
- **Simulation of high-dimensional probabilistic systems**
- **Particle transport** and **quantum dynamics**
- Benchmarking **noise models** and exploring **quantum error resilience**

---

##  Tasks Breakdown

###  Task 1 – Classical Simulation
Simulates the Galton Box using random binary decisions. Repeats this process for 5, 10, 15, 20, and 25 layers.

###  Task 2 – Quantum Galton Box
Implements quantum circuits using Hadamard gates and measurements, analyzing how quantum superposition distributes probabilities.

###  Task 3 – Biased Quantum Galton Box
Applies a bias to the quantum flips, altering probability distributions (e.g., bias toward '1' with 70% probability).

###  Task 4 – Noise Simulation
Uses **Qiskit Aer noise models** to introduce depolarizing errors into the quantum circuits, simulating realistic, noisy environments.

###  Task 5 – Method-Wise Comparison
Compares distributions using:

- **Total Variation Distance (TVD)**
- **Kullback–Leibler Divergence (KL)**
- (Optional) **Wasserstein Distance**

###  Task 6 – Report
Summarizes results, includes plots, analysis, and learning outcomes from all simulations.

###  Task 7 – Hardware Execution
Attempted real hardware execution using IBM Quantum, but due to Open Plan limitations (only simulator access), full execution on real devices was skipped.

---

##  Tools Used

- **Qiskit** (Quantum circuits, noise simulation)
- **NumPy, Matplotlib, SciPy** (Data processing, visualization, statistical comparisons)
- **Python 3.x** in Jupyter Notebooks
- **IBM Quantum Platform** (simulators used)

---

##  Outcomes

This project deepened understanding of how **quantum systems behave under uncertainty**, and how they compare to classical randomness. It showed the strengths of quantum simulations in reproducing statistical phenomena and highlighted current challenges, especially hardware access under free plans.

---

##  Repository Structure

```bash
Quanto_Gladiators/
│
├── Summary Report/
│    ├── summary.pdf
│    └── presentation.pdf
│
├── 1_Classical GB/               <--  Task 1: Classical Galton Box
│   ├── classical_galton_box.ipynb
│   ├── results/
│   │   ├── galton_box_5_layers.png
│   │   ├── galton_box_10_layers.png
│   │   ├── galton_box_15_layers.png
│   │   ├── galton_box_20_layers.png
│   │   ├── galton_box_25_layers.png
│   └── Classical_README.md
│
├── 2_Quantum GB/                 <--  Task 2: Quantum Galton Box
│   ├── quantum_galton_box.ipynb
│   ├── results_quantum/
│   │   ├── quantum_galton_box_5_layers.png
│   │   ├── quantum_galton_box_10_layers.png
│   │   ├── quantum_galton_box_15_layers.png
│   │   ├── quantum_galton_box_20_layers.png
│   │   ├── quantum_galton_box_25_layers.png
│   └── Quantum_README.md
│
├── task_3_Biased GB/         <--  Task 3: Biased Quantum Box
│   └── biased_quantum_galton_box.ipynb
│   ├── results_quantum_biased/
│   │   ├── biased_quantum_galton_box_5_layers.png
│   │   ├── biased_quantum_galton_box_10_layers.png
│   │   ├── biased_quantum_galton_box_15_layers.png
│   │   ├── biased_quantum_galton_box_20_layers.png
│   │   ├── biased_quantum_galton_box_25_layers.png
│   └── Biased_README.md 
│   
├── 4_Noise/         <--   Task 4: Noise Simulation (Qiskit Runtime)
│   └── noisy_galton_box.ipynb
│   ├── results\noise
│   │   ├── noisy_biased_galton_box_5_layers.png
│   │   ├── noisy_biased_galton_box_10_layers.png
│   │   ├── noisy_biased_galton_box_15_layers.png
│   │   ├── noisy_biased_galton_box_20_layers.png
│   │   ├── noisy_biased_galton_box_25_layers.png
│   └── Noise_README.md  
│
├── 5_Comparison/             <--  Task 5: Method-wise Comparison
│   ├── galton_box_comparison_5_layers.ipynb
│   ├── galton_box_comparison_10_layers.ipynb
│   ├── galton_box_comparison_15_layers.ipynb
│   ├── galton_box_comparison_20_layers.ipynb
│   ├── galton_box_comparison_25_layers.ipynb
│   ├── results/
│   │   ├── 5_layers/
│   │   │   └── galton_box_comparison_5_layers.png
│   │   ├── 10_layers/
│   │   │   └── galton_box_comparison_10_layers.png
│   │   ├── 15_layers/
│   │   │   └── galton_box_comparison_15_layers.png
│   │   ├── 20_layers/
│   │   │   └── galton_box_comparison_20_layers.png
│   │   └── 25_layers/ 
│   │       └── galton_box_comparison_25_layers.png     
│   └── Comparison_README.md
│
├── 6_Educational_toolkit/
│   ├── results/
│   ├── education_toolkit_README.md
│   ├── requirements.txt
│   └── voila quantum_dashboard_simulator.ipynb
│   
├── README.md                        <-- Project overview & task descriptions
├── requirements.txt                 <-- All required Python packages
└── .gitignore                       <-- Files to ignore (e.g., .ipynb_checkpoints)


```


