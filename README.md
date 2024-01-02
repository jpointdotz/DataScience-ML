Repo consists of these notebooks:

1 - EDA_ML_DNN_Alcohol_consumption.ipynb - The data is downloaded from Kaggle and as the name reads, dataset is dedicated to Alcohol consumption based on WHO report published in 2018. Basic analysis is the first to discover the basic attributes, features, type of data, .. of dataset followed by EDA with various analysis and data descriptions by means of Matplotlib artists and Seaborn. As within the data we can see Recorded and Unrecorded consumption which is based only on assumption of experts, I have tried to prepare ML linear regression and DNN regression model to predict Unrecoreded consumption based on Recorded. First simple Linear regression model is not very precise, after cleaning of outliers we can obviously obtain better precission, and even with the very simple DNN network (outliers cleaned) we can obtain MAE 0.73. Of course, several models can be used, such as decission tree, or XGBOOST as ensamble model. By easy change of output (scale instead of direct value) we can switch to classification. 

2 - EDA_ML_RFE_GridSearchCV_KFold_Cardio Fitness Dataset.ipynb - The data is downloaded from Kaggle, however no more info provided about various features. I have done  standard basic analyses followed by EDA, again artists by Matloblib and Seaborn, e.g. heatmap and pairplot offer quite interesting view of correlation among various features. I have decided to prepare model to predict expected run miles based on various features. In order to rule out not useful models, the very first short "first_check" function to be used on small dataset. In order to simplify model I have used LinearRegression model to go further on with K_fold and Grid search used to find the best hyperparameters, function RFE has been used to define the best suitable features. By means of all these features, R2 score is 0.79 what with only 180 lines of dataset is quite good (if not overfitted). 

3 - EDA_NLP_Drugs_side_effects_drugs.ipynb - Again the data is downloaded from Kaggle and are dedicated to Drugs side effects. Like in examples above, first basic and then EDA have been done. I have decided to make NLP model which based on input text of side effect can define at least the generic name. Feature engineering has been done to clean the data, e.g.removing of stopwords and followed by tokanization and padding of dataset. Standard tensorflow DNN with first Embedding layer has been set, then flattened and followed by Dense layers and trained. Validation accuracy unfortunately not OK. 

4 - EDA_Productivity Prediction of Garment Employees.ipynb - Data from Kaggle followed by basic and deeper EDA with heatmap. 

5 - EDA_XGBOOST_Risk_Factors_for_Cardiovascular_Heart_Disease.ipynb - Data as usual from Kaggle, Basic analysis followed by EDA and data wrangling. There are many issues with precision of data such as not correct height, weight, systolic and diastolic heart pressure. I have tried to clean, convert, adjust, ... some of them not possible to fully clean, so I kept some respective level just to finalize the notebook. Even there is no need to scale or normalize data when dealing with DecisionTree method, I am going to try out DNN as well so I perfomed scalling as well. In this one case eXtra Gradient Boost ensamble model known as XGBoost has been used (ensamble collection of Decission trees with voting) with final precision of 72% what is quite low for this type of model. The main issue I see are not OK input data. The analysis completed with DNN model (tensorflow) and with 100 epochs the model ended with the similar results like XGBoost but confusion matrix differs. 

6 - EDA_Regularization_of_Linear_Regression-L1-L2-L1L2.ipynb. Data of housing prices from Kaggle for regression model. The goal is to compare various regression models and the use of regularization L1, L2 or both. The data has been analyzed and fixed, as the dataset is very skewed normalization by means of PowerTransformer and method Yeo-Johnson has been applied what improved data a lot. There are highly correlated features among the data based on correlation analysis and in addtion Variance Inflation Factor formule has been applied to check the data as well. Four models : LinearRegression, LassoRegression, RidgeRegression and ElasticNet for data with NOT fixed and fixed Multi-Collinearity has been provided, however I did not find any improvement with regularization. On the other side, no GridSearchCV method to tweak hyperparamaters has been used, so the task for next time along to automatic pipeline. In these examples, the data without fixed collinearity had better results in terms of R2 and MSE, however we were using less features (multicollinear features have been dropped) what is not good approach with small volume features instead of creating/combining into different ones if possible out of context.

7 - EDA_LinearRegression-CooksDist_InfluentialPoints.ipynb - Dataset for linear regression of relationship between work experience and salary downloaded from Kaggle. Intention of this notebook is looking for outliers and influential points using Cook's distance, as outliers are quite tricky question ... Dataset is like expected quite normally distributed what is quite visible from histogram and Q-Q graphs, however standard deviation is quite high. I have perfomed standard OLS - Ordinary Least Squere method on datasted and R2 was 0.663, in order to see how the model will behave I have artifically added outlier which is marked in scatter by red color, after OLS fit R2 moved to 0.644 . There are different informations how the cook's distance should be set, as in my point of view with high variance of dataset it can differ. I have set the 4*cooks_d.mean() and the results you can see in graphs - the influential points which fulfill requirement are shown in red.

8 - EDA_DealingNonNormal_StubbornData.ipynb - Dataset from Kaggle but only one column used - df['price'] - Data are quite right skewed with long tail at first sight with non normal distribution. Various techniques used to obtain normal distribution - Logarithm, Lognormal, Box-Cox (lambda = -1. is a reciprocal transform, lambda = -0.5 is a reciprocal square root transform, lambda = 0.0 is a log transform, lambda = 0.5 is a square root transform, lambda = 1.0 is no transform) with calculated lambda -0.628, Reciprocal, Square Root and Yeo-Johnson transformation. 

9 - EDA_Drugs_DecisionTree_GridSCV_Pipeline.ipynb - Dataset from Kaggle, short basic analysis and EDA followed by Scikit DecissionTreeClassifier classification model using Pipeline with GridSearchCV for hyperparameters tuning. The best resutls on train set 0.5625 and on test set 0.35 only what I explain by low volume dataset consists only of 200 rows with 5 target values. 

10 - _Derivatives_QuadraticFunctionsOnly.ipynb - One short evening spent with calculation of derivative of quadratic functions, its derivative and tangent line based on results. In two plots are depicted function itself, tangent line + line equation in defined point and derived function.

11 - _HypotesisTesting-T-test-P-score-ConfidenceInterval.ipynb - playing with inferential statistics and hypotesis testing, p-value and confidence interval on dataset from Kaggle. Data of salary considered as the whole population and sample size of 30 used for inference. 
