Business Problem:

Kickstarter is a crowdfunding platform launched in 2009 that allows creators to fund their creative projects through online campaigns. The platform operates on an all-or-nothing funding model, where a project must reach its funding goal within a set timeframe to receive the pledged funds. Kickstarter has become a popular choice for creators and entrepreneurs looking to raise funds and test market demand for their ideas before investing significant resources into them.

The business problem we are trying to solve was to provide potential Kickstarter creators with insights into the likelihood of their campaigns succeeding. As Kickstarter campaigns can be a significant financial investment, it is essential to have an idea of the chances of success before launching a campaign. By identifying the most important predictors of success, we aim to provide potential Kickstarter creators with the tools to improve their chances of success. With a more knowledgeable base of prospects, we believe that creators will be encouraged to pursue more Kickstarter campaigns, driving revenue for both creators and Kickstarter. 

Dataset and Approach:
We analyzed a 2017 Kaggle dataset that contained information on over 20,000 Kickstarter campaigns. The dataset included fields such as the fundraising goal, amount pledged, length of time of the campaign, number of backers count, project category,  campaign name length, and success status.  To prepare the data for a random forest classification model, we removed some fields that were deterministic in nature (too good at predicting the outcome), such as amount pledged, fundraising goal, and backers count. We also performed feature engineering, such as one-hot encoding, to allow for categorical variables to be included in the model.  Once a random forest model was trained, we were able to predict the success or failure of a Kickstarter campaign based on the remaining fields in the dataset with the goal of providing valuable insights for creators seeking to launch successful campaigns in the future.

We decided to use a random forest classifier as opposed to another classification model such as a logistic regression for a few reasons. First, a random forest model can handle a large number of input features and still maintain high accuracy. Second, it is less prone to overfitting compared to other decision tree-based algorithms. Finally, it can provide feature importance scores, which can help in understanding the importance of different input features in predicting the target variable.

Model Performance:
With an accuracy of .772 the model was able to correctly predict the outcome in 77.2% of the cases. However with a true recall of .57 that means of all true positives outcomes the model only predicted 57% of them. The actual ability of the model to predict success is only marginally better than a coin flip.

Limitations:
One limitations in the dataset was that we did not analyze positive or negative correlations. Add more here
Another limitation was that the data had not been updated in 6 years.  This is a limitation because the market can change in that time.  Also, it would have been interesting to see COVID data since there was a shift in spending during that time period. 
