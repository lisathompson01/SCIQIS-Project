# Quantum State Teleportation with Noise Models

This repository contains a Jupyter Notebook that demonstrates **quantum state teleportation** using [Qiskit](https://qiskit.org/), and investigates how different types of **noise** affect the fidelity of teleportation.

The notebook is designed to be **educational**: it walks through the ideal teleportation protocol step by step, then introduces realistic noise models to show how experimental imperfections degrade performance.

---

## Features

- **Teleportation protocol**
  - Build the full circuit from scratch with clear markdown explanations.
  - Verify correctness on random input states.
  - Compute fidelity between input and output states.

- **Noise models tested**
  1. **Gate errors (depolarizing noise)** – random Pauli errors applied during gate operations.
  2. **Decoherence (T₁/T₂ relaxation/dephasing)** – loss of quantum information over time.
  3. **Measurement imperfections (readout errors)** – bit flips during classical readout that affect Bob’s correction step.

- **Visualizations**
  - Probability histograms for intuition.
  - Fidelity sweeps across error parameters.
  - Line plots and heatmaps to explore parameter ranges.

- **Conclusions**
  - Gate errors and decoherence both lower fidelity, with **two-qubit gates** contributing most strongly.
  - Readout errors directly affect Bob’s correction step and are especially harmful to teleportation success.
  - Fidelity (not probability counts) is the correct figure of merit for assessing teleportation success.

---
## Future Work

Since this was a one-week project, there were several aspects I didn’t have time to explore fully.  
In particular, I would like to:  
- Combine multiple noise sources (gate errors, decoherence, and measurement errors) to study their joint effect on fidelity.  
- Run the teleportation circuit on real IBM Quantum hardware via IBM Lab for comparison with simulation results.  
- Extend the study to continuous-variable quantum teleportation, which opens interesting connections to quantum optics.
- Refactor the notebook by moving many of the function definitions into separate Python files within the repository, making the notebook shorter, cleaner, and more modular.  
---

## Requirements

The notebook was developed with the following versions:

- **Python**: 3.12.7 (Anaconda, Clang 14.0.6)
- **Qiskit Terra**: 2.1.1
- **Qiskit Aer**: 0.17.1
- **Matplotlib**: 3.10.5

To install the dependencies in a fresh environment:

```bash
pip install qiskit qiskit-aer matplotlib pylatexenc
```

---

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```

2. Launch Jupyter Lab or Notebook:
   ```bash
   jupyter lab
   ```
   Open `Main.ipynb`.

3. Run cells in order. Each section contains **markdown explanations** before the code to guide you.

---

## Repository Structure

```
├── Main.ipynb        # Full teleportation notebook with noise models
├── README.md         # This file
```

---

## Learning Outcomes

By working through the notebook, you will:

- Understand the **quantum teleportation protocol** step by step.
- See how **ideal teleportation** achieves fidelity ≈ 1 for any input state.
- Learn how to **simulate realistic noise models** in Qiskit Aer.
- Quantify the effect of different noise sources using **state fidelity**.
- Interpret **visualizations** of how errors degrade teleportation performance.
