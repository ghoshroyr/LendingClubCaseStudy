


# Lending Club Case Study

## Table of Contents
* Problem Statement
* Objective
* Approach
* Brief about Data Cleaning
* Univariate and Multivariate analysis.
* Conclusion
* Technologies Used
* Acknowledgments
* Contact

## Problem Statement
Lending Club is a consumer finance marketplace for personal loans that matches borrowers who are seeking a loan with investors looking to lend money and make a return.

It specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant's profile.

Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). The credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed.

In other words, borrowers who default cause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'.

The core objective of the excercise is to help the company minimise the credit loss. There are two potential sources of credit loss are:
1) Applicant likely to repay the loan, such an applicant will bring in profit to the company 
  with interest rates.Rejecting such applicants will result in loss of business.


2)Applicant not likely to repay the loan, i.e. and will potentially default, then approving the 
  loan may lead to a financial loss* for the company

## Objective
The goal is to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA using the given dataset, is the aim of this case study.

If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilise this knowledge for its portfolio and risk assessment.

## Approach
1) Data Undertsanding.
2) Data Cleaning.
3) Data Shaping and Deriving.
4) Univariate Analysis
5) Segmented Univariate Analysis
6) Bivariate Analysis

## Brief about Data Cleaning
Data Cleaning is the process of getting rid of impurities and redundancies present in the data , which might cause errors in analysis process in later stages. In data cleaning we get rid of any null values , duplicate values and any variables which might not contribute to the data analysis.
In this Case study we got rid of Columns which are :
1) Behavourial in nature, such as the columns delinq_2yrs,earliest_cr_line,recoveries,etc.
2) Redundant in nature such as member_id, which is redundant compared to id column and thus could be removed.
3) Unnecessary in the scope of our analysis suchas,funded_amnt_inv,total_pymnt_inv,zip_code,etc.
4) Which have high number of null values such bc_open_to_buy,bc_util,avg_cur_bal,etc.
5) Which have very few unique records such as pymnt_plan,initial_list_status,policy_code,etc.
We also got rid of the rows which are not needed for the analysis such as the rows which have loan_status as 'Current' are dropped.
We have also imputed columns which have very low amount of missing values such as emp_length.

## Univariate and Multivariate Analysis
After cleaning the dataset we performed Univariate,Bivariate ,Segmented Univariate and Correlation Analysis on the dataset. 
Univariate Analysis of term revealed that loans with term length 36 months are much more prevalent than the loans with term length 60 months.
Similarly univariate analysis of loan_status revealed that the frequency of defaulted loans is much less than fully paid loans.
Univariate analysis of home_ownership and emp_length revealed that most borrowers are living on rented properties and most borrowers have 10+ years of work experience.
Univariate Analysis of Grade and Sub-Grade revealed that most loans are of grade A-B Category specifically A4-B5 Category.
Univariate analysis of derived variables issue_month and issue_year revealed that most loans are being approved towards the last quarter of each year and the number of loans being approved each year is exponentially rising.

Segmented univariate Analysis yielded interesting insights such as Segmented univariate Analysis of loan_amnt based on loan_status revealed that the higher the loan amount the higher the frequency of default.
Segmented univariate Analysis of DTI based on loan_status revealed that for DTI's 10-15 has the highest likelihood of default.
Segmented Univariate Analysis of term based on loan_status revealed that for loans having term length of 60 months have a higher frequency of default.
Bivariate Analysis of Grade vs DTI based on loan_status revealed that for lower grade loans the higher the DTI the higher the frequency of Default.
Bivariate Analysis of Interest Rate vs Grade revealed that interest rate decrease with increase loan grade.
## Conclusions
Conclusion drawn from Univariate analysis is that most loans are  lower grade loans,i.e, from A-B with term length of 36 months,with a median loan amount in the range 5000-14000,with interest rate of 10-15% are taken by individuals who have a median DTI in the range 10-15 with work experience of 10+ years with median annual income of about 40000-60000 and live in rented properties and live in California, New York,Florida and they take the loans mostly for debt consolidation.

Conclusion drawn from segmented Univariate Analysis is that most loans which are of amount more than 10000 have a higher chance of default,also the loans whose loan term length is 60 months have a higher chance of default.Also the individuals who have DTI 10-15 have a higher chance of both default and full pay.etc.

Conclusion of Bivariate analysis revealed that for low grade loans higher the DTI,higher the chance of default.

## Technologies Used
- Python - Version 3.12.0
- numpy - Version 1.26.2
- pandas - Version 2.1.3
- matplotlib - Version 3.8.2
- seaborn - Version 0.13.0
- Jupyter Notebook - Version 7.0.6
- Anaconda - Version 2.5.1

## Acknowledgements
1)The project reference course materieals from upGrads curriculum.


2)The project references insights and inferences from live presentation given by Akashdeep Makkar.


## Contact
Created by Riddhiman ghosh Roy - feel free to contact me!

LinkedIn: www.linkedin.com/in/riddhiman-g-16a069b4


Github: https://github.com/ghoshroyr


