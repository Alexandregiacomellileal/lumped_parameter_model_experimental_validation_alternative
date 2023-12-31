## Lumped Parameter Model Experimental Validation - Reduced Scale

<img width="935" alt="image" src="https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/assets/96079504/65399b18-67e1-4f0a-b62e-33b8e6a44171">


### Overview

This repository contains the experimental validation details for the lumped parameter model introduced in Section 2.2 of the associated research paper. The validation experiments were conducted using a scaled-down multi-grounded system, as described below.

[[23_model_rod1.acp](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/blob/main/23_model_rod1.acp)]

[[23_model.acp](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/blob/main/23_model.acp)]

[[23_model_rod3.acp] 
(https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/blob/main/23_model_rod3.acp)]

https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/blob/main/celulapi_COMSOL_k_RLC.acp

https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/blob/main/celulapi_COMSOL_k_RLC_rod1.acp

https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/blob/main/celulapi_COMSOL_k_RLC_rod3.acp






### Experimental Setup

The proposed lumped parameter model underwent experimental validation using a reduced-scale model of the grounding system detailed in Section 2.2 of the associated research paper. The grounding system was constructed with three 4 mm thick steel cylinders spaced 7.5 m apart, interconnected to a 15 m horizontal electrode. Each steel cylinder, symbolizing a turbine grounding, boasted a radius of 19.7 cm and a height of 43 cm, while the copper horizontal electrode had a cross-sectional area of 35 $mm^2$. The horizontal electrode was buried 12 cm below the ground. Each cylinder electrode was positioned on the same side at a distance of 28.5 cm from the horizontal electrode. The radial connection between the cylinder and horizontal electrodes was established using an insulated wire with a cross-sectional area of 10 $mm^2$, with a length of $s$ + 0.1 $(m)$. The soil had an average low-frequency resistivity of 86.8 Ω·m.  In Figure 1, the schematic of the grounding system is presented, capturing key moments during both its construction and the measurement process.

**Figure 1**
![experiment_git_hub (003)](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/assets/96079504/770ea421-a751-4447-ad05-807e82ab4ac5)

### Measurements clamp-on ground meter

Measurements Zmed <sub>meter</sub> were conducted using the UT-278A clamp-on meter attached to the interconnection cable linking each cylinder (representing the turbine grounding) to the horizontal electrode. The measurements were compared with simulated readings Zmed <sub>LPM</sub> obtained from the proposed equivalent electrical circuit model. The instrument resolution is 0.1 Ω, and its accuracy is ± (1.0% + 1 dig) for a range from 0.10 − 49.9 Ω. For a range from 50.0 − 99.9 Ω, its resolution is 0.5 Ω, and its accuracy is ± (1.5% + 1 dig).

### Electrical Circuit and Grounding Resistance Calculation

The electrical circuit for the measurements was established and simulated in ATP to acquire the meter readings Zmed<sub>LPM</sub> following the procedures detailed in Section 2.2 of the associated research paper. Furthermore, the lumped parameter modeling used in [our previous work](https://github.com/Alexandregiacomellileal/A-New-Approach-Towards-Error-Reduction-in-Ground-Resistance-Measurements-Based-on-Clamp-on-Method) [^1] was also established and simulated in ATP for comparative purposes. The ATP files used by the authors are attached and named *23_model.acp*, *23_model_rod1.acp*, *23_model_rod3.acp*, *celulapi_COMSOL_k_RLC.acp**, *celulapi_COMSOL_k_RLC_rod1.acp*, and *celulapi_COMSOL_k_RLC_rod3.acp*. 

### Measuring Apparent Resistivities

The apparent resistivity ($\rho_a^{wtg}$) of the turbines is computed using the formula $\ \rho_a^{wtg} = 2 \ \pi \ r_{eq}^{wtg} \ R_{FoP}^{wtg} \ (\Omega.m) $, where $R_{FoP}^{wtg}$ represents the grounding resistance measured by the low-frequency Fall-of-Potential Method ($\Omega$), and $r_{eq}^{wtg}$ is the radius of a semi-spherical electrode with an equivalent ground contact area as the turbine foundation (m).

The apparent resistivity ($\rho_a^{he}$) observed by the horizontal electrode is determined by averaging the apparent resistivities ($\rho_a^{wtg}$) of the turbines in their extremities, and this is cross-validated using the low-frequency Fall-of-Potential method.

In this study, the apparent resistivity for the cylinder electrodes was determined to be 81.1, 99.3, and 80.1 Ω·m, while the apparent resistivity for the horizontal electrode sections was recorded at 90.2 and 89.7 Ω·m. The measurements were conducted using the digital earth meter MTR-1522, which has a resolution of 0.01 Ω and an accuracy of ± (2.0% + 20 digits).


### $k$ Parameter Estimation

In our quest to mitigate the impact of mutual coupling in measurements and address distortions arising from the utilization of an equivalent semi-spherical representation of the horizontal electrode, we are engaged in refining the estimation process. Our focus is on enhancing accuracy and reliability by systematically assessing and adjusting the parameters involved in the measurement system.

According to Section 3.1 of the associated research article, the parameter k was estimated to be 0.69 for an s value of 28.5 cm. The COMSOL models for k estimation are attached and named *turbine_he_k.mph* and *turbine_two_sphere_k.mph*. Figure 2 displays images generated through the COMSOL Multiphysics computer simulation software. The framed image above the Figure 2 is associated with the estimation of $Zmed_{lumped}^{short} (\Omega)$ using the COMSOL model *turbine_two_sphere_k.mph*, while the one below is related to the estimation of $Zmed_{wire}^\infty (\Omega)$ using *turbine_he_k.mph*. 

**Figure 2**
![COMSOL_top](https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/assets/96079504/511ee963-843b-4130-85e0-bb90eaf88c03)

$Zmed_{wire}^\infty (\Omega)$ is the clamp-on reading taken with the turbine grounding and the horizontal electrode separated by a large distance, in a such way that the mutual couplings between these elements can be considered negligible. On the other hand, the $Zmed_{lumped}^{short} (\Omega)$ is the clamp-on reading taken with the turbine grounding and the horizontal electrode separated by a smaller distance $s$ and with the horizontal electrode being represented by two semi-spherical electrodes spaced so that one does not be influenced by the other. For a single lumped parameter cell representing the horizontal electrode, each semi-spherical electrode must have twice its grounding resistance. 

Table 1 displays results obtained at an average soil resistivity of 86.8 $(\Omega.m)$. Notably, the COMSOL simulation results reveal that the parameter $k$ remains consistent for a specified value of $s$ across a wide range of soil resistivities, spanning from 20 to 10240 $(\Omega.m)$.

**Table 1**
| $s \ (m)$ | $\rho \ (\Omega.m)$| ${Zmed}_{lumped}^{short} (\Omega) $ | ${Zmed}_{wire}^\infty (\Omega)$| $k$             |
|---------|---------|------------------------|-----------------------|-----------------|
| 0.285   | 86.8  | 41.624                 | 60.625                | 0.687     |

In instances where simulation software is unavailable for researching the parameter $k$ in the measuring circuit, the attached graph of Figure 3 serves as a valuable tool for estimating it according to the distance $s$ between the grounding elements. This estimate is particularly relevant in cases where the grounding configuration involves reduced-scale 1:40 cylindrical-shaped turbine foundations with multiple driven pillars, constructed of reinforced concrete, and horizontal electrodes.

**Figure 3**                   

<img src="https://github.com/Alexandregiacomellileal/lumped_parameter_model_experimental_validation_alternative/assets/96079504/abe2c145-1357-4577-b243-e09fb58d44f7" width="500" height="375">

### Results

All simulation input parameters for every ground resistance measurement circuit, along with their corresponding results, are accessible in the Excel file named *reduce_scale_251223.xlsx*. The obtained results demonstrate a robust agreement, with a Mean Absolute Percentage Error of of (1.75 ± 0.20) %, between the values registered by the clamp-on meter and those predicted by the proposed equivalent electrical circuit model. It is important to mention that an error propagation study was carried out to address measurement uncertainties. 

### Table of Results

#### Table 2 - Comparison between modeling and measurement results

| Turbine                           | 1      | 2      | 3      |
|-----------------------------------|--------|--------|--------|
| $Zmed_{{\text{meter}}} (\Omega)$ UT278A | 37.8   | 40.5   | 37.5   |
| $Zmed_{{\text{EFM}}} (\Omega)$ COMSOL| 38.18  | 41.04  | 37.71  |
| $Zmed_{{\text{LPM}}} (\Omega)$ [^1]| 46.90  | 55.69  | 46.41  |
| $Zmed_{{\text{LPM}}}(\Omega)$  proposed | 38.50  | 41.22  | 38.10  |
| $APE_{\text{EFM}}(percent)$ COMSOL   | 1.01   | 1.33   | 0.56   |
| $APE_{\text{LPM}}(percent)$ [^1] | 24.08  | 37.52  | 23.77  |
| $APE_{\text{LPM}}(percent)$  proposed| 1.85   | 1.79   | 1.60   |

[^1]: A.G. Leal, H.L. L ́opez-Salamanca, A.E. Lazzaretti, D.C. Marcilio, A new approach for ground resistance measurements in onshore wind farms based on clamp-on meters and artificial neural network, Electric Power Systems Research. 210 (2022) 108161.


#### Table 3 - Clamp-on meter readings - Final results including measurement error propagation study

| Turbine | $Zmed_{{\text{meter}}} (\Omega)$ | $Zmed_{{\text{LPM}}} (\Omega)$ | $APE_{\text{LPM}} (percent)$ |
|---------|---------------------------------|--------------------------------------|----------------------------|
| 1       | 37.8 $\pm$ 0.5                 | 38.50 $\pm$ 3.28                     | 1.85 $\pm$ 0.21            |
| 2       | 40.5 $\pm$ 0.5                 | 41.22 $\pm$ 3.50                     | 1.79 $\pm$ 0.19            |
| 3       | 37.5 $\pm$ 0.5                 | 38.10 $\pm$ 3.25                     | 1.60 $\pm$ 0.21            |


### Conclusion

The results serve as validation for the proposed lumped parameter model, with a strong agreement between experimental and simulated data.

