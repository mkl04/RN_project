# Time-series Forecasting

Implementation of MLP and LSTM for Enery Forecasting using genetic algorithms as optimization.

### Objective
Predict the total monthly energy load for the years 2020 and 2021, and compare with the actual one.

### Dataset
Operador Nacional do Sistema Elétrico ([ONE](http://www.ons.org.br/)).

Historical daily energy load data in different regions of Brazil from 2005 to the present.

As preprocessing, the number of the month was encoded as a binary value of 4 digits. For validation and test set, the values of the year 2018 and 2019 were set, respectively.

### Solution
To train the neural networks (MLP and LSTM), there were defined the main hyperparameters: number of units, windows size and number of epochs. These parameters were optimized using genetic algorithm with two different representation of individuals: binary and integer. The objective function were the metric MAPE for 12-steps ahead (one year).

### Results

The best results were achieved using MLP, with values of MAPE less than 2%. 

![Alt text](Figures/prediction.PNG?raw=true "Prediction")

It corroborated the hypothesis that the energy load in the quarantine months had a large difference from the trend over more than 10 years.

Another point observed is that little by little energy consumption in the southern states of Brazil is returning to normal estimates.

![Alt text](Figures/forecasting.PNG?raw=true "Forecasting")