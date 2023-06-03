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
  - w,b are parameters which define the straight line

## Cost Funtion:
<img width="1381" alt="Cost Function" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/ac8fd909-15ec-4e78-93f1-2060d078fc25">
- Aim is to minimize J(w,b) for values of w and b

### Simplified Cost Function:
- We set b=0, then f = wx
  - f -> function of x
  - J -> function of w
- In the Exmaple below we see the different J for different w
  - for every different w, we get. a different point in J
    - We need to find the minimum J for the ideal linear regression case
<img width="1380" alt="Simplified_LR" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/63f23bbc-8a4a-4b8e-88b3-61f91e873df8">

### Complex Cost function:
- J is a 3-D plane, and we need to find the valley in this to get best value of b,w to minimize J and get the ideal result
#### Contour Plots:
- A contour plot is a graphical technique for representing a 3-dimensional surface by plotting constant z slices, called contours, on a 2-dimensional format
  - The points on the J plot on a same circle, represent the same J (but fifferent Lines)
  - The minimum J is for the innermost Circle
<img width="1380" alt="Min_contour" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/6e8fb111-792e-4021-ba73-50aa2d934740">
