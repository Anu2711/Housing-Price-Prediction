This folder contains the random forest model trained to predict housing prices.

To obtain the final model, the following steps were applied:

* Preprocessing: This step involved creating some new variables and converting the existing variables into a more desirable form.
* Data Analysis: This step involved plotting the predictors against the response variable to better guess the relationship between the two. Additionally, some weird data points were identified and fixed in this step.
* Imputing Missing Data: The train and test data had missing values for some predictors such as `ayb`, `yr_rmdl`, `kitchens`, `stories` and `quadrant` which were imputed by intuition as well as by identifying the trends in those predictors.
* Initial Model Building: Then, the initial model was constructed.
* Iterative Model Building: Once the initial model was obtained, based on the residual plots a logarithmic transformation was applied to the response variable. This helped make the residual plots randomly distributed. After transformation, the dimension of the basis used to represent some of the smooth terms (`k`) (such as for `latitude`, `longitude`, `saledate`, `gba`, `bedrm` and `yr_since_rmdl`) was modified, which helped minimise the GCV. Finally, interaction terms were added to further minimise the GCV and obtain the final model.

The evaluation metric for this kaggle competition was RMSLE (Root-Mean-Squared-Logarithmic-Error).
The kaggle public score obtained for this model was: 0.13236
The kaggle private score obtained for this model was: 0.13801
