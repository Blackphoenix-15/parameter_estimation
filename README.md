# Genetic Toggle Switch with Stochastic Differential Equations (SDEs)

# Overview
This project models a genetic toggle switch, a bistable system influenced by stochastic differential equations (SDEs). The simulation incorporates Gaussian and Lévy noise, and a FCNN + Transformer model is used to estimate key parameters and predict system behavior.

 # System Dynamics
The genetic toggle switch consists of two mutually repressing genes, governed by nonlinear differential equations. The system is defined by:

# Gene Expression: Modeled using Hill functions and degradation rates.
Stochastic Effects: Incorporates Gaussian and Lévy noise to simulate real-world randomness.
Key Parameters: Includes production/degradation rates, Hill coefficient, and additional regulatory factors.
# Dataset
The dataset is stored in HDF5 format and contains:

U_data: Time-series data for protein U concentration.
V_data: Time-series data for protein V concentration.
Noise Contributions: Gaussian and Lévy noise effects.
Switch Parameters: Recorded values of a, b, r, k, e per sample.
🔹 Generation Process
500 samples of simulated toggle switch trajectories.
Time evolution solved numerically using Euler-Maruyama method.
Stochastic noise introduced with Gaussian + Lévy processes.
#  Model Architecture
The FCNN + Transformer model was trained for parameter estimation and system identification.

🔹 Components
FCNN (Fully Connected Neural Network): Feature extraction from time-series data.
Transformer Encoder: Captures long-range dependencies and sequential patterns.
Regression Head: Outputs estimated system parameters.
🔹 Training
Loss Function: Mean Squared Error (MSE)
Optimizer: Adam
Regularization: Early stopping based on validation loss
#  Results & Inference
Model successfully learns system dynamics despite stochastic noise.
Provides accurate estimations of key parameters (a, b, r, k, e).
Outperforms traditional regression models on noisy datasets.
#  Future Improvements
Graph Neural Networks (GNN) + Transformer for improved feature extraction.
Alternative Noise Models: Studying effects of different stochastic processes.
Comparisons with LSTMs and Diffusion Models for better time-series learning.
