
# Fixation Probability Calculation Notebook

This repository contains the `functions.ipynb` Jupyter notebook, offering a comprehensive suite of functions to calculate the fixation probabilities of static weighted networks. The methods implemented are based on the manuscript `Constant-selection evolutionary dynamics on weighted networks`, submitted to Proc of Royal Society A. The methods for the static netoworks are based on Hindersin et al. (2016), available at [efficientFixation](https://github.com/hindersin/efficientFixation), and further explored within the context.
## How to Use

The `functions.ipynb` notebook is equipped with functions designed for the analysis of fixation probabilities across various network configurations, including static networks and those subject to temporal switching. Below is a breakdown of the primary functions and their intended applications:

### Transition Probability Matrices

- **`T_weightMat_Mat(G, r)`**: Generates the 2^N x 2^N transition probability matrix for a network `G` with fitness value `r`, for Birth-death updating.

- **`T_weightMat_dB(G,r)`**: Generates the 2^N x 2^N transition probability matrix for a network `G` with fitness value `r`,for death-Birth updating.

- **`matrix_solver(M)`**: Compute the fixation probability of the transition matrix `M`.


### For Larger Symmetric Networks

- **Complete Graph  (2N x 2N)**: 
  - **`matrix_complete_weight_solver(w_1,w_2,N_1,N_2,r)`**: Computes the transition matrix for the star graph.


- **Star Graph  (2M(N+1) x 2M(N+1))**:
  - **`weighted_star_solver(N_1,N_2,w,r)`**:  Computes the transition matrix for the complete bipartite graph.


### For Simulations

- **Complete Graph  (2N x 2N)**: 
  - **`matrix_complete_weight_solver(2,1,2,48,i/100)`**: Computes the transition matrix for the star graph.


- **Star Graph  (2M(N+1) x 2M(N+1))**:
  - **`weighted_star_solver(10,10,2,i/100)`**:  Computes the transition matrix for the complete bipartite graph.

weighted_star_solver
## Dependencies

To utilize the notebook, ensure the following Python libraries are installed:

- **NumPy**: For numerical operations and matrix manipulations.
- **pandas**: For data manipulation and analysis.
- **NetworkX**: For the creation and manipulation of complex network structures.



