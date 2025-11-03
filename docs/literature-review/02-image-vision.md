# Image/Vision Integration Papers

This matrix focuses on the integration of computer vision and physics-informed machine learning. These papers are critical for applications involving satellite imagery, remote sensing, and extracting physical quantities from visual data.

## Overview

Image-based PIML is an emerging area that bridges computer vision and scientific computing. Key challenges include:

- Extracting physical fields from images (inverse problems)
- Ensuring physics consistency in image-to-physics mappings
- Handling multi-spectral and satellite imagery
- Dealing with observational noise and incomplete data
- Scaling to high-resolution imagery

---

| **Paper** | **Year** | **Input** | **Output** | **Method** | **Key Innovation** | **Performance** | **Limitations** | **Relevance** |
|---|---|---|---|---|---|---|---|---|
| [Bergsma et al. (Radon Sentinel-2)](https://doi.org/10.3390/rs11161918) | 2019 | Satellite images | Bathymetry | Radon transform | Wave patterns → depth | Good regional | Resolution limited | 5 - Image → physics |
| [Kudryavtsev et al. (Sun Glitter)](https://doi.org/10.1002/2016JC012425) | 2017 | Optical imagery | Wave spectra | Statistical analysis | Glitter → wave direction | Directional spectra | Clear sky only | 5 - Feature extraction |
| [de Michele et al. (Shallow Bathymetry)](https://doi.org/10.3390/rs13112149) | 2021 | Multi Sentinel-2 | Depth | Wave analysis + ML | Joint wave estimation | <2m error | Shallow only | 5 - Multi-image |
| [Caballero & Stumpf (ML + Dispersion)](https://doi.org/10.1364/OE.390316) | 2020 | Satellite + Empirical | Bathymetry | ML + wave physics | Hybrid regression | Regional accuracy | Calibration needed | 5 - Practical hybrid |
| [Buscombe & Ritchie (Landscape Classification)](https://doi.org/10.3390/geosciences8070244) | 2018 | Satellite imagery | Shorelines | CNN / Segmentation | Automated shoreline | Good accuracy | Needs training data | 4 - Segmentation baseline |
| [Liu et al. (Bathymetry Inversion)](https://doi.org/10.1029/2023WR035890) | 2024 | Surface obs | Bathymetry | DL surrogate / CNN | SWE surrogate | 10x faster | 2D only | 5 - Core method |
| [Adler & Öktem (Learned Primal-Dual)](https://doi.org/10.1109/TMI.2018.2799231) | 2018 | Measurements | Reconstruction | Unrolled optimization | Learned inverse | Inverse imaging | Medical focus | 4 - Inverse framework |
| [Geneva & Zabaras (Multi-fidelity)](https://doi.org/10.48550/arXiv.2006.04731) | 2020 | Low-res images | High-res physics | Transfer learning | Multi-fidelity NN | Physics SR | Needs paired data | 4 - Super-resolution |
| [Yang et al. (Physics-Informed GANs)](https://doi.org/10.1137/18M1225409) | 2020 | Simulation | Images | GAN + PDE loss | Physics-consistent images | Realistic | Training instability | 4 - Forward (physics→image) |
| [Xie et al. (tempoGAN)](https://doi.org/10.1145/3197517.3201304) | 2018 | Low-res sim | High-res sim |Spatio-temporal GAN | Physics SR | Fast | Fluid specific | 4 - Temporal SR |
| [Kohl et al. (Probabilistic U-Net)](https://doi.org/10.48550/arXiv.1806.05034) | 2018 | Images | Segmentation + UQ | Variational | U-Net + latent | Uncertainty in segmentation | Medical focus | 3 - UQ for segmentation |

----

| **Paper** | **Year** | **Scope** | **Key Contribution** |
|---|---|---|---|
| [Banerjee et al. (Physics-Informed CV Review)](https://doi.org/10.1145/3689037) | 2024 | Physics + CV | Comprehensive taxonomy | 
| [Karpatne et al. (Theory-Guided Data Science)](https://doi.org/10.1109/TKDE.2017.2720168) | 2017 | General framework | Physics-guided ML principles | 
| [Reichstein et al. (Deep Learning for Earth)](https://doi.org/10.1038/s41586-019-0912-1) | 2019 | Earth observation | DL + physics for climate |

---

## Key Papers Expanded

### Banerjee et al. - Physics-Informed Computer Vision (2024)

**Core Contribution**: Comprehensive review of how physics principles are integrated into computer vision tasks, including inverse problems, constraint enforcement, and multi-physics scenarios.

**Why It Matters**: Provides a taxonomy and roadmap for the emerging field of physics-informed vision. Essential reading for understanding the landscape.

**Key Sections**:
- Physics as constraints in vision models
- Inverse imaging problems with physics priors
- Applications in remote sensing and scientific imaging

---

### Liu et al. - Bathymetry Inversion via Deep Learning (2024)

**Core Contribution**: Deep learning surrogate model for solving shallow water equations (SWE) to invert bathymetry from surface observations.

**Why It Matters**: Directly addresses the bathymetry inversion problem using learned PDE surrogates. Achieves 10x speedup over traditional methods.

**Method**:
1. Train CNN to solve forward SWE problem
2. Use trained model in optimisation loop for inversion
3. Regularisation with physical constraints

**Limitations**: Currently limited to 2D problems, requires substantial training data

---

### Bergsma et al. - Radon Transform for Bathymetry (2019)

**Core Contribution**: Uses Radon transform to detect wave patterns in Sentinel-2 imagery and invert for bathymetry using linear wave theory.

**Why It Matters**: Demonstrates practical bathymetry estimation from freely available satellite imagery. Pure physics-based approach (no ML).

**Key Insight**: Wave dispersion relation provides direct link between observed wavelength and water depth.

**Data**: Sentinel-2 multispectral imagery (10m resolution)

**Citation**: Bergsma, E. W. J., Almar, R., & Maisongrande, P. (2019). Radon-augmented Sentinel-2 satellite imagery to derive wave-patterns and regional bathymetry. Remote Sensing, 11(16), 1918.

---

### de Michele et al. - Multi-Image Shallow Bathymetry (2021)

**Core Contribution**: Combines multiple Sentinel-2 images to jointly estimate wave parameters and bathymetry, improving robustness.

**Why It Matters**: Shows how temporal stacking of imagery improves inversion accuracy to <2m error in shallow coastal zones.

**Method**:
- Wave period estimation from multi-temporal imagery
- Joint optimization of wave and bathymetry parameters
- Validation with in-situ measurements

---

### Yang et al. - Physics-Informed GANs (2020)

**Core Contribution**: Incorporates physics losses (PDE residuals) into GAN training for generating physically consistent images.

**Why It Matters**: Demonstrates the reverse problem - generating images from physics - which provides insights for inverse mappings.

**Applications**: Flood simulation, flow visualization, scientific image synthesis


---

### Geneva & Zabaras - Multi-fidelity (2020)

**Core Contribution**: Transfer learning framework combining cheap low-fidelity simulations with sparse high-fidelity data for physics-based super-resolution.

**Why It Matters**: Addresses the simulation-to-reality gap. Can use FUNWAVE simulations to pre-train, then fine-tune on sparse real bathymetry.

**Method**:
1. Train on abundant low-fidelity data (coarse resolution or simplified physics)
2. Transfer to high-fidelity regime with limited data
3. Physics constraints ensure consistency

**Application**: Pre-train on synthetic Sentinel-2 + FUNWAVE pairs, fine-tune on real imagery with sparse in-situ bathymetry.

---

### Adler & Öktem - Learned Primal-Dual (2018)

**Core Contribution**: Unroll iterative optimization algorithms as neural networks, combining model-based and data-driven approaches.

**Why It Matters**: Provides principled way to combine physics (optimization) with learning (CNN). Each layer corresponds to an iteration of physics-based solver.

**Framework**:
```
Physical forward model → Iterative solver → Unroll as NN layers → Train end-to-end
```

**Key Insight**: Embed physical forward model within learnable architecture.

**Relevance**: Could unroll wave-to-bathymetry inversion as learnable layers with Boussinesq forward model embedded.

---

### Caballero & Stumpf - Hybrid ML + Dispersion (2020)

**Core Contribution**: Combines machine learning regression with physics-based dispersion relation for satellite-derived bathymetry.

**Why It Matters**: Practical hybrid approach balancing ML flexibility with physics guarantees. Demonstrates that hybrid > pure physics or pure ML.

**Method**:
1. ML extracts wave features from imagery
2. Physics (dispersion) constrains depth estimation
3. Empirical calibration for regional tuning

**Results**: Improved accuracy over pure physics (Radon) or pure empirical methods.

**Takeaway**: Don't need full PINN - even simple hybrid gives benefits.

---

### Kudryavtsev et al. - Sun Glitter Analysis (2017)

**Core Contribution**: Statistical framework for extracting wave spectra from sun glitter patterns in optical satellite imagery.

**Why It Matters**: Shows how to extract directional wave information from Sentinel-2, which is critical input for bathymetry inversion.

**Key Physics**: Sun glitter is created by specular reflection from wave facets oriented toward sun. Statistical properties of glitter → wave slope spectrum.

**Practical Value**: Provides wave direction and wavelength - the inputs needed for dispersion-based inversion.

**Limitation**: Requires sun glitter conditions (sun angle, sea state).

---

[← Back to Literature Review](README.md) | [← Previous: Core PIML](01-core-piml.md) | [Next: Oceanography →](03-oceanography.md)
