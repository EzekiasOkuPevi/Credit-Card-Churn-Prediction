# Abstract
In this research, I critically explored data from a credit card firm to unravel trends in customer behaviour and  generate actionable insights to help reduce customer attrition.
Abstract – Attrition is a crucial measure of the health of a business. Banks are faced with a major challenge of credit card churn, and this creates the need for tools that can effectively predict attrition.
In this research, we critically explored the credit card churn dataset to unravel trends in customer behaviour and generated actionable insights to help reduce attrition. We trained Random Forest model on the credit card churn dataset to serve as an effective tool for identifying customers who are likely to leave. The model achieved an accuracy of 95% proving its capacity to correctly classify churned and non-churned customers. The model had good precision score of 80% for churned
customers and 90% for non-churned customers. A Logistic Regression model was fitted with the data to investigate the statistical importance of each feature
in churn prediction and generate actionable insights to reduce attrition. Total Transaction Amount and Total transaction Count were seen to be important factors in predicting attrition. Our predictive model serves as a useful tool to financial organizations looking to stay ahead of the competition in the credit card industry.

# Dataset Description
The credit card churn dataset was gotten from Kaggle. It consists of 23 variables and 10,127 observations representing customer data in a credit card company.
These features include financial information such as earnings and credit limit, transaction history and demography. It has a target feature “Attrition” that indicates a churned or non-churned customer. The dataset is useful for analyzing elements that influence customer behavior and creating models to predict attrition. 

# Methodology
This research was implemented using a range of tools. Python programming language was used in Jupiter notebook for data cleaning, preprocessing, and modelling. Power BI and Rapid Miner were used for data exploration and visualization.

# Data Preprocessing
All rows with unknown values were dropped. All categorical features were mapped to categorical datatype for better handling. Dummy encoding was performed on nominal categorical features

# Exploratory Data Analysis
Count plots were used to explore the distribution of each categorical feature in the dataset.
This plot enabled us to identify an imbalance in the target class “Attrition Flag” with existing customers and attrited customers amounting to a ratio 5:1.

![image](https://github.com/user-attachments/assets/6760a071-ab69-4828-b564-e3d26eb94989)

A pie chart of percentage of attrited customer to existing customers in each income category was plotted and we can deduce from the chart that higher income category can be associated with a higher likelihood of churn.

![image](https://github.com/user-attachments/assets/1acea6c6-1a6d-4362-9cb3-0e0961a8a1be)

Box plot of Transaction count against Attrition Flag indicates a clear difference between the spread for existing and Attrited customers. Mean Count for attrited customers is centered around 40 while existing customers is centered around 50. This proves that Total Transaction count is a key feature in churn prediction.

![image](https://github.com/user-attachments/assets/5202039d-0d0c-4f90-8ccb-891871d1137e)

Correlation analysis was done using a correlation matrix plot in python using the seaborn library. With this plot, multicollinearity was observed among a few variables. For example, Customer Age has a strong positive correlation with Months on book, Avg open to buy and credit limit also have a strong positive correlation, Total Trans Ct and Total Transaction Amt also exhibit strong positive correlation. To reduce multicollinearity, one of the strongly correlated variables were removed.

![image](https://github.com/user-attachments/assets/7bdb5e60-a66c-410c-910e-5476a294f6ff)

Feature Importance: A feature ranking plot was also created to visually explain feature importance.

![image](https://github.com/user-attachments/assets/4966d558-d1d3-47f3-ac9e-2252f343e9b5)

# Predictive Modelling 
Random Forest model performed excellently with a high accuracy of 95%. Precision score of 0.80 and recall of 0.90 for attrited customers indicates a balanced and dependable classification of churned customers.

# Statistical Modelling
Logistic regression algorithm was fitted with the train dataset and the significance of each feature was determined using the p-value and a significance level of 0.05.
Hypothesis testing:
Null Hypothesis (H0): The corresponding feature has no effect on the dependent variable
Alternative Hypothesis (H1): The corresponding feature has significant effect on the dependent variable. Educational Level, Average Utilization Ratio, Card category and Total Amount Change Q1 – Q4 all had pvalues greater 0.05 this means there is not enough evidence to say that the features have any significant effect on the target variable.
Conversely, Total Transaction Amount, Total Transaction Count, Months Inactive, Income Category among others have p-values less than 0.05 this means there is enough evidence to suggest that the corresponding features are significant in the prediction of attrition. The results of the Logistic Regression model correspond with the output of the feature importance plot.

# Discussion
Insights:
Higher contact counts and longer inactive periods are connected to increased churn rates. Customers with higher income have a higher propensity to churn.

Actions:
Develop plans to re-engage customers who have been inactive for long periods of time. Provide personalized services to high-net worth customers to improve their experience and strengthen loyalty.
