- 05-01-25 19:12
- Sources: [[Convex Optimisation - Stephen Boyd and Lieven Vandenberghe|Convex Optimisation - Stephen Boyd and Lieven Vandenberghe]]
-  Links: [[Linear Programming]], [[Nonlinear Programming]], [[Least Squares]], [[Convex Optimisation]], [[Mathematics]]
---
## Solving Optimisation Problems

### Solution Method

A **solution method** for optimisation problems refers to an algorithm that computes a solution to a given problem, ensuring some level of accuracy. For a class of optimisation problems, the algorithm solves an **instance** of the problem.

**Key factors influencing algorithm effectiveness**:  
  1. **Form of objective and constraint functions**  
  2. **Number of variables and constraints**  
  3. **Special structures** (e.g., sparsity)
  
>[!faq] What is Sparcity?
> A problem is considered **sparse** if each constraint function depends on only a small number of variables. Sparse problems are generally easier to handle computationally.

### Challenges in Solving General Optimisation Problems

Even with **smooth objective and constraint functions** (like polynomials), optimisation problems remain surprisingly difficult to solve. Common challenges include:
- **Computation Time**: Some methods may require very long computational times.
- **Possibility of No Solution**: There's no guarantee of finding the exact solution.

To deal with these challenges, most solution methods involve **compromise** in one form or another.

---
## Special Classes of Problems with Effective Algorithms

Although most optimisation problems are difficult, there are exceptions where effective and reliable algorithms exist to solve problems efficiently, even with large numbers of variables and constraints.
### Examples of Problem Classes with Effective Algorithms:
1. **[[Least Squares]]**
	- Widely studied and have effective solution methods.
	- Used in fitting models to data.
2. **[[Linear Programming|Linear Programming (LP)]]**  
	- Effective algorithms exist for LP problems, even when they have large numbers of variables and constraints.
3. **[[Convex Optimisation]] or [[Nonlinear Programming|Nonlinear Programming (NLP)]]**
	- Another important class with **effective algorithms** that can handle large problems efficiently.
	- Like linear programming and least-squares problems, **convex optimisation or NLP** problems are solvable with reliability and efficiency.