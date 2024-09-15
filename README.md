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
+ Each word value was counted in "PROD_NAME" column to extract the brand name. Combined brands written in multiple ways.

# Data Analysis on Customer Segments
The 4 main questions answered in data analysis were:
1. Who spends the most on chips (total sales), describing customers by lifestage and how premium their general purchasing behaviour is
2. How many customers are in each segment
3. How many chips are bought per customer by segment
4. What's the average chip price by customer segment
Groupby sum TOT_SALES column and identified top 3 highest total sales contributing segments.
Plot the groupby into stacked bar chart with percentage text on each segment stack.

# Trends and insights

+ Most of the people purchase chips of these brands Kettle, Smiths, Doritos, Pringles and RRD respectively as compared to other brands.
+ Budget – older families, Mainstream – young singles/couples, and Mainstream – retirees shoppers have accounted for the majority of sales.
+ Mainstream young singles/couples and retirees spend more money on chips than other purchasers mainly due to the fact that there are more customers in these segments.
+ Additionally, young, middle-aged, and mainstream individuals and couples are more inclined to pay more for each bag of chips.
+ They are also 23% more likely to purchase 'Tyrrells' and '270g' pack sizes than the rest of the population.

# Task 2
## Experimentation and uplift testing
Extend your analysis from Task 1 to help you identify benchmark stores that allow you to test the impact of the trial store layouts on customer sales.

Here is the background information on your task

You are part of Quantium’s retail analytics team and have been approached by your client, the Category Manager for Chips, has asked us to test the impact of the new trial layouts with a data driven recommendation to whether or not the trial layout should be rolled out to all their stores.

Here is your task

Julia has asked us to evaluate the performance of a store trial which was performed in stores 77, 86 and 88.

To get started use the QVI_data dataset below or your output from task 1 and consider the monthly sales experience of each store.

This can be broken down by:

+ total sales revenue
+ total number of customers
+ average number of transactions per customer
Create a measure to compare different control stores to each of the trial stores to do this write a function to reduce having to re-do the analysis for each trial store. Consider using Pearson correlations or a metric such as a magnitude distance e.g. 1- (Observed distance – minimum distance)/(Maximum distance – minimum distance) as a measure.

Once you have selected your control stores, compare each trial and control pair during the trial period. You want to test if total sales are significantly different in the trial period and if so, check if the driver of change is more purchasing customers or more purchases per customers etc.
