Quantum Teleportation Project

This repository contains onw Jupyter notebook that implements and tests quantum teleportation using Qiskit. Each project builds on the previous one, moving from the basic teleportation protocol to more advanced verification with fidelity calculations and noisy channels.

Project 1 – Ideal Teleportation Protocol
File: Project 1.ipynb

This notebook implements the standard qubit teleportation circuit step by step:

1. Input State Preparation
   Arbitrary qubit states (e.g. |0>, |1>, |+>, |−>, |i+>, |i−>) are prepared for teleportation.

2. Entanglement Generation
   Alice and Bob share a Bell pair.

3. Bell Measurement
   Alice performs a CNOT and Hadamard gate, followed by measurement in the Bell basis.

4. Classical Feed-Forward
   Depending on Alice’s measurement outcomes, Bob applies Pauli-X or Pauli-Z corrections to recover the input state.

5. Verification
   The circuit is simulated, and measurement results confirm successful teleportation in the ideal (noise-free) case.

Project 2 – Fidelity and Noise Analysis
File: Project 2.ipynb

This notebook extends Project 1 by adding state verification and noise effects:

1. Fidelity Function
   Implements a custom fidelity function F(rho_in, rho_out) to compare the input state with Bob’s output state.

2. Random States on the Bloch Sphere
   Tests teleportation on a variety of random qubit states to evaluate protocol performance beyond fixed basis states.

3. Noisy Channels
   Introduces realistic noise models (depolarizing, amplitude damping, measurement errors) using Qiskit’s AerSimulator.
   Demonstrates how noise reduces teleportation fidelity.

4. Results and Analysis
   Fidelity values and measurement statistics are displayed in tables for comparison between the ideal and noisy cases.

Requirements
- Python 3.12
- Qiskit Terra 2.1+
- Jupyter Lab or Notebook
- Pandas (for result tables)

Install dependencies inside your environment:
pip install qiskit pandas

Running the Notebooks
1. Activate your environment (for example, teleportation).
2. Launch Jupyter Lab:
   jupyter lab
3. Open Project 1.ipynb or Project 2.ipynb and run the cells sequentially.

What You Will Learn
- How quantum teleportation works in theory.
- How to implement teleportation in Qiskit.
- How to test correctness using fidelity.
- How noise affects quantum information transfer.
