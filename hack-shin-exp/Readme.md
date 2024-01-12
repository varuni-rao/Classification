This folder contains a few notebooks I worked on as a part of a hackathon conducted at the end of Applied Data Sciences course offered by MIT Professional through Great Learning
We worked on it as a part of a 3 member team. However, the notebooks uploaded here includes only my work, so there are some missing links that was worked on by my other team members.

The objective is to determine the Overall Experience rating given by passengers of Shinkasen bullet travel based on the dataset made available. The dataset is provided in 4 .csv files. 
- Two files for the train set - Traveldata_train and Surveydata_train
- Two files for the test set - Traveldata_test and Surveydata_test

As a part of the project, I first did the necessary data preprocessing, which included merging the dataframe, statistical analysis, univariate and bivariate analysis, 
followed by missing values imputation and feature engineering (replacing string values with ordinal values for rating). 
To impute missing values, we used KNNImputer and I ran a loop to determine the accuracies for each value of k with XGBoost and finally selected the one that gave the best test accuracy.

Then we used MinMaxScalar to scale the dataset and make it ready for building models.

First, we tested the performance of all classifiers on the dataset and selected the top 7 which gave us an accuracy of more than 0.9 
- CatBoost, XGBoost, LightGBM, HistGradientBoosting, Random Forest, Extra Trees and MLPClassifier.
- I also built a Keras Sequential Classifier model which gave me an accuracy of over 0.94
- Finally, built the voting and stacking ensemble models using different combinations of top models.
- There are 2 versions of this: KNN14, which is using all features and 22features, which uses 22 features and was found to provide optimum solution by my team member using backward feature selection.
- Then I also used AutoML from flaml library to run some automated model selections to see if we find any model that gives us optimum results better than the regular GridSearch/RandomizedSearch and Optuna used by us for hyperparamter tuning

We achieved an accuracy of 0.9561 and ended up 7th on the leaderboard. The top accuracy was 0.9581. However, the whole process was incredible because in the short period of 10 days, I got to learn how to do classification, and also some new libraries such as Optuna, flaml and H2O which I had not learned earlier. I am still working on the H2O file and once it is ready, I will upload the same to this folder.
