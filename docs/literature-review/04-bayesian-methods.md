# Gaussian Processes & Bayesian Methods

This matrix covers probabilistic approaches to PIML, with emphasis on Gaussian Processes (GPs), Bayesian inference, and uncertainty quantification. These methods are essential for understanding and quantifying uncertainty in physics-informed predictions.

## Overview
- **Uncertainty Quantification**: Confidence intervals and error bars
- **Data Efficiency**: Principled learning from small datasets
- **Flexible Priors**: Incorporation of physics knowledge through constraints
- **Robust Inference**: Handling noisy and incomplete observations

Gaussian Processes are particularly powerful for spatially-correlated inverse problems.

---

## Papers by Method Type

### Gaussian Process Fundamentals

| **Paper** | **Year** | **Topic** | **Key Contribution** | **Relevance** |
|---|---|---|---|---|
| [Rasmussen & Williams (GP for ML)](http://www.gaussianprocess.org/gpml/) | 2006 | GP textbook | Comprehensive reference | 5 - Essential foundation |
| [MacKay (Intro to GP)](https://www.inference.org.uk/mackay/gpB.ps.gz) | 1998 | GP basics | Accessible tutorial | 4 - UQ methods |
| [Roberts et al. (GP Approximation)](https://doi.org/10.1098/rsta.2011.0550) | 2013 | Approximation theory | Error bounds for GPs | 3 - Theory |
| [Wilson & Nickisch (Kernel Interpolation)](https://arxiv.org/abs/1503.01057) | 2015 | Scalable GP | Fast structured kernels | 4 - Scalability |

### Physics-Constrained GPs

| **Paper** | **Year** | **Topic** | **Key Contribution** | **Relevance** |
|---|---|---|---|---|
| [Lange-Hegermann et al. (Linear Constraints)](https://proceedings.neurips.cc/paper_files/paper/2018/file/68b1fbe7f16e4ae3024973f12f3cb313-Paper.pdf) | 2018 | Constrained GP | Linear physics constraints | 4 - Physics constraints |
| [Lange et al. (Boundary)](http://proceedings.mlr.press/v130/lange-hegermann21a.html) | 2021 | Boundary GP | Boundary conditions | 4 - Domain boundaries |
| [Jidling et al. (PDE-GP)](https://doi.org/10.1016/j.nimb.2018.08.051) | 2018 | PDE priors | Encode PDEs in GP | 5 - Physics-informed GP |
| [Raissi et al. (Physics-GP)](https://doi.org/10.1016/j.jcp.2017.11.039) | 2018 | GP with physics | Combine GP + physics | 5 - GP-PINN connection |
| [Alvarez et al. (LMC)](https://arxiv.org/abs/1106.6251) | 2012 | Multi-output GP | Linear model of coregionalization | 4 - Multiple fields |

### Bayesian Neural Networks & Bayesian PINNs

| **Paper** | **Year** | **Topic** | **Key Contribution** | **Relevance** |
|---|---|---|---|---|
| [Yang et al. (B-PINNs)](https://doi.org/10.1016/j.jcp.2020.109913) | 2021 | Bayesian PINN | Variational inference for PINNs | 5 - UQ for PINNs |
| [Psaros et al. (Uncertainty SiML)](https://doi.org/10.1016/j.jcp.2022.111902) | 2023 | UQ survey | Comprehensive UQ review | 5 - Essential review |
| [Gal & Ghahramani (Dropout UQ)](https://arxiv.org/abs/1506.02142) | 2016 | Dropout as Bayesian | MC dropout for UQ | 4 - Practical UQ |
| [Blundell et al. (Weight Uncertainty)](https://arxiv.org/abs/1505.05424) | 2015 | Bayes by backprop | Variational BNN | 4 - Bayesian NN |
| [Lakshminarayanan et al. (Ensembles)](https://arxiv.org/abs/1612.01474) | 2017 | Deep ensembles | Simple UQ method | 4 - Practical approach |

### Inverse Problems & Geophysical Applications

| **Paper** | **Year** | **Topic** | **Key Contribution** | **Relevance** |
|---|---|---|---|---|
| [Valentine & Sambridge I](https://academic.oup.com/gji/article-pdf/215/2/1003/39586071/ggy303.pdf) | 2020 | GP inverse (continuous) | Probabilistic framework | 4 - Inverse problems |
| [Valentine & Sambridge II](https://academic.oup.com/gji/article-pdf/220/3/1648/31578302/ggz521.pdf) | 2020 | GP inverse (discrete) | Discrete inversion | 4 - Practical |
| [Laloy et al. (Inversion BNN)](https://agupubs.onlinelibrary.wiley.com/doi/pdfdirect/10.1002/2017WR022148) | 2018 | Hydrogeology inverse | BNN for subsurface | 4 - Geophysical inverse |
| [Zhu & Zabaras (Bayesian DL)](https://www.sciencedirect.com/science/article/pii/S0021999118302341) | 2018 | Bayesian inverse | Physics-constrained BNN | 5 - Bayesian physics |
| [Stuart (Inverse UQ)](https://doi.org/10.1017/S0962492910000061) | 2010 | Inverse theory | Bayesian inverse framework | 4 - Theory foundation |

### Scalable & Approximate Methods

| **Paper** | **Year** | **Topic** | **Key Contribution** | **Relevance** |
|---|---|---|---|---|
| [Titsias (Variational GP)](http://proceedings.mlr.press/v5/titsias09a/titsias09a.pdf) | 2009 | Sparse GP | Inducing points | 4 - Scalability |
| [Hensman et al. (Variational GP)](https://arxiv.org/abs/1309.6835) | 2013 | Scalable GP | Stochastic variational | 4 - Large data |
| [Gardner et al. (GPyTorch)](https://arxiv.org/abs/1809.11165) | 2018 | GP software | Scalable implementation | 4 - Practical tool |
| [McHutchon & Rasmussen](https://proceedings.neurips.cc/paper_files/paper/2011/file/a8e864d04c95572d1aece099af852d0a-Paper.pdf) | 2011 | Input noise | GP with input uncertainty | 4 - Image noise |

### Multi-Fidelity & Active Learning

| **Paper** | **Year** | **Topic** | **Key Contribution** | **Relevance** |
|---|---|---|---|---|
| [Kennedy & O'Hagan (Multi-fidelity)](https://academic.oup.com/biomet/article-pdf/87/1/1/590577/870001.pdf) | 2000 | Multi-fidelity GP | Combine simulation levels | 5 - Multi-fidelity framework |
| [Perdikaris et al.](https://royalsocietypublishing.org/doi/pdf/10.1098/rspa.2016.0751) | 2017 | Multi-fidelity NN | Transfer learning | 4 - PIML multi-fidelity |
| [Gramacy & Lee (Adaptive Sampling)](https://www.tandfonline.com/doi/pdf/10.1198/TECH.2009.0015) | 2009 | Sequential GP | Adaptive design | 4 - Active bathymetry sampling |

---

## Key Papers Expanded

### MacKay - Introduction to Gaussian Processes (1998)

**Core Contribution**: Accessible introduction to Gaussian processes for machine learning, covering regression, classification, and model comparison.

**Why It Matters**: Classic tutorial that remains one of the clearest introductions to GP methods.

**Key Concepts**:
- GPs as distributions over functions
- Kernel functions and their interpretation
- Bayesian model comparison and hyperparameter learning

---

### Valentine & Sambridge - Gaussian Process Inverse Problems (2020)

**Core Contribution**: Two-part series on using GPs for geophysical inverse problems. Part I covers continuous parameter spaces, Part II discrete.

**Why It Matters**: Comprehensive framework for probabilistic inversion in geophysics. Directly applicable to bathymetry inversion.

**Method**:
- GP prior on unknown field (e.g., bathymetry)
- Forward operator maps field to observations (e.g., wave patterns)
- Posterior GP gives probabilistic estimate with uncertainties

**Key Advantages**:
- Full posterior distribution (not just point estimate)
- Automatic regularization through GP prior
- Uncertainty quantification built-in

**Applications**: Seismic tomography, gravity inversion, electromagnetic inversion - all analogous to bathymetry inversion

---

### McHutchon & Rasmussen - GPs with Uncertain Inputs (2011)

**Core Contribution**: Extends GP regression to handle uncertainty in input variables, not just output noise.

**Why It Matters**: Satellite imagery has positional uncertainty (geolocation errors) and measurement uncertainty. This paper shows how to account for input noise in GP models.

**Key Insight**: Input uncertainty is not the same as output noise. Requires moment matching or sampling approaches.

**Application to Bathymetry**:
- Input: Wave parameters extracted from imagery (with uncertainty)
- Output: Bathymetry (also uncertain)
- Method accounts for both uncertainty sources

---

### Lange et al. - Linearly Constrained GPs (2018)

**Core Contribution**: Framework for imposing linear constraints on Gaussian processes to encode physical laws.

**Why It Matters**: Shows how to incorporate physics (PDEs, conservation laws, boundary conditions) as constraints on GP priors.

**Examples of Linear Constraints**:
- Divergence-free flow fields: ∇·u = 0
- Zero-mean constraints: ∫f(x)dx = 0
- Boundary conditions: f(x₀) = c

**Method**: Construct GP in null space of constraint matrix, ensuring all samples satisfy physics.

**Relevance**: Could constrain bathymetry GP to satisfy known properties (e.g., minimum depth, smoothness in certain regions)

---

### Lange et al. - Boundary-Aware GPs (2021)

**Core Contribution**: GP methods that respect domain boundaries (e.g., coastlines for bathymetry).

**Why It Matters**: Standard GPs don't naturally handle boundaries. This work shows how to impose hard boundary conditions.

**Applications**:
- Ocean bathymetry stops at coastline
- Boundary conditions at domain edges
- Dirichlet/Neumann conditions

**Method**: Modify kernel to enforce boundary conditions, or use boundary integral formulations.

---

### Rasmussen & Williams - GP for Machine Learning (2006)

**Core Contribution**: Definitive textbook on Gaussian processes for machine learning. Free online at gaussianprocess.org/gpml/

**Why It Matters**: The bible of GP methods. Comprehensive coverage from basics to advanced topics.

**Key Chapters for PIML**:
- Ch 2: Regression (fundamentals)
- Ch 4: Covariance functions (kernels for different priors)
- Ch 5: Model selection (choosing hyperparameters)
- Ch 9: Approximations (for scalability)

**Relevance**: Essential reference for GP-based bathymetry inversion.

---

### Jidling et al. - Probabilistic Space-Time Model (PDE-GP) (2018)

**Core Contribution**: Framework for encoding partial differential equations as priors in Gaussian processes.

**Why It Matters**: Directly incorporates PDEs (like wave equations) into GP priors. This is physics-informed GP!

**Method**:
1. Start with PDE: Lu = 0 (e.g., wave equation)
2. Define GP prior on solution u
3. Construct kernel such that samples satisfy PDE
4. Result: GP that automatically satisfies physics

**Application**: Could encode Boussinesq equation in GP prior for bathymetry that automatically satisfies wave physics.

**Key Advantage**: Physics is hard constraint, not soft penalty like PINNs.

---

### Raissi et al. - Physics-Informed GP (2018)

**Core Contribution**: Combines Gaussian processes with physics constraints for forward and inverse PDE problems.

**Why It Matters**: Bridges GP methods and physics-informed learning - precursor to PINNs from same author.

**Method**:
- GP prior on PDE solution
- Physics encoded in mean function or kernel
- Observations used to update posterior

**Connection to PINNs**: Same author (Raissi) developed both physics-informed GPs (2018) and PINNs (2019). GPs provide principled UQ that PINNs initially lacked.

---

### Psaros et al. - Uncertainty Quantification in PINNs (2023)

**Core Contribution**: Comprehensive review of uncertainty quantification methods for physics-informed neural networks.

**Why It Matters**: Essential guide for adding UQ to PINNs. Reviews all major approaches: Bayesian NNs, ensembles, dropout, etc.

**Methods Reviewed**:
1. **Bayesian PINNs** (Yang et al.) - Variational inference
2. **MC Dropout** (Gal & Ghahramani) - Dropout as approximate Bayesian
3. **Deep Ensembles** (Lakshminarayanan) - Train multiple models
4. **Bootstrap** - Resample data, train multiple models
5. **Conformal Prediction** - Distribution-free UQ

**Recommendations**: Ensembles for simplicity, Bayesian for principled UQ, dropout for practical speed.

---

### Kennedy & O'Hagan - Multi-Fidelity GP (2000)

**Core Contribution**: Framework for combining cheap low-fidelity simulations with expensive high-fidelity data.

**Why It Matters**: Foundational paper for multi-fidelity methods. Directly applicable to FUNWAVE (cheap) + real bathymetry (expensive).

**Method**:
- Model relationship between fidelity levels with GP
- Low-fidelity provides structure, high-fidelity corrects bias
- Optimal allocation of computational budget

**Application**: Use FUNWAVE simulations (fast, many samples) + sparse sonar bathymetry (slow, few samples) for optimal estimate.

**Impact**: Cited 2000+ times, spawned entire field of multi-fidelity modeling.

---

### Gal & Ghahramani - Dropout as Bayesian Approximation (2016)

**Core Contribution**: Dropout in neural networks can be interpreted as approximate Bayesian inference.

**Why It Matters**: Provides practical UQ for PINNs without expensive Bayesian inference. Just use dropout at test time!

**Method**:
1. Train PINN with dropout as usual
2. At inference: Keep dropout ON
3. Run multiple forward passes (MC sampling)
4. Variance of predictions = uncertainty estimate

**Advantages**: Dead simple to implement, works with existing PINNs

**Limitations**: Underestimates uncertainty compared to full Bayesian approach

**Practical**: Good first approach for adding UQ to bathymetry PINN.

---

### Zhu & Zabaras - Bayesian Deep Learning for Inverse Problems (2018)

**Core Contribution**: Bayesian deep learning framework for physics-constrained inverse problems.

**Why It Matters**: Shows how to do full Bayesian inference for inverse PDE problems with neural networks.

**Application**: Subsurface characterization (analogous to bathymetry!) - infer permeability field from pressure observations.

**Method**:
- Variational inference for posterior approximation
- Physics constraints via PDE residuals
- Handles both forward and inverse UQ

**Results**: Accurate posterior estimation even with sparse, noisy data.

**Relevance**: Direct parallel to bathymetry inverse problem structure.

---

## Bayesian PINNs

Combining the best of both worlds: Bayesian treatment of PINNs for uncertainty quantification.

### Variational Inference Approach (Yang et al., 2021)

**Method**:
1. Place prior on neural network weights: p(θ)
2. Define physics-informed likelihood: p(data, PDE residuals | θ)
3. Approximate posterior p(θ | observations) with variational distribution q(θ)
4. Minimize KL divergence: KL(q || p)

**Result**: Distribution over predictions, enabling uncertainty estimates

**Computational Cost**: Higher than standard PINNs due to sampling or variational inference

---

### Key Software Tools:
1. **GPyTorch** (Gardner et al.) - Scalable GP in PyTorch
2. **GPflow** - GP in TensorFlow
3. **BOTorch** - Bayesian optimization
4. **Pyro/NumPyro** - Probabilistic programming for Bayesian NNs
5. **scikit-learn** - Basic GP regression

---

[← Back to Literature Review](README.md) | [← Previous: Oceanography](03-oceanography.md) | [Next: Software & Tools →](05-tools-software.md)
