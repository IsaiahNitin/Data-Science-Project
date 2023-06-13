# Data-Science-Project
ASSESSING THE ACCURACY OF FETAL HEALTH PREDICTIONS FROM CARDIOTOCOGRAM DATA 
In this study, we aim to build a classification model to predict fetal health as Normal, Suspected or Pathogenetic based on three variables: Baseline Fetal Heart Beat (Baseline), Abnormal Short Term Variability (asv) and Percentage of time with abnormal long-term variability (plv). To accurately compare the variables, they must be scaled.

The dataset is then divided into a training dataset comprising 75% of the data and a test dataset comprising the remaining 25%. The training dataset is used to build and train our model, while the test dataset is used to assess the accuracy of our model.

To build our classification model, we use the k-nearest neighbors function with a rectangular weight function and a tunable number of neighbors. The engine is set to "kknn" (k-NN), and the mode is set to "classification".

We use the fit function to train our model, passing the k-nearest neighbors specifications with the fetal health variable as the target and with the Baseline Fetal Heart Beat (Baseline), Abnormal Short Term Variability (asv) and Percentage of time with abnormal long-term variability (plv) as our predictors.

Next, the training dataset is divided into 10 cross-validation folds, with the target variable (fetal_health) as the stratification variable. After drawing a cross-validation plot, we could select the most accurate K nearest neighbor value for our model.

Subsequently, our best k-NN model specification is created, and a new workflow is created, which adds the recipe and best model specification. The model is then fitted on the training data to make predictions on the test data (fetal_health_test).

Lastly, we try to evaluate the accuracy and confusion matrix for the k-Nearest Neighbors classification model. If the accuracy is high, our model is effective at predicting fetal health. If the accuracy is low, we may need to revise our variables and repeat the process.

To visualize our results, we will create a scatter plot of the predicted fetal health against one of the predictors, such as Baseline Fetal Heart Beat (Baseline), Abnormal Short Term Variability (asv) or Percentage of time with abnormal long-term variability (plv). This can help us see how well our model is able to separate the different classes of fetal health based on these predictors.
