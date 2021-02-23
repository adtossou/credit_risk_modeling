# credit_risk_modeling

This is an end-to-end credit risk modeling project, including PD, LGD, EAD, Expected Loss, and Scorecards. I collected the dataset from kaggle.com and it’s real-world data from The Lending Club, a financial institution that does peer-to-peer lending and alternative investing. Their product lines cover personal loans, auto refinancing loans, business loans, and medical financing. Website: www.lendingclub.com. The dataset used in modeling contains all available data for more than 800,000 consumer loans issued from 2007 to 2015.

I used Python (in the Anaconda environment) to do this. The project covers:
•	Data preprocessing:
o	Exploratory data analysis (EDA)
o	Data cleaning: missing observations, converting categorical labels to numeric, etc.
o	Variable/feature selection, that resulted in more parsimonious models
•	Data transformation: 
o	I used normalization here
•	Variable selection: 
o	I used techniques such as coarse classing, fine classing, weight of evidence and information value
•	Data splitting: 
o	I used an 80/20 split into training and testing sets
•	Cross-validation: 
o	I used 10-folds
•	Probability of default (PD): 
o	Model: logistic regression
o	Scorecard creation: model coefficients are rescaled to the 300-850 range to fit conventional credit score versions (e.g., FICO)
o	Performance measure: AUC
•	Loss given default (LGD):
o	it’s customary to use this formula here: 1 – Recovery Rate
o	the data is fits a Beta distribution. But I used Ordinary Least Squares (OLS) for modeling here, due to some limitations with Python
o	Performance measure: R-squared
•	Exposure at default (EAD)
o	I used OLS here
o	Performance measure: R-squared
•	Model validation:
o	I used the testing set for this
•	Expected loss (EL) calculation:
o	I used this formula: EL = PD * (1 – Recovery Rate) * EAD
