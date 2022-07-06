# NBA Draft Prediction for 2022 Class

[3]: https://mikeyo4800-streamlit-apps-test-ept0a0.streamlitapp.com/ "Streamlit App"

To see the model in production, visit our [Streamlit App][3]

## Business Goal

The New York Knicks have been struggling for years to perform competitvely in the league for a long time. There are several ways to build a team through the draft, free agency, and trades. Ideally, there would be a balance between the methods. Unfortunately, the Knicks haven't been successful with their young players to build through the draft. The last player drafted by the Knicks to sign a multi-year deal after rookie deal was Charlie Ward, who was drafted in 1994.

Our project's goal is to predict the upcoming 2022 rookie class into draft rounds 1 & 2 based on their college statistics to optimize the franchise's draft strategy, so they can acquire the quality players, who can increase the team's performance for years. 

## How To Navigate Through the Repo

[1]: https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021 "Kaggle"

In the data folder, you'll find the college basketball dataset we downloaded from [Kaggle][1]. 

In the notebooks folder, there is three notebooks. The data_cleaning_and_eda.ipynb file illustrates our data cleaning and exploratory data anaylsis process. The model_building.ipynb file showcases the models we built and optimized for accuracy. (LogisitcRegression, RandomForestClassifier, GradientBoostingClassifier, ExtraTreesClassifier, etc) Lastly, in the model_prediction.ipynb file, we pickle our best model and make predicitions on 2022 college basketball players who have not been drafted yet.

## Data Understanding

[2]: https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021 "College Basketball Players Dataset"

This project analyzes the data from [College Baseketball Players Dataset][2]. The data consists of two csv files. The first file is detailed college players stats from 2009 - 2021 who were drafted into the NBA. The second dataset is 2022 college players who have not been drafted into the nba yet.  


## Exploratory Data Analysis and Model Building

This project tests various machine learning models, including Logistic Regression, Decision Tree, K-Nearest Neighbor, Random Forest, Extra Trees, and various other ensemble methods. We first created the baseline models with basic parameters to analyze how the predictors performed. Then we performed exploratory data analysis on all predictors to see if there were any basketball stats that shown significant differences between round 1 players and round 2 players. Ultimately, we discovered 11 variables that shown significant differences between both classes using Welsch's t-Test.  

After finding the best predictors, we then applied hyperparameter tuning on different models using the Pipeline, GridSearchCV, and RandomizedSearchCV classes to optimize accuracy score on the test data. We further optimize by combining the tuned models into various ensemble models such as StackerClassifier and AdaBoosting.

## Conclusions

After many tests, the best model is GradientBoosting from sklearn.ensemble. We reached 85% accuracy scores on testing data and 79 % validation on training data.

## Next Steps
Further analyses could yield additional insights to improve to our predicition models:

- Drafted players performance in NBA: Compare players’ performance in NBA vs College to predict whether college performance predicts NBA performance.
- Impact on the player positions: Analyze player positions impact on performances and change in positions if any.
- Round Selected and Pick Number: Further classify the round and the order of picks. Ex: Player one is predicted first round pick three
