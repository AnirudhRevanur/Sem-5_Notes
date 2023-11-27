# Unit 3

## Ensemble Learning

- Is a technique that combines the predictions from multiple machine learning algos together
- It is used to make more accurate predictions then an individual model
- Learners that we use are ___weak learners___
- Comes at a cost of increased algorithmic and model complexity


### Key Idea 1

- We have learners where the output is just better than 50%, but not very high
- Multiple learners can be modelled using
  - Different Alogs
  - Different Hyperparameters on the same algorithm
  - Different subsets of the training data
  - Different features of the training data


### Key Idea 2

- Contruct multiple, diverse predictive models from adapted versions of the training data
- Combine the predictions of these models in some way, usually by weighted averaging or voting


### General Idea

- Decision Trees overfit, hence they have high variance
- Ensemble Learning ensures that the combined model of several weak learners have a less variance than the decision tree
- ___Averaging a set of observations reduces the variance___
- The errors must be made independent of each other


### Bias and Variance

- Model with High Bias is too simple and low predictors
- Pays little attention to the training data and oversimplifies the model
- High Error on Test and Training Data
- Model with High Variance is too complex and has too many predictors
- It cannot generalize this model to unseen data

- Low bias has high flexibility
- High Variance we give different subsets of training data
- More flexible representations have high Variance
- We want to have ___Low Bias and Low Variance___
- Basic models do not perform so well as they have high bias or too much variance

- Ensemble learning prevents overfitting

![Probability](Probability.png "Probability")


### Combining Ensemble Learners

- Learners can be unweighted
- Can be weighted to d<sub>j</sub> accuracy, 1/variance of the learner

![Prediction](Prediction.png "Prediction")

- The critical point of ensemble learners is that they need to be independent
- Using either different subsets or sub learners

### Types of Ensemble Methods
- Manipulate data distribution
  - Example: Bagging, Boosting
- Manipulate input features
  - Example: Random Forests
- Manipulate class labels
  - Example: Error-Correcting output coding

## Bagging

- We can make different learners to have independent errors by splitting the data into subsets and passing them to different learners
- As we are splitting the data, dataset might be small and we may end up with high variance and overfitting
- Can randomly smaple from the dataset creating new datasets of the same size, or a very large fraction of the data set with replacement
- This method is called ___Bootstrap Aggregation___ or ___Bagging___
- We have close to 67% of data from the original dataset.

- Probability of Data __Not__ being selected = (1 - 1/n)<sup>n</sup>

- Multiple subsets are created from the original dataset
- A weak model is created on each of these subsets
- Final predictions are done by combining the predictions from all the models

#### Error Calculation

- Can do K-fold cross validation for error calculation
- Usually 1/3 of the samples are left out in every subset
- These 1/3 samples are called "Out of the Bag Samples"
- Measure the error on the unused samples
- Average that error
- Average of the error gives us the error for that sample
- Accumulate the overall error of the "Out of Bag Samples" and find average
- This error calculation is close to the leave out one approach


- ___About 100 learners are enough___


## Boosting

- Let different learners ahve different weights
- These weights can be stated by accuracy or variance
- Let each learner progressively learn from the previous learner
- Learner 2 can make mistakes, but it is told to learn from Learner 1's mistakes and not repeat them again
- Make sure that all the weights add up to 1

|Boosting|Bagging|
|:------:|:-----:|
|1. Observations are weighted and therefore some will take part in the new set more often|Any element has the same probability to appear in a new data set|

- One of the most popular boosting technique is ___Adaboost___
- Use a weak learner called a decision stump
- One node and based the values it does a binary split
- Boosting this way so the model _learns slowly and incrementally_

- There is a chance to overfit


## Adaboost

- There is only 1 data set being used
- Initialize to the same normal weight, ie. 1/N, where N = Number of Instances
- Choose learner with highest accuracy
- Run the algorithm and collect the error rate = % of misclassified examples
- Ensure that the next learner does not misclassify the points that the first learner made a mistake on
- Continue until satisfied
- Finally take a vote of all the hypothesis (weighted) and state the hypothesis
- There are 2 weights: ___Instance Weight and Hypothesis Weight___

![Identity Function](Identity.png "Identity Function")

- Sum of weight * loss column stores the total error
- Compute the stump weight

- The main selling point of Adaboost is that the next learner learns frmo the mistakes of the previous
- We do this by increasing the weights of the instances that got it wrong and reduce the weights of the instances that got it right

- When the error rate is 0, alpha is close to infinity
- If the error rate is 0.5, the alpha value is zero, because it's as good as a coin toss
- If error rate is 1, then everything has been classified incorrectly and the alpha value is -infinity


## Maximum Likelihood 



