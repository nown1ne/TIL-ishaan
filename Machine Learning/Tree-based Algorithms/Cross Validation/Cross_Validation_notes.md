# Cross Validation:
- Cross-validation is a resampling method that uses different portions of the data to test and train a model on different iterations.
- It is mainly used in settings where the goal is prediction, and one wants to estimate how accurately a predictive model will perform in practice.
- Cross Validation allows us to compare different machine-learning methods and get a sense of how well they will work in practice.

## Procedure:
We need the data available to us to:
- (Testing the Algorithm)We need to estimate the parameters for the machine-learning methods
  - Reusing the same data for both training and testing is a bad idea because we need to know how the method will work on data it wasn't trained on.
- (Training the Algorithm)Evaluate how well the machine learning methods work

## Types of Cross Validation:
### Four Fold Cross Validation:
- Divide data into 4 blocks and test each method

<img width="1099" alt="Screenshot 2023-06-24 at 3 41 36 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/b4abc04d-0019-4582-bb8e-30a6954391a8">
<img width="1360" alt="Screenshot 2023-06-24 at 3 42 21 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/05703ae9-68b2-4ca7-926c-59af0bc52b86">

### Leave one out Cross Validation:
<img width="1218" alt="Screenshot 2023-06-24 at 3 44 37 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/006c4d05-a9d8-4396-b850-4996b228c0cb">

### Ten-Fold Cross Validation (Most Common Method)
