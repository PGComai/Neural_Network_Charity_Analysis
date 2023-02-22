# Neural_Network_Charity_Analysis
 
## Overview

This analysis looked at data on charity contributions from a company called AlphabetSoup. The dataset described each contribution using attributes such as amount requested, use case, and various other classification schemes, as well as whether or not the charity succeeded in its objective. The goal of this analysis was to attempt to predict the viability of a potential donation using a neural network trained on previous recipient data.

The data columns can be seen below:

![image](images/table.png)

## Results

### Preprocessing

IF_SUCCESSFUL is the target variable, and the rest of the columns are fed to the model as features. Two other columns were removed from the dataset because they contained identifying information about the recipients, which would not be helpful for the model.

### Modeling

The first neural network tested consisted of two hidden layers; the first with 80 neurons and the second with 30. Both layers used the relu activation function.

The accuracy of this initial model was around 74%, but the goal of this challenge was to improve the performance of the model beyond 75%. I was not able to achieve this in my analysis. I made no changes that improved the performance, only ones that lowered it anywhere from 1 to 10 percent.

The changes I implemented include:

- Adding a third hidden layer
- Increasing/decreasing the amount of neurons in each layer
- Trying different activation functions
- Including/excluding different columns or ranges of data

The most notable change came from removing the AFFILIATION column. This brought model performance down to 65%, which seems to mean that affiliation has some bearing on the neural networks outcome. Other columns did not prove as important, but still I was unable to cross the 75% accuracy threshold.

## Summary

The model performed better than random, but I am not satisfied with its performance. Throughout my testing the model would show a slightly lower accuracy when predicting testing data versus training data, which leads me to believe the model is suffering from overfitting. This fact combined with my inability to get increased accuracy makes me want to try different types of machine learning models. If none perform any better, then I would have to revisit the neural network.