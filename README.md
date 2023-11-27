# Credit-Card-Customer-Churns-1-

## 1) Objectives of the analysis:
### 1.1) Research problems description:
Customers in the banking industry can choose from a variety of service providers and actively switch from one to the next. The banking business has an annual churn rate of 15-25 percent in this highly competitive market.
Individualized customer retention is tough because most firms have a large number of customers and can't afford to devote much time to each of them. The costs would be too great, outweighing the additional revenue. However, if a corporation could forecast which customers are likely to leave ahead of time, it could focus customer retention efforts only on these "high risk" clients. The ultimate goal is to expand its coverage area and retrieve more customers' loyalty. The core to succeed in this market lies in the customer itself.
Customer churn is a critical metric because it is much less expensive to retain existing customers than it is to acquire new customers.

### 1.2) Research objectives:
To reduce customer churn, telecom companies need to predict which customers are at high risk of churn.
To detect early signs of potential churn, one must first develop a holistic view of the customers and their interactions across numerous channels, including CreditScore Geography, Gender, Age, Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary, to mention a few.
As a result, by addressing churn, these businesses may not only preserve their market position, but also grow and thrive. More customers they have in their network, the lower the cost of initiation and the larger the profit. As a result, the company's key focus for success is reducing client attrition and implementing effective retention strategy.
### 1.3) Research questions: 

We will explore the data and try to answer some questions like:
What's the % of Churn Customers and customers that keep in with the active services?
Are there any patterns in Churn Customers based on each of the attributes?
Is there any patterns/preference in Churn Customers based on whether or not customers have a credit card?
Many more questions that will arise during the analysis.

## 2) Data source:
**Data**: Customer Churn Prediction

**Shape**: 14 columns, 10000 entries

**Attribute**:

**RowNumber**—corresponds to the record (row) number and has no effect on the output.

**CustomerId**—contains random values and has no effect on customer leaving the bank.

**Surname**—the surname of a customer has no impact on their decision to leave the bank.

**CreditScore**—can have an effect on customer churn, since a customer with a higher credit score is less likely to leave the bank.

**Geography**—a customer’s location can affect their decision to leave the bank.

**Gender**—it’s interesting to explore whether gender plays a role in a customer leaving the bank.

**Age**—this is certainly relevant, since older customers are less likely to leave their bank than younger ones.

**Tenure**—refers to the number of years that the customer has been a client of the bank. Normally, older clients are more loyal and less likely to leave a bank.

**Balance**—also a very good indicator of customer churn, as people with a higher balance in their accounts are less likely to leave the bank compared to those with lower balances.

**NumOfProducts**—refers to the number of products that a customer has purchased through the bank.

**HasCrCard**—denotes whether or not a customer has a credit card. This column is also relevant, since people with a credit card are less likely to leave the bank.

**IsActiveMember**—active customers are less likely to leave the bank.

**EstimatedSalary**—as with balance, people with lower salaries are more likely to leave the bank compared to those with higher salaries.

**Exited**—whether or not the customer left the bank.

## 3) How to apply Data Mining to the analysis:
### 3.1) Analysis process:
#### 3.1.1) Data Preprocessing:
Looking for null variables
Find statistical numbers 
#### 3.1.2) EDA
Find the relationship between each variable and customer churn rate:

**Age variable**:

![Age variable.png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/496e6b38f9e8a5f6a976a69bc4e3083ed6e8cba3/Images/Age%20variable.png)

A majority of the churned customers fall within the 45 to 65 age range.
Among all the ages, 56-year-olds have the highest ratio of churned customers.
The age of 84 stands out with an unusually high rate of churn, which occurs due to the limited number of customers within this age bracket. Specifically, there are only two 84-year-old customers, and one of them churning results in a churn rate of 50% at age=84.

**Tenure**: Our objective is to determine the credit score ratio between customers who leave and customers who stay, categorized by years of customer service.

![Tenure.png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/496e6b38f9e8a5f6a976a69bc4e3083ed6e8cba3/Images/Tenure.png)


The figure displays the credit score ratio between customers who churn and those who stay, categorized by the number of years they have been with the company.
Based on our analysis, customers who have used the service for either less than a year or 10 years have a smaller representation than other tenures. Moreover, our churn rate appears to fluctuate around 20%, with the lowest rate of 17% observed for customers with a tenure of 7.

**Geography vs gender**: 

![Geography vs gender (1).png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/9b74249cdac38a1012f17c0423df3ac3f3e8888c/Images/Geography%20vs%20gender%20(1).png)


Our proposed plan is to showcase how customers utilize our service, categorized by region and gender, respectively.
In general, females exhibit a higher rate of churning. Furthermore, females in France and Germany demonstrate the highest percentage of churning.

![Geography vs gender (2).png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/9b74249cdac38a1012f17c0423df3ac3f3e8888c/Images/Geography%20vs%20gender%20(2).png)

Among the inactive group, the percentage of inactive male customers is the highest in France. It could be attributed to their significant number of records, coupled with a higher churn rate among female customers.
Despite having the least number of records, Germany still exhibits a high churn rate.

**“Numbers of products” by “Exited” and “Geography”**:

![“Numbers of products” by “Exited” and “Geography” (1).png
](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/9b74249cdac38a1012f17c0423df3ac3f3e8888c/Images/%E2%80%9CNumbers%20of%20products%E2%80%9D%20by%20%E2%80%9CExited%E2%80%9D%20and%20%E2%80%9CGeography%E2%80%9D%20(1).png)

It appears that customers who utilize four products tend to churn across all three countries. Notably, most customers primarily use one or two products.
Furthermore, the number of customers with 1, 2, and 3 products in Germany and Spain is approximately half of those in France.

![“Numbers of products” by “Exited” and “Geography” (2).png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/9b74249cdac38a1012f17c0423df3ac3f3e8888c/Images/%E2%80%9CNumbers%20of%20products%E2%80%9D%20by%20%E2%80%9CExited%E2%80%9D%20and%20%E2%80%9CGeography%E2%80%9D%20(2).png)

According to the graph, it appears that Germany and France have a similar number of churn customers, with a higher number of churns occurring at NumOfProduct=1. This indicates that Germany has a substantially higher churn rate.

#### 3.1.3) Model
Using StandardScaler to convert data to the same scale.
Remove outliers.
Predict the output by using some basic Machine Learning such as LogisticRegression, RandomForest, DecisionTree.  
Evaluating the prediction depends on Accuracy Score.

## 4) Final result:
**After run the data through various models we end up with the following results**:

![DecisionTree.png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/9b74249cdac38a1012f17c0423df3ac3f3e8888c/Images/DecisionTree.png)

![LogisticRegression.png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/9b74249cdac38a1012f17c0423df3ac3f3e8888c/Images/LogisticRegression.png)

![RandomForest.png](https://github.com/khvu0610/Credit-Card-Customer-Churns-1-/blob/9b74249cdac38a1012f17c0423df3ac3f3e8888c/Images/RandomForest.png)



As RandomForest model gave the best results, it will be selected as the final result of this project.

## 5) Conclusion:
In the case of imbalanced datasets, the Accuracy Score may not be the most reliable measure to assess model performance due to differences in the sample distribution between the training set and actual data. Instead, metrics such as Recall, f1 Score, and ROC curve, are more appropriate to evaluate an imbalanced dataset.
Based on the analysis, the following insights can be drawn:
Customer variability was not influenced by the HasCrcard variable.
German customers exhibit a high churn rate.
Customers who use 3 to 4 products are more likely to discontinue their relationship with the bank.
Customers who have been using the service for less than one year or over ten years are less represented than in other time periods.
Customers between the ages of 40 and 65 are more prone to leaving banks.
Individuals with credit scores ranging from 600 to 700 display elevated churn rates.
The predictions were generated using four classification models, with RandomForest yielding the highest f1 score.
