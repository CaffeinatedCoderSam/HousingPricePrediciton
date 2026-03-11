# HousingPricePrediciton
1. Introduction:
This project involved predicting house prices using the Ames dataset through exploratory data
analysis (EDA), advanced feature engineering, and the application of two machine learning
models: Random Forest and Gradient Boosting. The model performance was evaluated using
Log-RMSE on validation and test sets.
2. We first begin with Univariate and Bivariate EDA.
Univariate EDA: We visualized the distribution of SalePrice (log-transformed) and Gr Liv
Area to check for skewness and outliers.
Bivariate EDA: We plotted Gr Liv Area vs. log(SalePrice) and Garage Area vs.
log(SalePrice) to confirm their strong predictive relationship with the target variable.
3. Then we move onto creating 4 engineered features. Here is a list of the features we
have created and why:
LuxuryScore: A binary composite feature indicating whether a home is both large (>2500
sq ft) and has a spacious garage (>600 sq ft).
GarageEfficiency: Ratio of garage area to living area; useful for capturing relative garage
sizing.
AgeCat: House age binned into categorical groups (New, Modern, Old), which were
one-hot encoded for model use.
IsOverbuilt: A binary flag showing if the garage area is disproportionately large relative to
the house size (>80%).
Garage_YearBuilt: An interaction feature combining garage size and build year to reflect
changes in home construction trends.
4. Once we have completed EDA and feature engineering, let’s look at how we would be
splitting the data into train, test and validation sets and why we have chosen this.
60% Training, 20% Validation, and 20% Final Test.
Ensures models are tuned on validation data and evaluated fairly on a truly unseen test
set.
Helps avoid overfitting and gives a realistic view of future performance.
5. We have used an ensemble method where we use Random Forest algorithm along
with Gradient boosting for building the model. Here is a brief overview of the same:
Random Forest Regressor: Tuned max_depth, n_estimators, and max_samples.
Provided strong performance and clear feature importance.
Gradient Boosting Regressor: Tuned learning_rate, n_estimators, max_depth, and
subsample. Delivered better validation Log-RMSE and was selected as the final model.
Finally, to finish it off, we have re-trained the train and validation sets.
6. Conclusion:
All feature engineering was applied identically to both training and test sets.
One-hot encoded categories were aligned manually between train/test to avoid
mismatched dimensions.
Each step is clearly labeled and explained in markdown within the notebook.
Models were evaluated correctly using Log-RMSE, and features were interpreted
post-training to supp
