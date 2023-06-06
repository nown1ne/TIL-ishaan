# [YT Videos](https://www.youtube.com/watch?v=EuBBz3bI-aA)
## In Machine Learning, when we want to optimise model prediction, it is very important to understand the parameters which describe prediction errors and accuracy .
## Bias:
- Bias is the difference between the average prediction of our model and the correct target value which model is trying to predict.Bias is inherent to the algorithm we choose to make the Model. A biased model is one that makes incorrect assumptions about the dataset to make the target function easier to learn.
- The inability for a machine learning method to capture the true relationship is called bias.
  - Low Bias is desired : High Bias means UnderFitting of the model on training data.

  - Low Bias : Suggests less assumptions about the relation in data to predict the target function. Example: SVM, Decision Tree, KNN
  - High-Bias : Suggests more assumptions about the relation in data to predict the target function. Example: Linear Regression, Logistic Regression

#### Examples:
- The Straight Line has relatively high bias, since it can not capture the curve in the relationship between weight and height.
- The Squiggly Line has low bias, since it is flexible and can adapt to the curve in the relationship between weight and hight.

## Variance:
- Variance is the amount that the estimate of the target function will change if different training data was used. Variance is error from sensitivity to small fluctuations in the training set. High variance can cause an algorithm to model the random noise in the training data, rather than the intended result.
- The difference in fits between data sets is called Variance.
- Low Variance is desired : High Variance means OverFitting of the model on training data.

  - Low Variance: Small changes to the estimate of the target function with changes to the training dataset. Example: Linear Regression, Logistic Regression
  - High Variance: Large changes to the estimate of the target function with changes to the training dataset.Example: SVM, Decision Tree, KNN
#### Examples:
- The Squiggly Line has high variance so its performance might do well sometimes, and other times it might do terribly.
- The Straight Line has relatively low variance, because the Sums of Squares are very similar for different datasets.

## Example Data Set:
We measured the weight and height of a bunch of mice and plotted the data on a graph

<img width="467" alt="Data_SET" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/120bd2ec-aaa7-4d63-b44c-49336bfe1418">

### Inferences:
  - Light Mice tend to be Short
  - Heavier Mice tend to be taller but after a certain height, mice don't get any taller, just more obese.

### Firstly we split the data into 2 sets:
- Training Data (Blue)
- Testing Data (Green)

<img width="469" alt="Training_Testing" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/24a6627f-ac41-46c3-bc90-90225e7cbe52">

**We would know the exact mathematical formula that describes relationship between weight and height, so we're going to use two machine learning methods**

### Linear Regression:
- LR fits a stright line to the data, but that doesn't have the flexibilty of to replicate the true relationship(arc) it has higher bias.

<img width="524" alt="Straight_line" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/ccaa9c77-9d96-4415-9d66-58b9e0fe6109">

### Squiggly Line:
- Squiggly line can handle arc in the true relationship between wt and height , very little bias.

<img width="461" alt="Sqiggly_line" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/0ef4dc85-387c-4e63-babd-0b3d586a90f4">

#### Square sum analysis for Training Data:

<img width="871" alt="Sq analysis" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/e746b276-7f5d-4843-b68a-8a17c875472d">

- for squiggly sum = 0
- for straight line sum != 0

#### Square sum analysis for Testing Data:

<img width="863" alt="Testing Data" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/22f19bf2-5bde-4a09-a520-6d2778ae2e42">

- in this case straight line fits better than squiggly.
- The Squiggly Line has high variability, because it results in vastly different Sums of Squares for different datasets.

### Overfit:
Because the Squiggly Line fits the training set really well, but not the testing set, we say the sqiggly line is an Overfit

- Three commonly used methods for finding the sweet spot between simple and
complicated models are:
  - Regularisation 
  - Boosting
  - Bagging

### There is inverse relationship between bias and variance in machine learning.
#### Increasing the bias will decrease the variance.
#### Increasing the variance will decrease the bias.
- High Model Complexity : High Variance , Low Bias
- Low Model Complexity : High Bias , Low Variance

## 
