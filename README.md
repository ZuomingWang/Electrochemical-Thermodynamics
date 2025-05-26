# Electrochemical Activity Coefficient Analysis

This report analyzes experimental electrochemical data to determine activity coefficient factors for hydrochloric acid (HCl) in a hydrogen-silver chloride electrochemical cell. The data were sourced from unpublished work by T.F. Young and N. Anderson as cited in Klotz, consisting of potential measurements at 25°C across various HCl concentrations. The electrochemical cell configuration is:

$$H_{2}(g),Pt|HCl(aq)|AgCl(s)|Ag(s)$$

The hydrogen gas pressure was maintained at 1 bar, and both silver (Ag) and silver chloride (AgCl) were pure. Concentrations are expressed as mean ionic molality, defined as:
$m_{\pm}^{HCl} = \sqrt{m_{Cl^-}m_{H^+}}$.  

The purpose of this report is to derive the standard state potential, analyze the activity coefficients using the Debye-Hückel theory, and estimate the activity of a 0.01 molal HCl solution.

## Experimental Data

The experimental data, including mean ionic molality and corresponding cell potentials, are presented below. The total uncertainty in potential measurements is represented by ±5 × 10⁻⁵ V.

| $m_{\pm}^{HCl}$ [mol/kg] | $E$ [V] |
|------------------------|---------|
| 0.0029509 | 0.52456 ± 0.00005 |
| 0.0019461 | 0.54541 |
| 0.0012368 | 0.56813 |
| 0.0008945 | 0.58464 |
| 0.0007303 | 0.59484 |
| 0.0004065 | 0.62451 |
| 0.00022599 | 0.65437 |
| 0.00013528 | 0.68065 |
| 0.00009417 | 0.69914 |
| 0.00006140 | 0.72096 |
| 0.00005392 | 0.72759 |
| 0.000028901 | 0.75955 |

## Theoretical Background

### Cell Reaction and Nernst Equation

The overall reaction for the electrochemical cell is:

$$H_2(g) + 2AgCl(s) \to 2Ag(s) + 2HCl(aq)$$

For this reaction, two electrons are transferred ($n = 2$), and the cell potential is derived using the Nernst equation:

$$E = E^0 - \frac{RT}{nF} \ln Q$$

where the reaction quotient is $Q = (a_{H^+}a_{Cl^-})^2 = (a_{\pm})^4$.

The mean ionic activity is defined as $a_{\pm} = m_{\pm}\gamma_{\pm}$, where $m_{\pm}$ is the mean ionic molality and $\gamma_{\pm}$ is the mean ionic activity coefficient. For a 1:1 electrolyte like HCl, $\gamma_{\pm} = \sqrt{\gamma_+ \gamma_-}$.

Substituting into the Nernst equation:

$$E = E^0 - \frac{RT}{2F}\ln(a_{\pm}^4) = E^0 - \frac{2RT}{F}\ln(a_{\pm})$$

$$E = E^0 - \frac{2RT}{F}\ln(m_{\pm}) - \frac{2RT}{F}\ln(\gamma_{\pm})$$

### Debye-Hückel Theory

The Debye-Hückel limiting law provides an expression for the mean ionic activity coefficient:

$$\log \gamma_{\pm} = -A |z_{+} z_{-}| \sqrt{I}$$

where $A = 0.509 \text{kg}^{1/2} \cdot \text{mol}^{-1/2}$ at 25°C in water. For HCl, $|z_+ z_-| = 1$, and the ionic strength is:

$$I = \frac{1}{2}\sum_i z_i^2 m_i = \frac{1}{2}(1^2 m_{H^+} + 1^2 m_{Cl^-}) = m_{HCl}$$

For the 1:1 electrolyte HCl, the mean ionic molality equals the stoichiometric molality: $m_{\pm} = m_{HCl}$. Therefore, the ionic strength is:

$$I = m_{\pm}$$

Substituting into the Debye-Hückel expression:

$$\log \gamma_{\pm} = -0.509 \sqrt{m_{\pm}}$$

### Derivation of Linear Relationship

Rearranging the Nernst equation and converting natural logarithms to base-10:

$$E + \frac{2RT}{F} \ln(m_{\pm}) = E^0 - \frac{2RT}{F} \ln(\gamma_{\pm})$$

Converting to base-10 logarithms using $\ln(x) = \ln(10) \log(x) = 2.303 \log(x)$:

$$E + \frac{2RT}{F} \ln(10) \log(m_{\pm}) = E^0 - \frac{2RT}{F} \ln(10) \log(\gamma_{\pm})$$

Substituting the Debye-Hückel expression:

$$E + \frac{2RT \ln(10)}{F} \log(m_{\pm}) = E^0 + \frac{2RT \ln(10)}{F} \cdot 0.509 \sqrt{m_{\pm}}$$

This yields the linear relationship:

$$E + \frac{2RT \ln(10)}{F} \log(m_{\pm}) = E^0 + a \sqrt{m_{\pm}}$$

where the theoretical slope is:
$$a_{theory} = \frac{2RT \ln(10)}{F} \cdot 0.509$$

At 25°C, $\frac{RT}{F} = 0.02569 \text{V}$, so:
$$a_{theory} = 2 \times 0.02569 \times 2.303 \times 0.509 = 0.0601 \text{ V} \cdot \text{kg}^{1/2} \cdot \text{mol}^{-1/2}$$

## Data Analysis

### Determination of Standard Potential

The experimental data were plotted as $E + \frac{2RT \ln(10)}{F} \log(m_{\pm})$ versus $\sqrt{m_{\pm}}$. 
![1](https://github.com/user-attachments/assets/f612c83e-4c72-4163-acff-ab8566e576b4)

Linear regression yielded:

- **Standard state potential**: $$E^0 = 0.2220 \text{V}$$
- **Experimental slope**: $$a_{exp} = 0.056 \text{V}\cdot\text{kg}^{1/2}\cdot\text{mol}^{-1/2}$$

The experimental slope is approximately 7% lower than the theoretical Debye-Hückel prediction, indicating deviations from ideal behavior at higher concentrations.

### Comparison with Debye-Hückel Model

Using $E^0 = 0.2220$ V, the theoretical curve based on pure Debye-Hückel theory was compared with experimental data, revealing systematic deviations that increase with concentration.
![2](https://github.com/user-attachments/assets/9742fe1e-faec-4eaf-9cad-26d21ba12eeb)

## Activity Coefficient Calculation

### Analytical Expression for $\log \gamma_{\pm}$

From the experimental slope ($a_{exp} = 0.056 \text{V} \cdot \text{kg}^{1/2} \cdot \text{mol}^{-1/2}$):

$$E + \frac{2RT \ln(10)}{F} \log(m_{\pm}) = E^0 + 0.056 \sqrt{m_{\pm}}$$

Relating this to the Nernst equation:

$$\log \gamma_{\pm} = -\frac{F \cdot a_{exp}}{2RT \ln(10)} \sqrt{m_{\pm}}$$

![3](https://github.com/user-attachments/assets/388a7c43-cb18-407a-ad8a-85714d2b8de4)

At 25°C, $\frac{F}{2RT \ln(10)} = 8.465 \text{V}^{-1}$, so:

$$\log \gamma_{\pm} = -0.4739 \sqrt{m_{\pm}}$$

### Activity of a 0.01 Molal Solution

For $m_{\pm} = 0.01$ mol/kg:

$$\log \gamma_{\pm} = -0.4739 \times \sqrt{0.01} = -0.04739$$

$$\gamma_{\pm} = 10^{-0.04739} = 0.896$$

The mean ionic activity relative to the unit molality standard state is:

$$a_{\pm} = m_{\pm} \gamma_{\pm} = 0.01 \times 0.896 = 0.00896$$

## Error Analysis

The uncertainty in cell potential (±5 × 10⁻⁵ V) propagates through the linear regression analysis. The uncertainty in $E^0$ is approximately ±0.002 V, and the uncertainty in the activity coefficient at 0.01 molal is approximately ±0.01, giving $\gamma_{\pm} = 0.896 ± 0.01$.

## Conclusion

This analysis determined the standard state potential as $E^0 = 0.2220 ± 0.002 \text{V}$ and derived an empirical activity coefficient expression $\log \gamma_{\pm} = -0.4739 \sqrt{m_{\pm}}$ that deviates from pure Debye-Hückel theory. The experimental slope of $0.056 \text{V} \cdot \text{kg}^{1/2} \cdot \text{mol}^{-1/2}$ is 7% lower than the theoretical prediction of $0.0601 \text{V} \cdot \text{kg}^{1/2} \cdot \text{mol}^{-1/2}$, likely due to ion-ion interactions not accounted for in the limiting law.

The estimated mean ionic activity of a 0.01 molal HCl solution is $a_{\pm} = 0.00896 ± 0.00009$, demonstrating deviation from ideal behavior even at relatively low concentrations. This deviation emphasizes the importance of activity coefficients in accurate thermodynamic calculations for electrolyte solutions.

## References

Klotz, I. M. *Chemical Thermodynamics*. (Publication details unavailable).

Young, T. F., & Anderson, N. Unpublished electrochemical data, as cited in Klotz, I. M. *Chemical Thermodynamics*.
