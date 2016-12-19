#A Machine Learning Model that predicts whether a borrower will pay off their loan on time
I am trying to figure out on the perspective of conservative investor, which borrower will pay his/her loan and return the investment. Based on this model, investor will make a decision to lend loans (and to a person who is likely to pay off).

##Data
I am grabbing data from [Lending Money](https://www.lendingclub.com/public/how-peer-lending-works.action), which is an online credit market place that enables investors receive interest as a return.
I am going to be looking at 2007~2011 data to make sure loans are finished, 
- [Data](https://www.lendingclub.com/info/download-data.action)
- [Link](https://docs.google.com/spreadsheets/d/1YxDDHXkl3M4_axThL6leNqPtOdZFWw06ogOF5y9ycwE/edit?usp=sharing): reference sheet to column names. Only 'LoanStats' tab is considerable since it states approved loan datasets. *Important to understand the meaning of each*
- 'loan_status' tab meanings: reference to [here](https://help.lendingclub.com/hc/en-us/articles/215488038)

##Findings:
- Deleted columns
  - id: randomly generated number
  - member_id: randomly generated number
  - funded_amnt: leaks data from the future 
  - funded_amnt_inv: also leaks data from the future 
  - grade: contains redundant information 
  - sub_grade: also contains redundant information
  - emp_title: requires other data 
  - issue_d: leaks data from the future 
  - zip_code: redundant with the addr_state column 
  - out_prncp: leaks data from the future
  - out_prncp_inv: also leaks data from the future
  - total_pymnt: also leaks data from the future
  - total_pymnt_inv: also leaks data from the future
  - total_rec_prncp: also leaks data from the future
  - total_rec_int: leaks data from the future
  - total_rec_late_fee: also leaks data from the future
  - recoveries: also leaks data from the future
  - collection_recovery_fee: also leaks data from the future
  - last_pymnt_d: also leaks data from the future
  - last_pymnt_amnt: also leaks data from the future

- Achieved a true positive rate of 20% and a false positive rate of 7%. Investors can make money if the interest rate is high enough to offset the losses from 7% of borrowers defaulting, and 20% of borrowers is large enough to make enough interest money to offset the losses
  - By lowering a FPR, risk also lowered;however, it also means loosing a chance to make more loans 

