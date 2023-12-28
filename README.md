## Lumped Parameter Model Experimental Validation

### Overview

This repository contains the experimental validation details for the lumped parameter model introduced in Section 1 of the associated research paper. The validation experiments were conducted using a scaled-down multi-grounded system, as described below.

### Experimental Setup

![fig100](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation/assets/96079504/ba2851b3-8f18-4c76-a4f1-d1ad3feacb9d)


To validate the lumped parameter model introduced in Section 1, experiments were conducted using a scaled-down multi-grounded system. The system consisted of three 1.5 m rods spaced 7.5 m apart, interconnected to a 15 m horizontal electrode. Each copper rod symbolized a turbine grounding, boasting a cross-sectional area of 126 mm², while the copper horizontal electrode had a cross-sectional area of 35 mm².

The horizontal electrode was buried 0.12 m below the ground. Two different conditions were tested for the variable s, specifically at values 0.22 and 1.5 m. The radial connection between the rods and the horizontal electrode was established using an insulated wire. The soil had an average low-frequency resistivity of 86 Ω·m.

### Measurements

Measurements Zmed <sub>meter</sub> were conducted using the UT-278A clamp-on meter attached to the interconnection cable linking each rod to the horizontal electrode. The measurements were compared with simulated readings Zmed <sub>LPM</sub> obtained from the proposed equivalent electrical circuit model.

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
