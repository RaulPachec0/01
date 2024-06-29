Author: Raul Pacheco
28 June 2024


Sales Analysis
This project involves analyzing sales data for a retail company. The analysis includes tasks such as merging data files, cleaning data, and generating insights using various visualization techniques. Below is a summary of the process used for the analysis.

Prerequisites
Before running the analysis, ensure you have the following Python libraries installed:

pandas
matplotlib
You can install them using pip:

pip install pandas matplotlib

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 1: Merging 12 Months of Sales Data into a Single File
The sales data is stored in separate CSV files for each month. The first task involves merging these files into a single DataFrame. This is achieved by:

Loading each monthly CSV file into a DataFrame.
Concatenating these monthly DataFrames into one comprehensive DataFrame.
Saving this combined data into a new CSV file named all_data.csv.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 2: Read and Clean Data
Reading the Combined DataFrame
The combined sales data is read from the newly created all_data.csv file.

Data Cleaning
The data cleaning process includes:

Dropping Rows with NaN Values: Removing any rows that contain all NaN values to ensure data completeness.
Removing Invalid Entries: Deleting rows where the 'Order Date' column contains invalid entries that don't represent actual dates.
Converting Data Types: Ensuring that columns like 'Quantity Ordered' and 'Price Each' are correctly converted to numerical data types for accurate calculations.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Task 3: Add Additional Columns
Adding a City Column
To enhance the data, a new column 'City' is added. This column is derived from the 'Purchase Address' column and includes the city and state information extracted from the address string.

Adding a Month Column
A new 'Month' column is added by extracting the month information from the 'Order Date' column. This allows for monthly analysis of sales data.

Adding a Sales Column
A 'Sales' column is calculated by multiplying the 'Quantity Ordered' by the 'Price Each' for each order. This provides a direct measure of revenue for each transaction.



------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Question 1: What was the Best Month for Sales? How Much was Earned that Month?
To determine the best month for sales:

The sales data is grouped by the 'Month' column.
The total sales for each month are calculated.
A bar chart is generated to visualize the monthly sales performance, highlighting the month with the highest revenue.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Question 2: What City Had the Highest Number of Sales?
To identify the city with the highest sales:

The data is grouped by the 'City' column.
The total sales for each city are summed.
A bar chart is created to display the sales figures for each city, allowing easy comparison of sales performance across different locations.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Question 3: When Should Advertisements be Displayed to Maximize Customer Purchases?
To determine the optimal time for displaying advertisements:

The 'Order Date' column is converted to a datetime format.
New columns for 'Hour' and 'Minute' are extracted from the 'Order Date'.
The data is grouped by the 'Hour' column to count the number of orders placed each hour.
A line plot is generated to show the distribution of orders throughout the day, identifying peak hours for customer purchases.


------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Question 4: What Products are Most Often Sold Together?
To find products that are frequently sold together:

Orders with the same 'Order ID' are identified.
The products in each order are grouped together.
The frequency of different product combinations is counted.
The most common product pairs are listed, indicating popular combinations bought by customers.
Question 5: What Product Sold the Most? Why Do You Think it Sold the Most?
To identify the best-selling product and analyze why it sold the most:

The data is grouped by the 'Product' column to sum the total quantity ordered for each product.
A bar chart is created to visualize the quantity sold for each product.
The average price of each product is also calculated and plotted alongside the quantity sold.
This dual-plot helps in understanding the relationship between product price and sales volume, providing insights into why certain products perform better.

This README file summarizes the key steps in the sales analysis, including data merging, cleaning, augmentation, and generating insights through various analyses and visualizations.