- 04-01-25 01:11
- Sources: [[Convex Optimisation - Stephen Boyd and Lieven Vandenberghe|Convex Optimisation - Stephen Boyd and Lieven Vandenberghe]]
- Links: [[Linear Programming]], [[Nonlinear Programming]], [[Convex Optimisation]], [[Mathematics]]
---
## An optimisation problem has the general form:
$$ 
	\begin{aligned} 
		& \text{minimize} & \quad f_0(x) \\ 
		& \text{subject to} & \quad f_i(x) \leq b_i, \, i = 1, \dots, m. 
	\end{aligned} 
$$**Where**:
- $x = (x_1, \dots, x_n): \text{Optimization variable.}$
- $f_0 : \mathbb{R}^n \to \mathbb{R}: \text{Objective function.}$
- $f_i : \mathbb{R}^n \to \mathbb{R}, \, i = 1, \dots, m: \text{Constraint functions.}$ 
- $b_1, \dots, b_m: \text{Bounds for constraints.}$ 

A vector $( x^\ast )$ is **optimal** if: 
$$ 
	\begin{gathered} 
		f_0(z) \geq f_0(x^\ast)\text{ for all } z \text{ with }f_i(z) \leq b_i, \, i = 1, \dots, m. 
	\end{gathered} 
$$
---
## Types of Problems 
### 1. [[Linear Programming]] Objective and constraint functions are linear:
$$ 
	\begin{gathered}
		& f_i(\alpha x + \beta y) = \alpha f_i(x) + \beta f_i(y), \\
		& \text{for all } x,\ y \in \mathbb{R}^n,\ \text{and all } \alpha, \ \beta \in \mathbb{R}.
	\end{gathered} 
$$
### 2. [[Convex Optimisation]] or [[Nonlinear Programming]]
Objective and constraints are convex:
$$ 
	\begin{gathered}
		& f_i(\alpha x + \beta y) = \alpha f_i(x) + \beta f_i(y), \\
		& \text{for all } x,\ y \in \mathbb{R}^n,\ \text{and all } \alpha + \beta = 1, \ \alpha, \ \beta \geq 0.
	\end{gathered} 
$$
- **Convexity** generalises linearity by relaxing equality to inequality.
---
## Applications
### Portfolio Optimisation
   - **Variable** $(x_i)$: Investment in asset $(i)$.  
   - **Constraints**: 
$$ 
	\begin{aligned} 
		& \text{Budget limits: } & \sum_{i=1}^n x_i \leq \text{total budget}, \\ 
		& \text{Nonnegativity: } & x_i \geq 0, \, \text{for all } i, \\ 
		& \text{Minimum expected return: } & \sum_{i=1}^n r_i x_i \geq R_{\text{min}}. 
	\end{aligned} 
$$
- **Objective**: Minimise risk, e.g., portfolio return variance: 
$$ 
	\text{minimise } \text{Var}(\text{portfolio return}). 
$$
### Device Sizing in Electronics 
- **Variable**: Widths and lengths of devices.
- **Constraints**: 
$$ 
	\begin{aligned} 
		& \text{Manufacturing limits: } & w_{\text{min}} \leq w_i \leq w_{\text{max}}, \\ 
		& \text{Timing requirements: } & \text{circuit timing constraints}, \\ 
		& \text{Area limit: } & \sum w_i \cdot l_i \leq A_{\text{max}}.
	\end{aligned} 
$$
- **Objective**: Minimise total power consumption:
$$
	\text{minimise } P_{\text{total}}.
$$
### Data Fitting 
- **Variable**: Model parameters $(x)$. 
- **Constraints**: 
$$
	x \geq 0 \quad \text{(nonnegativity or prior information)}.
$$
- **Objective**: Minimise misfit or prediction error: 
$$ 
	\text{minimise } \| \text{observed data} - \text{predicted data} \|. 
$$