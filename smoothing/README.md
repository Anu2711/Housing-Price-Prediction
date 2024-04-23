This folder contains the random forest model trained to predict housing prices.

To obtain the final model, the following steps were applied:

* Preprocessing: This step involved creating some new variables and converting the existing variables into a more desirable form.
* Data Analysis: This step involved plotting the predictors against the response variable to better guess the relationship between the two. Additionally, some weird data points were identified and fixed in this step.
* Imputing Missing Data: The train and test data had missing values for some predictors such as `ayb`, `yr_rmdl`, `kitchens`, `stories` and `quadrant` which were imputed by intuition as well as by identifying the trends in those predictors.
* Model Building: To build the model, the `ranger` function in the `ranger` library was used. To improve the accuracy of the model, the parameters, `mtry`, `min.node.size` and `split.rule` was tuned using grid search. The best model was selected depending on which model had the highest $R^2$ value.

The evaluation metric for this kaggle competition was RMSLE (Root-Mean-Squared-Logarithmic-Error).
The kaggle public score obtained for this model was: 0.20693
The kaggle private score obtained for this model was: 0.19368
