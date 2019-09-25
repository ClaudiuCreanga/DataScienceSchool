exploratory data analysis -> the main task here is the selection and refining the features of the model

-> it is the hotspot of the system. you can come back and readjust. important to get it right.

in life science most of the data is frozen, retrospective. we don't have access to the patient to get more data from him, as google ads more data continuously from it's searches

cross validation score. you take the train data and run the crossvalidation for the data. for ex you run it 10 times, each time you take a block of 10% of the data as validation and you calculate your accuracy score. at the end you get an average accuracy score and you compare it to the accuracy score of the test. if it's much bigger then you overfitted. 

in the cross validation we see how the model perdforms with different sample sizes.
we want a model that changes with different samples, otherwise it's a sign that we overfit. 
cross validation is a good way to see if you're model is overfitting. 

when you see the training score and the validation score being the same for different sizes of the data then you can deduct that it is the best size. if you see the training score getting closer to the validation score it's good because your model will generalise better. you want the two lines to converge. 

irvine machine learning repository is good

with cross validation you can do parameter tuning, you also get an idea of how well your model generalise to new data. 
http://adni.loni.usc.edu/
https://github.com/cambiotraining/DataScienceSchool
https://github.com/adrianobioinfo/autumn_school

reduce outliers in feature engineering

if 2 features are highly correlated then you can merge them into 1
 
 you can see the importance of feature with sklearn with model.feature_importances_
 
you can check for the optimal number of features with sklearn with RFECV:
https://scikit-learn.org/stable/auto_examples/feature_selection/plot_rfe_with_cross_validation.html

model.score(X_test, y_test)
model.score doesn't take predictions, it takes the x_test as the first param. 

Principal component analysis -> PCA: used to reduce the dimensionality of your model. you take only the features that describe the most variance among the data. so maybe only 3 features are enough for you to predict the data. 

After trying multiple models, it's a good idea to use a Voting Classifier. You pass all the predictions to a voting classifier and this classifier will take the best feature detections from every classifier. 
this is called stacking models on top of each other -> e used to combine information from multiple predictive models to generate a new model

Gaussian processes go really well with small datasets. Another advantage that you are unlikely to overfit because the model is very flexible. You are pretty sure how the model will perform in practice.
you have a prior. you chose this prior before you look at any data. and then as you see the data you adjust the prior function. 
The prior function has a likelihood that 

https://www.automaticstatistician.com/index/

Bayesian inference

Bayesian inference -> a method for updating our beliefs about the world based on evidence that we observe

