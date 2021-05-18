# titanic

The titanic dataset was analysed to check the possibility of survival of a particular passenger given their gender, where they will be gettinoff, their age, whether they were
first class passengers or not and so on.

Preprocessing:
Age, Cabin and Embarked variables had missing values in them. The Cabin variable was dropped due to having almost 77% of its values missing. 
Missing values in age was imputed with the median and the missing values in Embarked variable was imputed with the mode. 
Categorical variables (Sex, Embarked) were category encoded. 
As there was a class imbalance in the target variable (Survived), resampling techniques (SMOTE; Synthetic Minority Oversampling Technique) were applied to create balance in 
the train set. 

Model Fitting:
Random Forest model was fitted first (Decision trees not considered as they are weak learners). 
GridSearchCV was carried out to tune the paramenters of the random forest model. 
The tuned random forest model yielded an accuracy of 83%. This model gave a kaggle score of 0.7578..

Next, ensemble learning techniques were considered (Adaboost, GradientBoost, XGBoost)
The Adaboost model gave an accuracy of 84.3%, Gradientboost model gave an accuracy of 83.9% & XGBoost model gave an accuracy of 85.8%
Since XGBoost model resulted in the highest accuracy out of the other boosting techniques, hyperparameter tuning was only conducted for this model.
The tuned XGBoost model gave an accuracy of 85.4% and the kaggle score was 0.78229

