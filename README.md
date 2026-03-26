# Globular Cluster Analysis of M4 using Gaia Data

## Overview

This project analyzes Gaia astrometric data to identify and characterize stars belonging to the globular cluster M4. By applying filters based on position, parallax, and proper motion, the cluster is isolated and used to estimate its distance, structure, and dynamical properties.

---

## Why This Matters

Globular clusters are dense, gravitationally bound systems of stars that provide insight into stellar evolution and the structure of the Milky Way. Gaia’s high-precision measurements allow us to study stellar motions and distributions in detail, making it possible to estimate cluster properties such as distance, size, and internal dynamics.

---

## Methods

* Loaded Gaia dataset containing RA, Dec, parallax, and proper motion
* Applied quality cuts to remove unreliable measurements
* Selected stars with positive parallax to estimate distances
* Filtered stars using proper motion to isolate cluster members
* Estimated cluster center using mean RA and Dec
* Converted angular separations into projected physical distances
* Calculated spatial dispersion and velocity dispersion
* Modeled cluster dynamics using a simple harmonic oscillator approximation

---

## Results

### Data Filtering

* Total stars in dataset: **104,734**
* Usable sources: **102,433**
* Positive parallax sources: **86,442**
* Stars after proper motion cut: **17,216**
* Final M4 cluster sample: **4,005**

### Cluster Properties

* Cluster center RA: **245.8961 deg**
* Cluster center Dec: **-26.5214 deg**
* Mean proper motion (RA): **-12.493 mas/yr**
* Mean proper motion (Dec): **-19.002 mas/yr**

### Distance

* Median parallax: **0.5257 mas**
* Estimated distance: **1902.2 pc (1.902 kpc)**

### Structural Properties

* Projected spatial dispersion: **5.389 pc**
* Median projected radius: **2.991 pc**
* 90th percentile radius: **7.980 pc**

### Dynamical Properties

* Projected velocity dispersion (σ₁D): **6.104 km/s**
* Angular frequency (ω): **1.158 1/Myr**
* Oscillation period: **5.425 Myr**

The results show a compact, gravitationally bound stellar system with consistent proper motion and spatial clustering, characteristic of a globular cluster.

---

## Important Note on Velocity Dispersion

The velocity dispersion calculated here is the projected one-dimensional dispersion (σ₁D). Assuming isotropy, the full three-dimensional dispersion satisfies:

σ₃D² ≈ 3σ₁D²

This assumption is commonly used when estimating the dynamical properties of stellar systems.

---

## Visualizations

### Sky Position (RA vs Dec)

![Sky Plot](sky_plot.png)

### Proper Motion Distribution

![Proper Motion](proper_motion.png)

### Cluster Member Selection

![Cluster Selection](cluster_selection.png)

### Radial Distribution

![Radial Distribution](radial_distribution.png)

---

## How to Run

1. Clone the repository
2. Install required libraries:

   * NumPy
   * Pandas
   * Matplotlib
3. Ensure the Gaia dataset file is in the project directory
4. Run:

   ```
   jupyter notebook globular-cluster-analysis-gaia.ipynb
   ```

---

## Tools Used

* Python
* NumPy
* Pandas
* Matplotlib

---

## Future Improvements

* Compute full 3D velocity dispersion explicitly
* Apply error-weighted analysis using measurement uncertainties
* Compare results with published M4 cluster values
* Extend analysis to additional globular clusters

---

## Author

Danessa Ruff

Michigan State University
