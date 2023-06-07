# Linear Regression:
Linear regression analysis is used to predict the value of a variable based on the value of another variable. 
 - The variable you want to predict is called the dependent variable. 
 - The variable you are using to predict the other variable's value is called the independent variable.

![1_QiU6DcP_r9qWLznMw0-M_Q](https://github.com/IshaanAdarsh/TIL/assets/100434702/2a46b281-6241-45c0-9727-eae3537c47f3)

#### Basically, Linear Regression is all about finding an equation of a line that almost fits the given data so that it can predict the future values.

## Hypothesis:
![1_-0_jhjes5pxxr8Dz3MNxKg](https://github.com/IshaanAdarsh/TIL/assets/100434702/7b04d4a2-8e6c-4a14-a5b2-87c47476b897)
- It is the equation of a straight line. Where
  - Θ₀ -> Base value (intercept of the line (Gives an additional degree of freedom))
  - Θ₁ -> Linear regression coefficient (scale factor to each input value)
  - h(x) -> Predicted Value
#### Now all you have to do is find the appropriate base price and the value of Θ₁ based on your dataset so that you can predict the output.

## Cost Functions: 
![1_mDEzcRicu3Oc2rrvB7A-uw](https://github.com/IshaanAdarsh/TIL/assets/100434702/943c0098-8698-4aee-b9d5-b0f78dc07f70)
- To calculate our cost function, what we need is h(x) for all m examples i.e m predicted prices corresponding to m houses.
- Now, to calculate h(x), we need a base price and the value of Θ₁. Note that these are the values which we will tune to find our best fit.
- **We need something to start with, so we will randomly initialize these two values.**

## Gradient Descent:
![1_3qlkq6_wWNgno2g162udzQ](https://github.com/IshaanAdarsh/TIL/assets/100434702/13b54417-0c35-472e-b0c1-f52591177c10)
![1_YEGHkUxBENGkBswPQcF91w](https://github.com/IshaanAdarsh/TIL/assets/100434702/944c6ecb-5f86-4c16-8eb6-529f35f0f2ce)
- So basically we are updating our old input by subtracting it with the partial derivative of our cost function w.r.t the old input.
- It will continue to do this until a minimum value Θ is reached

![1_iNPHcCxIvcm7RwkRaMTx1g](https://github.com/IshaanAdarsh/TIL/assets/100434702/288a9de7-3889-42fe-a12d-d4b3aa4232ee)
- The above figure is a good depiction of gradient descent. Note how the steps are getting smaller and smaller as we are reaching the minimum.

## Linear Regression Visualization:
![1*p3gOraOrKuOE33fmjq47Kg](https://github.com/IshaanAdarsh/TIL/assets/100434702/dc2cc8ed-ae3f-4807-a29f-582c004efde0)
