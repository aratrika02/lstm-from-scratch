# LSTM-from-scratch
This project has been developed with the goal of achieving an in-depth understanding of how Long 
Short-Term Memory (LSTM) networks work and to that end, implements it entirely from scratch without 
using any built-in LSTM libraries. Only basic matrix operations and activation functions have been used in 
constructing each component of an LSTM network, from gating mechanisms, cell state updates to 
backpropagation through time (BPTT). 

The performance of the model thus built is comprehensively evaluated 
over a vehicle trajectory prediction task over a time-series dataset consisting of 9400 .csv files, each comprising 
12 vehicular features over 67 timesteps. The task is to predict the vehicle coordinates for the next 5 timesteps by 
training the model over the first 62 timesteps. The model performance has been assessed over a series of 
experimentations: first using regular stochastic gradient descent (SGD) and then using SGD with momentum. 
The model parameters (number of LSTM units=32,64,128, learning rate, step decay of learning rate) has been varied to 
obtain the optimal hyperparameters for the best model performance. Root Mean Square Error (RMSE) has been 
used as the primary evaluation metric.

Finally, an LSTM model with 32 units, leveraging SGD with momentum and applying a decayed learning rate (initial learning rate = 1e-2 and is halved after every 
10 epochs) emerges as the model with the best performance, achieving a denormalized test RMSE of 1.5384. 
