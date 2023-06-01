# Linear Regression:
## Regression vs Classification:
Understanding what the overall process of supervised learing.
- Data has the `right answers`.
- Types of Models: 
  - Regression Models predicts numbers
    - It has infinitely many possible outputs
  - Classification Model predicts categories
    - It has small number of possible outputs

<img width="1091" alt="Regression vs Classification" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/96d1d7c8-30fc-49cd-bc30-25935be3086c">

## Terminology:
- Training Set: Data used to train the model
  - Notation:
    - x = 'input'(or)'feature' variable
    - y = 'output'(or)'target' variable
    - m = number of training examples
    - (x,y) = single training example

<img width="1090" alt="Terminology " src="https://github.com/IshaanAdarsh/TIL/assets/100434702/f1edff3d-6f8e-40b3-97b1-bd53eee608c9">

## Process of Training Data
```
                                          ŷ (prediction/esitmated y)
                                          ▲
                                          |
                                          |
training set ---> learning algorithm ---> f model(function/hypothesis)
                                          |
                                          |
                                          ▲
                                          x (feature)
```
Univariate Linear Regression: 
- f = wx + b
