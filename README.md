# DL-ROM in the loop

This repository contains the official source code implementation of the paper
*DL-ROM in the loop: a deep learning-based reduced order feedback control of high-dimensional parametrized systems*

`Data` folder contains the scenario parameters and the simulated snapshots for the optimal transport test cases

`NN` folder contains the autoencoders, the policies and the forward maps built and trained in the optimal transport test cases

To run the test cases, the library [dlroms](https://github.com/MatteoTomasetto/dlroms) is required to handle meshes, finite element spaces, neural networks and proper orthogonal decomposition.
This library is a fork of the [dlroms](https://github.com/NicolaRFranco/dlroms.git) library, that is written and currently maintained by [Nicola Rares Franco](https://github.com/NicolaRFranco), Ph.D., MOX, Politecnico di Milano.

## Optimal transport in a vacuum
`OptimalTransportVacuum.ipynb` presents the optimal transport in a vacuum test case where the state -- whose dynamics is described by the Fokker-Planck equation -- is moved from an initial position to a target destination. Different starting positions and final endpoints may be considered. The velocity on the entire domain is instead regarded as control action.

<p align="center" width="100%">
  <img width=30% src="./gifs/OptimalTransportVacuum/State_test.gif" >
    
  <img width=30% src="./gifs/OptimalTransportVacuum/Control_test.gif" >
  <br />
  Optimal state and control trajectory corresponding to the initial position (−0.24, −0.14) and the target position (0.48,−0.03) in the test set 
</p>

<p align="center" width="100%">
  <img width=30% src="./gifs/State_test_latentloop.gif" >
    
  <img width=30% src="./gifs/Control_test_latentloop.gif" >
  <br />
  Optimal state and control trajectory provided by the latent feedback loop corresponding to the initial position (−0.24, −0.14) and the target position (0.48,−0.03) in the test set 
</p>

