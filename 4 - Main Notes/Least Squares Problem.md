- 19-01-25 16:15
- Sources: [[Convex Optimisation - Stephen Boyd and Lieven Vandenberghe]]
- Links: [[Least Squares]], [[Mathematics]]
---
## Solving the Least Squares Problems

> [!faq] **What is a [[Least Squares]] Problem?**
> A **least squares** problem is an optimisation problem with no constraints ($\text{i.e.}, m = 0$) and an objective which is a sum of squares of terms of the form $a^T_ix-b_i$: $$\text{minimise } f_0(x) = \|Ax - b\|_2^2 = \sum_{i=1}^k (a_i^T x - b_i)^2$$
> Here $A \in \mathbb{R}^{k \times n}\ \ (\text{with } k \geq n),\ \ a_i^T$ are the rows of $A$, and the vector $x \in \mathbb{R}^n$ is the optimisation variable.
> 
>*more simply, **least squares problem** minimises the sum of the squared differences between a model's predictions and the observed data.*
### Analytical Solution

The least square problem can be expressed as solving linear equations:
$$(A^TA)x=A^Tb \ \ \Rightarrow \ \ x=(A^TA)^{-1}A^Tb$$
### Performance

1. **General Case**: $\text{Time complexity}\propto n^2k$, 
	- **Where**:
		- $n$ is the number of variables;
		- and $k$ is the number of terms.
	- **Example**: A desktop computer can handle hundreds of variables and thousands of terms **in seconds**. It should be expected with **Moore's Law** an exponential decrease in solution times as hardware improves.

2. **Sparse Matrices**: A matrix with significantly fewer nonzero entries than $kn$.
	- **Where** exploiting the sparsity significantly reduces computational time.
	- **Example**: Problems with tens of thousands of variables and hundreds of thousands of terms can be solved **in about a minute** on a desktop computer.

3. Extremely Large Problems: 
	- **Where** challenges arise with millions of variables and real time requirements.

## Using Least Squares
*Continue from section 1.2.1 page 5*