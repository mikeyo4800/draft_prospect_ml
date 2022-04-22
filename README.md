# NBA Draft Classification for 2022 Class

## How To Navigate Through the Repo

In the data folder, you'll find the college basketball datasets as well as csv files filled with various tested models.

The data_cleaning.ipynb file illustrates our data cleaning and exploratroy data anaylsis process.

The feature_models.ipynb file showcases our feature engineering and the testing of different models.

The predictions.ipynb shows our final model in action, with its various predictions on the upcoming college basketball 2022 class. 

## Overview

[1]: https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021?select=modern_RAPTOR_by_player.csv "College Basketball Players Dataset"

This project analyzes the data from [College Baseketball Players Dataset][1] in Kaggle. The data consists of detailed college players stats from 2009 - 2021, and players stats from 2022. Another data contains the info of college players who were drafted to NBA teams in both round 1 & 2.  

Based on dataset, we are using machine learning models to determine the college players' quality for for draft round 1 and draft round 2 and provide suggestions for New York Knicks. 


## Business Problem

The New York Knicks have been struggling for years to perform competitvely in the league for a long time. There are several ways to build a team through the draft, free agency, and trades. Ideally, there would be a balance between the methods. Unfortunately, the Knicks haven't been successful with their young players to build through the draft. The last player drafted by the Knicks to sign a multi-year deal after rookie deal was Charlie Ward, who was drafted in 1994.

Our model's purpose is to classfy the upcoming 2022 rookie class to optimize the franchise's draft strategy. So they can acquire the quality players, who can increase the team's performance for years. 



## Data Understanding

The College Basketball Players 2009-2021 (`CollegeBasketballPlayers2009-2021.csv`) has the detail statistics of each college players from 2009 to 2021. We combined it with DraftedPlayers2009-2021(`DraftedPlayers2009-2021.xlsx`), so we have the draft pick info if the players were drafted to the NBA teams.

The College Basketball Players 2022 (`CollegeBasketballPlayers2022.csv`) has the detail statistics of each college player from 2022, which we have tested on our final model. 


## Methods

This project tests various machine learning models, including Logistic Regression, Decision Tree, K-Nearest Neighbor, Random Forest, Extra Trees, and various other ensemble methods. We first created the baseline models with basic parameters to analyze how the predictors performed. Then we applied hyperparameter tuning on different models using the Pipeline, GridSearchCV, and RandomizedSearchCV to find the best working model. We further optimize by combining the tuned models into various ensemble models such as Stacker Classifier and AdaBoosting.

## Conclusions

After many tests, the best model is GradientBoosting from sklearn.ensemble. We reached 85% accuracy scores on testing data and 79 % validation on training data.

## Next Steps
Further analyses could yield additional insights to improve to our predicition models:

- Drafted players performance in NBA: Compare players’ performance in NBA vs College to predict whether college performance predicts NBA performance.
- Impact on the player positions: Analyze player positions impact on performances and change in positions if any.
- Round Selected and Pick Number: Further classify the round and the order of picks. Ex: Player one is predicted first round pick three
