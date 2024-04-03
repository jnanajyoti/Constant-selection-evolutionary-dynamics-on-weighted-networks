
# Fixation Probability of weighted networks

This repository contains the `functions.ipynb` Jupyter notebook, offering a suite of functions to calculate the fixation probabilities of static weighted networks, assuming constant-selection evolutionary dynamics. It is an accompaniment of [Bhaumik & Masuda (2024)](https://arxiv.org/abs/2403.17208) . The methods for the static netoworks are based on Hindersin et al. (2016), available at [efficientFixation](https://github.com/hindersin/efficientFixation), and further explored within the context. [NM: I don't understand "further explored within the context". Either explain better or delete.]

## How to Use

The `functions.ipynb` notebook is equipped with functions designed for the analysis of fixation probabilities across various unweighted and weighted networks. Below is a breakdown of the primary functions and their intended applications:

### Transition probability matrices

- **`T_weightMat_Mat(G, r)`**: Generates the $$2^N$$ 2<sup>N</sup> x 2<sup>N</sup> transition probability matrix for a network `G` with fitness value `r` for the mutant type, and for Birth-death updating.

- **`T_weightMat_dB(G,r)`**: Generates the 2<sup>N</sup> x 2<sup>N</sup> transition probability matrix for a network `G` with fitness value `r`, and for death-Birth updating.

- **`matrix_solver(M)`**: Compute the fixation probability of the mutant for various values of *r* [NM: Am I correct in having added 'for various values of r'? Also make r mathmode (i.e. italic in latex). BTW, I do not think it is a recommended practice to make G and R etc. be quoted by backslashes. We do it only for functions or code part? I may be wrong. Follow the most standard convention of markdown/github code documentation.][JB: Both `` and ** are used. Since for our purposes ** is more apt, I used it.] given the transition matrix `M`.


### For larger symmetric networks

- **Complete graph  (N<sub>1</sub>+1)(N<sub>2</sub>+1) x (N<sub>1</sub>+1)(N<sub>2</sub>+1)**: 
  - **`matrix_complete_weight_solver(w_1,w_2,N_1,N_2,r)`**: Computes the fixation probability for the weighted complete graph. See section 4.2.1 of the paper for the definition of the weighted complete graph.


- **Star graph  (2(N<sub>1</sub>+1)(N<sub>2</sub>+1) x 2(N<sub>1</sub>+1)(N<sub>2</sub>+1))**:
  - **`weighted_star_solver(N_1,N_2,w,r)`**:  Computes the fixation probability for the weighted star graph. See section 4.2.2 of the paper for the definition of the weighted complete graph.


### Simulations on arbitrary weighted networks

- **Unweighted networks**: 
  - **`simulate(G,r)`**: Simulates the Birth-death process on the network `G` with mutant fitness `r`. The function returns the string 'blue' or 'red', depending on whether the resident or the mutant fixated.
  - **`simulation_count(G,n,r)`**: Simulates `n` times the Birth-death process on the network `G` with mutant fitness `r`. The function returns the proportion of runs in which the mutant fixated, which gives a numerical estimate of the fixation probability.


- **Weighted networks**:
  - **`weighted_simulate(G,r)`**: Simulates the Birth-death process on the weighted network `G` with mutant fitness `r`.
  - **`weighted_simulation_count(G,n,r)`**: Simulates the Birth-death process on the weighted network `G` with mutant fitness `r` `n` times, and returns the proportion of runs where the mutant fixated.

[NM: You said switching networks, but there is no appearance of that. Remove the switching network part? Or disect it into different repositories? If you are willing to make the temporal network code open, like this, I am supportive of that though it is post publication of the JMB paper. (I do not remember if we have done so already.)]
[Sorry, I wasn't finished editing the repository, that's why the readme had the temporal network text in it. Our switching temporal network code is available in [https://github.com/naokimas/Fixation-Probability]]

[NM: (1) Show examples for the case of general networks. In particular, people may be confused what G should be. Good to have a mock weighted network as an example to be put in this repository, which you use as input to an example usage to be written around here. (2) No mentioning to the case of six-node networks. You should not explain all details of the code for generating all figures, because it is too tedious and people are not interested in using much of the code (and we are thus responding to the request of the journal as well as releasing the code for the sake of interested readers where they are useful). So, apart from the six-node case (and an example usage mentioned above), no further documentation is necessary. But just place the code for generating each figure of the paper (which people are not intersted in using), without specific documentation except that which code creates which figures, perhaps in a new subfolder? Well, I may be wrong. As you are using jupiter notebook, how figures are generated may be self-explanatory, in which case it is already good. But you should still tell which notebook is for what.]

## Networks on six nodes
For each of the 112 networks on six nodes, we constructed 100 random weight assignments. [6_nodes_Bd](6_nodes_Bd.ipynb) contains the code for generation and classification of these weighted networks for the Bd updating rule, and [6_nodes_dB](6_nodes_dB.ipynb) contains the code for generation and classification of these weighted networks for the Bd updating rule

## Tutorial
The [Tutorial](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/main/Tutorial.ipynb) notebook illustrates the usage of the functions that we defined using a toy network.

## Data
The [Data](jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/Data) directory contains all the fixation probability data that we generated.

### Small Networks
The data for the fixation probabilities for the 100 different weight assignments for the 112 non isomorphic connected network on six nodes are provided [here](Data/Six_Nodes).  [weighted_networks_Bd.npy)](Data/Six_Nodes/weighted_networks_Bd.npy) contains the results for the Birth-death process, while [weighted_networks_dB.npy)](Data/Six_Nodes/weighted_networks_dB.npy) contains the result for the death-Birth process.

### Larger Symmetric Networks
The data for the larger symmetric networks, that is, the weighted complete and star graphs are provided in [here](Data/Larger_Symmetric_Networks).

### Empirical Network Data
The empirical network metadata are provided in [Network Data](Data/Empirical_Networks/Network_Data), for each of the six empirical networks. The simulated data for the fixation probabilities for these networks are provided in [Simulation_Results](Data/Empirical_Networks/Simulation_Results).

## Figures
-[Figure 1](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/2779d4a5f9c167210467fe6ae6e0804254f25d09/Figures/Schematic_diagams.ipynb)
-[Figure 2](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/2942fa9369377f0c15dfa69c13e363e0a309c92e/6_nodes_Bd.ipynb) 
-[Figure 3](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Weights_on_complete_graphs.ipynb)
-[Figure 4](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Weights_on_complete_graphs.ipynb)
-[Figure 5](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Weights_on_star_graphs.ipynb)
-[Figure 6](https://github.com/jnanajyoti/Constant-selection-evolutionary-dynamics-on-weighted-networks/blob/791515a48ad502f5c09d2bf089f23c40a3c365f4/Figures/Empirical_Network_Plots.ipynb)

## Dependencies

To use the notebook, ensure the following Python libraries are installed:

- **NumPy**: For numerical operations and matrix manipulations.
- **pandas**: For data manipulation and analysis.
- **NetworkX**: For the creation and manipulation of complex network structures.



