
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
  - **`matrix_complete_weight_solver(w_1,w_2,N_1,N_2,r)`**: Computes the fixation probability for the weighted complete graph, as described in Sec 4.2.1.


- **Star Graph  (2M(N+1) x 2M(N+1))**:
  - **`weighted_star_solver(N_1,N_2,w,r)`**:  Computes the fixation probability for the weighted star graph, as described in Sec 4.2.2.


### For Simulations

- **Unweighted networks**: 
  - **`simulate(G,r)`**: Simulates the Birth-death process on the network `G` with mutant fitness `r`.
  - **`simulation_count(G,n,r)`**: Simulates the Birth-death process on the network `G` with mutant fitness `r` `n` times, and returns the proportion of runs where the mutant fixated.


- **Weighted networks**:
  - **`weighted_simulate(G,r)`**: Simulates the Birth-death process on the weighted network `G` with mutant fitness `r`.
  - **`weighted_simulation_count(G,n,r)`**: Simulates the Birth-death process on the weighted network `G` with mutant fitness `r` `n` times, and returns the proportion of runs where the mutant fixated.


## Dependencies

To utilize the notebook, ensure the following Python libraries are installed:

- **NumPy**: For numerical operations and matrix manipulations.
- **pandas**: For data manipulation and analysis.
- **NetworkX**: For the creation and manipulation of complex network structures.



