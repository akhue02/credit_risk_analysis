# credit_risk_analysis

## Analysis
I was tasked by Jill to carry out Credit card risk analysis using the data set provided in the LoanStats_2019Q1.csv file. Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, I was informed to employ different techniques to train and evaluate models with unbalanced classes. Jill also advised me to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduces bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once done, I evaluated the performance of these models and made a written recommendation on whether they should be used to predict credit risk.

## Results
After carrying out the analysis as mentioned above, the following observations were made.

#### Random Over sampler

![RandomOverSampler](https://github.com/akhue02/credit_risk_analysis/blob/main/naive_random_oversampling.png)

* After carrying out the analysis using RandomOversampler algorithm, we got the balanced accuracy of 0.646. High Risk Precision and recall values are 0.01 and 0.74 and Low Risk precision and recall values are 1 and 0.55.  


#### SMOTE 

![SMOTE](https://github.com/akhue02/credit_risk_analysis/blob/main/SMOTE%20Oversampling.png)

* After carrying out the analysis using SMOTE algorithm, we got the balanced accuracy of 0.659. High Risk Precision and recall values are 0.01 and 0.63 and 
  Low Risk precision and recall values are 1 and 0.69.  

#### Combination(over and undersampling) 
![Combination](https://github.com/akhue02/credit_risk_analysis/blob/main/Combination%20Over%20and%20Under%20sampling.png)

* After carrying out the analysis using RandomOversampler algorithm, we got the balanced accuracy of 0.6400. High Risk Precision and recall values are 0.01 and 0.70 and 
  Low Risk precision and recall values are 1 and 0.58.  
  
 ####  Undersampling
 ![Undersampling](https://github.com/akhue02/credit_risk_analysis/blob/main/Undersampling.png)
 * After carrying out the analysis using RandomOversampler algorithm, we got the balanced accuracy of 0.54421. High Risk Precision and recall values are 0.01 and 0.67 and 
  Low Risk precision and recall values are 1 and 0.42.  
## Summary: 

In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
