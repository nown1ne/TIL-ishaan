# [Yt Video](https://www.youtube.com/watch?v=jS1CKhALUBQ)

## Bayes' Theorem:
- It is a fundamental concept in probability theory and statistics that describes the probability of an event based on prior knowledge or information. It is named after Thomas Bayes, an 18th-century British mathematician.
- Bayes' Theorem can be expressed as:
`P(A|B) = (P(B|A) * P(A)) / P(B)`

Where:
-   P(A|B) is the probability of event A occurring given that event B has occurred.
-   P(B|A) is the probability of event B occurring given that event A has occurred.
-   P(A) and P(B) are the probabilities of events A and B occurring independently.

## Naive Bayes' Classifier:
- It is a machine learning algorithm that utilizes Bayes' Theorem to make predictions or classify data. It is called "naive" because it assumes independence among the features, meaning that the presence or absence of one feature does not affect the presence or absence of another feature. Despite this simplifying assumption, Naive Bayes' Classifier often performs well in practice and is computationally efficient.
- The formula for Naive Bayes' Classifier can be written as:
`P(C|X) = (P(X|C) * P(C)) / P(X)`

Where:
-   P(C|X) is the probability of class C given the features X.
-   P(X|C) is the probability of features X occurring given class C.
-   P(C) is the prior probability of class C.
-   P(X) is the prior probability of features X.

The Naive Bayes' Classifier approximates the probabilities P(C|X) using the training data and applies the maximum a posteriori (MAP) rule to classify new instances. It calculates the probability of each class given the features and selects the class with the highest probability as the predicted class.

Naive Bayes' Classifier is commonly used in various applications, including:

1.  Text Classification: It can classify documents into categories, such as spam detection or sentiment analysis.
2.  Recommendation Systems: It can predict user preferences based on historical data.
3.  Medical Diagnosis: It can assist in diagnosing diseases based on symptoms.
4.  Fraud Detection: It can identify fraudulent transactions based on patterns and features.

### Example:
Email spam classification using Naive Bayes' Classifier. Given a set of emails with labeled spam and non-spam, the classifier learns the probability distribution of features (words) for each class. When a new email arrives, the classifier calculates the probability of it being spam or non-spam based on the occurrence of words in the email. It assigns the email to the class with the higher probability, enabling effective spam filtering.
