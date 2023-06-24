# [Hyperparameter Tuning](https://www.youtube.com/watch?v=DTcfH5W6o08)
# [GridSearchCV and RandomizedSearchCV](https://www.youtube.com/watch?v=aijB8qbEOQ4)
# Hyperparameter Tuning:
Hyperparameter tuning takes advantage of the processing infrastructure of Google Cloud to test different hyperparameter configurations when training your model. 
It can give you optimized values for hyperparameters, which maximizes your model's predictive accuracy.

![67819opt](https://github.com/IshaanAdarsh/TIL/assets/100434702/5ade7a2b-6291-4ae2-b74a-a8c4d1bec04f)

## Types of parameters:
<img width="1293" alt="Screenshot 2023-06-24 at 4 23 02 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/bc61a6e3-ad42-4277-b38e-3a47450a939c">

<img width="650" alt="Screenshot 2023-06-24 at 4 24 48 PM" src="https://github.com/IshaanAdarsh/TIL/assets/100434702/6cd45a45-3ea5-4685-a2f2-91b34fdd60fd">

## Understanding Hyperparameter Tuning:
Imagine you have a toy car that you can control using buttons. Now, the car has some special settings that you can adjust to make it go faster or slower, turn left or right more sharply, or even change the color of its body.

In the same way, when we talk about hyperparameter tuning in machine learning, we are trying to find the best settings for a special computer program called a model. This model helps us make predictions or find patterns in data, just like the toy car helps us move around.

The hyperparameters are like the special settings of the model. They control how the model behaves and how well it can make predictions. By tuning the hyperparameters, we try different combinations of settings to see which ones work the best.

### Random Search Method:
Now, let's talk about GridSearchCV and RandomizedSearchCV. These are two ways to help us find the best hyperparameter settings for our model.

Imagine you have a bunch of different toys, each with its own special settings. GridSearchCV is like looking at all the toys on a grid and trying out every possible combination of their settings. It goes through each toy, tries different settings, and keeps track of how well the toy performs. In the end, it tells us which combination of settings worked the best.

RandomizedSearchCV, on the other hand, is like picking toys randomly from a big toy box. Instead of trying every possible combination, it randomly selects different toys with different settings. It tries them out and keeps track of their performance. Even though it doesn't try every combination like GridSearchCV, it can still find really good settings because it explores a wide variety of toys and settings.

So, GridSearchCV and RandomizedSearchCV are tools that help us find the best hyperparameter settings for our model. GridSearchCV tries out every combination of settings like toys on a grid, while RandomizedSearchCV randomly picks and tries out different settings like toys from a toy box.
