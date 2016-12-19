#A Machine Learning Model that predicts whether a borrower will pay off their loan on time
I am trying to figure out on the perspective of investor, which borrower will pay his/her loan and return the investment. Based on this model, investor will make a decision to lend loans (and to a person who is likely to pay off).

##Data
I am grabbing data from [Lending Money](https://www.lendingclub.com/public/how-peer-lending-works.action), which is an online credit market place that enables investors receive interest as a return.
I am going to be looking at 2007~2011 data to make sure loans are finished, 
- [Data](https://www.lendingclub.com/info/download-data.action)
- [Link](https://docs.google.com/spreadsheets/d/1YxDDHXkl3M4_axThL6leNqPtOdZFWw06ogOF5y9ycwE/edit?usp=sharing): reference sheet to column names. Only 'LoanStats' tab is considerable since it states approved loan datasets. *Important to understand the meaning of each$

#easdfdsfdfdf#Findings:
- Need to remove below columns
  -id: randomly generated field by Lending Club for unique identification purposes only
member_id: also a randomly generated field by Lending Club for unique identification purposes only
funded_amnt: leaks data from the future (after the loan is already started to be funded)
funded_amnt_inv: also leaks data from the future (after the loan is already started to be funded)
grade: contains redundant information as the interest rate column (int_rate)
sub_grade: also contains redundant information as the interest rate column (int_rate)
emp_title: requires other data and a lot of processing to potentially be useful
issue_d: leaks data from the future (after the loan is already completed funded)


zip_code: redundant with the addr_state column since only the first 3 digits of the 5 digit zip code are visible (which only can be used to identify the state the borrower lives in)
out_prncp: leaks data from the future, (after the loan already started to be paid off)
out_prncp_inv: also leaks data from the future, (after the loan already started to be paid off)
total_pymnt: also leaks data from the future, (after the loan already started to be paid off)
total_pymnt_inv: also leaks data from the future, (after the loan already started to be paid off)
total_rec_prncp: also leaks data from the future, (after the loan already started to be paid off)


total_rec_int: leaks data from the future, (after the loan already started to be paid off),
total_rec_late_fee: also leaks data from the future, (after the loan already started to be paid off),
recoveries: also leaks data from the future, (after the loan already started to be paid off),
collection_recovery_fee: also leaks data from the future, (after the loan already started to be paid off),
last_pymnt_d: also leaks data from the future, (after the loan already started to be paid off),
last_pymnt_amnt: also leaks data from the future, (after the loan already started to be paid off).
