# Building Neural Differential Equations from Scratch

Welcome to **NeuroDiffEqLab**! This project is a practical journey in building Neural Differential Equations (Neural DEs) from scratch, inspired by foundational research papers. Here, you’ll find implementations of a range of models, from basic Neural ODEs to advanced frameworks like Neural SDEs, Neural CDEs, and PINNs.

![Project Banner](images/project_banner.png)

---

## Table of Contents
- [Project Overview](#project-overview)
- [Implemented Models](#implemented-models)
  - [1. Neural Ordinary Differential Equations (Neural ODEs)](#1-neural-ordinary-differential-equations-neural-odes)
  - [2. Augmented Neural Ordinary Differential Equations (ANODEs)](#2-augmented-neural-ordinary-differential-equations-anodes)
  - [3. Neural Stochastic Differential Equations (Neural SDEs)](#3-neural-stochastic-differential-equations-neural-sdes)
  - [4. Neural Controlled Differential Equations (Neural CDEs)](#4-neural-controlled-differential-equations-neural-cdes)
  - [5. Physics-Informed Neural Networks (PINNs)](#5-physics-informed-neural-networks-pinns)
- [Installation](#installation)
- [Usage](#usage)
- [Examples and Visualizations](#examples-and-visualizations)
- [References](#references)

---


## Project Overview

**NeuroDiffEqLab** provides an in-depth, low-level exploration of Neural Differential Equations. Every model is implemented without high-level libraries, focusing on the mathematical foundation and methods from the original research. This approach offers full control over each component—from forward integration to backpropagation with adjoint methods.

The repository is organized around Jupyter notebooks and source files, complete with explanations and visualizations, making it ideal for both learners and researchers to explore the mechanisms and applications of Neural DEs.


![Neural ODE Diagram](images/neural_ode_example.png)

## Implemented Models

### 1. Neural Ordinary Differential Equations (Neural ODEs)

**Description**: Neural ODEs model the hidden state dynamics of a neural network as a continuous-time ODE. They provide a flexible framework for learning complex temporal dynamics with adaptive computation.

![Neural ODE Example](images/neural_ode_example.png)

**Reference**:  
Chen, R. T. Q., Rubanova, Y., Bettencourt, J., & Duvenaud, D. (2018). [Neural Ordinary Differential Equations](https://arxiv.org/abs/1806.07366). *arXiv preprint arXiv:1806.07366*.

### 2. Augmented Neural Ordinary Differential Equations (ANODEs)

**Description**: ANODEs enhance the expressiveness of Neural ODEs by augmenting the hidden state with additional dimensions, allowing the model to capture more complex dynamics.

![Augmented Neural ODE Example](images/augmented_neural_ode_example.png)

**Reference**:  
Dupont, E., Besse, F., George, F., Courville, A., & Ganguli, S. (2019). [Augmented Neural ODEs](https://arxiv.org/abs/1904.01681). *arXiv preprint arXiv:1904.01681*.

### 3. Neural Stochastic Differential Equations (Neural SDEs)

**Description**: Neural SDEs incorporate stochasticity into the ODE framework, enabling the modeling of data with inherent randomness and uncertainty.

![Neural SDE Example](images/neural_sde_example.png)

**Reference**:  
Tzen, B., & Raginsky, M. (2019). [Neural Stochastic Differential Equations for Time-Series Modeling](https://arxiv.org/abs/1906.11036). *arXiv preprint arXiv:1906.11036*.

### 4. Neural Controlled Differential Equations (Neural CDEs)

**Description**: Neural CDEs are designed to handle irregularly sampled time-series data by treating observations as control paths, offering robust performance on sparse and irregular datasets.

![Neural CDE Example](images/neural_cde_example.png)

**Reference**:  
Kidger, P., Pfaff, T., Tzen, B., & Raginsky, M. (2020). [Neural Controlled Differential Equations for Irregular Time-Series](https://arxiv.org/abs/2010.03212). *arXiv preprint arXiv:2010.03212*.

### 5. Physics-Informed Neural Networks (PINNs)

**Description**: PINNs integrate physical laws described by partial differential equations (PDEs) into the training of neural networks, enabling the solution of complex physical systems with embedded domain knowledge.

![PINN Example](images/pinn_example.png)

**Reference**:  
Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). [Physics-Informed Neural Networks: A Deep Learning Framework for Solving Forward and Inverse Problems Involving Nonlinear Partial Differential Equations](https://arxiv.org/abs/1711.10561). *Journal of Computational Physics, 378*, 686-707.

## Installation

### Prerequisites

- Python 3.7 or higher
- [pip](https://pip.pypa.io/en/stable/installation/)
- [Jupyter Notebook](https://jupyter.org/install)

### Steps

1. **Clone the repository**

    ```bash
    git clone https://github.com/benjaminfranklin03/NeuroDiffEqLab.git
    cd NeuroDiffEqLab
    ```

2. **Create a virtual environment**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install the dependencies**

    ```bash
    pip install -r requirements.txt
    ```

4. **Launch Jupyter Notebook**

    ```bash
    jupyter notebook
    ```

## Usage

Each model is implemented in its respective Jupyter Notebook within the `notebooks/` directory. Follow the step-by-step guides in each notebook to understand the implementation details and experiment with different datasets.

### Neural ODE

- **File**: `notebooks/NeuralODE.ipynb`
- **Description**: Implements a basic Neural ODE using the Runge-Kutta method.
- **Usage**: Explore the forward pass, training process, and evaluate on simple datasets.

### Augmented Neural ODE

- **File**: `notebooks/AugmentedNeuralODE.ipynb`
- **Description**: Enhances Neural ODEs by increasing the dimensionality of the hidden state.
- **Usage**: Test on complex trajectory datasets to observe improved expressiveness.

### Neural SDE

- **File**: `notebooks/NeuralSDE.ipynb`
- **Description**: Introduces stochasticity into the Neural ODE framework.
- **Usage**: Model data with inherent randomness, such as financial time-series.

### Neural CDE

- **File**: `notebooks/NeuralCDE.ipynb`
- **Description**: Handles irregularly sampled time-series data using Controlled Differential Equations.
- **Usage**: Apply to healthcare or traffic datasets with irregular sampling intervals.

### PINN

- **File**: `notebooks/PINN.ipynb`
- **Description**: Solves partial differential equations by embedding physical laws into the neural network.
- **Usage**: Implement solutions to the heat equation or other PDEs and compare with analytical solutions.

## Examples and Visualizations

Visualizations are integral to understanding the dynamics of each Neural DE model. Below are some example plots generated by the implementations:

![Neural ODE Trajectory](images/neural_ode_example.png)
*Figure 1: Example trajectory generated by Neural ODE.*

![Augmented Neural ODE Trajectory](images/augmented_neural_ode_example.png)
*Figure 2: Example trajectory generated by Augmented Neural ODE.*

![Neural SDE Multiple Trajectories](images/neural_sde_example.png)
*Figure 3: Multiple stochastic trajectories generated by Neural SDE.*

![Neural CDE Irregular Sampling](images/neural_cde_example.png)
*Figure 4: Handling of irregular sampling in Neural CDE.*

![PINN PDE Solution](images/pinn_example.png)
*Figure 5: Solution to the heat equation using PINN compared to the analytical solution.*

*(Replace placeholders with actual images once generated.)*

## References

- Chen, R. T. Q., Rubanova, Y., Bettencourt, J., & Duvenaud, D. (2018). Neural Ordinary Differential Equations. *arXiv preprint arXiv:1806.07366*. [Link](https://arxiv.org/abs/1806.07366)

- Dupont, E., Besse, F., George, F., Courville, A., & Ganguli, S. (2019). Augmented Neural ODEs. *arXiv preprint arXiv:1904.01681*. [Link](https://arxiv.org/abs/1904.01681)

- Tzen, B., & Raginsky, M. (2019). Neural Stochastic Differential Equations for Time-Series Modeling. *arXiv preprint arXiv:1906.11036*. [Link](https://arxiv.org/abs/1906.11036)

- Kidger, P., Pfaff, T., Tzen, B., & Raginsky, M. (2020). Neural Controlled Differential Equations for Irregular Time-Series. *arXiv preprint arXiv:2010.03212*. [Link](https://arxiv.org/abs/2010.03212)

- Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). Physics-Informed Neural Networks: A Deep Learning Framework for Solving Forward and Inverse Problems Involving Nonlinear Partial Differential Equations. *Journal of Computational Physics, 378*, 686-707. [Link](https://arxiv.org/abs/1711.10561)

---
