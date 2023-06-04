# Classification Problems:
- In this the output varibale y can take only a handful number of variables unlike linear regression where infinite numbers are considered
- In these problems linear regression is not a good algoritm to classify these problems

## Binary Classification:
- Where there are only 2 ouptuts for y 
  - Negative Class (0->False)
  - Positive Class (1->True)
For Binary Classification, LR is not Optimal as:
- Even after setting a THreshold, if there are any outliers, it causes issues
<img width="1380" alt="LR_not ideal" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/4eeb9bf8-7f70-47d0-90fa-b399390f61a5">

# Logistical Regression:
- For binary classification, logistical regression is used, it a type of classification

<img width="775" alt="To solve" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/ead7abb3-fcd9-4451-a371-e7ed86d42c9b">

## Sigmoid Funtion and its use in Logistical Regression:
-  The logistic function in linear regression is a type of sigmoid, a class of functions with the same specific properties. Sigmoid is a mathematical function that takes any real number and maps it to a probability between 1 and 0.

<img width="1380" alt="Sigmoid_funct" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/36b24575-4b50-4377-9bd6-1ac3e82a62b5">

## Interpretation of logistic regression output:

<img width="1380" alt="Output_Interpretation" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/f15c414f-0a9a-4ad7-805a-10ed418ed355">

## Decision Boundary:
Condition for the binaries:
<img width="576" alt="Condition" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/605a11a2-aa9c-4b75-8095-0500c33b271f">

Types of Decision Boundary:
 - Linear Decision Boundary:
<img width="1278" alt="Linear" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/11bfe5df-9075-4f5c-a737-1bd2dc51be66">

 - Non-Linear Decision Boundary:
<img width="1298" alt="Non-Linear" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/4e1880d3-2178-42ca-86dc-dd229462afa9">

## Cost Function for Logistic Regression:
### Complex Cost Funtion:
<img width="1293" alt="Training_Set" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/93a91134-f0f4-408b-8043-3b1e114181fb">
<img width="1269" alt="LR_not working" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/08a20005-06d8-49cc-99da-d76e3da44e8d">
<img width="1318" alt="Improved Cost function" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/5fdbae55-868b-4d7e-977c-386e38e5e87b">
<img width="1315" alt="Explainaition" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/55e1369b-36c7-499b-8d23-5fe0fe550206">
<img width="1317" alt="Summary_Cost_Funct" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/c0816672-44da-417a-9fdf-6b598237cfed">

### Simplified Cost Function:
<img width="1318" alt="Loss_Func" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/ae19e301-3f93-4e65-8d8a-3bbc1a326892">
<img width="1301" alt="Cost_Funct" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/eccc04ea-2e51-4a01-bae9-4d8691532cee">
