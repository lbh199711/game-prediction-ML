# game-prediction-ML
Predicting league of legends gamer result with different machine learning methods.

## Introduction
League of Legends is a popular competitive online game, where a total of 10 players are split
into blue and red teams. Players will choose unique characters to fight against the opponent’s
team. The goal of the game is to destroy the other team’s Nexus.<br>

In this experiment, we will be going through several methods of machine learning models to try
to predict the result of the game and compare their performance.<br>

## Experiment
The data set we are using is found on Kaggle. This dataset contains the stats for the game at the
10 minutes mark. Players have similar skill levels due to the game’s matchmaking system. There
are 19 features indicating the stats per team (38 in total) collected in-game. This includes kills,
deaths, gold, experience, etc. The target has a value of 1 or 0, indicating whether the blue team
has won at the end of the game. There are around 10,000 samples in total.<br>

In this experiment, we will apply different machine learning models to this data set and
compare their performance with each other, and also with the baseline model.<br>

## Method
We will test out 3 machine learning models on this dataset: Linear regression, Logistic
regression, and 1-layer Neural Network. For all 3 models, we will be using TensorFlow’s neural
network framework for ease of implementation.<br>

Before any game has been played, theoretically speaking either side should have an equal
chance of winning. The point of the task is to predict as many games correctly as possible, and
so, we set the measure of success to the accuracy of the model’s prediction comparing to the
target.<br>

The dataset is split 60-20-20 into training, validation, and testing set. All the features in the
datasets are normalized by the training data. This assumes validation and testing set will have
similar distribution when compared to the training data.<br>

During training, we will use the grid search to optimize the hyperparameters using the
validation accuracy, then use the best model against the test dataset.

### To see the full report of this experiment, check out the pdf in this repo.
