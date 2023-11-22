# Loan Data From Prosper
## by Mohammed Barakah


## Dataset

This dataset originates from Prosper, the pioneering peer-to-peer lending platform in the United States, known for facilitating over $7 billion in funded loans. It comprises 113,937 individual loans, each associated with 81 distinct variables.

>  [ columns information](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0)


## Preliminary Wrangling
out of the 81 columns i choosed the data set i would focus on into a data fram which includes:
* Term: The length of the loan expressed in months.	
* BorrowerAPR: The Borrower's Annual Percentage Rate (APR) for the loan.
* BorrowerRate: The Borrower's interest rate for this loan.
* ProsperRating: The Prosper Rating assigned at the time the listing was created between AA - HR.  Applicable for loans originated after July 2009.	
* ProsperScore: A custom risk score built using historical Prosper data. The score ranges from 1-10, with 10 being the best, or lowest risk score.  Applicable for loans originated after July 2009.
* IncomeRange: The income range of the borrower at the time the listing was created.
* LoanOriginalAmount: The origination amount of the loan.
* LoanOriginationDate: The date the loan was originated.

#### Wrangling
changed the Loan Origination Date into a date time category
created a better representation of the Listing category

## Summary of Findings

### Univariate Exploration

In the exploration, BorrowerRate follows a nearly normal distribution, albeit with a slight leftward skew, Notably, there is a prominent peak in the distribution around the 31% mark.
The majority of loans have their origins in the year 2013.
According to the visualizations, the states with the highest listing counts are CA, TX, NY, FL, and IL, aligning with the rankings of the most populous states in the United States. Conversely, the states with the fewest listings are WY, ME, and ND. In essence, the distribution of Prosper listings appears to mirror the population distribution across the United States.
And majority of borrowers are assigned lower scores. In fact, there is a direct relationship between lower scores and higher borrower counts.

### Bivariate Exploration
Using a Heatmap i find out that, ProsperRating (numeric) displays a robust correlation with BorrowerRate and ProsperScore. Notably, the DebtToIncomeRatio does not exhibit any notable correlation.
also usin box plot, ProsperRating doesn't demonstrate a substantial correlation. It appears that whether the rating is good or bad doesn't significantly impact the borrower's APR percentage. However, in the case of ProsperScore, there is a distinct negative relationship with BorrowerAPR.

### Multivariate Exploration
 Relationship between BorrowerAPR and ProsperScore across various letter ratings. The patterns reveal that borrowers with the lowest rating (HR) tend to have the highest APR, while those with a high rating (A) enjoy the lowest APR. This visualization effectively distinguishes between different groups of individuals in terms of the APR they receive, based on their rating and scores.
By utilizing a bar chart, I discovered that loans with a duration of 5 years typically exhibit higher borrower APRs.

## Key Insights for Presentation

Borrowers with higher score ratings tend to enjoy more favorable BorrowerAPRs, regardless of the loan amount they take. Conversely, borrowers with lower score ratings tend to face higher BorrowerAPRs, regardless of the loan amount they borrow.