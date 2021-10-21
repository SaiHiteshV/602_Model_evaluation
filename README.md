# 602_Model_evaluation

### Observation
#### Data
- The data has no missing values.
- The data has no categorical variables.
- The columns Number of pregnancies, Triceps skinfold thickness, Serum insulin, Diabetes pedigree function and Age are right skewed.
- The columns Plasma glucose, Diastolic blood pressure and Body mass index have a normal distibution.
- The target variable is imbalanced.

#### Simple Logistic regression model
- The accuracy of the model is 69.6%
- As the target variable is unbalanced I am selecting recall as a measure to determine the performance of the model.
- Out of 100 0's the model can recall 76 of them and out of 100 1's the model can recall 63 of them.

#### Creating Pipeline for Logistic regression with Grid search view using accuracy
- For the grid search with accuracy as the main evaluation criteria the model has a best score of 0.777.
- The best set of hyperparameters for this model are C : 1, Class weight : None, and solver : loblinear

#### Creating Pipeline for Logistic regression with Grid search view using recal
- For the grid search with recall as the main evaluation criteria the model has a best score of 0.738.
- The best set of hyperparameters for this model are C : 1, Class weight : balanced, and solver : sag.
- Despite a lower score compared to the previous model the second model performs better for classification.
