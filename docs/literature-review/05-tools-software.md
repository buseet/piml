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
| [Weights & Biases](https://wandb.ai/) | Experiment tracking | `pip install wandb` | Training monitoring |
| [TensorBoard](https://www.tensorflow.org/tensorboard) | Visualization | Included with TF/PyTorch | Loss curves, metrics |
| [ParaView](https://www.paraview.org/) | Scientific viz | Download binary | 3D field visualization |
| [Plotly](https://plotly.com/) | Interactive plots | `pip install plotly` | Web dashboards |

---


### Backend Comparison (PyTorch vs TensorFlow vs JAX)

| **Aspect** | **PyTorch** | **TensorFlow** | **JAX** |
|------------|-------------|----------------|---------|
| **Ease of Learning** | High (Pythonic) | Medium (more complex API) | Medium (functional style) |
| **Debugging** | Easy (eager execution) | Harder (graph-based) | Medium (JIT compilation) |
| **Performance** | Good | Good | Excellent (XLA) |
| **Autodiff** | Easy | Easy | Most flexible |
| **GPU/TPU** | Great GPU | Good both | Excellent both |
| **PIML Ecosystem** | Largest | Medium | Growing fast |
| **Best For** | Research, flexibility | Production (legacy) | High-performance research |


## Detailed Tool Descriptions

### NVIDIA Modulus

**What It Is**: Industrial-grade platform for physics-ML applications, developed by NVIDIA.

**Key Features**:
- Pre-built PINN architectures
- Neural operators (FNO, DeepONet, etc.)
- Symbolic API for defining PDEs
- Multi-GPU scaling
- Integration with NVIDIA optimization tools

**Example Use Case**:
```python
import modulus
from modulus.sym.eq.pde import NavierStokes

# Define PDE symbolically
ns = NavierStokes(nu=0.01, rho=1.0, dim=2)

# Create PINN model
model = modulus.sym.models.FullyConnected(...)

# Train with physics loss
modulus.train(model, pde=ns, data=data)
```

**Pros**: Production-ready, well-documented, fast
**Cons**: NVIDIA ecosystem, may be overkill for research

**Installation**: `pip install nvidia-modulus`

**Documentation**: https://docs.nvidia.com/deeplearning/modulus/

---

### Neuromancer

**What It Is**: Open-source framework for neural state space models with differentiable physics.

**Key Features**:
- Differentiable physics simulators
- Constrained optimization layers
- Control and dynamical systems focus
- PyTorch-based

**Philosophy**: Treat physics as differentiable computational graphs within neural networks.

**Example Applications**:
- Constrained control
- System identification
- Hybrid physics-data models

**Pros**: Flexible, research-oriented, active development
**Cons**: Steeper learning curve than Modulus

**Installation**: `git clone https://github.com/pnnl/neuromancer && pip install -e neuromancer`

---

### DeepXDE

**What It Is**: User-friendly library for PINNs, with extensive examples and excellent documentation.

**Key Features**:
- Supports PyTorch, TensorFlow, and JAX backends
- 50+ example problems with working code
- Easy API for defining PDEs
- Built-in optimizers and learning rate schedules
- Supports various neural network architectures

**Example Use Case**:
```python
import deepxde as dde

# Define PDE
def pde(x, y):
    dy_t = dde.grad.jacobian(y, x, i=0, j=1)
    dy_xx = dde.grad.hessian(y, x, i=0, j=0)
    return dy_t - 0.01 * dy_xx

# Define geometry and boundary conditions
geom = dde.geometry.Interval(-1, 1)
timedomain = dde.geometry.TimeDomain(0, 1)
geomtime = dde.geometry.GeometryXTime(geom, timedomain)

bc = dde.icbc.DirichletBC(geomtime, lambda x: 0, lambda _, on_boundary: on_boundary)
ic = dde.icbc.IC(geomtime, lambda x: np.sin(np.pi * x[:, 0:1]), lambda _, on_initial: on_initial)

# Combine into PINN problem
data = dde.data.TimePDE(geomtime, pde, [bc, ic], num_domain=2000, num_boundary=100, num_initial=100)
net = dde.nn.FNN([2] + [50] * 3 + [1], "tanh", "Glorot normal")
model = dde.Model(data, net)

# Train
model.compile("adam", lr=0.001)
model.train(iterations=10000)
```

**Pros**: Easiest to learn, best documentation, multi-backend
**Cons**: Slightly less performance than custom implementations

**Installation**: `pip install deepxde`

**Documentation**: https://deepxde.readthedocs.io/

**GitHub**: https://github.com/lululxvi/deepxde (3000+ stars)

---

### FBPINNs - Finite Basis Physics-Informed Neural Networks

**What It Is**: Implementation of domain decomposition methods for PINNs (Moseley et al., 2023).

**Why It Matters**: Solves scalability issues of standard PINNs by decomposing large domains into smaller subdomains.

**Use Case for Bathymetry**: Large satellite images can be divided into tiles, each solved independently.

**Code**: https://github.com/benmoseley/FBPINNs

**Key Idea**:
```
Large domain → Divide into subdomains → Train local PINNs → Combine solutions
```

**Implementation Tips**:
- Choose subdomain size based on wave wavelength
- Use overlapping regions for continuity
- Can parallelize across GPUs

---

### x-invert

**What It Is**: Framework for solving inverse problems with neural networks.

**Features**:
- Plug-and-play inversion
- Multiple architectures
- Regularization techniques

**GitHub**: https://github.com/swing-research/x-invert

**Relevance**: Direct application to bathymetry inversion from images

---

### BOTORCH - Bayesian Optimization

**What It Is**: Library for Bayesian optimization built on PyTorch and GPyTorch.

**Use Case in PIML**: Hyperparameter tuning for PINN/neural operator models.

**Why Bayesian Optimization**:
- Expensive function evaluations (training a PINN takes time)
- Need global optimization
- Want uncertainty-aware search

**Website**: https://botorch.org

**Example**:
```python
from botorch import optimize_acqf
from botorch.models import SingleTaskGP

# Define objective (e.g., validation loss as function of hyperparameters)
# Use Bayesian optimization to find best hyperparameters
```
---

[← Back to Literature Review](README.md) | [← Previous: Bayesian Methods](04-bayesian-methods.md)
