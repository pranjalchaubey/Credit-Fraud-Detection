# Credit-Fraud-Detection
Detecting credit card fraud using classic ML algorithms. Nothing fancy here.

<br/>Dataset is supplied by Kaggle, _IEEE-CIS Fraud Detection_.  
You can check about the contest here,  
https://www.kaggle.com/c/ieee-fraud-detection/data

------------

This repository was created to practice applying ML algorithms on imbalanced datasets, and try feature selection techniques.  
The inherently imbalanced dataset was balanced using _random undersampling_. Oversampling using _SMOTE_ was also considered but discarded since the machine running the notebook was old, and the dataset is large (over half a million rows with 430+ columns).

<br/>Feature selection on the dataset was done using the _Boruta algorithm_ (Borutapy library). Correlations among the features were checked before and after feature selection. Below are the feature correlations of the selected features,  
<br/>
[![Correlations: Selected Features](https://github.com/pranjalchaubey/Credit-Fraud-Detection/blob/master/img/corr_selected_features.png "Correlations: Selected Features")](https://github.com/pranjalchaubey/Credit-Fraud-Detection/blob/master/img/corr_selected_features.png "Correlations: Selected Features")

<br/>Logistic Regression Classifier was used to predict whether a transaction was fraud or not. Since no feature engineering was performed, the classifier had a recall of 56% on the test dataset. Note that in these kind of ML problems, _recall_ matters more than _accuracy_.  
Below is the confusion matrix obtained from classifier predictions, 
<br/><br/>
[![Confusion Matrix](https://github.com/pranjalchaubey/Credit-Fraud-Detection/blob/master/img/confusion_matrix.png "Confusion Matrix")](https://github.com/pranjalchaubey/Credit-Fraud-Detection/blob/master/img/confusion_matrix.png "Confusion Matrix")
