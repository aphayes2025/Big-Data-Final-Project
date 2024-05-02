# Big-Data-Final-Project

Abstract

I developed a machine learning model using NFL game logs spanning four seasons (2019-2022) to predict game outcomes. Leveraging data visualizations, I discerned feature relationships and trained a feed forward neural network model, achieving a 60% prediction accuracy.

Introduction

My long-standing interest in American football led me to create a machine learning model for predicting NFL game outcomes. Motivated by a competitive football pool with friends, I aimed to gain an edge using machine learning techniques. The model was trained on pregame features like average points per game, QB rating, and team momentum. 

Theory and Methods

Utilizing feature engineering and aggregation, I crafted additional metrics such as average points and recent win percentages. Data visualization aided in identifying relevant features and mitigating multicollinearity issues. The dataset, containing over a thousand rows and fifty-six features, underwent training and testing split using scikit-learn. A neural network model with four dense layers was constructed and trained using ReLU activation functions and the Adam optimizer.

Results

The model achieved just below 64% accuracy after 10 epochs of training. A graph depicting training and validation accuracy was provided.

Discussion

Despite efforts to improve consistency, the model exhibited wide accuracy variations. Interestingly, features like sacks and rushing attempts showed high correlations with winning outcomes. Weather data integration yielded inconclusive results, despite notable weather-impacted games like Bears vs 49ers Week 1, 2022.

Conclusion

The project yielded a machine learning model predicting 60% of NFL games correctly, offering potential competitive advantage in football pools.

References

Marin, Pol. “Netty - My Personal NBA Game-Winner Predictor.” Medium, Data & Sports, 13 Jan. 2024, medium.com/data-sports/netty-my-personal-nba-game-winner-predictor-63cc728025c5.

Sadness, The Factory of. “Machine Learning Model for NFL Betting (Model 5.0).” Medium, Medium, 15 May 2023, medium.com/@bravenewworld21/machine-learning-model-for-nfl-betting-model-5-0-8e916428c330.

Fivethirtyeight. “Data/NFL-Elo at Master · Fivethirtyeight/Data.” GitHub, github.com/fivethirtyeight/data/tree/master/nfl-elo. Accessed 22 Apr. 2024.

“NFL Team Stats 2002 - Feb. 2024 (ESPN).” Kaggle, 15 Feb. 2024, www.kaggle.com/datasets/cviaxmiwnptr/nfl-team-stats-20022019-espn.
