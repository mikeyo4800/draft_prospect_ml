{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# NBA Draft Classification for 2022 Class"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## How To Navigate Through the Repo"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "In the data folder, you'll find the college basketball datasets as well as csv files filled with various tested models.\n",
    "\n",
    "The data_cleaning.ipynb file illustrates our data cleaning and exploratroy data anaylsis process.\n",
    "\n",
    "The feature_models.ipynb file showcases our feature engineering and the testing of different models.\n",
    "\n",
    "The predictions.ipynb shows our final model in action, with its various predictions on the upcoming college basketball 2022 class. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Overview\n",
    "\n",
    "[1]: https://www.kaggle.com/datasets/adityak2003/college-basketball-players-20092021?select=modern_RAPTOR_by_player.csv \"College Basketball Players Dataset\"\n",
    "\n",
    "This project analyzes the data from [College Baseketball Players Dataset][1] in Kaggle. The data consists of detailed college players stats from 2009 - 2021, and players stats from 2022. Another data contains the info of college players who were drafted to NBA teams in both round 1 & 2.  \n",
    "\n",
    "Based on dataset, we are using machine learning models to determine the college players' quality for for draft round 1 and draft round 2 and provide suggestions for New York Knicks. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Business Problem\n",
    "\n",
    "The New York Knicks have been struggling for years to perform competitvely in the league for a long time. There are several ways to build a team through the draft, free agency, and trades. Ideally, there would be a balance between the methods. Unfortunately, the Knicks haven't been successful with their young players to build through the draft. The last player drafted by the Knicks to sign a multi-year deal after rookie deal was Charlie Ward, who was drafted in 1994.\n",
    "\n",
    "Our model's purpose is to classfy the upcoming 2022 rookie class to optimize the franchise's draft strategy. So they can acquire the quality players, who can increase the team's performance for years. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Data Understanding\n",
    "\n",
    "The College Basketball Players 2009-2021 (`CollegeBasketballPlayers2009-2021.csv`) has the detail statistics of each college players from 2009 to 2021. We combined it with DraftedPlayers2009-2021(`DraftedPlayers2009-2021.xlsx`), so we have the draft pick info if the players were drafted to the NBA teams.\n",
    "\n",
    "The College Basketball Players 2022 (`CollegeBasketballPlayers2022.csv`) has the detail statistics of each college player from 2022, which we have tested on our final model. "
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Methods\n",
    "\n",
    "This project tests various machine learning models, including Logistic Regression, Decision Tree, K-Nearest Neighbor, Random Forest, Extra Trees, and various other ensemble methods. We first created the baseline models with basic parameters to analyze how the predictors performed. Then we applied hyperparameter tuning on different models using the Pipeline, GridSearchCV, and RandomizedSearchCV to find the best working model. We further optimize by combining the tuned models into various ensemble models such as Stacker Classifier and AdaBoosting."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Conclusions\n",
    "\n",
    "After many tests, the best model is GradientBoosting from sklearn.ensemble. We reached 85% accuracy scores on testing data and 79 % validation on training data."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Next Steps\n",
    "Further analyses could yield additional insights to improve to our predicition models:\n",
    "\n",
    "- Drafted players performance in NBA: Compare players’ performance in NBA vs College to predict whether college performance predicts NBA performance.\n",
    "- Impact on the player positions: Analyze player positions impact on performances and change in positions if any.\n",
    "- Round Selected and Pick Number: Further classify the round and the order of picks. Ex: Player one is predicted first round pick three"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.8.5"
  },
  "toc": {
   "base_numbering": 1,
   "nav_menu": {},
   "number_sections": true,
   "sideBar": true,
   "skip_h1_title": false,
   "title_cell": "Table of Contents",
   "title_sidebar": "Contents",
   "toc_cell": false,
   "toc_position": {},
   "toc_section_display": true,
   "toc_window_display": false
  },
  "varInspector": {
   "cols": {
    "lenName": 16,
    "lenType": 16,
    "lenVar": 40
   },
   "kernels_config": {
    "python": {
     "delete_cmd_postfix": "",
     "delete_cmd_prefix": "del ",
     "library": "var_list.py",
     "varRefreshCmd": "print(var_dic_list())"
    },
    "r": {
     "delete_cmd_postfix": ") ",
     "delete_cmd_prefix": "rm(",
     "library": "var_list.r",
     "varRefreshCmd": "cat(var_dic_list()) "
    }
   },
   "types_to_exclude": [
    "module",
    "function",
    "builtin_function_or_method",
    "instance",
    "_Feature"
   ],
   "window_display": false
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
