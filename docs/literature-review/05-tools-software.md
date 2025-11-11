# Software, Tools & Tutorials

This matrix catalogs frameworks, libraries, codebases, and educational resources for implementing Physics-Informed Machine Learning. These are practical resources for turning theory into working code.

## Overview

- **Frameworks**: High-level platforms for building PIML models
- **Libraries**: Specialized tools for specific tasks
- **Codebases**: Open-source implementations of papers
- **Tutorials**: Educational materials and courses
- **Solvers**: Traditional numerical PDE solvers (for comparison/validation)

---
## PIML Frameworks

| **Tool** | **Backend** | **Key Features** | **Installation** | **Best For** |
|----------|-------------|------------------|------------------|--------------|
| [NVIDIA Modulus](https://docs.nvidia.com/deeplearning/modulus/modulus-v2209/user_guide/basics/modulus_overview.html) | PyTorch | Pre-built PINNs, FNO, Multi-GPU | `pip install nvidia-modulus` | Production, GPU-accelerated |
| [DeepXDE](https://github.com/lululxvi/deepxde) | TF/PyTorch/JAX | Easy PINN API, Many examples | `pip install deepxde` | Research, beginners |
| [SciANN](https://github.com/ehsanhaghighat/sciann) | TensorFlow | Functional API, Keras-like | `pip install sciann` | Quick prototyping |
| [Neuromancer](https://github.com/pnnl/neuromancer) | PyTorch | Differentiable physics, Control | `pip install neuromancer` | Dynamical systems |
| [JAX-CFD](https://github.com/google/jax-cfd) | JAX | Fluid dynamics, Fast | `pip install jax-cfd` | High-performance CFD |

### Bayesian & UQ Tools

| **Tool** | **Backend** | **Key Features** | **Installation** | **Best For** |
|----------|-------------|------------------|------------------|--------------|
| [GPyTorch](https://gpytorch.ai/) | PyTorch | Scalable GPs, Fast | `pip install gpytorch` | Gaussian processes |
| [BOTorch](https://botorch.org/) | PyTorch | Bayesian optimization | `pip install botorch` | Hyperparameter tuning |
| [Pyro](https://pyro.ai/) | PyTorch | Probabilistic programming | `pip install pyro-ppl` | Bayesian deep learning |
| [NumPyro](https://num.pyro.ai/) | JAX | Probabilistic (JAX) | `pip install numpyro` | Fast Bayesian inference |
| [TensorFlow Probability](https://www.tensorflow.org/probability) | TensorFlow | Bayesian layers, GPs | `pip install tensorflow-probability` | TensorFlow ecosystem |

### Neural Operator Libraries

| **Tool** | **Backend** | **Operators** | **Installation** | **Best For** |
|----------|-------------|---------------|------------------|--------------|
| [neuraloperator](https://github.com/neuraloperator/neuraloperator) | PyTorch | FNO, DeepONet, etc. | `pip install neuraloperator` | Operator learning |
| [DINO (DeepONet)](https://github.com/lululxvi/deeponet) | TensorFlow | DeepONet variants | Clone repo | DeepONet research |
| [PhysicsNeMo](https://github.com/NVIDIA/modulus) | PyTorch | FNO, AFNO | `pip install nvidia-modulus` | Production operators |

### Code Repositories

| **Repository** | **Paper** | **Method** | **Link** | **Use Case** |
|----------------|-----------|------------|----------|--------------|
| FBPINNs | Moseley et al. 2023 | Domain decomposition | [GitHub](https://github.com/benmoseley/FBPINNs) | Large-scale PINNs |
| cPINNs | Jagtap et al. 2020 | Conservative PINNs | [GitHub](https://github.com/AmeyaJagtap/Conservative_PINNs) | Conservation laws |
| Self-adaptive PINNs | Wang et al. 2021 | Adaptive weights | [GitHub](https://github.com/levimcclenny/SA-PINNs) | Auto-balancing |
| Hidden Physics | Raissi 2020 | Discover PDEs | [GitHub](https://github.com/maziarraissi/HFM) | Equation discovery |

### Educational Resources

| **Resource** | **Type** | **Focus** | **Link** | **Level** |
|--------------|----------|-----------|----------|-----------|
| Physics-Based Deep Learning Book | Textbook | Comprehensive PIML | [physicsbaseddeeplearning.org](https://physicsbaseddeeplearning.org) | Beginner-Advanced |
| Ben Moseley DLSC-2023 | Course | Scientific computing | [ETHzurich](https://camlab.ethz.ch/teaching/deep-learning-in-scientific-computing-2023.html) | Intermediate |
| Ben Moseley AISE-2024 | Course | AI for science | [ETHzurich](https://camlab.ethz.ch/teaching/ai-in-the-sciences-and-engineering-2024.html) | Advanced |
| SciML workshops/lectures Ben Moseley  | Course/workshop | SciML | [GitHub](https://github.com/stars/benmoseley/lists/sciml-workshops-lectures) | Beginner-Advanced |
| DeepXDE Examples | Tutorials | 50+ PINN examples | [Docs](https://deepxde.readthedocs.io/) | Beginner |
| Modulus Examples | Tutorials | Industry examples | [GitHub](https://github.com/NVIDIA/modulus/tree/main/examples) | Intermediate |
| Steve Brunton PIML Series | Course Series | Comprehensive PIML  | [Youtube](https://www.youtube.com/watch?v=JoFW2uSd3Uo&t=982s) | Beginner |

### Some other repos and links that doesn't fit anywhere
 |**Resource** | **Link** | **Focus** |
 |--------------|----------|-----------|
 | pinns | [GitHub](https://github.com/TheodoreWolf/pinns) | example of pinns using PyTorch |
 | Finnish Inverse Problems Society | [link](https://fips.fi/category/open-datasets/) | open tomography examoles |



### PDE Solvers (Traditional)

| **Solver** | **Method** | **Domain** | **Link** | **Use in PIML** |
|------------|------------|------------|----------|-----------------|
| FUNWAVE | Boussinesq | Coastal waves | [Docs](https://fengyanshi.github.io/) | Bathymetry, validation |
| SWASH | Nonhydrostatic | Nearshore waves | [Website](https://swash.sourceforge.io/) | Wave modeling |
| FEniCS | Finite element | General PDEs | [FEniCS Project](https://fenicsproject.org/) | Training data generation |
| OpenFOAM | Finite volume | CFD | [OpenFOAM](https://www.openfoam.com/) | Fluid dynamics data |

### Visualization & Analysis

| **Tool** | **Purpose** | **Installation** | **Best For** |
|----------|-------------|------------------|--------------|
| [Python Graph Gallery](https://python-graph-gallery.com) | Collection of hundreds of charts made with python | Visualisation | Educational |
| [Weights & Biases](https://wandb.ai/) | Experiment tracking | `pip install wandb` | Training monitoring |
| [TensorBoard](https://www.tensorflow.org/tensorboard) | Visualization | Included with TF/PyTorch | Loss curves, metrics |
| [ParaView](https://www.paraview.org/) | Scientific viz | Download binary | 3D field visualization |
| [Plotly](https://plotly.com/) | Interactive plots | `pip install plotly` | Web dashboards |

---

[← Back to Literature Review](README.md) | [← Previous: Bayesian Methods](04-bayesian-methods.md)
