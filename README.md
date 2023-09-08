# Richter's Predictor: Modeling Earthquake Damage
Predicting the level of damage to buildings caused by the 2015 Gorkha earthquake in Nepal based on aspects of building location and construction. Competition hosted by DrivenData.
This repository contains my solution for the "Richter's Predictor: Modeling Earthquake Damage" competition hosted by DrivenData. In this competition, the goal was to predict the level of damage to buildings caused by the 2015 Gorkha earthquake in Nepal based on aspects of building location and construction. The target variable is damage_grade, which represents the level of damage to the building.

## Problem Overview

The dataset provided for this competition mainly consists of information on the buildings' structure and their legal ownership. The 38 features include both numerical and obfuscated categorical variables. Each row in the dataset represents a specific building in the region that was hit by the Gorkha earthquake. 

## My Approach

### Data Preprocessing
With a substantial dataset containing 260,601 entries, there was no need to remove features. However, the geographical location was presented in three categorical variables with up to 11,861 classes. To handle this, an autoencoder neural network was employed to encode the geolocation effectively. This reduced the dimensionality of the input data while retaining its essential characteristics.

### Model Selection
For the prediction task, I opted to use the XGBoost algorithm. XGBoost is a robust and efficient gradient boosting library known for its strong performance in various machine learning competitions.

### Hyperparameter Tuning
To optimize the performance of the XGBoost model, I employed Optuna, a hyperparameter optimization framework. Optuna helped me search for the best set of hyperparameters, ensuring that my model was fine-tuned for this specific problem.

### Result
My model achieved a micro-averaged F1 score of 0.7523 on the test data, which placed me at the 135th position out of 2,170 participants on DrivenData's leaderboard.
