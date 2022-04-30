# Credit_Risk_Analysis

# Overview
The purpose of this analysis is to utilize machine learning models to predict credit risk. We will use several resampling algorithms, including oversampling, undersampling, combined approaches, and models that reduce bias, to make recommendations on which, if any, should be used to predict credit risk.

## Results
### Resampling Models
*  **Naive Random Oversampling** -
    This oversampling model produced an avg balanced accuracy score of 65.73%. This model also returned an overall precision score of .99, which *seems* to indicate an excellent predictive response rate, however, this is primarily due to a high precision in the low risk category . With an overall recall score of .60, this tends to lean towards a lower confidence in the accuracy of our data. Our overall F1 score in this model falls at .75 which appears to be a decent score but because the majority of this is for low risk, it does not fare well for the high risk applicants.  The lower recall score aligns with our accuracy score to indicate that, while this model **may** be effective, our client would likely benefit from running their data through several different models.

    ![NRO](https://github.com/agordon16/Credit_Risk_Analysis/blob/1a28b2d4601ec5688415d03c7cc19b118d45940f/Images/NaiveRamdonOversamplingjpg.jpg) 


*  **SMOTE Oversampling** -
    This model produced a balanced accuracy score of 66.22%, overall precision score of .99, and overall recall score of .69. An overall F1 score of .81 indicates a better model than our previous Naive Random Oversampling model, but again, the  majority falls to low risk and thus this could skew the avg. However, with a balanced accuracy score close to the previous model, we should continue to run the data through more models.

    ![SMOTE](https://github.com/agordon16/Credit_Risk_Analysis/blob/1a28b2d4601ec5688415d03c7cc19b118d45940f/Images/SMOTE%20Oversamplingjpg.jpg)


*  **Undersampling** -
    This model returned a balanced accuracy score of 55.41%, overall precision score of .99, and overall recall score of .69. An overall F1 score of .56 tends to indicate that this may not be the best predictive model to use.

    ![Under](https://github.com/agordon16/Credit_Risk_Analysis/blob/1a28b2d4601ec5688415d03c7cc19b118d45940f/Images/Undersampling.jpg)

*  **SMOTEENN** -
    This final model produced a balanced accuracy score of 68.76%, overall precision score of .99,  and overall recall score of .57. With an overall F1 score of .72, it falls below several of the other models analyzed and does not suggest this as the best model to use.

    ![SMOTEENN](https://github.com/agordon16/Credit_Risk_Analysis/blob/1a28b2d4601ec5688415d03c7cc19b118d45940f/Images/SMOTEENN.jpg)



### Classifier Models
*  **Balanced Random Forest** -
    Our first classifier model returns a balanced accuracy score of 78.78%, an overall precision score of .99, and overall recall score of .91. An F1 score of .95 appears to make this a much better predictive model than the resampling models shown previously, however, again the majority lies with low risk and may skew the data.

    ![BalRan](https://github.com/agordon16/Credit_Risk_Analysis/blob/1a28b2d4601ec5688415d03c7cc19b118d45940f/Images/BalancedRandomForest.jpg)


* **Easy Ensemble Classifier** -
    This classifier model returns a balanced accuracy score of 92.54%, an overall precision score of .99, and overall recall score of .94. With an overall F1 score of .97, this appears to be the best of our tested models as the F1 scores are a bit more balanced(although still favoring low risk applicants). 

    ![EEC](https://github.com/agordon16/Credit_Risk_Analysis/blob/1a28b2d4601ec5688415d03c7cc19b118d45940f/Images/EasyEnsembleClassifier.jpg)
    

## Summary
After reviewing the array of machine learning models used to analyze credit risk data, it would appear the Easy Ensemble Classifier provides the best results. While all precision scores tended to lean towards an average of .99, this was mainly due to the larger low risk score which brings the averge up substantially. That being said, we must keep in mind the disparity in data set size. This disparity leads to the idea that more research for a better model is warranted.

| Risk Category  | Total Set   |  Resampling |  Ensemble |
|:--- |:--- |:--- |:--- |
| High Risk   |  347   |  101 | 87 |
| Low Risk    |68470   |17204 |17118 |


