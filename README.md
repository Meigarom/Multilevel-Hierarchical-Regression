# Multilevel-Hierarchical-Regression
This repo contains notes and code from the book "Data Analysis Using Regression and Multilevel-Hierarchical Models

## Chapter 03 - Linear Regression: the basics
Linear regression is a method that summarizes how the average values of a numerical **outcome** variable vary over subpopulations defined by linear functions of **predictors**.

### 3.1. One predictor
- For a binary predictor, the regression coefficient is the difference between the averages of the two groups
- kid.score = 78 + 12 mom.hs + error : This model summarizes the difference in average test scores between the children of mothers who completed high school and those with mothers who did not.

### 3.2. Multiple predictor
- Typical advice is to interpret each coefficient "with all the other predictors held constant".
kid.score = 26 + 6 mom.hs + 0.6 mom.iq + error

1. The **intercept**. If a child had a mother with an IQ of 0 and who did not complete high school, then we would predict this child's test score to be 26. This is not a useful prediction, since no mothers have IQs of 0.

2. The **coefficient of maternal high school completion**. Comparing children whose mothers have the same IQ, but who differed in whether they completed high school, the model predicts an expected difference of 6 in their test scores.

3. The **coefficient of maternal IQ**. Comparing children with the same value of mom.hs, but whose mothers differ by 1 point in IQ, we would expect to see a difference of 0.6 points in the child's test score (equivalently, a difference of 10 in mothers'IQs corresponds to a difference of 6 points for their childre ).

- It's not always possible to change on predictor whicl holding all othres constant. For example, a model that includes interactions between predictors like mom.hs * mom.IQ + mom.IQ^2.

