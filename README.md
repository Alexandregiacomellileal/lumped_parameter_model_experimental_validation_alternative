## Lumped Parameter Model Experimental Validation - Reduced Scale

![reduce_scale_git_alternative](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/assets/96079504/42daa77c-4bac-4b21-8305-aef9f31a88cd)

### Overview

This repository contains the experimental validation details for the lumped parameter model introduced in Section 2.2 of the associated research paper. The validation experiments were conducted using a scaled-down multi-grounded system, as described below.

### Experimental Setup

<img src="https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/assets/96079504/2ae43894-9204-4769-99b4-26f66578caee" width="400" height="350">

The proposed lumped parameter model underwent experimental validation using a reduced-scale model of the grounding system detailed in Section 2.2 of the associated research paper. The grounding system was constructed with three 4 mm thick steel cylinders spaced 7.5 m apart, interconnected to a 15 m horizontal electrode. Each steel cylinder, symbolizing a turbine grounding, boasted a radius of 19.7 cm and a height of 43 cm, while the copper horizontal electrode had a cross-sectional area of 35 $mm^2$.

The horizontal electrode was buried 12 cm below the ground. Each cylinder electrode was positioned on the same side at a distance of 28.5 cm from the horizontal electrode. The radial connection between the cylinder and horizontal electrodes was established using an insulated wire with a cross-sectional area of 10 $mm^2$, with a length of $s$ + 0.1 $(m)$. The soil had an average low-frequency resistivity of 86.8 Ω·m.

### Measurements clamp-on ground meter

Measurements Zmed <sub>meter</sub> were conducted using the UT-278A clamp-on meter attached to the interconnection cable linking each rod to the horizontal electrode. The measurements were compared with simulated readings Zmed <sub>LPM</sub> obtained from the proposed equivalent electrical circuit model. The instrument resolution is 0.1 Ω, and its accuracy is ± (1.0% + 1 dig) for a range from 0.10 − 49.9 Ω. For a range from 50.0 − 99.9 Ω, its resolution is 0.5 Ω, and its accuracy is ± (1.5% + 1 dig).

### Electrical Circuit and Grounding Resistance Calculation

The electrical circuit for the measurements was established and simulated in ATP to acquire the meter readings Zmed<sub>LPM</sub> following the procedures detailed in Section 2.2 of the associated research paper. Furthermore, the lumped parameter modeling used in [our previous work](https://github.com/Alexandregiacomellileal/A-New-Approach-Towards-Error-Reduction-in-Ground-Resistance-Measurements-Based-on-Clamp-on-Method) was also established and simulated in ATP for comparative purposes. The ATP files used by the authors are attached and named **23_model.acp**, **23_model_rod1.acp**, **23_model_rod3.acp**, **celulapi_COMSOL_k_RLC.acp**, **celulapi_COMSOL_k_RLC_rod1.acp**, and **celulapi_COMSOL_k_RLC_rod3.acp**. 

### Measuring Apparent Resistivities

The apparent resistivities of the turbines $\rho_a^{wtg}$ is calculated as follows:

$\ \rho_a^{wtg} = 2 \ \pi \ r_{eq}^{wtg} \ R_{FoP}^{wtg}, \ \Omega \$

Where:
- $R_{FoP}^{wtg}$ represents the grouding resistance mesused by Low-frequency Fall-of_potential Method ($\Omega \cdot \text{m}$)
- $r_{eq}^{wtg}$ is the radius of a semi-spherical electrode with the same ground contact area as the cylinder, i.e., the turbine foundation (m),
 
The apparent resistivity for the cylinder electrodes was estimated at 81.1, 99.3, and 80.1 Ω · m. Correspondingly, the apparent resistivity for the horizontal electrode sections was recorded at 90.2 and 89.7 Ω·m. The electrode’s apparent resistivity values were determined using , incorporating the grounding resistance of the electrodes estimated through the low-frequency FOP method. The equipment used was the digital earth meter MTR-1522. The instrument resolution is 0.01 Ω, and its accuracy is ± (2.0% + 20 dig).


### $k$ Parameter Estimation

As per Section 2.2 of the associated research paper, the parameter $k$ was estimated to be 0.74 for an $s$ value of 0.22 m and 0.90 for an $s$ value of 1.5 m.
The COMSOL models used by the authors are attached and named **rod_1.5_he_k.mph** and **vrod_1.5_two_sphere_k.mph**. The graph below depicts the fluctuation of the parameter $k$ about the increasing distance $s$ between the turbine and the horizontal electrodes.

<img src="https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation/assets/96079504/f3d72683-0fc8-4b29-bddf-039e2b4e0f16" width="400" height="300">

### Results

The obtained results demonstrate a robust agreement, with a Mean Absolute Percentage Error of 1.39 ± 0.12%, between the values registered by the clamp-on meter and those predicted by the proposed equivalent electrical circuit model. It is important to mention that an measurement error propagation study was carried out to address measurement uncertainties.

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

