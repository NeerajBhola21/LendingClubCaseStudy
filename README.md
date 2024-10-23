# Lending Club Case Study
> Outline a brief description of your project.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
### Problem Statement
You work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
1. If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
2. If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.

### Objective
The main objective of this analysis is to:

- Understand the factors that contribute to loan defaults.
- Analyze the key factors affecting loan repayment using both univariate and bivariate analysis.
- Build predictive models to classify the loan status of borrowers.
- Provide business insights to help reduce defaults by highlighting risk factors.

### Dataset
The dataset used for this project contains detailed loan records of borrowers from the Lending Club platform. It includes both categorical and numerical features, such as loan amount, interest rate, employment status, and loan grade.
The loan dataset provided includes 39717 rows and 111 columns.

### Data Summary

    loan_amnt: The loan amount applied by the borrower.
    int_rate: The interest rate on the loan.
    annual_inc: The borrower's annual income.
    loan_status: The final status of the loan (fully paid, charged off, current).
    grade and sub_grade: Lending Club's internal grading system.
    emp_title: Job title of the borrower.
    term: Duration of the loan (in months) - 2 variant were (i) 36 months, (ii) 60 months.
    purpose: The stated reason for the loan (e.g., debt consolidation, home improvement).
    home_ownership:	The home ownership status provided by the borrower during registration. Our values are: RENT, OWN, MORTGAGE, OTHER.
    
## Approach
### Data Cleaning
- No header, footers, summary or rows numbers were found in the dataset.  
- no duplicates rows found.
- 1140 rows present of loan_status=‘current’ which has been deleted as loan_status =‘current’ is not required for analysis. 
- 55 columns have all the rows values as “null / blank” and doesn’t participate in analyze has been removed.
- ‘url’ and ‘member_id’ is unique in nature and has been deleted. Have considered ‘id’ for further analysis.  
- ‘desc’ and ‘title’  contains text/description values and doesn’t participate has been dropped from analysis.
- Limiting our analysis to ‘Group’ level only hence sub-group has been dropped.
- Using  domain knowledge, behavioral data is captured and hence will not available during the loan approval and is not considered in  this analysis.
- 21 behavioral data columns has deleted.
- 8 columns whose values were 1, since this is a unique value it has been dropped from analysis.  
- There were two columns which is having more that 50% of data as “NA” has been removed.
- After completing all the data cleaning process, we are left with 38577 rows and 20 columns for our analysis.

### Exploratory Data Analysis (EDA)

- Univariate Analysis: Studied the distribution of key numerical features such as loan_amnt, annual_inc, and int_rate using histograms and boxplots.
- Bivariate Analysis: Analyzed the relationship between loan_status and other features like int_rate, annual_inc, and purpose using stacked bar plots and correlation heatmaps.
- Categorical Feature Analysis: Examined categorical features such as grade, home_ownership, and verification_status to understand their influence on loan defaults.

## Conclusions
### 1. Annual Income -
It is oserved that the applicants with higher incomce are less likely to be in charge off category. It shows a negative correlation with Chargeoff due to financial stability.
### 2. Interest Rate -
Charged off proportion increases with higher intrest rates. i.e Interest Rate and Chargeoff shows positive Correlation.
### 3. Home Ownership -
Applicant owning a house are ledd likely to default the loan. Whereas, those who are not owning the home is having high chances of loan defaults.
### 4. Purpose of loan - 
Applicant applied for loan for a small business have found to be less percentage of chargeoff.
### 5. State -
Applicants form 'DE' States is holding highest number of loan defaults while, from CA is having low number of loan defaults
### 6. Bankruptcies
Lower the Bankruptcies, lower the risk.

## Technologies Used
- Python: The primary programming language used for data analysis and model development.
- Pandas (version 1.3.3): For data undersatnding, manipulation, imputation and preparation.
- NumPy (version 1.21.2): For numerical computations, used primarily for array operations and statistical calculations.
- Matplotlib (version 3.4.3): For data visualization, used to create plots such as histograms, boxplots, pie and bar charts.
- Seaborn (version 0.11.2): High-level visualization library based on Matplotlib, used for statistical graphics like heatmaps and count plots.
- Jupyter Notebook: For writing and organizing the code, visualizations, and documentation interactively.

## Contact
Created by @neerajbhola21 and @mrudhulk - feel free to contact me!


End of Document