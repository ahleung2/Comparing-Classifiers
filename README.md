# Comparing Classifiers

## Overview:
The goal is to build and compare classifcation models that can accurately predict which clients are likely to subscribe to a term deposit based on a list of selected features. 

## Data:
The dataset explored comes from the UCI Machine Learning repository and is related with direct marketing campaigns of a Portuguese banking institutions. More specifically, the dataset covers seventeen campaigns that occurred between May 2008 and November 2010. For more details, please refer to the following notebook: [Notebook](https://github.com/ahleung2/Comparing-Classifiers/blob/main/Leung_Aaron_Comparing_Classifiers.ipynb)

## Findings: 
- There is **significant class imbalance** in the target variable which can affect the performances of the classification models. 
- All four base models had comparable accuracy. KNN had the shortest train time while SVM had the longest. Additionally, Decision Tree model had the highest training accuracy but a noticeable drop in testing accuracy which could be due to overfitting.
- When improving the base models, we adjusted the performance metric to **optimize for recall** as this best aligns with our business goal. Similar to the base model, the SVM model appeared computationally expensive especially with larger datasets. Because of the extremely long runtime, no data was obtained for this model. Among the other three models, Decision Tree Model achieved the best recall score at the expense of the precision score.
- Both Logistic Regression and Decision Tree provides insight into key drivers for clients subscribing to a term deposit. Both models suggested that several social and economic attributes, as well as successful previous marketing campagins, are key drivers. In terms of differences, Logistic Regression model indicated that clients are more likely to subscribe to a term deposit in the months of August, March and July. In contrast, Decision Tree model suggested that features like age and education are important to consider. 

## Conclusion: 
Based on the results, the Decision Tree Model appears to be the best classifier in terms of recall score. Additionally, the Decision Tree Model provides feature importance scores which gives us better insight into which features are more useful when making a prediction. Some actionable items include focusing on key months mentioned above or targeting by age-group (as age is an important feature).

## Future Considerations and Next Steps:
Overall, we were able to gain meaningful insight into key drivers for client subscribing to a term deposit. While the Decision Tree model achieved the highest recall score, the score is still relatively low. Further preprocessing and hyperparameter tuning are necessary to optimize the recall score. Additionally, it would be beneficial to retry using the SVM after reducing the size of the dataset. Lastly, addressing class imbalance is important as well. Tehcniques such as random undersampling could be employed to address this.
