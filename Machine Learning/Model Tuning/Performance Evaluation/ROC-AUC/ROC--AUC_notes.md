# [Blog](https://www.analyticsvidhya.com/blog/2020/06/auc-roc-curve-machine-learning/?fbclid=IwAR3NiyvLoVEQxRCerb5A3YVU8Qtuf9fpnG5ERWGLBQsfKbpvfuccI-7DI7U)
# [Yt Video](https://www.youtube.com/watch?v=4jRBRDbJemM)
# Dataset:
<img width="1035" alt="Dataset" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/da08f715-250a-49ae-84b5-b0598d1d6c61">

# ROC (Receiver Operating Characteristic Curve):
- An ROC curve (receiver operating characteristic curve) is a graph showing the performance of a classification model at all classification thresholds.
- Used to find the Threshold to be set to get optimal Confusion Matrix, it is based on the amount of false positives we ar willing to accept/

<img width="794" alt="ROC" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/97c163e3-bc23-4389-bf3c-3f28d48d6184">

### Y-Axis:
- True Positive Rate (Sensitivity):
  - The True Positive Ratetells you what proportion of obese samples were correctly classified

### X-Axis:
- False Positive Rate (1-Specificity):
  - Tells us the proportion of not obese samples that that were incorrectly classified and are False Positives

### Green Line:
- The Green Diagonal Line shows where TPR = FPR

# AUC (Area under the Curve):
- It makes it easier to compare one ROC curve to another

<img width="1143" alt="AUC" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/7f0d0b2d-f5f0-482d-bb50-a135f74db9f8">
