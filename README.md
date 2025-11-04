# Physics-Informed Machine Learning (PIML) Resources

A collection of Physics-Informed Machine Learning resources, literature review, tutorials, and code examples. This repository serves as a knowledge hub for researchers, practitioners, and students interested in combining physics knowledge with machine learning.

## What is PIML? ☜(ﾟヮﾟ☜)

Physics-Informed Machine Learning (PIML) integrates domain knowledge from physics, engineering, and science into machine learning models. By incorporating physical laws, governing equations, and constraints, PIML methods can:

- Learn from smaller datasets
- Produce physically consistent predictions
- Generalise better to unseen scenarios
- Provide interpretable and trustworthy results

## Repository Structure

```
piml/
├── docs/                      # Documentation and written resources
│   ├── literature-review/     # Comprehensive literature matrices
│   └── fundamentals/          # Core concepts and introductions
├── notebooks/                 # Interactive Jupyter notebooks
└── examples/                  # Standalone code examples
└── resources/                 # Additional materials and datasets
```

## Quick Navigation

- **[Literature Review](docs/literature-review/)** contains 50+ papers organized into five thematic matrices
  - [Core PIML Papers](docs/literature-review/01-core-piml.md): Foundational papers on PINNs, neural operators, and domain decomposition
  - [Image/Vision Integration](docs/literature-review/02-image-vision.md): Methods for extracting physics from images (critical for remote sensing)
  - [Oceanography & Bathymetry](docs/literature-review/03-oceanography.md): Wave modeling, bathymetry inversion, and ocean physics
  - [Bayesian Methods](docs/literature-review/04-bayesian-methods.md): Gaussian processes, uncertainty quantification, and probabilistic approaches
  - [Software & Tools](docs/literature-review/05-tools-software.md):Frameworks, libraries, and tutorial resources

- **[Fundamentals](docs/fundamentals/)**: Introduction to PIML concepts
- **[Notebooks](notebooks/)**: Interactive tutorials with explanations
- **[Examples](examples/)**: Ready-to-use code implementations

## Getting Started ฅ(^•ﻌ•^ฅ)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/piml.git
cd piml
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Explore the notebooks:
```bash
jupyter notebook notebooks/
```

## Contributing

This repository is actively evolving. Contributions, suggestions, and feedback are welcome! Please feel free to:

- Open issues for questions or suggestions
- Submit pull requests for improvements
- Share your own PIML examples or case studies

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
**Note**: This repository consolidates knowledge from the broader PIML research community. 

**Last Updated**: November 2025 | **Status**: Active Development
