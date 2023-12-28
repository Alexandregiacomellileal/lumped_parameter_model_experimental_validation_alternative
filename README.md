# lumped_parameter_model_experimental_validation

\appendix
\section{Lumped parameter model experimental validation}
To validate the lumped parameter model introduced in Section \ref{sub: Modeling}, the authors conducted experiments using a scaled-down multi-grounded system, as illustrated in Figure \ref{fig:ablation100}. The constructed grounding system consisted of three 1.5 m rods spaced 7.5 m apart, interconnected to a 15 m horizontal electrode. Each copper rod, symbolizing a turbine grounding, boasted a cross-sectional area of 126 mm², while the copper horizontal electrode had a cross-sectional area of 35 $mm^2$.


The horizontal electrode was buried 0.12 m below the ground. Each rod was positioned on the same side at a distance of $s$ meters from the horizontal electrode. Two different conditions were tested for the variable $s$, specifically at values of 0.22 and 1.5 m. The radial connection between the rods and the horizontal electrode was established using an insulated wire with a cross-sectional area of 10 $mm^2$, with a length of $s$ + 0.1 (m). The soil has an average low-frequency resistivity of 86 $\Omega$.m.

 \begin{figure}[ht]
    \centering
    \includegraphics[width=0.7
    \linewidth]{fig102.pdf}
    \caption{Scaled-down grounding system for experimental validation }
    \label{fig:ablation100}
\end{figure}  


The measurements $Zmed_{meter}$ were conducted using the UT-278A clamp-on meter attached to the interconnection cable linking each rod to the horizontal electrode, resulting in three readings. The instrument resolution is \(0.1 \, \Omega\), and its accuracy is $\pm \ (1.0\% + 1\ dig)$. for a range from \(0.10-49.9 \, \Omega\). For a range from \(50.0-99.9\, \Omega\), its resolution is \(0.5\, \Omega\), and its accuracy is $\pm \ (1.5\% + 1\ dig)$.



The electrical circuit for these measurements was established and simulated to acquire the meter readings $Zmed_{LPM}$ following the procedures detailed in Section \ref{sub: Modeling}. However, a distinction lies in the approach used to calculate the grounding resistance of the rod. The Sunde \cite{ref18} formula best describes scenarios where cylindrical electrodes are vertically installed, particularly when their length significantly exceeds their cross-section. Therefore, the grounding resistance of the rod was calculated as $
R_{rod}= \frac{\rho_a^{rod}}{ 2 \pi l_{rod}} \left [ ln\left (\frac{4l_{rod}}{ a_{rod}} \right ) -1 \right ]$ $(\Omega)$. Here, $\rho_a^{rod}$ represents the apparent resistivity observed by the rod ($\Omega$.m), $l_{rod} $ is the rod's length (m), and $a_{rod}$ is the rod's radius (m). The rod shunt capacitance $C_{rod}$ is calculated using the formula $C_{rod} = \frac{\rho_a^{rod} \ \varepsilon}{R_{rod}}$ (F), where $\varepsilon$ represents the permittivity of the soil, which has been estimated at $7.9686 \times 10^{-11} \, \text{F/m}$. The apparent resistivities $\rho_a^{rod}$ are measured using the driven rod method with the low-frequency Fall-of-Potential method. The equipment used was the digital earth meter MTR-1522. The instrument resolution is \(0.01 \, \Omega\), and its accuracy is $\pm \ (2.0\% + 20 \ dig)$. The apparent resistivity observed by the horizontal electrode is determined by averaging the apparent resistivities observed by the rods and is cross-validated using the Fall-of-Potential method. As per Section \ref{sub:k}, the parameter $k$ was estimated to be 0.74 for an $s$ value of 0.22 m and 0.90 for an $s$ value of 1.5 m. Table \ref{tab:comp10} displays the summarized results of this section.

\begin{table}[!htb]

\centering
\renewcommand{\arraystretch}{0.8} % Adjust the value as needed
\small
\caption{Clamp-on ground meter readings.}
\begin{tabular}{c c c c c c}
\hline
\textbf{$ s\ (m)$} & 
\textbf{$k$} & 
 rod & 
\textbf{$Zmed_{meter} (\Omega)$} & 
\textbf{$Zmed_{LPM} (\Omega)$} & 
\textbf{$APE_{LPM} (\%)$} \\
\hline

 &
  &
1 &
63.5 $\pm$ 1.5 &
64.37 $\pm$ 3.84 &
1.37 $\pm$ 0.09
\\ 

0.22&
0.74&
2 &
46.3 $\pm$ 1.2 &
47.06 $\pm$ 2.86&
1.64 $\pm$ 0.13
\\ 

&
&
3 &
35.5 $\pm$ 0.5 &
35.34 $\pm$ 2.20&
0.45 $\pm$ 0.17
\\ 
\hline

&
&
1 &
72.5 $\pm$ 1.6 &
73.43 $\pm$ 4.35 &
1.28 $\pm$ 0.08
\\ 


1.50&
0.90 &
2 &
56.0 $\pm$ 1.3 &
55.45 $\pm$ 3.34 &
0.98 $\pm$ 0.11
\\ 


&
&
3 &
39.1 $\pm$ 0.5 &
40.12 $\pm$ 2.47&
2.61 $\pm$ 0.15
\\ 
\hline

\end{tabular}
\label{tab:comp10}
\end{table}

%


The obtained results demonstrate a robust agreement, with a Mean Absolute Percentage Error of 1.39 $\pm$ 0.12 \%, between the values registered by the clamp-on meter and those predicted by the proposed equivalent electrical circuit model. This finding serves as validation for our measurement lump parameter model.
