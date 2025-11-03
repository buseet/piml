# Core PIML Papers

This matrix covers foundational papers in Physics-Informed Machine Learning, including the original PINN formulation, extensions, neural operators, and scalability improvements.

## Overview

These papers establish the theoretical and methodological foundations of PIML. They address core challenges such as:

- Solving forward and inverse problems with sparse data
- Incorporating differential equations into learning
- Scaling to large domains and complex PDEs
- Quantifying uncertainty in physics-informed predictions
- Learning generalisable solution operators

---

## Papers by Year

### 2019 - Foundation Year

| **Paper** | **Problem Type** | **PDE/Operator** | **Data Type** | **Architecture** | **Loss Design** | **Key Innovation** | **Results** | **Limitations** | **Relevance** |
|---|---|---|---|---|---|---|---|---|---|
| [Raissi et al. (Original PINNs)](https://doi.org/10.1016/j.jcp.2018.10.045) | Forward/Inverse | Burgers, NS, Schrödinger | Sparse, clean | FC NN | L_f + λL_u | First PINN formulation | <1% error | Needs direct observations | 5 - Foundation |
| [Kharazmi et al. (hp-VPINNs)](https://doi.org/10.1016/j.cma.2019.112741) | Forward | Various | Sparse | Variational | Variational form | Variational formulation | Better convergence | Complex implementation | 3 - Alternative approach |
| [Lu et al. (DeepONet)](https://doi.org/10.1038/s42256-021-00302-5) | Forward | General operators | Dense | Branch-trunk | Operator loss | Learn operators not functions | Universal approximation | Needs operator data | 5 - Foundation |

### 2020 - Extensions & Variants

| **Paper** | **Problem Type** | **PDE/Operator** | **Data Type** | **Architecture** | **Loss Design** | **Key Innovation** | **Results** | **Limitations** | **Relevance** |
|---|---|---|---|---|---|---|---|---|---|
| [Jagtap et al. (cPINNs)](https://doi.org/10.1016/j.cma.2020.113028) | Forward | Conservation laws | Sparse | Conservative FC | Conservative form | Ensures conservation | Better for shocks | Domain specific | 4 - Conservation |
| [Jagtap & Karniadakis (XPINNs)](https://doi.org/10.4208/cicp.OA-2020-0164) | Forward | Various | Sparse | Domain decomposed | Interface conditions | Parallel decomposition | Scalable | Interface complexity | 4 - Scalability |
| [Li et al. (FNO)](https://doi.org/10.48550/arXiv.2010.08895) | Forward | Periodic PDEs | Dense | Fourier layers | Spectral loss | Fourier space learning | Very fast | Periodic domains | 4 - Speed |

### 2021 - Specialized Methods

| **Paper** | **Problem Type** | **PDE/Operator** | **Data Type** | **Architecture** | **Loss Design** | **Key Innovation** | **Results** | **Limitations** | **Relevance** |
|---|---|---|---|---|---|---|---|---|---|
| [Yang et al. (B-PINNs)](https://doi.org/10.1016/j.jcp.2020.109913) | Forward/Inverse | Various PDEs | Noisy | Bayesian NN | L_f + λL_u + KL | Uncertainty quantification | 40% UQ improvement | Computational cost | 4 - UQ needed |
| [Yang et al. (Seismic Neural Operators)](https://doi.org/10.1785/0320210026) | Inverse | Wave | Seismic data | Neural operator | Physics + data | Wave modeling | Good inversion | Domain specific | 3 - Wave physics |

### 2022 - Advanced Architectures

| **Paper** | **Problem Type** | **PDE/Operator** | **Data Type** | **Architecture** | **Loss Design** | **Key Innovation** | **Results** | **Limitations** | **Relevance** |
|---|---|---|---|---|---|---|---|---|---|
| [Wang et al. (Respecting Causality)](https://doi.org/10.48550/arXiv.2203.07404) | Forward | Time-dependent | Temporal | Causal training | Causal weights | Respects causality | Better for dynamics | Time-dependent only | 4 - Temporal |
| [Rahman et al. (U-NO)](https://doi.org/10.48550/arXiv.2204.11127) | Forward | Complex PDEs | Dense | U-Net operator | Multi-scale | U-Net + operators | Fine details | Memory intensive | 4 - U-Net for images |
| [Yu et al. (gPINNs)](https://doi.org/10.1016/j.cma.2022.114823) | Forward | Various | Sparse | Gradient-enhanced | L_f + L_∇ | Use gradient data | Better accuracy | Needs gradients | 3 - When gradients available |

### 2023 - Robustness & Scalability

| **Paper** | **Problem Type** | **PDE/Operator** | **Data Type** | **Architecture** | **Loss Design** | **Key Innovation** | **Results** | **Limitations** | **Relevance** |
|---|---|---|---|---|---|---|---|---|---|
| [Moseley et al. (FBPINNs)](https://doi.org/10.1007/s10444-023-10065-9) | Forward | Various | Sparse | Domain decomposed | Local losses | Scalable decomposition | Large domains | Complex setup | 4 - For large images |
| [Bajaj et al. (Recipes When Physics Fails)](https://doi.org/10.1088/2632-2153/acb416) | Both | Various | Imperfect | Adaptive FC | Adaptive weights | Robust to errors | 50% error recovery | Needs tuning | 4 - Image noise |

### 2024 - Latest Developments

| **Paper** | **Problem Type** | **PDE/Operator** | **Data Type** | **Architecture** | **Loss Design** | **Key Innovation** | **Results** | **Limitations** | **Relevance** |
|---|---|---|---|---|---|---|---|---|---|
| [Li et al. (Physics-Informed Neural Operator)](https://doi.org/10.1145/3648506) | Forward | General PDEs | Dense | DeepONet | Operator loss | Learn solution operators | 100x speedup | Data hungry | 3 - Architecture ideas |
| [Zou et al. (Deep Helmholtz)](https://doi.org/10.1093/gji/ggae342) | Forward | 3D Elastic wave | High-freq | Deep Helmholtz | Frequency domain | 3D wave propagation | High accuracy | Computationally heavy | 3 - Advanced waves |
| [Brunton et al. (ML for PDEs)](https://doi.org/10.48550/arXiv.2303.17078) | Review | Various | Various | Multiple | N/A | Survey of methods | N/A | N/A | 3 - Overview |

---

## Key Papers Expanded

### Raissi et al. - Physics-Informed Neural Networks (2019)

- **Core Contribution**: Introduced the PINN framework for solving PDEs by minimising a composite loss function that includes both data fidelity and PDE residuals.

- **Why It Matters**: This is the foundational paper that launched the field. Essential reading for anyone working with PINNs.

---

### Li et al. - Fourier Neural Operator (2020)

- **Core Contribution**: Neural operator architecture that learns in Fourier space for fast, resolution-invariant PDE solving.

- **Why It Matters**: Achieves unprecedented speed (milliseconds) for solving complex PDEs on regular grids.

- **Method**: Performs convolutions in Fourier space where they become multiplications (faster).

- **Limitation**: Works best for periodic problems or problems on regular grids.

- **Use Case**: Turbulence, climate modelling, any spectral problem.

---

### Jagtap & Karniadakis - XPINNs (2020)

- **Core Contribution**: Extended PINNs with domain decomposition, allowing different neural networks for different subdomains.

- **Why It Matters**: Handles complex geometries and enables parallel training across subdomains.

- **Key Innovation**: Carefully designed interface conditions ensure continuity across subdomain boundaries.

- **Comparison with FBPINNs**: XPINNs use separate NNs per subdomain; FBPINNs use overlapping basis functions. Both achieve scalability.

---
### Yang et al. - Bayesian PINNs (2021)

- **Core Contribution**: Extended PINNs to Bayesian framework for uncertainty quantification using variational inference.

- **Why It Matters**: Critical for applications requiring reliability estimates and confidence intervals.

- **Key Insight**: The uncertainty can be decomposed into epistemic (model) and aleatoric (data) components.

---

### Moseley et al. - Finite Basis PINNs (2023)

- **Core Contribution**: Domain decomposition approach that divides large domains into smaller subdomains, solving local PINNs in parallel.

- **Why It Matters**: Addresses scalability challenges of PINNs for large spatial domains.

- **Implementation**: Code available at https://github.com/benmoseley/FBPINNs

---

### Bajaj et al. - When Physics Fails (2023)

- **Core Contribution**: Adaptive weighting strategies for handling imperfect physics models or noisy/incomplete physics knowledge.

- **Why It Matters**: Real-world applications often involve model uncertainty and observational noise.

---

## Method Comparison Table

| **Method** | **When to Use** | **Pros** | **Cons** | **Training Time** | **Inference Speed** | **Best For** |
|------------|-----------------|----------|----------|-------------------|---------------------|--------------|
| **Standard PINN** | Single scenario, good physics knowledge | Simple, flexible | Can be slow, training tricks needed | Medium | Fast | General purpose |
| **B-PINN** | Need uncertainty, critical decisions | UQ built-in, robust | Slow training, complex | Slow | Medium | High-stakes applications |
| **DeepONet** | Repeated solves, varying conditions | Very fast inference, generalize | Needs lots of data | Medium | Very fast | Query-based systems |
| **FNO** | Periodic problems, regular grids | Extremely fast, scalable | Periodic/grid only | Medium | Very fast | Spectral problems |
| **FBPINN** | Large domains, satellite images | Scalable, parallel | Setup complexity | Medium* | Fast | Large spatial domains |
| **XPINNs** | Complex geometries, decomposition | Flexible domains | Interface handling | Medium* | Fast | Multi-domain problems |
| **cPINNs** | Conservation laws critical | Guarantees conservation | Limited scope | Medium | Fast | Fluid dynamics, shocks |
| **gPINNs** | Have gradient measurements | Better accuracy | Needs gradient data | Medium | Fast | When ∇u available |
| **Causal PINN** | Time-dependent dynamics | Respects causality | Time problems only | Medium | Fast | Temporal evolution |

\* Parallelizable across GPUs

---

## Decision Flowchart: Which Method to Choose?

```
START: What's your problem?

├─ Need to solve ONCE with sparse data?
│  └─ Standard PINN or Self-adaptive PINN
│
├─ Need to solve MANY TIMES (different conditions)?
│  ├─ Periodic/regular grid? → FNO
│  ├─ General operator? → DeepONet
│  └─ Various geometries? → Neural Operator + Transfer Learning
│
├─ Large spatial domain (e.g., satellite image)?
│  └─ FBPINNs or XPINNs (domain decomposition)
│
├─ Need UNCERTAINTY estimates?
│  └─ Bayesian PINN
│
├─ Conservation laws CRITICAL?
│  └─ cPINNs
│
├─ Have GRADIENT data available?
│  └─ gPINNs
│
├─ Physics model IMPERFECT or noisy?
│  └─ Self-adaptive PINN or Bajaj et al. methods
│
├─ TIME-DEPENDENT problem?
│  └─ Causal PINN
│
└─ Not sure / Just learning?
   └─ Start with Standard PINN
```

---


## Research Directions

1. **Scalability**: FBPINNs and neural operators for large-scale problems
2. **Uncertainty**: Bayesian methods for reliable predictions
3. **Robustness**: Adaptive methods for imperfect physics
4. **Architecture**: U-Net operators for structured data (images)
5. **Speed**: Neural operators for repeated forward solves
6. **Hybrid Methods**: Combine different approaches (e.g., PINN + neural operator)
7. **Multi-Fidelity**: Leverage low-cost simulations with sparse high-fidelity data

---


[← Back to Literature Review](README.md) | [Next: Image/Vision Integration →](02-image-vision.md)
