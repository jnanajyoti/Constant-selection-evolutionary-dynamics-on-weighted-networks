
# Fixation Probability Calculation Notebook

This repository contains the `functions.ipynb` Jupyter notebook, offering a comprehensive suite of functions to calculate the fixation probabilities within static and dynamically switching networks. The methodology implemented herein draws inspiration from the work by Hindersin et al. (2016), available at [efficientFixation](https://github.com/hindersin/efficientFixation), and further explored within the context of the study by Bhaumik & Masuda (2023) as detailed in their publication [here](https://link.springer.com/article/10.1007/s00285-023-01987-5).

## How to Use

The `functions.ipynb` notebook is equipped with functions designed for the analysis of fixation probabilities across various network configurations, including static networks and those subject to temporal switching. Below is a breakdown of the primary functions and their intended applications:

### Transition Probability Matrices

- **`T_Mat(G, r)`**: Generates the 2^N x 2^N transition probability matrix for a network `G` with fitness value `r`.

- **`matrix_solver(M)`**: Placeholder for additional documentation.

- **`switch_matrix_solver(M, N, t)`**: Placeholder for additional documentation.

### For Larger Symmetric Networks

- **Star Graph + Complete Graph Switching Networks (2N x 2N)**:
  - **`star_Tmat(n, r)`**: Computes the transition matrix for a star graph.
  - **`complete_Tmat(n, r)`**: Computes the transition matrix for a complete graph.
  - **`star_complete_agg_Tmat(n, r)`**: Aggregates transition matrices for star and complete graph switching.
  - **`switch_matrix_2n_solver(M, N, t)`**: Placeholder for additional documentation.
  - **`star_complete_solver(n, r)`**: Placeholder for additional documentation.

- **Star Graph + Complete Graph Switching Networks (2M(N+1) x 2M(N+1))**:
  - **`bipartite_Tmat(m, n, r)`**: Placeholder for additional documentation.
  - **`star_2mn_Tmat(l, n, r)`**: Placeholder for additional documentation.
  - **`star_bipartite_sum_Tmat(m, n, r)`**: Placeholder for additional documentation.
  - **`switch_matrix_2mn_solver(a, b, r, s, t)`**: Placeholder for additional documentation.
  - **`matrix_starbp2mn_solver(r, a, b)`**: Placeholder for additional documentation.

### Random Initialization

- **`random_switching_fixn(G1, G2, r, tau)`**: Computes fixation probabilities with random initializations for given networks `G1` and `G2`.

### Stochastic Matrix

- **`S_Mat(G1, G2, r, p)`**: Generates a stochastic matrix based on networks `G1`, `G2`, fitness `r`, and probability `p`.

## Dependencies

To utilize the notebook, ensure the following Python libraries are installed:

- **NumPy**: For numerical operations and matrix manipulations.
- **pandas**: For data manipulation and analysis.
- **NetworkX**: For the creation and manipulation of complex network structures.



