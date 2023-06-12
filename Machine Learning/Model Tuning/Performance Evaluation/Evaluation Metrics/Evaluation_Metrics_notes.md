# [Blog(Medium)](https://medium.com/ml-cheat-sheet/machine-learning-evaluation-metrics-b89b8832e275)
# [Blog](https://www.kdnuggets.com/2020/05/model-evaluation-metrics-machine-learning.html)

# Evaluation Matrics:
The importance of evaluation metrics in assessing the performance of machine learning models. The choice of metrics depends on the type of problem being solved, such as classification or regression. Classification metrics and regression metrics have different considerations, influencing the weighting of different characteristics in the results and guiding the selection of the appropriate algorithm or model version.

## Classification metrics
- Accuracy
- Precision
- Recall
- F-Score
- ROC (Receiver operating characteristic)
- AUC (Area under the curve)

### Accuracy: 
In a classification problem, the accuracy metric is commonly used to evaluate the performance of a model. Accuracy is calculated using a confusion matrix, which summarizes the prediction results and provides insights into the types of errors made by the model.

#### Confusion Matrix:
The confusion matrix consists of four categories:
- True Positive (TP): Observations that are positive and correctly predicted as positive.
- True Negative (TN): Observations that are negative and correctly predicted as negative.
- False Positive (FP): Observations that are actually negative but incorrectly predicted as positive.
- False Negative (FN): Observations that are actually positive but incorrectly predicted as negative.

By analyzing the confusion matrix, we can understand how the model is confused when making predictions and gain insights into the specific types of errors (FP or FN) being made.

#### Mathematical Definition
`Accuracy = (TP + TN) / (TP + TN + FP + FN)`

### Recall or Sensitivity:
- The recall is also known as the true positive rate. It is the number of positives our model claims compared to the actual number of positives there are throughout our data.

#### Mathematical Definition
`recall = TP / (TP+FN)`
- For high recall, we need to minimize FN

### Precision:
- Precision is also known as the positive predictive value. It is the number of accurate positives our model claims compared to the number of positives it actually claims.

#### Mathematical Definition
`precision = TP / (TP+FP)`
- For high Precision, we need to minimize FP

### Recall vs Precision:
In certain scenarios, recall and precision play different roles and one may be more important than the other.

#### Recall a better measure than precision:
- When it comes to selecting potential buyers from a large pool of customers, as described in the first example, recall becomes more important. The objective is to ensure that all potential buyers are included in the selection, even at the cost of some false positives. In this case, missing a potential buyer (false negative) is a bigger concern than including non-buyers (false positives), so a high recall is desired.

#### Precision a better measure than recall:
- On the other hand, in recommendation systems like Amazon, YouTube, or Netflix, precision is often more critical. False negatives (missing relevant recommendations) are less concerning, but precision aims to ensure that the recommended items are highly relevant and tailored to the user's preferences. In these cases, precision is emphasized to provide accurate and useful recommendations to users.

### F-score:
- Accuracy is a great measure but only when you have symmetric datasets where values of false positive and false negatives are almost the same.
  -  It uses Harmonic Mean in place of Arithmetic Mean by punishing the extreme values more.
  - F-score helps to measure Recall and Precision at the same time.
  - It is difficult to compare two models with low precision and high recall or vice versa. So to make them comparable, we use F-Score.

### ROC (Reciever operating characteristic curve) :
- It is a graph showing the performance of a classification model at all classification thresholds.
This curve represents two axes:
  - True positive rate (recall/sensitivity)
  - False-positive rate (1- specificity) : FPR = FP/ FP+TN

- A ROC curve represents a classifier with a random performance level. The curve separates the space into two areas for good and poor performance levels.
- ROC is usually used to compare classifier performances, Like the figure shows, classifier A outperforms better than classifier B.

### AUC (area under the curve):
- It is an area under the curve calculated in the ROC space. It is the metric we consider when we want to evaluate a model’s performance when using the ROC curve, also called AUROC. Although the theoretical range of the AUC score is between 0 and 1, the actual scores of meaningful classifiers are greater than 0.5.

- An excellent model has AUC near to 1, which means it has a good measure of separability.

<img width="580" alt="Real1" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/392446dd-1811-4ff4-8f49-a203d874fd90">

- A poor model has AUC near to 0, which means it has the worst measure of separability.

<img width="594" alt="Real2" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/0a160ace-48ef-4b15-9d5f-05f56e9cbd37">

- Acceptable models have AUC greater than 0.5.

<img width="596" alt="Real3" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/8407a8d6-c3c1-4eca-bcf4-0dfd2ba16b65">

### Regression metrics

Unlike a classification problem, the objective of a regression problem is not to make predictions on a discrete variable (dog vs cat). Instead, we would be tasked with predicting house prices.

The objective is to evaluate our performance against the ground truth among all the predictions. The ground truth is historical data containing true house prices.

-   Mean Absolute Error (MAE)
-   Mean Squared Error (MSE)
-   R2 Score
-   Adjusted R2

#### Mean Absolute Error:
- MAE measures the average magnitude of the errors in a set of predictions, without considering their direction. It's the average over the test sample of the absolute differences between prediction and actual observation where all individual differences have equal weight.

<img width="556" alt="MAE" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/4959b231-fe38-4808-bd4c-0ebd002778ea">

- It is usually intended to measure average model bias.

<img width="600" alt="MAE 2" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/20a8e25c-fa65-4e85-8f2e-a373bfd93ed5">

- Generally,** the mean absolute error **(**MAE**)is a common measure of forecast error in time series analysis, where the terms "mean absolute deviation" is sometimes used in confusion with the more standard definition of mean absolute deviation.

#### Mean Squared Error
- Both **the mean squared error** and **the mean absolute error** tell you how close a regression line is to a set of points. **MSE** is just like the **MAE** but *squares* the difference before summing them all instead of using the absolute value. We can see this difference in the equation below. As we can conclude from the formula, MSE assigns more weight to the bigger errors. The algorithm then continues to add them up and average them. If you are worried about the outliers, this is the metric that you should look at!

<img width="630" alt="MSE" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/85b8d666-be5d-4c57-a050-882a479ed1dc">

- R-squared (R²) is a statistical metric that measures how well a regression model fits the data. It quantifies the proportion of the variance in the dependent variable (target) that can be explained by the independent variables (features).

#### R Squared Score: 
- An R-squared value ranges from 0 to 1, where:

- 0 indicates that the model does not explain any of the variability in the dependent variable.
- 1 indicates that the model perfectly predicts the dependent variable using the independent variables.
  - For example, if a predictive model has an R-squared value of 0.8, it means that 80% of the variation in the target variable can be explained by the independent variables. A higher R-squared value indicates a better fit, as more of the variation in the target variable is accounted for by the model.

- However, it is important to note that R-squared alone does not determine the overall quality or validity of the model. It is just one of many evaluation metrics used in regression analysis. Other factors such as the significance of coefficients, model assumptions, and additional evaluation metrics should also be considered when assessing the model's performance.

<img width="716" alt="R2" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/6878bd75-2dfa-4683-9d70-2f49718d9ad2">

- The major shortcoming of **R2** is that only the dispersion is quantified if it is used alone. A model that systematically over/under-predicts all the time will still result in good **R2** values close to **ONE** even though all predictions were incorrect. Thus, Generally, it is better to consider ***adjusted R-squared*** rather than **R-squared** according to the nature of your data and model.

#### Adjusted R2:

- The **adjusted R-squared** compares the explanatory power of regression models that contain more than one predictor. Suppose you compare a **three-predictor model** (3 features: **Y'i = b0 + b1X1i + b2X2i + b3X3i**) with a higher R-squared to a one-predictor model (**Y'i = b0 + b1X1i**).

- We can not compare these 2 models using the **R squared** value. Is the three predictor model better than the one predictor model because it has a higher R squared value? Or, it could be that the R squared is higher because the model has more predictors? **Simply we need to compare the adjusted R-squared values to find out!**

- The adjusted R-squared is a modified version of R-squared that has been adjusted for the number of predictors in the model. The adjusted R-squared increases only if the new term improves the model more than would be expected by chance. It decreases when a predictor improves the model by less than expected by chance (imagine having eyes color as a predictor when trying to predict people with heart decease). The adjusted R-squared can be negative, but it's usually not. It is always lower than the R-squared.

<img width="659" alt="AR2" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/58bbf5d0-e291-4bec-bdc0-aab10b8e61aa">
