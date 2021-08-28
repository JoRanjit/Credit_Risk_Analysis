# :credit_card: Credit_Risk_Analysis

### Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Machine learning is the use of statistical algorithms to perform tasks such as learning from data patterns and making predictions. There are many different models - this project employs *'imbalanced-learn' and 'scikit-learn'* libraries to build and evaluate models using resampling.
#### We are using the credit card credit dataset from LendingClub, a peer-to-peer lending services company. 

#### As part of deliverable 1 - we use Resampling Models to Predict Credit Risk and SMOTEENN algorithm to predit credit risk. And we will compare the accuracy scores of each algorithm. With each model we will calculate the following:
:one: Accuracy Score
:two: Confusion Matrix
:three: Imbalanced Classification Report

#### :black_medium_square: Step #1 - We oversampled this data using 'RandomOverSampler' algorithm:

:ballot_box_with_check: The model's Accuracy Score = 0.6814

![naive_score]( https://github.com/JoRanjit/Credit_Risk_Analysis/blob/main/Images/naive_ROS_metrics.PNG)

#### :black_medium_square: Step #2 - Next we used SMOTE Oversmapling algorithm:

:ballot_box_with_check: The model's Accuracy Score = 0.6844

![smotescore]( https://github.com/JoRanjit/Credit_Risk_Analysis/blob/main/Images/SMOTE_metrics.PNG)

#### :black_medium_square: Step #3 - Next we undesampled the dataset using ClusterCentroid resampler:

:ballot_box_with_check: The model's Accuracy Score = 0.5917

![undersampler]( https://github.com/JoRanjit/Credit_Risk_Analysis/blob/main/Images/undersampling_metrics.PNG)

### As part of deliverable 2 - we used a combinatorial approach of over and undersampling using the SMOTEENN algorithm.

:ballot_box_with_check: The model's Accuracy Score = 0.6819

![smotenn]( https://github.com/JoRanjit/Credit_Risk_Analysis/blob/main/Images/SMOTEenn_metrics.PNG)

<h3> With the above accuracy scores - it is clear that: :heavy_check_mark: SMOTE Oversampling algorithm with an accuracy rate of :heavy_check_mark: 0.6844 is the better choice. </h3>

### As part of deliverable 3 - compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. And we will compare the accuracy scores of both algorithms.

#### :black_medium_square: Step #1 - We resampled the training data using the BalancedRandomForestClassifier algorithm with 100 estimators.

:ballot_box_with_check: The model's Accuracy Score = 0.7284

![bal_ran_forest]( https://github.com/JoRanjit/Credit_Risk_Analysis/blob/main/Images/bal_ran_for_metrics.PNG)

#### :black_medium_square: Step #2 - Next, resample the training data using the EasyEnsembleClassifier Adaboost algorithm with 100 estimators.

:ballot_box_with_check: The model's Accuracy Score = 0.9317

![adaboost]( https://github.com/JoRanjit/Credit_Risk_Analysis/blob/main/Images/adaboost_metrics.PNG)

## :triangular_flag_on_post: SUMMARY

* Of the 4 resamplers - :trophy: SMOTE Oversampling algorithm with the accuracy score of 0.6844 is the topper.
* Of the 2 ensemblers - :trophy: EasyEnsembleClassifier Adaboost algorithm with the accuracy score of 0.9317 is the best.

* Aaaboost algorithm also assigned a recall score of 0.92 to high_risk items whch also shows that that is the best model of all the 6 that we used today. 

* The top 5 features used by the model are:
  * total_rec_prncp
  * total_pymnt_inv
  * total_pymnt
  * last_pymnt_amnt
  * total_rec_int
  
But eventhough the model had good accuracy scores and recall rates compared to others, we still - 
## :no_entry:  DO NOT recommend any of these models as the precision scores to predict a high risk is still very very low at 0.09.

