# Neural Network Charity Analysis

## Overview
The purpose of this analysis is to create a machine learning program that aids us in predicting when funding is approved. 

## Results 
### Data Preprocessing
* What variable(s) are considered the target(s) for your model?
  * Our target for this model was when an application successfully obtained funding.
* What variable(s) are considered to be the features for your model?
  * Features are all variables that give us groupable information. This may include application based features such as application type, object based features such as affiliation, organization, and classification, or money based features such as income and asking amount. All features are different aspects of the application process that help us categorize points that could affect the outcome. 
* What variable(s) are neither targets nor features, and should be removed from the input data?
  * There were only two fields that we dropped. EIN and NAME. Both of these fields are unique to each organization and do not help us predict overall success rates. Although we may be able to use this information if we were to look for a bias in application selection. 
### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * The amount of neurons varied but I found the greatest success using 30-80 neurons, when going to low or high we lost accuray. 
  * We had 3-5 layers, and saw no major changes between adding layers.
  * Biggest change was when we changed activation functions, linear was clearly the worst activation function whereas relu tended to give higher pass rates. I used elu in certain positions and found on average it did perform slightly better then relu.
* Were you able to achieve the target model performance?
  * Sadly no, I don't believe any of the columns should be dropped and wasn't able to change the data enough to get a higher rating. 
* What steps did you take to try and increase model performance?
  * Changed Bin sizes, Seeing if adding more fields helped fix some of our questions. 
  * Dropping columns such as classifications which had many single digit classification.
  * fidgeting with neurons, layers, and activation functions. 
  * attempting to use 2-3 other optimizers (all performed significantly worse)

## Summary
Overall this machine learning algorithm needs a lot of work, I would recommend adding a "decision maker" aspect as one of the columns. As someone who works in compliance, sometimes we are unable to answer questions with a yes or no and the individual deciding to give funding may impact the overall results. One individual may be more conservative or giving compared to others which can tilt the scale. 
