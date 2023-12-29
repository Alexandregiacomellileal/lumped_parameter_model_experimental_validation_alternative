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

The electrical circuit for the measurements was established and simulated in ATP to acquire the meter readings Zmed<sub>LPM</sub> following the procedures detailed in Section 2.2 of the associated research paper. Furthermore, the lumped parameter modeling used in [our previous work](https://github.com/Alexandregiacomellileal/A-New-Approach-Towards-Error-Reduction-in-Ground-Resistance-Measurements-Based-on-Clamp-on-Method) [^1] was also established and simulated in ATP for comparative purposes. The ATP files used by the authors are attached and named **23_model.acp**, **23_model_rod1.acp**, **23_model_rod3.acp**, **celulapi_COMSOL_k_RLC.acp**, **celulapi_COMSOL_k_RLC_rod1.acp**, and **celulapi_COMSOL_k_RLC_rod3.acp**. 

### Measuring Apparent Resistivities

The apparent resistivity ($\rho_a^{wtg}$) of the turbines is computed using the formula $\ \rho_a^{wtg} = 2 \ \pi \ r_{eq}^{wtg} \ R_{FoP}^{wtg} \ (\Omega) $, where $R_{FoP}^{wtg}$ represents the grounding resistance measured by the Low-frequency Fall-of-Potential Method ($\Omega \cdot \text{m}$), and $r_{eq}^{wtg}$ is the radius of a semi-spherical electrode with an equivalent ground contact area as the turbine foundation (m).

The apparent resistivity observed by the horizontal electrode is determined by averaging the apparent resistivities of the turbines in their extremities, and this is cross-validated using the Low-frequency Fall-of-Potential method.

In this study, the apparent resistivity for the cylinder electrodes was determined to be 81.1, 99.3, and 80.1 Ω·m, while the apparent resistivity for the horizontal electrode sections was recorded at 90.2 and 89.7 Ω·m. The measurements were conducted using the digital earth meter MTR-1522, which has a resolution of 0.01 Ω and an accuracy of ± (2.0% + 20 digits).


### $k$ Parameter Estimation

The electrical circuit for these measurements was established and simulated to acquire the meter readings $Zmed_{\text{LPM}}$ following the procedures detailed in Section 2.2. the parameter k was estimated to be 0.69 for an s value of 28.5 cm. The COMSOL models used by the authors are attached and named **rod_1.5_he_k.mph** and **vrod_1.5_two_sphere_k.mph**. The graph below depicts the fluctuation of the parameter $k$ about the increasing distance $s$ between the turbine and the horizontal electrodes.

### Results

The obtained results demonstrate a robust agreement, with a Mean Absolute Percentage Error of of 1.75 ± 0.20 %, between the values registered by the clamp-on meter and those predicted by the proposed equivalent electrical circuit model. It is important to mention that an measurement error propagation study was carried out to address measurement uncertainties.

### Table of Results

# Comparison between modeling and measurement results

| Turbine                           | 1      | 2      | 3      |
|-----------------------------------|--------|--------|--------|
| $Zmed_{{\text{meter}}} UT278A (\Omega)$ | 37.8   | 40.5   | 37.5   |
| $Zmed_{{\text{EFM}}} (\Omega)$ COMSOL | 38.18  | 41.04  | 37.71  |
| $Zmed_{{\text{LPM}}} (\Omega)$ [^1]| 46.90  | 55.69  | 46.41  |
| $Zmed_{{\text{LPM}}}(\Omega)$  proposed | 38.50  | 41.22  | 38.10  |
| $APE_{\text{EFM}}(percent)$ COMSOL           | 1.01   | 1.33   | 0.56   |
| $APE_{\text{LPM}}(percent)$ [^1] | 24.08  | 37.52  | 23.77  |
| $APE_{\text{LPM}}(percent)$  proposed| 1.85   | 1.79   | 1.60   |

[^1]: A.G. Leal, H.L. L ́opez-Salamanca, A.E. Lazzaretti, D.C. Marcilio, A new approach for ground resistance measurements in onshore wind farms based on clamp-on meters and artificial neural network, Electric Power Systems Research. 210 (2022) 108161.


# Clamp-on meter readings - Final results including measurement error propagation study

| Turbine | $Zmed_{{\text{meter}}} (\Omega)$ | $Zmed_{{\text{LPM}}} (\Omega)$ | $APE_{\text{LPM}} (percent)$ |
|---------|---------------------------------|--------------------------------------|----------------------------|
| 1       | 37.8 $\pm$ 0.5                 | 38.50 $\pm$ 3.28                     | 1.85 $\pm$ 0.21            |
| 2       | 40.5 $\pm$ 0.5                 | 41.22 $\pm$ 3.50                     | 1.79 $\pm$ 0.19            |
| 3       | 37.5 $\pm$ 0.5                 | 38.10 $\pm$ 3.25                     | 1.60 $\pm$ 0.21            |


### Conclusion

The results serve as validation for the proposed lumped parameter model, with a strong agreement between experimental and simulated data.

