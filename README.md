# Building Neural Ordinary Differential Equations from Scratch

Welcome to **NeuroDiffEqLab**! 🚀 This project is a deep dive into understanding and building Neural Ordinary Differential Equations (Neural ODEs) from scratch, both manually and using JAX. The project serves as an exploration into implementing these models, training them on simple tasks, and analyzing their behaviors.



---

## Table of Contents
- [Project Overview](#project-overview)
- [Implemented Models](#implemented-models)
  - [1. Basic Neural ODE from Scratch](#1-basic-neural-ode-from-scratch)
  - [2. Neural ODE with JAX](#2-neural-ode-with-jax)
- [Installation](#installation)
- [Usage](#usage)
- [Results and Insights](#results-and-insights)
- [References](#references)

---

## Project Overview

**NeuroDiffEqLab** focuses on implementing and understanding Neural ODEs through two primary approaches:
- A basic implementation from scratch to gain insight into the underlying mechanics.
- A JAX-based implementation to leverage its efficiency and automatic differentiation capabilities.

The repository showcases the process of constructing these models and training them on a simple regression task and a dynamic system (e.g., Van Der Pol oscillator).

---

## Implemented Models

### 1. Basic Neural ODE from Scratch

**Description**: This implementation involves building a Neural ODE model without relying on high-level libraries, allowing for a thorough understanding of the mathematical underpinnings. The model is trained on a very simple regression task, where it basically just has to predict the trajectory from a starting point A to a point B.

![Basic Neural ODE Example](images/neural_ode_example.png)

**Key Features**:
- Handcrafted ODE solver.
- Manual backpropagation through the adjoint method.
- Analysis of training results and model behavior.

### 2. Neural ODE with JAX

**Description**: This version takes advantage of JAX’s powerful automatic differentiation and efficient computation on GPUs. The model is trained on a slightly more complex system of ODEs, like the Van Der Pol oscillator, to explore how well it can capture non-linear dynamics.

![JAX Neural ODE Example](images/jax_neural_ode_example.png)

**Key Features**:
- Utilizes JAX’s autograd for efficient gradient computation.
- Demonstrates improved performance and flexibility over manual implementation.
- Insights into handling dynamic systems with continuous-time models.

---

## Installation

Follow these steps to set up the project:


### Steps

1. **Clone the repository**

    ```bash
    git clone https://github.com/yourusername/NeuroDiffEqLab.git
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

4. **Run the notebooks**

    Open the project notebooks to explore the implementations step by step.

---

## Usage

Each implementation can be found in the `notebooks/` directory:

- **`NeuralODE_scratch.ipynb`**: Details the basic implementation, training on simple regression data.
- **`NeuralODE_JAX.ipynb`**: Explores the JAX implementation and training on the Van Der Pol oscillator system.

Simply open the notebooks in Jupyter and follow along to see the code, explanations, and results. Additionally, some visualizations can be found in the training plots.

---

## Results

### Basic Neural ODE
- Building a neural ODE from scratch was a fun experience and it really showed me how they worked from a more fundamental level, but the implementation also came with many headaches.
- Calculating gradients manually was really unstable and I had all kinds of issues with underflow, exploding gradients, etc. but I somewhat fixed it with gradient clipping.

### Neural ODE with JAX
- I was able use JAX's autodiff tool instead of doing everything manually.
- The training was much much smoother and building the neural ODE was much faster and much more stable than any adjoint method I was able to implement.

---

## References

This project draws inspiration from:

- **Chen, R. T. Q., Rubanova, Y., Bettencourt, J., & Duvenaud, D. (2018)**. [Neural Ordinary Differential Equations](https://arxiv.org/abs/1806.07366). *arXiv preprint arXiv:1806.07366*.

---
