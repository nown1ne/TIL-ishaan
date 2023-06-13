# [Yt Video](https://www.youtube.com/watch?v=H3EjCKtlVog)

# Gaussian Naive Bayes:
Gaussian Naive Bayes is a popular classification algorithm based on the Bayes' theorem, which assumes that the features are conditionally independent given the class label. It is commonly used for solving classification problems with continuous or real-valued features. Here's a detailed explanation of Gaussian Naive Bayes along with a visual example using code snippets.

<img width="1390" alt="Screenshot 2023-06-13 at 12 05 23 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/343ca3b8-ff34-4dd1-9504-bda5e032afd8">

1. Algorithm Overview:
   - Gaussian Naive Bayes calculates the probability of each class label given the input features and then assigns the label with the highest probability as the predicted class.
   - It assumes that the features follow a Gaussian (normal) distribution within each class.

2. Training Phase:
   - During the training phase, the algorithm estimates the parameters of the Gaussian distribution for each feature within each class. These parameters include the mean and variance of each feature.
   - The algorithm calculates the class prior probabilities, which are the probabilities of each class occurring in the training data.

3. Prediction Phase:
   - Given a new instance with feature values, Gaussian Naive Bayes calculates the conditional probability of each class given the features using Bayes' theorem.
   - The conditional probability is calculated by multiplying the class prior probability with the product of the probabilities of each feature value given the class, according to the Gaussian distribution parameters estimated during training.
   - The predicted class label is the one with the highest conditional probability.

Now, let's illustrate Gaussian Naive Bayes with a visual example using Python code snippets:

```python
# Import the necessary libraries
from sklearn.datasets import load_iris
from sklearn.naive_bayes import GaussianNB
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

# Load the Iris dataset
data = load_iris()
X = data.data  # Features
y = data.target  # Class labels

# Split the dataset into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create a Gaussian Naive Bayes classifier
gnb = GaussianNB()

# Train the classifier
gnb.fit(X_train, y_train)

# Make predictions on the test set
y_pred = gnb.predict(X_test)

# Calculate the accuracy of the classifier
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)
```

In this example, we load the Iris dataset, which is a popular dataset for classification tasks. We split the dataset into training and testing sets using `train_test_split` from the `sklearn.model_selection` module. Then, we create an instance of the Gaussian Naive Bayes classifier (`GaussianNB`) and train it using the training data.

Next, we make predictions on the test set using the trained classifier (`predict` method). Finally, we calculate the accuracy of the classifier by comparing the predicted labels with the actual labels (`accuracy_score`).

This visual example demonstrates how Gaussian Naive Bayes can be applied to a real dataset for classification tasks. By learning the parameters of the Gaussian distribution for each class, the algorithm can make predictions based on the likelihood of a particular instance belonging to each class.

Note: This example uses the scikit-learn library, which provides efficient implementations of machine learning algorithms in Python.
