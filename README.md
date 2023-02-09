Repo consists of 5 notebooks:

1 - EDA_ML_DNN_Alcohol_consumption.ipynb - The data is downloaded from Kaggle and as the name reads, dataset is dedicated to Alcohol consumption based on WHO report published in 2018. Basic analysis is the first to discover the base attributes, features, type of data, .. of dataset followed by EDA with various analysis and data descriptions by means of Matplotlib artists and Seaborn. As within the data we can see Recorded and Unrecorded consumption which is based only on assumption of experts, I have tried to prepare ML linear regression and DNN regression model to predict Unrecoreded consumption based on Recorded. First simple Linear regression model is not very precise, after cleaned outliers we can obviously obtain better precission, and even with very simple DNN network (outliers cleaned) we can obtain MAE 0.73. Of course, several model can be used, such as decission tree, or XGBOOST as ensamble model. By easy change of output (scale instead of direct value) we can switch to classification. 

2 - EDA_ML_RFE_GridSearchCV_KFold_Cardio Fitness Dataset.ipynb - The data is downloaded from Kaggle, however no more info provided about various features. I have done  standard basic analyses followed by EDA, again artists by Matloblib and Seaborn, e.g. heatmap and pairplot offer quite interesting view of correlation among various features. I have decided to prepare model to predict expected run miles based on various features. In order to rule out not useful models, the very first short "first_check" function to be used on small dataset. In order to simplify model I have used LinearRegression model to go further on with K_fold and Grid search used to find the best hyperparameters, function RFE has been used to define the best suitable features. By means of all these features, R2 score is 0.79 what with only 180 lines of dataset is quite good (if not overfitted). 

3 - EDA_NLP_Drugs_side_effects_drugs.ipynb - Again the data is downloaded from Kaggle and are dedicated to Drugs side effects. Like in examples above, first basic and then EDA has been done. I have decided to make NLP model which can based on input text of side effect define the at least generic name. Feature engineering has been done to clean the data such as removing of stopwords followed by tokanization and padding of dataset. Standard tensorflow DNN with first Embedding layer has been done, then flattened followed by Dense layers and trained, validation accuracy unfortunately not OK. 

4 - EDA_Productivity Prediction of Garment Employees.ipynb - Data from Kaggle followed by basic and deeper EDA with heatmap. 

5 - EDA_XGBOOST_Risk_Factors_for_Cardiovascular_Heart_Disease.ipynb - Data as usual from Kaggle, Basic analysis followed by EDA and data wrangling. There are many issues with precision of data such as not correct height, weight, systolic and diastolic heart pressure. I have tried to clean, covnert, adjust, ... some of them but I kept these in some level just to finalize the notebook. In this one case eXtra Gradient Boost ensamble model known as XGBoost has been used (ensabmle for Decission trees with voting) with final precision of 72% what is quite low for this type of model. The main issue I see with not OK input data. 
