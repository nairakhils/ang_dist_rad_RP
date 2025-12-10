# Angular Distribution of Radiation from a Relativistic Charge

A Jupyter notebook ([Colab](https://colab.research.google.com/github/nairakhils/ang_dist_rad_RP/blob/main/ang_dist_rad_rp.ipynb)) for visualizing the **angular distribution of radiation** emitted by an accelerated charge moving at relativistic velocities. This project explores how radiation patterns depend on the charge's velocity and acceleration direction, demonstrating key relativistic effects like beaming and the headlight effect.

## Overview

This notebook implements and visualizes the angular distribution formula for radiation from a relativistic accelerated charge. The radiation pattern is strongly influenced by:
- The charge's velocity (β = v/c)
- The Lorentz factor (γ)
- The angle between acceleration and velocity (α)
- The azimuthal direction of acceleration (φₐ)

## Physics Background

### Key Parameters

- **β** = v/c: Velocity in units of the speed of light
- **γ** = 1/√(1-β²): Lorentz factor
- **θ**: Polar angle in lab frame (angle from z-axis)
- **φ**: Azimuthal angle in lab frame
- **α**: Tilt angle of acceleration from z-axis
- **φₐ**: Azimuthal angle of acceleration direction

### Mathematical Formulation

The observed radiated power per unit solid angle is:

$$\frac{dP_A}{d\Omega} = \frac{q^2 a'^2}{4\pi c^3} \frac{\sin^2\theta'}{\gamma^4 (1-\beta\cos\theta)^4}$$

where θ' is the angle in the rest frame, related to lab frame angles by:

$$\cos\theta' = \cos\alpha\cos\Theta + \sin\alpha\sin\Theta\cos(\phi - \phi_a)$$

The angle Θ is related to θ through relativistic aberration.

## Features

### Visualizations

1. **3D Surface Plots**: Interactive 3D visualizations of radiation patterns in spherical coordinates
2. **Relativistic Beaming**: Demonstrates how radiation becomes increasingly forward-focused as γ increases
3. **Parameter Sweeps**: Comprehensive exploration of:
   - Velocity dependence (β variations)
   - Acceleration angle dependence (α variations)
   - Azimuthal angle variations (φₐ)
   - Ultra-relativistic regime (β → 1)
4. **Polar Plots**: 2D polar coordinate representations for easier pattern comparison
5. **Vector Visualization**: Shows velocity and acceleration directions with quiver arrows

### Key Physical Insights

- **Relativistic Beaming**: As γ increases, radiation becomes concentrated in a forward cone with half-angle ~1/γ
- **Acceleration Direction Effects**:
  - **α = 0°** (parallel): Maximum beaming, symmetric about z-axis
  - **α = 90°** (perpendicular): Radiation still beamed forward, but with asymmetric lobes
  - **α = 180°** (antiparallel): Similar to parallel case with different intensity
- **The Headlight Effect**: For large γ, most radiation is emitted within a narrow cone around the velocity direction, regardless of acceleration direction

## Requirements

- Python 3.x
- NumPy
- Matplotlib

The notebook will automatically install matplotlib if not already present.

## Usage

1. Open the notebook `ang_dist_rad_rp.ipynb` in Jupyter Notebook or JupyterLab
2. Run all cells to generate the visualizations
3. Modify parameters (β, α, φₐ) in the code cells to explore different scenarios

### Example Parameters

```python
beta = 0.9        # Velocity (0 < β < 1)
alpha = 45.0      # Acceleration angle in degrees
phi_a = 0.0       # Azimuthal angle in degrees
```

## Applications

This visualization is relevant for understanding:
- **Synchrotron radiation**: Radiation from charged particles in magnetic fields
- **Bremsstrahlung**: Radiation from decelerating charges
- **Astrophysical jets**: Relativistic jets from active galactic nuclei and gamma-ray bursts
- **Particle accelerators**: Radiation patterns in high-energy physics experiments

## File Structure

```
ang_dist_rad_RP/
├── ang_dist_rad_rp.ipynb    # Main Jupyter notebook
├── README.md                 # This file
└── LICENSE                   # License file
```

## License

See the LICENSE file for details.

