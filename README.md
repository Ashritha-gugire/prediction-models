# prediction-model
## Predicting Loan Defaults using Logistic Regression and Decision trees
### Introduction
This project aims to predict loan defaults using Logistic Regression and Decision Tree models. By analyzing various factors related to borrowers and loan characteristics, we seek to help banks assess the risk of loan default more accurately.

### Dataset

Size: 4110 rows and 16 columns
Year: 2017
Key Features: Loan amount, interest rate, annual income, debt ratio, credit history, employment duration, etc.

### Exploratory Data Analysis (EDA)
_Key findings from the EDA:_

-- Average loan amount: $16,000
-- Average monthly installment: $489
-- Average interest rate: 11.38%
-- Most common loan purpose: Debt consolidation
-- Most common loan term: 3 years
-- 13.3% of borrowers had a history of bankruptcy.


### Key Visualizations:
![image](https://github.com/user-attachments/assets/0a0ea030-d60b-48b6-877b-9a70e4780034)
Loan Term Distribution
    "3 Years" : 70
    "5 Years" : 30


![image](https://github.com/user-attachments/assets/99374e1c-b92f-463a-84f0-95fc0a8833fd)
Loan Purpose Distribution
    "Debt Consolidation" : 50
    "Credit Card" : 30
    "Other" : 20


Bankruptcy vs. Loan Default
![image](https://github.com/user-attachments/assets/7d825467-9daf-4433-86b9-2d1ed4d3f4be)

Interest Rate vs. Loan Default
![image](https://github.com/user-attachments/assets/97ade7fd-a4e0-4cb8-aac1-d491e7ff7688)


Annual Income vs. Loan Amount for Defaulters
![image](https://github.com/user-attachments/assets/50c22290-813c-410c-a495-e30be9676d0f)

### Models and Performance
1. Decision Tree
![image](https://github.com/user-attachments/assets/cfbe9f5e-dc7a-4472-9fa4-453ef61f7f12)


Accuracy: 91.8%
Precision: 88%
Recall: 99.3%
F1-score: 93.8%
![image](https://github.com/user-attachments/assets/3e986eb1-014b-4192-8f56-17efed29db45)


2. Logistic Regression

Accuracy: 92%
Precision: 91.3%
Recall: 86.9%
F1-score: 89%
![image](https://github.com/user-attachments/assets/d71786f7-e310-4318-8bd7-e7a4f1f9d969)

**Key Findings**

Higher interest rates correlate with increased likelihood of loan default.
Larger loan amounts surprisingly decreased odds of default, possibly due to more careful planning.
Longer loan terms decreased the odds of defaulting.
Higher income borrowers were less likely to default.
The interaction between loan amount and interest rate is significant.
Debt consolidation and credit card payments are the most common reasons for taking out loans.
Borrowers with a history of bankruptcy are more likely to default (41.8% vs 11.5% for those without).

_Future Work_

Explore anonymized variables in more depth
Analyze demographic and cultural factors
Investigate correlations between independent variables
Experiment with different types of models beyond logistic regression and decision trees

_Tools Used_

R (for statistical analysis and modeling)
Logistic Regression
Decision Tree


In this project, I was only able to examine basic predictor variables such as interest and amount. I did not find many more patterns between other variables, but I would be interested in studying the other variables more in-depth. Anonymized variables specifically were mostly skipped over, so future steps could include researching those. I would also be interested in re-analyzing the variables that I did use by splitting them into different categories. Perhaps this would help identify special patterns in the data that were not clear in previous models. Exploring how demographics and cultural background tie into loan defaulting would also be an interesting extension of this project. Perhaps some cultures emphasize the importance of honor more than others would, thus discouraging using loans and especially defaulting on loans. 

Another option for future research would be examining correlations between independent variables more. Although there were a few graphs of correlations between independent variables in the Exploratory Data Analysis, I largely focused on correlations between default rates and predictor variables in this project. Learning more about how independent variables affect each other may give insight on how they affect default rates. Looking at the coefficients for Model 4, I was surprised that increasing the amount of the loan causes the odds to decrease in general. This may be because borrowers who take out larger loans are more cautious or plan it out more carefully. For example, amortization schedules for mortgages would tend to be more well-planned than repayment for a loan taken out on impulse. However, if interest is raised as well, then the lowering effect of higher loan amounts on probability of default diminishes. Thus, Model 4 implies that the ideal loan with minimal probability of default would have a large amount and a low interest rate.


It is also interesting that a longer term would cause the odds of defaulting to decrease; perhaps this is because borrowers have more time to pull themselves out of debt. Aside from those two predictor variables, interest, income, and the interaction between amount and interest all are expected because wealthier borrowers are more likely to be able to pay back a loan, and high interest loans are less likely to be paid back. 

Generally, I found Model 4, which used the predictor variables of amount, interest, term, income, and an interaction between amount and interest, to perform the best because it balanced simplicity and performance. It was one of the most accurate models I was able to build, but it was not overly complicated, and every predictor variable still had a significant effect on the probability of default. 

In terms of future research, combining some predictor variables from Model 4 with other predictor variables that were left relatively unexplored could yield a better model. If possible, using different types of models would also allow for different interpretations of the same variables. Logistic regression models seem to assume predictor variables have a linear or onedirectional trend. Interest worked particularly well with the logistic regression models because it had such a linear relationship with default rates. However, most variables such as credit balance or loan amount are often more complicated than that. I would be interested in exploring other types of models that could reflect the more complex nature of predictor variables.

### Conclusion: 
Through Exploratory Data Analysis, we discovered correlations in and between predictor variables that would guide us in building our model. We were able to conclude that the probability of a loan default may be predicted by loan interest rates, loan amount, and borrower income, among other factors. We also proved the credibility of our models with evaluation metrics that measured accuracy and error. The predictor variable that best suited logistic regression was interest because of its linear correlation with default. To further improve this research, different predictor variables or types of models may be examined.
