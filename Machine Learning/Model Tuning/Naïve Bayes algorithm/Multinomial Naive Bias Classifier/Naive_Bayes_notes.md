# [Yt Video](https://www.youtube.com/watch?v=jS1CKhALUBQ)

## Dataset:
- It we want to classify mails into span and regular messages
  - Regular Messages:
    - Make Histogram of all the words that occur in regular messages, we use this to calculate the probabilities of seeing each word  and then classfiy them as regular mail

#### Likelihood: 
Probablilites calculated of discrete, individual words, and not the probability of something continuous, like weight and height, these are called likelihoods


<img width="835" alt="Screenshot 2023-06-12 at 9 08 49 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/c225fba0-65ef-4696-b11c-e14818c3e6bf">
<img width="866" alt="Screenshot 2023-06-12 at 9 09 03 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/7eec6963-0fac-42da-81f9-1dd250282d9f">
<img width="834" alt="Screenshot 2023-06-12 at 9 09 15 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/45b138ab-68e2-4f49-b04f-2ef6f1a171d4">
<img width="830" alt="Screenshot 2023-06-12 at 9 09 24 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/09e22bbb-91ce-47b1-a279-5f38ee7891d2">
<img width="826" alt="Screenshot 2023-06-12 at 9 09 34 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/6a17b73a-5fbb-48b4-bad4-6ddce9081798">
<img width="868" alt="Screenshot 2023-06-12 at 9 09 58 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/df99d3bb-cae6-4d30-9cfe-0e24564a8a82">

---------x---------
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
