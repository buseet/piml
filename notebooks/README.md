# PIML Notebooks

Interactive Jupyter notebooks for hands-on learning of Physics-Informed Machine Learning. These notebooks combine explanations, visualizations, and executable code.

## Organization

Notebooks are organized by difficulty and topic:

```
notebooks/
├── 01-introduction/        # Getting started, simple examples
├── 02-basic-examples/      # Core PIML methods
└── 03-advanced-topics/     # Specialized techniques and applications
```

## Getting Started

### Installation

1. Install dependencies:
```bash
pip install -r ../requirements.txt
```

2. Launch Jupyter:
```bash
jupyter notebook
```

3. Start with notebooks in `01-introduction/`

### Running in the Cloud

**Google Colab**: Click the "Open in Colab" badge at the top of each notebook

## Notebook Series

### 01 - Introduction  ☜(ﾟヮﾟ☜)
*Prerequisites: Basic Python, calculus*

Learn PIML fundamentals through simple, visual examples:
- [Coming Soon] **Harmonic Oscillator PINN** - Your first physics-informed model
- [Coming Soon] **Heat Equation 1D** - Understanding PDE constraints
- [Coming Soon] **Data vs Physics Trade-off** - Loss balancing exploration

[See series details →](01-introduction/README.md)

---

### 02 - Basic Examples ¯\_(ツ)_/¯ 
*Prerequisites: Complete 01-introduction series*

Implement core PIML methods:
- [Coming Soon] **Burgers Equation** - Classic PINN benchmark
- [Coming Soon] **2D Poisson Equation** - Multi-dimensional problems
- [Coming Soon] **Wave Propagation** - Time-dependent dynamics
- [Coming Soon] **Simple Inverse Problem** - Parameter estimation

[See series details →](02-basic-examples/README.md)

---

### 03 - Advanced Topics ¯\(°_o)/¯
*Prerequisites: Complete 02-basic-examples series*

Explore specialized techniques and applications:
- [Coming Soon] **Bayesian PINN** - Uncertainty quantification
- [Coming Soon] **Neural Operator (DeepONet)** - Learning operators
- [Coming Soon] **FBPINNs** - Domain decomposition
- [Coming Soon] **Bathymetry Inversion** - Satellite imagery application
- [Coming Soon] **Multi-Fidelity Learning** - Combining simulation levels

[See series details →](03-advanced-topics/README.md)

---

## Notebook Features

Each notebook includes:

### Theory Section
- Problem formulation
- Governing equations
- Solution approach

### Implementation
- Step-by-step code with comments
- Visualization of results
- Comparison with analytical/numerical solutions

### Exercises
- Hands-on modifications to try
- Questions to test understanding
- Extensions for further exploration

### References
- Related papers from [Literature Review](../docs/literature-review/)
- Additional resources

## Tips for Success

### 1. Run the Code
Don't just read - execute cells and experiment! Change parameters, modify architectures, break things and fix them :).

### 2. Visualize Everything
Plot intermediate results. Visualize loss curves, PDE residuals, predictions. Understanding comes from seeing beautiful images.

### 3. Start Simple
Don't skip the introductory notebooks. Simple examples build intuition that transfers to complex problems.

### 4. Experiment with Hyperparameters
Try different:
- Network architectures (width, depth)
- Learning rates
- Physics loss weights
- Activation functions

### 5. Expect Failures
Not all hyperparameter combinations work. PIML training can be finicky. Learn from failures...

### 6. Compare with Ground Truth
Whenever possible, compare PINN predictions with:
- Analytical solutions
- Traditional numerical methods (FEM, FDM)
- Known data

## Common Issues

### Training Not Converging?
- Check loss balancing (physics vs data weights)
- Try different optimizers (L-BFGS often works better than Adam for PINNs)
- Increase network size or change activation function
- Add more collocation points

### Out of Memory?
- Reduce batch size or number of collocation points
- Use smaller network
- Enable gradient checkpointing

### Slow Training?
- Use GPU if available
- Reduce collocation points (but check physics satisfaction)
- Consider domain decomposition for large problems

## Contributing Notebooks

Have a tutorial to share? Notebook contributions are welcome!

## Companion Resources

- **[Fundamentals](../docs/fundamentals/)**: Conceptual background before coding
- **[Guides](../docs/guides/)**: Written tutorials for deeper dives
- **[Examples](../examples/)**: Standalone Python scripts
- **[Literature Review](../docs/literature-review/)**: Theory and papers

---

**Current Status**: Structure established, notebooks in development. Check back for updates as notebooks are added!

**Have Questions?** Open an issue in the repository.

**Found a Bug?** Please report it so we can fix it!

---

[← Back to Main](../README.md)
