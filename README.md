# Credit_Risk_Analysis
## Overview
This project seeks to analyze credit risk using classification techniques and machine learning.  Using Jupyter Notebooks, Python, and Pandas, algorithms will be created to train and test data from clients to judge credit risk.  Imbalanced-learn and scikit-learn libraries for pandas will be used in this process.  Oversampling will be conducted with RoandomOVerSample and SMOTE algorithms.  Undersampling will be performed with ClusterCentroids algorithm.   A combination of over and under sampling using SMOTEEN algorithm will conclude traditional resampling techniques.  Bias reduction using BalancedRandomForestClassifier and EasyEnsembleClassifier algorithms will be used to see if bias reduction is necessary, or successful.  Comparisons will be made between algorithm performance to determine which method will be recommended to the company for use.  
## Software
    •	Jupyter Notebooks
    •	Python
    •	Pandas
    •	Sckikit-learn library
    •	Imbalanced-learn library
## Results
The project results illustrate the variance in each algorithm types’ of ability to effectively make predictions.  The first four algorithms utilize sampling techniques that help to balance the size in data classes for training.  Native Random Oversampling takes existing data from the smaller class and randomly duplicates the data to increase the size of the data set to meet the other class size.  SMOTE oversampling creates new data points based on existing data to fill the gap between data classes.  Under sampling randomly selects data in the larger class to use in training that is equal in size as the small class.  SMOTEENN is a combination of over and under sampling techniques where the smaller class is oversampled and then cleaned using an under-sampling strategy.   The final two algorithms use ensemble classifiers where a layer effect of classifiers is used to learn upon the deficiencies of the previous classifier. 
The areas of evaluation are included below for each algorithm type:
Balanced accuracy score- is used to determine the overall accuracy of an algorithm to classify correctly.  Balanced accuracy helps to deal with imbalanced datasets such as the one for this project.  It is the average recall obtained on each class.  
Precision: also known as positive predictive value, is the reliability of a positive classification made by the algorithm.  It is the number of correct predictions divided by total predictions made.  
Recall: the measure of sensitivity of the algorithm.  It is a measure of positive classifications that proved to be positive.  In other words, the number correctly identified of those classified as positive. 

Native Random Oversampling

      o	Balanced accuracy scores- 0.6114
      o	Precision - .99
      o	Recall- .61
      
![Native_Random_Oversampling](https://user-images.githubusercontent.com/79231355/124516149-a788c480-dda6-11eb-8914-f4c70cac5cbd.png)

SMOTE Oversampling

      o	Balanced accuracy scores-0.6255
      o	Precision - .99
      o	Recall- 0.65
      
![SMOTE_Oversampling](https://user-images.githubusercontent.com/79231355/124516137-a48dd400-dda6-11eb-8044-0fd66f4118c4.png)

UnderSampling

      o	Balanced accuracy scores-0.6255
      o	Precision - .99
      o	Recall - .65
     
![Undersampling](https://user-images.githubusercontent.com/79231355/124516124-a0fa4d00-dda6-11eb-8fdb-6189da655a02.png)

SMOTEENN

      o	Balanced accuracy scores – 0.6255
      o	Precision – 0.99
      o	Recall – 0.56

![Combination_Over_Under_Sampling](https://user-images.githubusercontent.com/79231355/124516111-9b9d0280-dda6-11eb-826c-6632a4f7d56f.png)

Balanced Random Forest Classifier

      o	Balanced accuracy scores – 0.7917
      o	Precision - .99
      o	Recall – 0.9
      
![Balanced_Random_Forest](https://user-images.githubusercontent.com/79231355/124516098-96d84e80-dda6-11eb-9da0-344915c7a6aa.png)

Easy Ensemble AdaBoost Classifier

      o	Balanced accuracy scores – 0.91099
      o	Precision  - .99
      o	Recall - .95
      
![AdaBoost_Classifier](https://user-images.githubusercontent.com/79231355/124516077-87590580-dda6-11eb-9f12-21dce1a493a4.png)

      
## Summary
All the algorithms can adequately predict credit risk with the supplied data.  However, some do this more accurately and consistently than others.  The drawbacks of filling in or removing data for training purposes of the algorithm in such an unbalanced data set become clear when compared to the ensemble classifiers.  Although the highest score for any of the three measurements is one, achieving this value would indicate the algorithm is not working correctly or was trained incorrectly.  With this information, the best fit algorithm for this purpose is utilizing the Easy Ensemble AdaBoost Classifier.  
