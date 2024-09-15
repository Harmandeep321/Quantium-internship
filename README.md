# Quantium Virtual Experience Program in Data Analytics
This is program consists of 3 tasks
All these code files were my personal submissions for this program. Except the data files which were assigned by Quantium.
Code and Resources Used

Packages: pandas, numpy, seaborn, sklearn, matplotlib, datetime, scipy

# Task 1 - Data preparation and Customer Analytics
Conduct analysis on your client's transaction dataset and identify customer purchasing behaviours to generate insights and provide commercial recommendations.

## Background information for the task
We need to present a strategic recommendation to Julia that is supported by data which she can then use for the upcoming category review however to do so we need to analyse the data to understand the current purchasing trends and behaviours. The client is particularly interested in customer segments and their chip purchasing behaviour. Consider what metrics would help describe the customers’ purchasing behaviour.

Main goals of this task are :
1. Examine transaction data - check for missing data, anomalies, outliers and clean them
2. Examine customer data - similar to above transaction data
3. Data analysis and customer segments - create charts and graphs, note trends and insights
4. Deep dive into customer segments - determine which segments should be targetted

## Data Cleaning:
+ Date column was in integer format. So the date column was changed to date time format.
+ There are 365 days in a year but in the DATE column there are only 364 unique values so one was missing. As it was a Christmas day and store was closed there was no anomaly. Value was kept as zero transaction for "TOT_SALES". 
+ Checked if all the products in given data are chips.
+ Some product names are written in more than one way. Example : Dorito and Doritos, Grains and GrnWves, Infusions and Ifzns, Natural and NCC, Red and RRD, Smith and Smiths and Snbts and Sunbites. It was cleaned 
 thereafter.
+ Split and frequency of each word in "PROD_NAME" column. Removed all rows containing "salsa" in "PROD_QTY" column.
+ Checked for outliers and removed outliers rows in "PROD_QTY" column.
+ Each word value was counted in "PROD_NAME" column to extract the brand name. Combined brands written in multiple ways. Created a
