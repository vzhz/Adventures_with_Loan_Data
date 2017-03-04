# C8 Data Question - Dataset README
This document provides assumptions and definitions for the Loan Volume Reports.

## Data Source
Common Origination and Disbursement (COD) System	

## Data Refresh Schedule
Data will be refreshed each quarter for at least seven prior quarters to account for adjustments.  After the adjustment period, the data will be final.	
	
## Assumptions	
1. Loans are included in the columns RECIPIENTS, # OF LOANS ORIGINATED, $ OF LOANS ORIGINATED, # OF DISBURSEMENTS, and $ OF DISBURSEMENTS if the period begin date of the loan falls within the award year reported on the spreadsheet and the first disbursement of that loan falls within that quarter.  Disbursements occurring prior to the award year are counted in quarter 1 and disbursements occurring after the end of the award year are counted in quarter 4.  For the Year-To-Date data, all numbers are cumulative.  	
1. Disbursements are included in the columns # OF DISBURSEMENTS and $ OF DISBURSEMENTS if the loan was included in the loan origination counts and the dates of the disbursements were less than or equal to the last day of the quarter reported on this spreadsheet.  For fourth quarter reports it is the cumulative number of disbursements as of the date the report is created in order to include any late disbursements.  Disbursements for the second, third, and fourth quarters are cumulative from the beginning of the award year.	
1. Consolidation loans are not included in either query	
1. A school appears on the report only if at least one loan originated at that school qualifies for inclusion on the report.	
1. Loans with a current loan status of cancelled are excluded from both queries	
1. Disbursements in history with an amount of zero are not counted in the number of disbursements.	

## Field Definitions	
### OPE ID 
An 8-digit code identifying the school at its main branch

### School 
The name of the school associated with the OPE ID

### State 
The state in which the main campus is located

### Zip Code 
The zip code of the main campus

### School Type 
Indicates the control or ownership of the school.

### Recipients 
The number of loan recipients for the loan type during the award year for the time period reported on the spreadsheet.  For Subsidized, Unsubsidized, and Graduate PLUS loans, this is a count of student borrowers.  For Parent PLUS loans, this is a count of the students on whose behalf the loan was taken.  Since students can have multiple loan types in the same award year, you cannot sum the recipient counts from the four categories to obtain an accurate count of total recipients for the loan program during that award year.

### \# of Loans Originated 
The number of loans initiated for the loan type during the award year for the time period reported on the spreadsheet.

### $ of Loans Originated 
The dollar amount of the loans initiated for the loan type during the award year for the time period reported on the spreadsheet.  This is the expected total loan amount if the loan is fully disbursed.

### \# of Loans Disbursed 
The number of disbursements made for the loan type during the award year and quarter reported on the spreadsheet.

### $ of Loans Disbursed 
The dollar amount of disbursements made for the loan type during the award year for the time period reported on the spreadsheet.
