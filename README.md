"Dissimilarity measures for generalized Lotka-Volterra systems on networks"
 by Nicolás A. Márquez , Maryam Chaib De Mares, and Alejandro P. Riascos
 March 13, 2026

We present examples of a framework to quantify dissimilarities between generalized Lotka Volterra systems that differ in interaction parameters, network structure, or in the functional form of the governing equations. 




The material provided here allows the reproduction of the data used in Figures 1(a–d), 2(c–e), and 5(e) of the article.

The simulations are based on the numerical integration of Lotka–Volterra (LV) and generalized Lotka–Volterra (gLV) dynamical systems, and on the evaluation of the dissimilarity measure introduced in the manuscript to compare the evolution of two dynamical processes.

All numerical experiments were performed using Python and standard scientific computing libraries, including NumPy, SciPy, Matplotlib, and NetworkX.

The repository is organized into directories corresponding to each set of figures.


------------------------------------------------------------
1. Code_Figures_1a-d
------------------------------------------------------------

This directory contains the Python notebooks used to generate the numerical results shown in Figures 1(a–d) of the manuscript.

These simulations analyze the classical two-species Lotka–Volterra predator–prey model. The notebooks compare the dynamics of a reference system with parameter alpha and a modified system with parameter alpha*. Both systems start from identical initial conditions.

The notebooks compute:

- The prey population trajectories u(tau) and u*(tau)
- The predator population trajectories v(tau) and v*(tau)
- The dynamical dissimilarity between the two systems:
  D^(LV)(tau)
- The maximum dissimilarity:
  D_max^(LV)(tau)



------------------------------------------------------------
2. Codes_Datasets_Figure_2c-e
------------------------------------------------------------

This directory contains the codes and datasets used to generate the results shown in Figures 2(c–e).

The simulations consider generalized Lotka–Volterra (gLV) dynamics on directed networks with three nodes. The goal is to compare the dynamical evolution of two systems defined on networks with the same set of species but different interaction structures.

The notebooks perform the following steps:

1. Construction of the network topology.
2. Definition of the interaction matrices Lambda and Lambda*.
3. Numerical integration of the gLV equations.
4. Computation of the dissimilarity measure:
   D^(LV)(t)


------------------------------------------------------------
3. Codes_Datasets_Figure_5e
------------------------------------------------------------

This directory contains the codes and datasets used to generate the results shown in Figure 5(e).

The simulations consider generalized Lotka–Volterra dynamics on a network with community structure composed of 12 nodes arranged in three cliques of four nodes each. The cliques are interconnected through a ring-like structure, forming a globally connected network.

For each realization of the experiment:

1. A reference interaction matrix Lambda is generated, where the nonzero interaction weights are drawn from a uniform distribution in the interval (0,1].
2. A modified matrix Lambda* is constructed by randomly flipping the sign of each interaction with probability (1 - p), while preserving the absolute value of the interaction strength.
3. The gLV equations are numerically integrated for both systems using identical initial conditions.
4. The dynamical dissimilarity between the resulting trajectories is computed.
5. The maximum dissimilarity
   D_max{Lambda, Lambda*}
   is recorded.

The simulations are repeated for different values of the sign-flip probability and averaged over multiple realizations. The datasets stored in this folder contain the values used to compute the ensemble averages plotted in Figure 5(e). All the datasets contain 200 realizations of D_max{Lambda, Lambda*}.


------------------------------------------------------------
Software requirements
------------------------------------------------------------

The notebooks require Python 3 and the following libraries:

NumPy
SciPy
Matplotlib
NetworkX

The notebooks can be executed using Jupyter Notebook or JupyterLab by running the cells sequentially.

