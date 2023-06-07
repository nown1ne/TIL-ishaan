# Linear Regression Model and Classification:
<img width="821" alt="Regression_over" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/a818ecec-be1d-4cf8-a16c-bce669fdc3c4">
<img width="819" alt="Classification_under" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/4e04b9b5-ba42-4abc-b8a2-e64a80c61dee">

### Underfitting:
  - High Bias as it doesn't fit the training set well
    - Example: wx + b
### Overfitting: 
  - High variance as it fits the training set extremely well
    - Example: ax^4 + bx^3 + cx^2 + dx + e

# Solving Overfitting:
## Collect more training data:
- By collecting more training data it makes the curve more defined. (Best Method)
## Select features (to include/exclude):
- if we have all feautres but insufficient data it can cause overfitting so to solve this we only select specific features and train the model according to these features.
  - Disadvantage:
    - useful features could be lost
## Regularization (Reduce the size of parameters):
- Reduce the size of parameters 𝑤𝑗, in exluding features you outright remove the 𝑤𝑗 but by reducing them the curve can be more drfined and fit the training data.

<img width="755" alt="Regularization_Intuition" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/bdf6c90c-ecfc-489c-833c-74c806308f8e">

### Cost Funtion for Regularization:
<img width="725" alt="Cost_Function" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/97225f85-0621-4b65-ad0a-566d5e6484cb">
- Lambda = 0 -> Overfit
- Lambda = Large -> Underfit
 
