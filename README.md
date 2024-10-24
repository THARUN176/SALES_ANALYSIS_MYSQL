# Costco Sales Data Analysis

## Overview

This project seeks to analyze Costco's sales data to identify high-performing branches and products, explore sales trends across various product categories, and understand customer behavior. The goal is to enhance and optimize sales strategies.

## Project Objectives

The primary aim of this project is to derive insights from Costco's sales data, identifying the various factors that influence sales across different branches.

## Data Description

The dataset consists of 17 columns and 1000 rows:

| Column                  | Description                             | Data Type      |
| :---------------------- | :-------------------------------------- | :------------- |
| invoice_id              | Identifier for the sales transaction    | VARCHAR(30)    |
| branch                  | Branch where the sale occurred          | VARCHAR(5)     |
| city                    | Location of the branch                  | VARCHAR(30)    |
| customer_type           | Type of customer                        | VARCHAR(30)    |
| gender                  | Gender of the customer                  | VARCHAR(10)    |
| product_line            | Category of the product sold            | VARCHAR(100)   |
| unit_price              | Price of each product                   | DECIMAL(10, 2) |
| quantity                | Number of units sold                    | INT            |
| VAT                     | Tax amount on the purchase              | FLOAT(6, 4)    |
| total                   | Total cost of the transaction           | DECIMAL(10, 2) |
| date                    | Date of the transaction                 | DATE           |
| time                    | Time of the transaction                 | TIMESTAMP      |
| payment_method          | Payment method used                     | VARCHAR(30)    |
| cogs                    | Cost of Goods Sold                      | DECIMAL(10, 2) |
| gross_margin_percentage  | Gross margin percentage                 | FLOAT(11, 9)   |
| gross_income            | Gross income                            | DECIMAL(10, 2) |
| rating                  | Customer rating                         | FLOAT(2, 1)    |

### Areas of Analysis

1. **Product Analysis**

   Conducted an in-depth examination of various product lines to identify top performers and areas needing improvement.

2. **Sales Analysis**

   Analyzed the sales trends of different products to assess the effectiveness of current sales strategies and identify necessary modifications for increased revenue.

3. **Customer Analysis**

   Explored different customer segments, their purchasing behaviors, and the profitability associated with each segment.

## Methodology

1. **Data Wrangling:** The initial step involves inspecting the data for any **NULL** or missing values, followed by appropriate data replacement techniques to ensure completeness.

   - Created a database.
   - Created a table and inserted the data.
   - Identified columns with missing values. There are no **NULL** values as we set **NOT NULL** constraints during table creation, effectively filtering them out.

2. **Feature Engineering:** This step generates new columns from existing data to provide deeper insights.

   - Introduced a new column called `time_of_day` to categorize sales into Morning, Afternoon, and Evening. This will help identify peak sales periods throughout the day.
   - Created a `day_name` column to indicate the day of the week for each transaction (e.g., Mon, Tue, Wed). This will help ascertain which days are busiest for each branch.
   - Added a `month_name` column to denote the month of each transaction (e.g., Jan, Feb, Mar). This will aid in determining the month with the highest sales and profits.

3. **Exploratory Data Analysis (EDA):** Conducted EDA to answer the identified questions and objectives of the project.

4. **Conclusion:** Summarized findings and insights derived from the analysis.

## Key Business Questions

### General Questions

1. How many unique cities are represented in the dataset?
2. Which city houses each branch?

### Product Analysis

1. How many unique product lines are in the dataset?
2. What is the most commonly used payment method?
3. Which product line generates the highest sales?
4. What is the total revenue generated each month?
5. Which month recorded the highest COGS?
6. Which product line yields the most revenue?
7. Which city has the highest revenue?
8. Which product line incurs the highest VAT?
9. Categorize each product line as "Good" or "Bad" based on whether its sales exceed the average.
10. Which branch sold more products than the average sold?
11. What is the most common product line among different genders?
12. What is the average rating for each product line?

### Sales Analysis

1. How many sales occur during different times of the day across weekdays?
2. Which customer type contributes the most to revenue?
3. Which city has the highest VAT percentage?
4. Which customer type incurs the most VAT?

### Customer Analysis

1. How many unique customer types are present in the dataset?
2. How many distinct payment methods are utilized?
3. What is the most prevalent customer type?
4. Which customer type makes the most purchases?
5. What is the gender distribution of customers?
6. How is gender distributed across different branches?
7. During which time of day do customers provide the highest ratings?
8. At which time of day do customers give the most ratings per branch?
9. Which day of the week sees the highest average ratings?
10. What is the best day of the week for average ratings across branches?
