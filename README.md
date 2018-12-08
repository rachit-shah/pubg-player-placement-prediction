# pubg-player-placement-prediction
Kaggle Competition https://www.kaggle.com/c/pubg-finish-placement-prediction 
PUBG Player Placement Prediction  
(ALDA Project Group P09)

Player Unknown Battle Ground’s (PUBG) is an online Multiplayer battle royale game developed by PUBG Corporation. It is a player versus player action game in which no more than 100 player fight in a battle royale. Players can choose to enter the match solo, duo or with a small team up to 4 people. However, there are events and custom games which allow team sizes more than 4. We will address this discrepancy during feature engineering. The last person or the last team alive wins the match. The player has to knock down their opponents so as to survive till the last. During the game, players search buildings, ghost towns to find weapons, vehicles, armor, and other equipment.

The data is part of a Kaggle competition which has scraped 65000 games worth of data using an API. The goal is to predict the win percentage of the player based on 28 given features. For example, in a solo game of 100 players if a player got rank of 80, then its winPlacePerc will be (100-80)/(100-1)=0.204 using the formula winPlacePerc = (maxPlace-winPlace)/(maxPlace-1). The problem is then
essentially a regression problem to predict the winPlacePerc of the player between [0,1]. These types of problems are solved by doing extensive exploratory data analysis and feature engineering before applying a regression model. We gained insights in the features and added new relevant features by exploring the game and the semantics of the features. We were provided with the Training Dataset so we devided it into Training and Validation Dataset in 70 and 30 ratio respectively.

We first used the LGBM (Light Gradient Boosting Machine) (5) Regressor to train our training dataset after doing exploratory analysis on the data. We compared 10 other models namely Neural Network, Multiple Linear Regression, Decision tree, etc. with the same dataset. We reported the accuracy of each model that we got on the validation data.

For detailed explanation, please read report.
