# Building Neural Differential Equations from Scratch

Welcome to **NeuroDiffEqLab**! This project is a practical journey in building Neural Differential Equations (Neural DEs) from scratch, inspired by foundational research papers. Here, you’ll find implementations of a range of models, from basic Neural ODEs to advanced frameworks like Neural SDEs, Neural CDEs, and PINNs.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Implemented Models](#implemented-models)
- [Installation](#installation)
- [Repository Structure](#repository-structure)
- [Usage](#usage)
- [Examples and Visualizations](#examples-and-visualizations)
- [References](#references)
- [Acknowledgements](#acknowledgements)

---

## Project Overview

**NeuroDiffEqLab** provides an in-depth, low-level exploration of Neural Differential Equations. Every model is implemented without high-level libraries, focusing on the mathematical foundation and methods from the original research. This approach offers full control over each component—from forward integration to backpropagation with adjoint methods.

The repository is organized around Jupyter notebooks and source files, complete with explanations and visualizations, making it ideal for both learners and researchers to explore the mechanisms and applications of Neural DEs.

## Implemented Models

- **Neural Ordinary Differential Equations (Neural ODEs):** Continuous-time trajectories defined by neural networks, based on Chen et al.'s paper.
- **Augmented Neural ODEs (ANODEs):** Extends Neural ODEs with an augmented state space for complex dynamics.
- **Neural Stochastic Differential Equations (Neural SDEs):** Models dynamics under uncertainty, inspired by Tzen and Raginsky.
- **Neural Controlled Differential Equations (Neural CDEs):** Adapts to irregular time-series by treating data as control paths, based on Kidger et al.
- **Physics-Informed Neural Networks (PINNs):** Solves PDEs by embedding physical laws into neural network training, as presented by Raissi et al.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/benjaminfranklin03/NeuroDiffEqLab.git
   cd NeuroDiffEqLab
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebooks:**

   Navigate to the `notebooks` directory and open any model notebook in Jupyter:

   ```bash
   jupyter notebook notebooks/NeuralODE.ipynb
   ```

## Repository Structure

```plaintext
NeuroDiffEqLab/
├── notebooks/            # Jupyter notebooks for each model, with explanations and visualizations
├── src/                  # Source code for core components, such as custom solvers and adjoint methods
├── images/               # Images and diagrams used in README and documentation
├── results/              # Saved plots, animations, and results from model runs
├── README.md             # Project overview and documentation
└── requirements.txt      # List of dependencies


## Usage

Each notebook provides a from-scratch implementation of a specific model, designed to be self-contained and highly documented. Simply navigate to the desired notebook and follow along with the explanations and visualizations.

For example, to explore Neural ODEs:

1. Go to `notebooks/NeuralODE.ipynb`.
2. Run each cell sequentially to understand the model's components and how it performs on sample data.
3. Experiment with hyperparameters, solver choices, and architectures to see how they impact model behavior.


## Examples and Visualizations

...

## References

This project was inspired by key research papers in Neural Differential Equations. For further reading, check out the foundational papers that shaped each model:

- **Neural ODEs:**
   Chen, R. T. Q., Rubanova, Y., Bettencourt, J., & Duvenaud, D. (2018). Neural Ordinary Differential Equations. *Advances in Neural Information Processing Systems*.

- **Augmented Neural ODEs:**
   Dupont, E., Doucet, A., & Teh, Y. W. (2019). Augmented Neural ODEs. *Advances in Neural Information Processing Systems*.

- **Neural SDEs:**
   Tzen, B., & Raginsky, M. (2019). Neural Stochastic Differential Equations: Deep Latent Gaussian Models in the Diffusion Limit. *arXiv preprint arXiv:1905.09883*.

- **Neural CDEs:**
   Kidger, P., Morrill, J., Foster, J., & Lyons, T. (2020). Neural Controlled Differential Equations for Irregular Time Series. *Advances in Neural Information Processing Systems*.

- **Physics-Informed Neural Networks (PINNs):**
   Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear partial differential equations. *Journal of Computational Physics, 378*, 686-707.

- **On Neural Differential Equations:**
   Kidger, P. (2022). On Neural Differential Equations. PhD Thesis, University of Oxford.

```
