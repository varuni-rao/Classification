This folder contains the Notebook file for Predicting Loan Default of applicants.

The dataset was provided to us as part of Capstone Project for the MIT/GL ADSP program. While, I worked on the Regression Project, I have worked on this dataset post my course.
For this project, I selected Recall as the metric to compare performance. 
Here, we need to make sure that we are correctly able to detect all the applicants who default, rather than how many predictions are correct. Hence, the choice of metric

The dataset has 5960 rows and 13 columns. 
It has some outliers and spurious data as well as missing values. 
The features are a mix of numerical and categorical data. 
I use 3 different statistical methods to detect outliers and using domain knowledge treat only the ones that are questionable before the split.
Next, I split the dataset and then use Iterative Imputer which is still in trial stage to impute missing values and Isolation Forest to compare the outliers in train as well as test set.
Then, I try a bunch of sklearn models and tree-based models to see which model fits the best to this particular dataset and select the top 6 and hyperparameter tune them.
Finally, with about 21 models obtained by hypertuning, I select the best model, which turns out to be ExtraTreesClassifer.
As a topping on the cherry, I also combined the 2nd best to 6th best model from different algorithms, and combined their results using a hard voting Classifier to check if they outperform ExtraTreesClassifier, but, theye did not.

Other combinations of ensemble of these models, such as soft voting, fewer models, or stacking or weighted voting and weighted stacking can also be tried int he future.
