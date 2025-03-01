- 20-01-25 18:16
- Sources: [[A Gentle Introduction to Power Flow - Letif Mones]]
- Links: [[Electricity Grids]], [[Graph Theory]], [[Power Flow]]
---
## Overview of Power Grids

> [!faq] **What are Power Grids?**
> **Power grids** are highly complex systems comprising numerous interacting components. Their operation requires careful coordination to ensure the continuous balance of **power injections** (generation) and **withdrawals** (demand), all while meeting:
> - **Physical constraints:** Network stability and losses.
> - **Economic constraints:** Cost minimisation.
> - **Environmental constraints:** Emissions and renewable integration.

### Graph Representation of Grids

Power grids can be abstracted and analysed using graph theory, where the components of the grid are represented mathematically:
- **Nodes (buses):** Represent significant locations within the grid, such as generation points, load centres, or substations. 
- **Edges (lines):** Represent transmission or distribution lines that physically connect the buses.
#### **Directed graph** (arrows show flow direction): $$\mathbb{G}_D(\mathcal{N},\mathcal{E})$$
- **Where**:
	 - $\mathcal{N}$: Set of nodes (buses).
	 - $\mathcal{E} \subseteq \mathcal{N} \times \mathcal{N}$: Set of directed edges (branches), representing power flow with a specific orientation (e.g., from one bus to another).
	![[Directed Graph.png|Directed Graph]]

#### **Undirected** graph (no flow direction): $$\mathbb{G}_D(\mathcal{N},\mathcal{E}\cup\mathcal{E}^R)$$
- **Where**:
     - $\mathcal{N}$: Same set of nodes (buses).
     - $\mathcal{E}$: Set of forward edges.
     - $\mathcal{E}^R\subseteq\mathcal{N}\times\mathcal{N}$: Set of reverse-orientated edges, corresponding to $\mathcal{E}$ but without explicit orientation.
    ![[Undirected Graph.png|Undirected Graph]]
	*In this representation, the direction of power flow is not explicitly shown.*

### Mathematical Framework

- **Sets**:
	- $\mathcal{N} \subseteq \mathbb{Z}^+$ represents the set of all nodes (buses).
	- $\mathcal{E} \subseteq \mathcal{N} \times \mathcal{N}$ represents the set of directed edges between nodes. 
	- $\mathcal{E}^R \subseteq \mathcal{N} \times \mathcal{N}$ represents the reverse-oriented edges.

- **Interpretation**:
	- Directed graphs are suitable for cases where power flow direction matters, such as detailed operational analysis.
	- Undirected graphs simplify the representation for broader studies, such as topology or connectivity analysis.