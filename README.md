## Tensile Stress-Strain Curve Analysis for 3D-Printed Polymers
*Code written by Francis Sanguyo*

*Date: April 21-28, 2026*

*MATSE 121.02 LAB Post-Lab 5*

*Mechanical Properties of 3D-Printed Poly(Lactic Acid) (PLA), Poly(Ethylene Terephthalate) Glycol (PETG), and Thermoplastic Polyurethane (TPU) Under Tensile Loading*


**Outline:**



1. Import packages

2. Read the CSV data files
 - Remove the final few entries of each stress and strain list as these entries occur after slippage of grips or fracture of the material.

3. Calculate the stress-strain curve (engineering and true values) for each material.

 - 3.1 Calculate the cross-sectional area of each material.

$(Area) = (thickness) \times (width)$

 - 3.2 Compute the engineering stress and strain.

$\sigma = \dfrac{F}{A_0}, \qquad A_0 = \text{initial cross-sectional area}$

$\varepsilon = \dfrac{\Delta L}{L_0}, \qquad L_0 = \text{initial length}$

 - 3.3 Compute the true stress and strain

$\varepsilon_T = \ln(1 + \varepsilon)$

$\sigma_T = \sigma(1 + \varepsilon)$

4. Plot the stress-strain curves of the materials tested

 - 4.1 Provide initial plots of the engineering stress-strain curves.

 - 4.2 Provide initial plots for the true stress-strain curves.

 - 4.3. Save the engineering and true stress and strain values per material as CSV files.


5. Compute the different mechanical properties ($E$, $\sigma_Y$, $\sigma_{UTS}$, $\sigma_F$, $\% EL%$, $U_r$ and $U_t$) of the polymer samples based on the engineering stress-strain curves.

 - 5.1. Using linear regression and 0.2% method, get the elastic and plastic regions of each curve.

 - 5.2. From the elastic region, obtain the elastic modulus ($E$), yield strength ($\sigma_Y$), and modulus of resilience ($U_r$) of each material.

*For each engineering stress-strain curve, determine the first equation of the line σ = A + Bε (A = intercept, B = slope) which closely fits all the points in between of these boundaries.*

*For the 0.2% method, get the second equation of the line σ = A + B(ε - 0.002), or more simply  σ = (A - 0.002B) + Bε or just σ = C + Dε which has been translated to the right by 2% strain.*

*Then using linear interpolation find the strain εY around the end of the linear region (within 20%) where the difference function D(ε) = becomes zero and switches signs*

 - 5.3. Find the peak(s) and fracture point of each curve within the plastic region of each curve.

 - 5.4. From the plastic region, obtain the ultimate tensile strength ($\sigma_{UTS}$), fracture strength ($\sigma_F$), percent elongation ($\%EL$), and toughness ($U_t$) of each material.

 - 5.5 - Special: Compute the True Stress for Zero Plastic Strain

 - 5.6. Save the computed mechanical properties of each polymer to a CSV file.


6. Model the elastic and early plastic region of each engineering stress-strain curve using the Ramberg-Osgood equation.

$\varepsilon = \varepsilon_E + \varepsilon_P$

$\varepsilon = \dfrac{\sigma}{E} + K(\dfrac{\sigma}{E})^{n}$

 - 6.1. Get the Ramberg-Osgood parameters $K$ and $n$ which best fit the elastic and early plastic regions.

 - 6.2. Plot the predicted values of the Ramberg-Osgood equation alongside the engineering stress-strain plots

 - 6.3. Save data on the Ramberg-Osgood equation to a CSV file.
