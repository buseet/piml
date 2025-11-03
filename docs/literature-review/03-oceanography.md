# Oceanography & Bathymetry Papers

This matrix covers domain-specific literature in oceanography, wave physics, and bathymetry. These papers provide the physical understanding and modeling approaches essential for ocean-related PIML applications.

## Overview

- Wave dynamics and propagation
- Shallow water equations and Boussinesq models
- Ocean surface processes (waves, currents, wind interaction)
- Satellite remote sensing of ocean properties
- Numerical methods for wave simulation


---

## Papers & Resources

### Wave Theory & Physics

| **Paper** | **Year** | **Focus** | **Method** | **Key Result** | **Relevance** |
|---|---|---|---|---|---|
| [Mei et al. (Theory of Gravity Waves)](https://doi.org/10.1142/9789813147195_0001) | 2005 | Comprehensive wave theory | Textbook | Foundation for wave physics | 5 - Essential theory |
| [Dean & Dalrymple (Water Wave Mechanics)](https://doi.org/10.1142/1232) | 1991 | Wave mechanics | Textbook | Engineering wave theory | 4 - Practical reference |
| [Touboul et al. (Waves & Currents)](https://doi.org/10.3390/jmse12030509) | 2024 | Wave-current interaction | Weakly nonlinear | Variable bathymetry | 4 - Physics model |
| [Kirby & Dalrymple (Refraction-Diffraction)](https://doi.org/10.1017/S0022112083002232) | 1983 | Wave transformation | Parabolic model | Refraction and diffraction | 4 - Wave propagation |
| [Peregrine (Long Waves)](https://doi.org/10.1017/S0022112067002605) | 1967 | Boussinesq equations | Analytical | Original Boussinesq derivation | 5 - Foundation |

### Remote Sensing & Satellite

| **Paper** | **Year** | **Focus** | **Data Source** | **Method** | **Key Result** | **Relevance** |
|---|---|---|---|---|---|---|
| [Kudryavtsev et al. (Sun Glitter)](https://doi.org/10.1002/2016JC012425) | 2017 | Wave spectra | Optical imagery | Statistical analysis | Directional spectra | 5 - Image analysis |
| [Drusch et al. (Sentinel-2)](https://doi.org/10.1016/j.rse.2011.11.026) | 2012 | Mission overview | Multispectral | Satellite mission | Mission description | 3 - Data source |
| [Pleskachevsky et al. (SAR Wave)](https://doi.org/10.1007/s10236-011-0460-1) | 2011 | Wave from SAR | Radar imagery | Spectral analysis | Wave parameters from SAR | 4 - SAR altimetry |
| [Jackson et al. (SAR Bathymetry)](https://doi.org/10.1016/j.csr.2013.11.025) | 2014 | Bathymetry | SAR | Wave inversion | Depth from SAR waves | 5 - SAR bathymetry |
| [Lyzenga et al. (Passive Bathymetry)](https://doi.org/10.1029/JC090iC01p01031) | 1985 | Optical bathymetry | Multispectral | Water penetration | Depth from color | 4 - Classical method |

### In-Situ Measurements & Validation

| **Paper/Resource** | **Year** | **Focus** | **Instrument** | **Method** | **Key Result** | **Relevance** |
|---|---|---|---|---|---|---|
| [Herbers et al. (Wave Buoy Arrays)](https://doi.org/10.1175/1520-0485(2002)032%3C1181:NDOSGW%3E2.0.CO;2) | 2001 | Directional waves | Wave buoys | Statistical analysis | Validation standard | 4 - Validation data |
| [Raubenheimer et al. (ADCP Waves)](https://doi.org/10.1061/9780784404119.273) | 1998 | Nearshore waves | ADCP | Pressure + velocity | Nearshore validation | 4 - In-situ method |
| [Stockdon & Holman (Wave Runup)](https://doi.org/10.1016/j.coastaleng.2005.12.005) | 2006 | Wave runup | Video + lidar | Empirical formula | Runup prediction | 3 - Coastal processes |

### Numerical Wave Models & Software

| **Resource** | **Year** | **Focus** | **Method** | **Key Features** | **Relevance** |
|---|---|---|---|---|---|
| [FUNWAVE Documentation](https://fengyanshi.github.io/) | Current | Boussinesq waves | Fully nonlinear | Breaking, runup, parallel | 5 - Your PDE! |
| [SWASH Manual](https://swash.sourceforge.io/) | Current | Nonhydrostatic | Phase-resolving | Vertical structure | 4 - Alternative model |
| [Roelvink et al. (XBeach)](https://doi.org/10.1016/j.coastaleng.2009.08.006) | 2009 | Nearshore processes | Coupled model | Morphodynamics | 3 - Beach evolution |
| [Madsen & Sørensen (Boussinesq)](https://doi.org/10.1016/0378-3839(92)90019-Q) | 1992 | Boussinesq formulation | Higher-order | Improved dispersion | 4 - Theory reference |

### PIML & Data-Driven Oceanography

| **Paper** | **Year** | **Focus** | **Data Source** | **Method** | **Key Result** | **Relevance** |
|---|---|---|---|---|---|---|
| [Yoon et al. (Ocean Pressure PINN)](https://doi.org/10.1121/10.0025235) | 2024 | Pressure reconstruction | Sparse sensors | PINN | 10% data coverage | 5 - PIML ocean application |
| [Zanna & Bolton (Data-Driven Ocean)](https://doi.org/10.1029/2020GL088376) | 2020 | Ocean modeling | Climate data | ML surrogate | Parameterization | 4 - Data-driven approach |
| [de Bezenac et al. (DL Dynamics)](https://doi.org/10.48550/arXiv.1711.07970) | 2017 | Ocean dynamics | Satellite | Deep learning | Learn physics | 4 - Learn from observations |

---

## Key Papers Expanded

### Yoon et al. - Ocean Pressure Field Reconstruction with PINNs (2024)

**Core Contribution**: Reconstructs full ocean pressure fields from sparse sensor measurements using physics-informed neural networks with Navier-Stokes constraints.

**Why It Matters**: Demonstrates PIML effectiveness in oceanography with minimal data (10% coverage). Direct parallel to bathymetry inversion from sparse observations.

**Method**:
- PINN with hydrostatic pressure and incompressibility constraints
- Sparse sensor data as boundary conditions
- Temporal evolution prediction

**Results**: High accuracy reconstruction with uncertainty estimates

**Relevance**: Same problem structure as bathymetry inversion - sparse observations → full field reconstruction

---

### Kudryavtsev et al. - Sun Glitter and Wave Spectra (2017)

**Core Contribution**: Theoretical and practical framework for extracting wave spectra from sun glitter patterns in satellite imagery.

**Why It Matters**: Shows how surface wave information is encoded in optical satellite imagery. Critical for understanding what can be extracted from Sentinel-2 type data.

**Key Physics**: Sun glitter is produced by specular reflection from wave facets. Statistical analysis of glitter patterns reveals wave spectrum.

**Applications**:
- Wave direction estimation
- Wave period and wavelength measurement
- Validation for wave models

---

### Touboul et al. - Wave-Current Interactions Over Variable Bathymetry (2024)

**Core Contribution**: Weakly nonlinear theory for wave propagation over currents and variable bathymetry. Provides analytical solutions for certain regimes.

**Why It Matters**: Provides the physics foundation for understanding wave behavior in coastal zones with complex bathymetry and currents.

**Key Equations**:
- Modified dispersion relation accounting for currents
- Refraction and shoaling coefficients
- Energy conservation principles

**Applicability**: Relevant for interpreting wave patterns observed in satellite imagery over variable depth.

---

### Sentinel-2 Mission (Drusch et al., 2012)

**Overview**: Sentinel-2 is ESA's high-resolution multispectral imaging mission for land and coastal monitoring.

**Key Specifications**:
- 13 spectral bands (visible to SWIR)
- 10m, 20m, 60m spatial resolution
- 5-day revisit time (two satellites)
- Global coverage, freely available

**Relevance for Bathymetry**:
- Visible bands (blue, green, red) penetrate clear water
- 10m resolution captures wave patterns
- High temporal resolution enables multi-temporal analysis
- Open data policy facilitates research

**Challenges**:
- Cloud cover in tropical regions
- Sun glint contamination
- Atmospheric correction requirements
- Limited depth penetration in turbid water

---

### Peregrine - Long Waves on Beach (1967)

**Core Contribution**: Original derivation of Boussinesq equations for long waves in shallow water.

**Why It Matters**: Foundation for all modern Boussinesq wave models (including FUNWAVE). Understanding the approximations is critical for knowing when these models apply.

**Key Approximations**:
- Long waves: λ >> h (wavelength much greater than depth)
- Weakly dispersive: Valid for kh < π
- Weakly nonlinear: Wave height much less than depth

**Historical Impact**: Enabled practical modeling of nearshore wave dynamics before computational power existed for full Navier-Stokes.

---

### Jackson et al. - SAR Bathymetry (2014)

**Core Contribution**: Method for deriving bathymetry from Synthetic Aperture Radar (SAR) wave observations.

**Why It Matters**: Provides alternative to optical (Sentinel-2) approaches - works through clouds and in all lighting conditions.

**Method**:
1. Extract wave wavelength from SAR imagery
2. Apply dispersion relation (similar to optical methods)
3. Account for SAR-specific imaging effects

**Advantages**: All-weather capability, independent validation for optical methods

**Limitations**: Coarser resolution than optical, requires wave presence

**Complementarity**: Combine SAR + optical for robust all-conditions bathymetry.

---

### Lyzenga et al. - Passive Optical Bathymetry (1985)

**Core Contribution**: Classical method for bathymetry from water color using multispectral imagery.

**Why It Matters**: Different physical principle than wave-based methods - uses water penetration of light, not surface waves.

**Method**:
```
Depth ∝ ln(Blue band reflectance) - ln(Green band reflectance)
```

**Advantages**:
- Works in calm water (no waves needed)
- Simple, well-established
- Calibration-based

**Limitations**:
- Limited to very shallow water (<20m in clear water)
- Requires water clarity
- Needs empirical calibration

**Complementarity**: Use for shallow zones where wave methods struggle; wave methods for deeper zones.

---

### Herbers et al. - Directional Wave Measurements (2001)

**Core Contribution**: Analysis of directional wave spectra from wave buoy arrays.

**Why It Matters**: Gold standard for wave validation. Provides ground truth for satellite-derived wave parameters.

**Key Measurements**:
- Wave height (significant wave height H_s)
- Wave period (peak period T_p)
- Wave direction (directional spectrum)

**Application**: Validate wave features extracted from Sentinel-2 before using for bathymetry inversion.

---

### Zanna & Bolton - Data-Driven Ocean Modeling (2020)

**Core Contribution**: Machine learning approach to learn sub-grid scale parameterizations in ocean models.

**Why It Matters**: Shows how ML can replace unknown physics in ocean modeling. Parallel to using ML for unknown bathymetry.

**Method**:
- High-resolution simulation as ground truth
- ML learns mapping from coarse variables to sub-grid terms
- Dramatically improves coarse model accuracy

**Relevance**: Demonstrates data-driven approach for missing physics - applicable when wave theory is uncertain or incomplete.



---

## Practical 

### Key Data Sources for Bathymetry Validation:
1. **Sentinel-2** (10m optical) - Primary imagery source
2. **SAR** (TerraSAR-X, Sentinel-1) - All-weather complement
3. **Wave buoys** (NDBC, CDIP) - Wave parameter validation
4. **Multibeam sonar** - High-accuracy bathymetry reference
5. **Lidar** (bathymetric) - Shallow water reference

### Preprocessing Steps
1. Atmospheric correction
2. Cloud and cloud shadow masking
3. Sun glint detection and masking/correction
4. Georeferencing and orthorectification
5. Temporal compositing (if using multi-temporal)

### Validation Metrics
- Mean Absolute Error (MAE) in depth
- Root Mean Square Error (RMSE)
- Percentage of pixels within error threshold (e.g., <1m, <2m)
- Spatial correlation with reference bathymetry

---

[← Back to Literature Review](README.md) | [← Previous: Image/Vision](02-image-vision.md) | [Next: Bayesian Methods →](04-bayesian-methods.md)
