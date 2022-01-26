# Book_Club_Project

##This report is based off of the findings from the Charles Book Club data set that was provided. Throughout this report, variables will be referenced by the column name that they were assigned to in the excel spreadsheet. This report covers basic statistics and correlations that were found within the dataset. All visualizations can be found at the end of the report.

Summary statistics were calculated for the variables labeled “M”, “R”, and “F” (See visualization 1). For each variable, the median is slightly less than the mean. This suggests that the bell curve for each variable is slightly skewed to the right. The average time since last purchase is over thirteen months. This should be taken into account when developing a marketing strategy to attract repeat customers.

Next, bar plots were constructed to show comparative values. The first bar plot compares the number of men and women who responded to the test mailing (See visualization 2). This chart shows that 2,818 (70.45%) of the respondents were female and that 1,182 (29.55%) of the respondents were male. This data holds true only if the value of 1 was intended to represent a response from a female.

The second bar plot that was constructed pertained to the purchase of the book titled “Florence” (See visualization 3). This chart shows that 3,662 (91.55%) customers did not purchase the book and that 338 (8.45%) customers did purchase the book. This percentage would be more meaningful if there were other book titles with purchase records to compare to.

The variables “M”, “R”, and “F” were grouped by whether the customer had or had not bought “Florence”. These variables in their respective groups were then compared by their average values (See visualizations 4, 5, and 6). The grouping by “Florence” seemed to have minimal effect on the variables.

The three variables chosen from the scatterplot matrix are “FirstPurch”, “CookBks”, and “ItalCook”. Visualization 7 shows the entire matrix, whereas visualization 8 shows only the three variables chosen. It looks as if there may be a slight correlation between “FirstPurch” and “CookBks”. The other two scatter plots suggest no correlation. The correlation value in the heatmap (see visualization 9) confirms that there is a correlation between “FirstPurch” and “CookBks”. It confirms that is the only correlation among the three variables chosen.

The boxplots in visualization 10 group the variables “M”, “R”, and “F” by the variable “Florence”. This factor affected the boxplot of variable “M” minimally. It affected the other two variables by increasing the interquartile range.

<img width="205" alt="image" src="https://user-images.githubusercontent.com/95591222/151230118-729768d3-76b3-4227-a9d7-60a46e3e9524.png">
<img width="206" alt="image" src="https://user-images.githubusercontent.com/95591222/151230163-2ddf3e36-e067-4c8a-9476-06449f4e6969.png">
<img width="155" alt="image" src="https://user-images.githubusercontent.com/95591222/151230186-f31d615d-9967-4eb4-bfa8-03fe57e06a44.png">
<img width="277" alt="image" src="https://user-images.githubusercontent.com/95591222/151230209-1fdc7fef-9838-4a1c-baf1-f218818104d4.png">
<img width="254" alt="image" src="https://user-images.githubusercontent.com/95591222/151230231-2773674f-30a8-4318-8f38-8c123bb53c17.png">
<img width="301" alt="image" src="https://user-images.githubusercontent.com/95591222/151230261-b96c01b4-f213-4c60-ba8d-3c57badcb74d.png">

Date Modeling

Using five different data modeling techniques we can see what model gives us the best output. The model’s output is as follows: 
Decision Tree (DT)- The decision tree gives us an average misclassification score of 8.3%. This implies that the model is wrong 8.3% of the time. The average accuracy score using a 10-fold cross validation is 9.1%

Logistic Regression (LOG)- This model’s average misclassification score implies the model is wrong 7.8% of the time. The average accuracy score using a 10-fold cross validation is 9.2%

kNN- The average misclassification score implies the model is wrong 8.5% of the time. The average accuracy score using a 10-fold cross validation is 9.1%

Discriminant Analysis (DA)- The discriminate analysis gives us an average misclassification score of 8.1%. This implies the model is wrong 8.1% of the time. The average accuracy score using a 10-fold cross validation is 9.1%

Neural Networks (MLP)- The average misclassification score implies the model is wrong 7.8% of the time. The average accuracy score using a 10-fold cross validation is 9.2%

In conclusion, both neural networks and logistic models have the same accuracy score of 0.922. The data is heavily skewed for negative results therefore the true positives for each model are very small relative to data set.

#Roc Curve

The Roc curve tells us how good the model is for distinguishing the given classes, in terms of the predicted probability. Based on the ROC curves the neural networks model (MLP) at 0.529 is the best model and the kNN at 0.497 is the worst. This roc curve suggests that all the models aren’t any better than simply guessing. 

<img width="215" alt="image" src="https://user-images.githubusercontent.com/95591222/151230638-5246255f-2005-4413-b2bd-0586db21481c.png">

#Lift Charts

The lift curve is an evaluation curve that assesses the performance of your model. It shows how many times more than average the model reaches targets. The lift charts and cumulative gains models do not perform significantly better than using no model. This shows the models are not giving us a very good prediction. It is recommended to make sure preprocessing parameters are correct or may suggest we have bad data. 
