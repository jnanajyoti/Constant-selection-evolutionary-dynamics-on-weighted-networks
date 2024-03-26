
# Fixation Probability Calculation Notebook

This repository contains the `functions.ipynb` Jupyter notebook, offering a comprehensive suite of functions to calculate the fixation probabilities within static and temporal switching networks. The methods implemented are based on Bhaumik & Masuda (2023) as detailed in their publication [here](https://link.springer.com/article/10.1007/s00285-023-01987-5). The methods for the static netowkrs are based on Hindersin et al. (2016), available at [efficientFixation](https://github.com/hindersin/efficientFixation), and further explored within the context
## How to Use

The `functions.ipynb` notebook is equipped with functions designed for the analysis of fixation probabilities across various network configurations, including static networks and those subject to temporal switching. Below is a breakdown of the primary functions and their intended applications:

### Transition Probability Matrices

- **`T_Mat(G, r)`**: Generates the 2^N x 2^N transition probability matrix for a network `G` with fitness value `r`.

- **`matrix_solver(M)`**: Placeholder for additional documentation.

- **`switch_matrix_solver(M, N, t)`**: Placeholder for additional documentation.

### For Larger Symmetric Networks

- **Complete Graph  (2N x 2N)**: 
  - **`star_Tmat(n, r)`**: Computes the transition matrix for the star graph.


- **Star Graph  (2M(N+1) x 2M(N+1))**:
  - **`bipartite_Tmat(m, n, r)`**:  Computes the transition matrix for the complete bipartite graph.




## Dependencies

To utilize the notebook, ensure the following Python libraries are installed:

- **NumPy**: For numerical operations and matrix manipulations.
- **pandas**: For data manipulation and analysis.
- **NetworkX**: For the creation and manipulation of complex network structures.



