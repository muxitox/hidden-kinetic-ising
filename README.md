# Kinetic Ising Model with Hidden Units


## Abstract

This project contains an implementation of a Kinetic Ising model with latent hidden units that vary over time.

[ERROR] Random numger generator calls have been modified to correctly invoke to Gaussian functions, some experiments must be remade. Make sure H biases are set to 0, only J are initialized.

## Description of the code

The code to reproduce the results can be found in the 'hidden_kinetic_ising' and 'kinetic_ising' folder:

* 'kinetic_ising/kinetic_ising.py', contains code for simulating the standard Ising model.
* 'hidden_kinetic_ising/hidden_kinetic_ising_it2.py', contains the class that peforms that initializes the parameters and executes the learning loop through the fit function.
* 'hidden_kinetic_ising/sim_fit_sim_HI2.py', includes the main that coordinates all the scripts and allows to modify the seeds to reproduce the results or to create new ones.


The data is stored in the 'results' folder. We store the graphs with the evolution of the learning process and the final parameters and moments after learning. A file located in a folder with the next structure 'sqrt_size/10/6' means that this file corresponds an experiment with 10 original neurons where only 6 and visible and with an initialization of J in the original model in the following way: self.J = self.rng.random((self.size, self.size)) / np.sqrt(self.size).

A file with the name '"\722"\_10_6_0_5000_6500_eta001_5000_100' means the following respectively:
* 722: the seed.
* 10: the number of total neurons.
* 5000: the number of steps taken in the original simulation.
* 6500: the number of steps taken in the inner simulations.
* eta0001: the learning rate is equal to 0.01.
* 5000: maximum iterations of the learning loop.
* 5000: the burn-in in the simulations.

.png files include graphs showing the behavior of the systems.
.npz files include the parameters and results achieved after inference.

