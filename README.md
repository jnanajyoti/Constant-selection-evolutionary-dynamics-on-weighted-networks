## Fixation-Probability

The <a href="https://github.com/jnanajyoti/Fixation-Probability/blob/main/functions.ipynb">functions.ipynb</a> notebook contains all the functions for calculating the fixation probabilities of a network. This code is based on the [code](https://github.com/hindersin/efficientFixation) provided in [Hindersin, et. al. (2016)](https://www.sciencedirect.com/science/article/abs/pii/S0303264716301885) .

# How to use the code?
All the functions used for calculation fixation probability of static networks and switching temporal networks in [Bhaumik & Masuda, 2023](https://link.springer.com/article/10.1007/s00285-023-01987-5), are present in `functions.ipynb`.

-2^N x 2^N matrices
    - `T_Mat(G,r)`: outputs the 2^N x 2^N transition probability matrix for a given network. Inputs are as follows:
        - network G
        - fitness value r
    -`matrix_solver(M)`:
    -`switch_matrix_solver(M,N,t)`:
-Larger symmetric networks
      - 2N x 2N star graph + complete graph switching networks
        -`star_Tmat(n,r)` : 2N x 2N
        -`complete_Tmat(n,r)`
        -`star_complete_agg_Tmat(n,r)`
        -`switch_matrix_2n_solver(M,N,t)`:
        -`star_complete_solver(n,r)`:
      -2*M*(*N+1*) x 2*M*(*N+1*) star graph + complete  graph switching networks
        -` bipartite_Tmat(m,n,r)`:
        -`star_2mn_Tmat(l,n,r)`:
        -`star_bipartite_sum_Tmat(m,n,r)`:
        -`switch_matrix_2mn_solver(a,b,r,s,t)`:
        -`matrix_starbp2mn_solver(r,a,b)`:
-Random Initialization
        -`random_switching_fixn(G1,G2,r,tau)`:
-Stochastic matrix
        -`S_Mat(G1,G2,r,p)`:

## Dependencies
The file <a href="https://github.com/jnanajyoti/Fixation-Probability/blob/main/functions.ipynb">functions.ipynb</a> depends on  NumPy, pandas, and NetworkX.
