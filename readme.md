Can we predict the hardness of finding the ground state of a problem Hamiltonian
 with a quantum solver from easy to get classical data?

We focus on the exact cover 3 (EC3) problem which is known to have a hardness related feature,
the number of clauses (M) per variable (N), M/N.
We find the ground state of EC3 problem instances through quantum annealing
 and set the final fidelity as the measure of hardness.
We use simulated annealing energies as the classical data to predict the fidelities.
We design a convolutional neural network to learn such mapping.

Notebook annealing_ec3_data_gen.ipynb contains the code for fast generation of data.
Notebook correlations_analysis.ipynb performs an analysis of the correlation between simulated annealings and fidelity.
To train a neural network to learn the mapping from simulated annealing to fidelity,
see for instance https://github.com/b-irsigler/ML_MC/blob/main/causal_CNN_regressor_RayTune.ipynb .

Once it is working, it is interesting to know on what the network is focusing to make such predictions with techniques like gradCAM.

