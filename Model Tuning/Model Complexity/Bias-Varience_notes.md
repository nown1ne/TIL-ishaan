# [YT Videos](https://www.youtube.com/watch?v=EuBBz3bI-aA)
## Bias:
- Bias is the difference between the average prediction of our model and the correct target value which model is trying to predict.
- The inability for a machine learning method to capture the true relationship is called bias.
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

## We would know the exact mathematical formula that describes relationship between weight and height, so we're going to use two machine learning methods:

### Linear Regression:
- LR fits a stright line to the data, but that doesn't have the flexibilty of to replicate the true relationship(arc) it has higher bias.
<img width="524" alt="Straight_line" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/ccaa9c77-9d96-4415-9d66-58b9e0fe6109">

### Squiggly Line:
- Squiggly line can handle arc in the true relationship between wt and height , very little bias.
<img width="461" alt="Sqiggly_line" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/0ef4dc85-387c-4e63-babd-0b3d586a90f4">
