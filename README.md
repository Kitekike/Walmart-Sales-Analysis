Walmart Sales Data Analysis

**About**
The project aims to evaluate Walmart's sales data from various branches across the United States to understand each branch's performance, the products sold, and customer behaviors. The study aims to optimize and improve the organization's decision-making strategies. The database's source is   https://www.kaggle.com/code/amrabdelatyfathalla/walmart-time-series-analysis

'' In this recruiting competition, jobseekers are provided historical sales data for 45 Walmart stores in different regions. Each store contains many departments, and participants must project the sales for each department in each store. The dataset includes selected holiday markdown events to add to the challenge. These markdowns are known to affect sales, but it is challenging to predict which departments are affected and the extent of the impact'' **https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting**
W
Purpose of the Project

The main aim is to understand Walmart's sales performance by evaluating different factors of the various branches.
Data
The dataset was retrieved from https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting, mainly used in a competition to rank the recruiters in 2014. This dataset entails sales transactions from 3 Walmart branches in Yangon, Naypyitaw, and Mandalay. It comprises 17 columns and 1000 rows.

Column	Description	Data Type
Invoice_id	Invoice of the sales made	VARCHAR (30)
Branch	Branch at which sales were made	VARCHAR (5)
City	The location of the branch	VARCHAR (30)
Customer_type	Type of customer	VARCHAR (30)
Gender	Gender of the customer making a purchase	VARCHAR (10)
Product_line	Product line of sold product	VARCHAR (100)
Unit_price	Price of each product	DECIMAL (10,2)
Quantity	Amount of the product sold	INT
VAT	Amount of tax on the purchase	FLOAT (6,4)
Total	Total cost of the purchase	DECIMAL (10,2)
Date	Date when the purchase was made	DATE
time	Time the purchase was made.	TIMESTAMP
Payment_method	The total amount paid	DECIMAL (10,2)
Cogs	Cost of goods sold	DECIMAL (10,2)
Gross_margin _percentage	Gross margin percentage	FLOAT (11,9)
Gross income	Gross income	DECIMAL (10,2)
rating	Rating	FLOAT (2,1)
		

The Analysis

Product Analysis
Analyse product line to gain insights into how different product lines perform and how they can be improved over time.
Sales Analysis
This analysis aims to evaluate the sales trend of the products sold in the stores, hence the need for analysis to implement strategic business decisions to improve business sales.
Customer Analysis
Customer analysis aims to uncover different purchase trends, customer segmentation, and profitability. This will assist in place marketing and ensure the requested products are available for the customer's needs.

Approach Used.
1. Data wrangling
The initial stage of inspection involved analysing the data to ensure that all missing and Null values were detected, and data replacement methods were used to replace the missing or null values.
1.	Build a database

2.	Create a table and insert the data. 

3.	Select columns with null values in them. Our database does not contain null values, as we set all of them  NOT NULL for each field while creating the tables. Hence, no null values are filtered out.


2. Feature Engineering
This is essential in generating new columns from the existing ones.
Added   a new column named time_of_day to give insights of the sales based on morning, afternoon and evening. This will help answer the question on which part of the day most sales are made.
Added a new column named day_name that contains the extracted days of the week on which the given transaction took placerating new (Mon, Tue, Wed, Thur, Fri,) This assist to answer the question on which week of the day each branch is busiest.
Added a new column named month_name that contains the extracted months of the year on which the given transaction took place (Jan, Feb, Mar) Assisted in determining which month of the year has the most sales profit.
2.Exploratory Data Analysis (EDA): Exploratory data analysis is done to answer the listed questions and aims of this project.

3.Conclusion.


BUSINESS QUESTIONS 
Generic Questions
How many unique cities does the data have?
In which city is each branch?
Product

How many unique product lines does the data have?
What is the most common payment method?
What is the most selling product line?
What is the total revenue by month?
What month had the largest COGS?
What product line had the largest revenue?
What is the city with the largest revenue?
What product line had the largest VAT?
Fetch each product line and add a column to those product line showing "Good", "Bad". Good if its greater than average sales
Which branch sold more products than average product sold?
What is the most common product line by gender?
What is the average rating of each product line?

Sales

Number of sales made in each time of the day per weekday
Which of the customer types brings the most revenue?
Which city has the largest tax percent/ VAT (Value Added Tax)?
Which customer type pays the most in VAT?

Customer.

How many unique customer types does the data have?
How many unique payment methods does the data have?
What is the most common customer type?
Which customer type buys the most?
What is the gender of most of the customers?
What is the gender distribution per branch?
Which time of the day do customers give most ratings?
Which time of the day do customers give most ratings per branch?
Which day for the week has the best avg ratings?
Which day of the week has the best average ratings per branch?
Revenue And Profit Calculations
$ COGS = units Price * quantity $

$ VAT = 5% * COGS $

VAT is added the COGS, and this is what is billed to the customer.

$ total(gross_sales) = VAT + COGS $

$ gross Profit (gross Income) = total(gross_sales) - COGS $

Gross Margin is gross profit expressed in percentage of the total (gross profit/revenue)

$ \text {Gross Margin} = \frac {\text {gross income}}{\text{total revenue}} $

Example with the first row in our DB:

Data given:
$ \text {Unite Price} = 45.79 $
$ \text {Quantity} = 7 $
$ COGS = 45.79 * 7 = 320.53 $
$ \text {VAT} = 5% * COGS\= 5% 320.53 = 16.0265 $
$ total = VAT + COGS\= 16.0265 + 320.53 = 336.5565$ 
\text{Gross Margin Percentage} = \frac{\text{gross income}}{\text{total revenue}}\=\frac{16.0265}{336.5565} = 0.047619\\approx. 4.7619% $

CODE
The answers to the questions are  in file 
