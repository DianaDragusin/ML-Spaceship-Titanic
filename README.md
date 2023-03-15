# ML-Spaceship-Titanic
During my participation in the Spaceship Titanic competition on Kaggle, I developed and implemented a solution that achieved an accuracy rate of 0.79307. The objective of the project was to predict which passengers were transported to another dimension when the spaceship collided with the spacetime anomaly, using data from .csv files containing passenger information.

Throughout the project, I gained a deeper understanding of machine learning theory and familiarized myself with various classifiers. Additionally, I explored different optimization techniques such as data imputation, feature engineering and hyperparameter tuning, which helped me improve the accuracy of my model.

The first method I used to improve the accuracy of my model was data imputation, which resulted in an accuracy of 0.78770. I used the 'mean' strategy for numerical values and the 'most frequent' strategy for string values. For the 'Transported' column, which was a boolean type and did not have any null values, I did not use any imputation strategy. The model was able to learn better as it had more data to work with.

The second method I used was feature engineering, in which I closely analyzed the features of the model. First, I plotted mutual information to estimate the amount of information that a feature provides about the target variable. I noticed that the 'Vip', 'Age', and 'Destination' features assigned very little information about the target variable, so I decided to remove them from the model's features. This decision led to an improvement in the model's accuracy, which reached 0.79261 . 

I conducted some additional experiments, such as considering the money spent on the spaceship as an indicator that the people were not in cryosleep. However, this new feature only complicated the model. Next, I investigated the 'Cabin' column and split it into three columns, and finally, I removed the 'PassengerId' and only used the passenger's group because several passengers belonged to the same group and may have shared the same fate as a result of staying together. 

The third method I used was hyperparameter tuning for the RandomForestClassifier. I defined a set of parameters and used a GridSearchCV on the model with these parameters. This process was used to find the best possible configuration to maximize the accuracy. Different configurations of the parameters led to different performance scores. By this time my accuracy rate reached 0.79307.
