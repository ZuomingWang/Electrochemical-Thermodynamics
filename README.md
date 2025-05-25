# Electrochemical-Thermodynamics
# Electrochemical Activity Coefficient Analysis
This is an example of analysis of experimental electrochemical data to determine the activity coefficient factors. 
(Based on Klotz) T.F. Young and N. Anderson (unpublished) measured the potentials of a

$$H_{2}(g),Pt|HCl(aq)|AgCl(s)|Ag(s)$$

cell at 25°C as a function of HCl concentrations; H₂ pressure was 1 bar and the Ag and AgCl were pure. HCl(aq) concentrations were reported as mean ionic molality where
$m_{±}^{HCl} = \sqrt{m_{Cl^-}m_{H^+}}$.


| $m_{±}^{HCl}$ \, $[\text{mol/kg}]$ | $\mathcal{E} \, [\text{V}]$ |
|-------------------------------------|-------------------------------|
| 0.0029509                           | 0.52456 ± 0.00005            |
| 0.0019461                           | 0.54541                      |
| 0.0012368                           | 0.56813                      |
| 0.0008945                           | 0.58464                      |
| 0.0007303                           | 0.59484                      |
| 0.0004065                           | 0.62451                      |
| 0.00022599                          | 0.65437                      |
| 0.00013528                          | 0.68065                      |
| 0.00009417                          | 0.69914                      |
| 0.00006140                          | 0.72096                      |
| 0.00005392                          | 0.72759                      |
| 0.000028901                         | 0.75955                      |


The total uncertainty in concentration and potential is included in the $±5 \times 10^{-5}$ V potential uncertainty.

---


**(a)**

Write the underlying reaction for this electrochemical cell and show that the measured potential in this system should be given as:

$$
\mathcal{E} = \mathcal{E}^0 - \frac{2RT}{\mathcal{F}} \ln m_{±} - \frac{2RT}{\mathcal{F}} \ln \gamma_{±}
$$

where $m_{±}$ and $\gamma_{±}$ refer to the aqueous HCl.  
**Answer for (a)**\
Overall reaction:

$$
H_2(g) + 2AgCl(s) \to 2Ag(s) + 2HCl(aq).
$$

Apply Nernst equation:

$$
\mathcal{E} = \mathcal{E}^0 + \frac{RT}{z\mathcal{F}} \ln Q.
$$

Here, $z=-2$ and $Q = (a_{H^+}a_{Cl^-})^2 = (a_{\pm}^2)^2 = a_{\pm}^4$. Thus:

$$
\mathcal{E} = \mathcal{E}^0 - \frac{RT}{2\mathcal{F}}\ln(a_{\pm}^4) = \mathcal{E}^0 - 2\frac{RT}{\mathcal{F}}\ln(a_{\pm}).
$$

Since $a_{\pm} = m_{\pm}\gamma_{\pm}$:

$$
\mathcal{E} = \mathcal{E}^0 - 2\frac{RT}{\mathcal{F}}\ln(m_{\pm}) - 2\frac{RT}{\mathcal{F}}\ln(\gamma_{\pm}).
$$

-->

$$
\boxed{\mathcal{E} = \mathcal{E}^0 - \frac{2RT}{\mathcal{F}} \ln m_{±} - \frac{2RT}{\mathcal{F}} \ln \gamma_{±}}
$$

---
**(b)**

The standard state electrochemical potential can be determined by correcting the measured potential by the known molality and extrapolating to zero concentration where $\gamma_{±} = 1$. In the limiting form of the Debye-Hückel theory, the mean ionic activity coefficient is given as:

$$
\log \gamma_{±} = -0.509 |z_{+} z_{-}| \sqrt{I}, 
$$

where $I$ (also known as $\mu$) is the total ionic strength and is **directly proportional to $m_{±}$**. Show that this suggests that the data should follow a form (where $a$ is a constant):

$$
\mathcal{E} + \frac{2RT}{\mathcal{F}} \log m_{±} = \mathcal{E}^0 + a \sqrt{m_{±}}
$$

**Answer for (b)**\
Given:

$$
\log \gamma_{±} = -0.509 |z_{+} z_{-}| \sqrt{I},
$$

For HCl, $|z_+ z_-| = 1$. \
The ionic strength is proportional to the molality of the salt:

$$
I = k \, m_{±},
$$

where $k$ is a constant of proportionality. Thus:

$$
\log \gamma_{±} = -0.509 \sqrt{k \, m_{±}}.
$$

Define constant $b = -0.509\sqrt{k}$:

$$
\log \gamma_{±} = b\sqrt{m_{±}},
$$

where $b < 0$.
Substitute:

$$
\mathcal{E} = \mathcal{E}^0 - \frac{2RT}{\mathcal{F}}\ln m_{±} - \frac{2RT}{\mathcal{F}}(b\sqrt{m_{±}})\,ln(10).
$$

-->

$$
\mathcal{E} + \frac{2RT}{\mathcal{F}}\ln m_{±} = \mathcal{E}^0 - \frac{2ln(10)RT}{\mathcal{F}}b\sqrt{m_{±}}.
$$

Define a constant $a = -\frac{2ln(10)RT}{\mathcal{F}}b$. Since $b$ was a constant that depends only on known parameters, $a$ is also a constant.
Therefore,

$$
\boxed{\mathcal{E} + \frac{2RT}{\mathcal{F}}\log m_{±} = \mathcal{E}^0 + a\sqrt{m_{±}}.}
$$

---
**(c)**

Show that the constant $a$ would equal $0.0602$ if the Debye-Hückel model were correct.  
**Answer for (c)**\
Let the ionic strength $I$ for HCl equal to its molality (assuming ideal behavior at infinite dilution):

$$
I = m_{±}.
$$

From (b), we have: 

$$
a = -\frac{2ln(10)RT}{\mathcal{F}}b,
$$

where $b = -0.509\sqrt{k}=-0.509$. (since $I = k \, m_{±}$).\
Thus:

$$
a = -\frac{2ln(10)RT}{\mathcal{F}}(-0.509)\approx0.06019
$$

Therefore, if the Debye-Hückel model were correct, then the derived constant $a$ would be:

$$
\boxed{a \approx 0.0602.}
$$

---
**(d)**

Plot the experimental data in the form 

 $\mathcal{E} + \frac{2RT}{\mathcal{F}} \ln m_{±}$ 
 
as a function of the square root of the mean ionic molality $(\sqrt{m_{±}})$ and determine the standard state electrochemical potential of this cell  $\mathcal{E}^0$  and the constant $a$.

**Answer for (d)**
![image](https://github.com/user-attachments/assets/1f63be61-07fd-4826-89f0-a626c8f5b842)
From the linear fit:
The standard state electrochemical potential $\mathcal{E}^0$ is approximately **0.222 V**.
The constant $a$ is approximately **0.056**.

---
**(e)**

On the same graph, draw the curve corresponding to the limiting form of the Debye-Hückel theory (given above). For Debye-Hückel, use the approximation $I = m_{±}$, and your experimentally determined value of $\mathcal{E}^0$.  
**Answer for (e)**
![image](https://github.com/user-attachments/assets/82ef8aae-4b3e-4fab-b977-7da2a2365a88)
**(f)**

From the value of the parameter $a$, obtain an analytical expression for $\log \gamma_{±}$ in this system (will look much like Debye-Hückel but with a slightly different constant and without the total ionic strength).  
**Answer for (f):**\
Given $a = 0.056$, and from **(a)**:

$$
\mathcal{E} + \frac{2RT}{\mathcal{F}}\log m_{±} = \mathcal{E}^0 + a\sqrt{m_{±}}.
$$

From the fundamental:

$$
\mathcal{E} = \mathcal{E}^0 - \frac{2RT}{\mathcal{F}} \ln m_{±} - \frac{2RT}{\mathcal{F}} \ln \gamma_{±}.
$$

Therefore,

$$
\log\gamma_{±} = -\frac{F a}{2RT \ln(10)} \sqrt{m_{±}}.
$$

-->

$$
\boxed{\log\gamma_{±} = -\frac{0.056F}{2RT \ln(10)} \sqrt{m_{±}}.}
$$

---
**(g)**

Plot the mean ionic activity coefficient $\gamma_{±}$ as a function of the log of the molality from $10^{-4}$ to $10^{-1}$ molal on log-linear axes. Compare with the Debye-Hückel model by overlaying the result expected from Debye-Hückel.  
**Answer for (g)**
![image](https://github.com/user-attachments/assets/dc127d75-bd3f-415f-afc1-1d8d987915e7)

**(h)**

What is the estimated activity of a 0.01 molal solution ($m_{±} = 0.01$) relative to the unit molality Henrien standard state?  
**Answer for (h)**

From **(g)**:

$$
\log\gamma_{±} = -\frac{F a}{2RT \ln(10)}\sqrt{m_{±}} = -\frac{0.056F}{2RT \ln(10)} \sqrt{m_{±}}.
$$

At the given conditions,
the coefficient: $$\frac{F a}{2RT\ln(10)} \approx 0.4739.$$
Thus, 

$$
\log\gamma_{±} = -0.4739 \cdot \sqrt{0.01} = -0.4739 \cdot 0.1 = -0.04739.
$$

-->

$$\gamma_{±} = 10^{-0.04739} \approx 0.896.$$

Therefore, the activity:

$$
a = (0.01)(0.896) = 0.00896 \approx 0.009.
$$

$$
\boxed{a \approx 0.009}.
$$
