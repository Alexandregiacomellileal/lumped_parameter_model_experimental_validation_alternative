## Lumped Parameter Model Experimental Validation

### Overview

This repository contains the experimental validation details for the lumped parameter model introduced in Section 1 of the associated research paper. The validation experiments were conducted using a scaled-down multi-grounded system, as described below.

### Experimental Setup

![fig100](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation/assets/96079504/ba2851b3-8f18-4c76-a4f1-d1ad3feacb9d)


To validate the lumped parameter model introduced in Section 1, experiments were conducted using a scaled-down multi-grounded system. The system consisted of three 1.5 m rods spaced 7.5 m apart, interconnected to a 15 m horizontal electrode. Each copper rod symbolized a turbine grounding, boasting a cross-sectional area of 126 mm², while the copper horizontal electrode had a cross-sectional area of 35 mm².

The horizontal electrode was buried 0.12 m below the ground. Two different conditions were tested for the variable s, specifically at values 0.22 and 1.5 m. The radial connection between the rods and the horizontal electrode was established using an insulated wire. The soil had an average low-frequency resistivity of 86 Ω·m.

### Measurements clamp-on ground meter

Measurements Zmed <sub>meter</sub> were conducted using the UT-278A clamp-on meter attached to the interconnection cable linking each rod to the horizontal electrode. The measurements were compared with simulated readings Zmed <sub>LPM</sub> obtained from the proposed equivalent electrical circuit model.

### Electrical Circuit and Grounding Resistance Calculation

The electrical circuit for the measurements was established and simulated to acquire the meter readings Zmed<sub>LPM</sub> following the procedures detailed in Paper. Notably, the approach used to calculate the grounding resistance of the rod differs, utilizing the Sunde formula. This formula is particularly suitable for scenarios where cylindrical electrodes are vertically installed, especially when their length significantly exceeds their cross-section.

The grounding resistance of the rod R<sub>rod</sub> is calculated as follows:

\math\[ R_{\text{rod}} = \frac{\rho_a^{\text{rod}}}{2 \pi l_{\text{rod}}} \left( \ln\left(\frac{4l_{\text{rod}}}{a_{\text{rod}}}\right) - 1 \right) \, \Omega \]

Where:
- $\rho_a^{rod}$ represents the apparent resistivity observed by the rod (\(\Omega \cdot \text{m}\)),
- $l_{rod}$ is the rod's length (m),
- $a_{rod}$ is the rod's radius (m).

The rod shunt capacitance C<sub>rod</sub> is calculated using the formula:

$\[ C_{rod} = \frac{\rho_a^{rod} \ \varepsilon}{R_{rod}} \, \text{F} \]$

Where:
- $\varepsilon$ represents the permittivity of the soil, estimated at $7.9686 \times 10^{-11} \, \text{F/m}$.

### Measurement Methods

The apparent resistivities $\rho_a^{rod}$ are measured using the driven rod method with the low-frequency Fall-of-Potential method. The equipment used for these measurements is the digital earth meter MTR-1522. The instrument has a resolution of \(0.01 \, \Omega\), and its accuracy is $\pm (2.0\% + 20 \, \text{dig})$.

The apparent resistivity observed by the horizontal electrode is determined by averaging the apparent resistivities observed by the rods. This observation is cross-validated using the Fall-of-Potential method.

### Parameter Estimation

As per Section \ref{sub:k}, the parameter $k$ was estimated to be 0.74 for an $s$ value of 0.22 m and 0.90 for an $s$ value of 1.5 m.


### Grounding Resistance Calculation

The grounding resistance of each rod R<sub>rod</sub> was calculated using the Sunde formula, taking into account the apparent resistivity observed by the rod. The rod shunt capacitance C<sub>rod</sub> was also calculated using the formula provided.

### Results

The obtained results demonstrate a robust agreement, with a Mean Absolute Percentage Error of 1.39 ± 0.12%, between the values registered by the clamp-on meter and those predicted by the proposed equivalent electrical circuit model.

### Table of Results

| s (m) | k | Rod | Zmed<sub>meter</sub> (Ω) | Zmed<sub>LPM</sub> (Ω) | APE<sub>LPM</sub> (%) |
|-------|---|-----|-------------------|----------------|---------------|
| 0.22  | 0.74 | 1 | 63.5 ± 1.5 | 64.37 ± 3.84 | 1.37 ± 0.09 |
| 0.22  | 0.74 | 2 | 46.3 ± 1.2 | 47.06 ± 2.86 | 1.64 ± 0.13 |
| 0.22  | 0.74 | 3 | 35.5 ± 0.5 | 35.34 ± 2.20 | 0.45 ± 0.17 |
| 1.50  | 0.90 | 1 | 72.5 ± 1.6 | 73.43 ± 4.35 | 1.28 ± 0.08 |
| 1.50  | 0.90 | 2 | 56.0 ± 1.3 | 55.45 ± 3.34 | 0.98 ± 0.11 |
| 1.50  | 0.90 | 3 | 39.1 ± 0.5 | 40.12 ± 2.47 | 2.61 ± 0.15 |

### Conclusion

The results serve as validation for the proposed lumped parameter model, with a strong agreement between experimental and simulated data.

## License

This project is licensed under the [License Name] - see the [LICENSE.md](LICENSE.md) file for details.
