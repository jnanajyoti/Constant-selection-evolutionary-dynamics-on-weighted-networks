
# Fixation Probability of weighted networks

This repository contains the `functions.ipynb` Jupyter notebook, offering a suite of functions to calculate the fixation probabilities of static undirected weighted networks, assuming constant-selection evolutionary dynamics. It is an accompaniment of [Bhaumik & Masuda (2024)](https://arxiv.org/abs/2403.17208) . The methods for the static netoworks are based on Hindersin et al. (2016), available at [efficientFixation](https://github.com/hindersin/efficientFixation).

## How to Use

The `functions.ipynb` notebook is equipped with functions designed for the analysis of fixation probabilities across various unweighted and weighted networks. Below is a breakdown of the primary functions and their intended applications:

### Transition probability matrices

- **`T_weightMat_Mat(G, r)`**: Generates the $2^N \times 2^N$ transition probability matrix for a network `G` with fitness value `r` for the mutant type, and for Birth-death updating.

- **`T_weightMat_dB(G,r)`**: Generates the $2^N \times 2^N$ transition probability matrix for a network `G` with fitness value `r` for the mutant type, and for death-Birth updating.

- **`matrix_solver(M)`**: Compute the fixation probability of the mutant for various values of $r$ given the transition matrix `M`.


### For larger symmetric networks

- **Weighted complete graph**: 
  - **`matrix_complete_weight_solver(w_1,w_2,N_1,N_2,r)`**: Computes the fixation probability for the weighted complete graph. See section 4.2.1 of the paper for the definition of the weighted complete graph.


- **Weighted star graph**:
  - **`weighted_star_solver(N_1,N_2,w,r)`**:  Computes the fixation probability for the weighted star graph. See section 4.2.2 of the paper for the definition of the weighted star graph.


### Simulations on arbitrary undirected networks

- **Unweighted networks**: 
  - **`simulate(G,r)`**: Simulates the Birth-death process on network `G` with mutant's fitness `r`. The function returns the string 'blue' or 'red', depending on whether the resident or the mutant has fixated.
  - **`simulation_count(G,n,r)`**: Simulates `n` times the Birth-death process on network `G` with mutant's fitness `r`. The function returns the proportion of runs in which the mutant has fixated, which gives a numerical estimate of the fixation probability.


- **Weighted networks**:
  - **`weighted_simulate(G,r)`**: Simulates the Birth-death process on weighted network `G` with mutant's fitness `r`. The output of the function is the same as that of `simulate(G,r)`.
  - **`weighted_simulation_count(G,n,r)`**: Simulates `n` times the Birth-death process on weighted network `G` with mutant's fitness `r`. The output of the function is the same as that of `simulation_count(G,n,r)`.


## Networks on six nodes
For each of the 112 networks on six nodes, we constructed 100 random weight assignments. 
- The [6_nodes_Bd.ipynb](6_nodes_Bd.ipynb) notebook contains the code for generation and classification of these weighted networks for the Bd updating rule.
- The [6_nodes_dB.ipynb](6_nodes_dB.ipynb) notebook contains the code for generation and classification of these weighted networks for the dB updating rule.

## Tutorial
The [Tutorial.ipynb](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/main/Tutorial.ipynb) notebook illustrates the usage of the functions that we defined using a toy network.

## Data
The [Data](jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/Data) directory contains all the fixation probability data that we generated for the paper.

### Small networks
The data for the fixation probabilities for the 100 different weight assignments for the 112 non-isomorphic connected networks on six nodes are provided [here](Data/Six_Nodes).  [weighted_networks_Bd.npy](Data/Six_Nodes/weighted_networks_Bd.npy) contains the results for the Bd updating rule, while [weighted_networks_dB.npy](Data/Six_Nodes/weighted_networks_dB.npy) contains the result for the dB updating rule.

### Larger symmetric networks
The data for the larger weighted complete and weighted star graphs are [here](Data/Larger_Symmetric_Networks).

### Empirical network data
 The numerically obtained fixation probabilities for the empirical networks are provided in [Simulation_Results](Data/Empirical_Networks/Simulation_Results).

## Figures
- [Figure 1](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/2779d4a5f9c167210467fe6ae6e0804254f25d09/Figures/Schematic_diagams.ipynb)
- [Figure 2](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/2942fa9369377f0c15dfa69c13e363e0a309c92e/6_nodes_Bd.ipynb) 
- [Figure 3](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Weights_on_complete_graphs.ipynb)
- [Figure 4](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Weights_on_complete_graphs.ipynb)
- [Figure 5](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Weights_on_star_graphs.ipynb)
- [Figure 6](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Empirical_Network_Plots.ipynb)

## Dependencies

To use the notebook, ensure the following Python libraries are installed:

- **NumPy**: For numerical operations and matrix manipulations.
- **pandas**: For data manipulation and analysis.
- **NetworkX**: For the creation and manipulation of complex network structures.



