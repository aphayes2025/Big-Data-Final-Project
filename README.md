# Big-Data-Final-Project

Abstract


I used football game logs from four NFL seasons (2019-2022) to create a machine learning model that would predict the outcome of a game. I used data visualizations to help me figure out the relationships between my features and predictions. I then trained a feed forward neural network model to then predict the winner of each game. The model successfully predicted 60% of the games correctly.
Introduction

	I have been following American football since I was a kid, and spend a lot of time watching the sport with my friends and family. Every year my friends and I take part in a season-long football pool, where each person picks a team to win each week. If the team that you selected wins, you advance to the next week. The catch is that you can’t select the same team again. My friends get very competitive and invest a lot of time looking at which teams will win each week. The premise of my project is to create a machine learning model that could predict which NFL team would win. I wanted to leverage machine learning in order to gain a competitive advantage over my friends in our league pool. I decided to train the model on features that we see from a pregame point of view. These features include average points per game, elo qb rating, team momentum based on the previous 5 game win percentages, and other relevant team metrics indicative of a team's performance. Overall, my goal is to use machine learning to gain an edge in predicting NFL game outcomes and beating my competitive friends.


Theory and Methods

	In the first phase of my project, I used feature engineering and aggregation to create additional features. Specifically, I created metrics like average points per game and percentage of wins in the last five games through data aggregation. This approach proved to be a lot easier than sourcing these niche statistics from an external platform through an API or web scraping. I then converted all of my features into averages, to create a pregame view of both teams. I did this with a dictionary by keeping track of the team names as the key for each feature.
Next, I used data visualization in order to help me discern what features were relevant to predicting a game's outcome. I created multiple heatmaps of feature correlations to identify relationships between different features and their impact on the outcome. My goal was to find any potential multicollinearity issues among my features to create a more optimal model. I ended with fifty-six features for over thousand rows of data.  
Finally, I ridded of all rows that were week 1, since they didn't have any averages yet.  Having identified key features, I split the data up into training and testing data using scikit-learn. Then I constructed a neural network model comprising four dense layers. The first three layers contained 64, 32, 32 neurons respectively, using ReLU activation functions. The final layer consisted of a single neuron with a sigmoid activation function, for binary classification. The model was compiled with the Adam optimizer and a binary cross-entropy loss function. I trained the model for 10 epochs, with a validation split of 20% to monitor the models performance.
Results

A heatmap of feature correlation provides the pairwise relationships between our variables. The bottom rows contain the correlations between the given features and the predictor (win). 

Above is my model that I created. I trained for 10 epochs and scored an accuracy of just below 64%. 



Here is a graph displaying the training accuracy and validation accuracy throughout my model. 
Discussion
	The most interesting result was the inconsistency of my model when fitting. The accuracies ranged from 52-65%, a very wide range for a feed forward neural network. I tried to improve the consistency through learning rate tuning, and dropout layers for regularization. Both these techniques did not prove to help. Additionally, examining feature correlation matrix heatmaps was interesting. Features like number of sacks, and number of rushing attempts correlated very highly with winning outcomes, contrary to what I would guess as a fan. 
Also, I explored how weather affected football games, however this effort turned out to be futile. I first got the latitude and longitude of every stadium and then added those as columns for every game I had in my dataframe. After I used the free OpenMeteo API and got the temperature, wind speed, and precipitation amount. I could not find a big enough correlation for the data to be useful in my model. Even though there were a handful of games that the scores were heavily affected by weather (Ex: Bears vs 49ers Week 1 2022 season). I believe with more time I could find a better way to scale the impact weather had on games. 
In addition, I could have explored better types of models suited for my data or other ways to stabilize it. Also, with the right data, I believe people could develop a similar model to make profits from sports betting. By using past sport betting lines, spreads and more, it could provide accurate results. 
Conclusion
In this project, I hoped to create a machine learning model that would be able to accurately predict football games. I used data science methods that I had learned from this course to complete this, creating a machine learning model that predicted 60% of games correctly. My friends aren’t ready for me to win the football pool this year!


References
Marin, Pol. “Netty - My Personal NBA Game-Winner Predictor.” Medium, Data & Sports, 13 Jan. 2024, medium.com/data-sports/netty-my-personal-nba-game-winner-predictor-63cc728025c5. 
Sadness, The Factory of. “Machine Learning Model for NFL Betting (Model 5.0).” Medium, Medium, 15 May 2023, medium.com/@bravenewworld21/machine-learning-model-for-nfl-betting-model-5-0-8e916428c330. 
Fivethirtyeight. “Data/NFL-Elo at Master · Fivethirtyeight/Data.” GitHub, github.com/fivethirtyeight/data/tree/master/nfl-elo. Accessed 22 Apr. 2024. 
“NFL Team Stats 2002 - Feb. 2024 (ESPN).” Kaggle, 15 Feb. 2024, www.kaggle.com/datasets/cviaxmiwnptr/nfl-team-stats-20022019-espn. 
