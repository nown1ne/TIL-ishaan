# [Blog](https://www.analyticsvidhya.com/blog/2017/09/understaing-support-vector-machine-example-code/)
### [SVM 1](https://www.youtube.com/watch?v=efR1C6CvhmE)
### [SVM 2](https://www.youtube.com/watch?v=Toet3EiSFcM)
### [SVM 3](https://www.youtube.com/watch?v=Qc5IyLW_hns)

## Dataset:
<img width="653" alt="Dataset" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/7aca01d4-6759-404d-b80d-a2c5e422fbb9">

- Red dots are not obese mice
- Green Dots are obese mice

### Maximum Margin Classifiers:
<img width="553" alt="MMC" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/2edb2122-0fc3-47f8-9312-3cdbfcb76617">

- We focus on the obersvations at the adges of each cluster, we draw a line at the middle (maximum margin)
  - Left of the MMC is not obese
  - Right of the MMC is obese
- The MMC are super sensitive to outlier in training data (not ideal)

#### Margin:
- The shortest distance between the observations and the threshold is called margin.

### Soft Margin:
- When we allow misclassifications the distance between the distance and the observations is called a **Soft Margin**.
- We pick a threshold which is less sensetive to training data and allowed missclassifications(high bias) but performed better for new data (low variance)

<img width="560" alt="Soft Margin" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/1b6042ca-c427-45a7-b680-6a12362f129f">

#### How to choose soft margin:
-  We used **Cross Validation** to detemine how many miss-classifications and observations to allow inside of the **Soft Margin** to get best classification.

## Support Vector Classifiers:
### 1-D Data:
- When we use a **soft margin** to detemine the location of a threshold then we are using a **Soft Margin Classifier** aka **Support Vector Classifier** to classify observations.

<img width="606" alt="SVC" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/931295a1-284e-4a1a-9e56-64083f2f42d2">

### 2-D Data:
- When the Data is 2-D, the Support Vector Classifier is a **stright line**. We use **Cross-Validations** to determine the best fit.

<img width="529" alt="2-D SVC" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/8ed33a1a-9e9d-45f2-9aaa-9f6798e6f817">

- Similarly for **3-D Data** the Support Vector Classifier is a **Plane**.

<img width="1409" alt="3-D SVM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/0b17dbd0-e2cb-46e5-91c2-63392ed3dcef">

# Support Vector Machines (SVM):
- The SVC's can classify the new data properly:
- Drug Dosages work only if the amount is just right
<img width="815" alt="New_Dataset" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/7ecdbce7-dafb-4a1d-907d-11e914ccd89c">

## Prodedure:
- We start with a lower dimension data set
- We add a y-axis so we can draw a graph (Move data to higher dimension)
- Y-axis values = (dosages)^2

<img width="1106" alt="^2" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/1a1b134e-c8f5-4103-a9b7-a9fb1a39b765">

- Find a Support Vector Classifier which seprates the higher dimension data into 3 parts
<img width="1133" alt="SVM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/09893ea6-9d2b-4fdf-b738-8a8b89a6e2ff">

## Kernel Functions:
- In order to make the mathematics possible, Support Vector Machines use something called Kernel Functions to systematically find Support Vector Classifiers

### Polynomial Kernel:
<img width="200" alt="Poly-Kernel" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/729c9446-d294-4155-be14-550dd381a3c0">

- **a,b** refer to the two observations we want to calculate the higher dimensional relationship.
- **r** determines the polynomial's coefficient 
- **d** determines the degree of the polynomial
  - r & d are determined by **Cross-Validation**

For the given Data set we used r = 1/2 and d = 2
<img width="1074" alt="Example" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/a2a0da56-3f74-4f01-a2f7-9bc4d7ec203e">

#### Relationship between 2 variables:
- We just simply substitute the values and the value obtained is the 2-D relationship (we did this without converting the value into 2-D data(BAM))

### Radial Kernel:
