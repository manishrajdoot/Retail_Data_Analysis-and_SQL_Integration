![Picsart_24-10-03_10-18-46-688](https://github.com/user-attachments/assets/6de17e1d-a7b6-497e-9a12-0d493a423db5)

#Project Title: Retail Data Analysis and SQL Integration
[Project_Link](https://github.com/manishrajdoot/Retail_Data_Analysis-and_SQL_Integration)



#Project Overview:

This project involves analyzing a retail dataset, cleaning the data, deriving key metrics, and loading the cleaned data into a SQL Server database for further use. The dataset contains various features related to retail orders, including pricing, product details, customer demographics, and shipping information.




#Key Steps Involved:


#Data Import and Exploration:

*The dataset was imported from Kaggle using the kaggle API.

*The dataset includes retail order details such as Order ID, Order Date, Ship Mode, City, State, Product ID, List Price, Cost Price, Quantity, Discount Percent, etc.


#Data Cleaning:

*Missing values such as 'Not Available' and 'unknown' were handled during data import using na_values.

*Column names were normalized by converting them to lowercase and replacing spaces with underscores for easier access.

*Converted the order_date from an object data type to a datetime format for accurate time-based analysis.


#Feature Engineering:

Derived new columns:


*Discount: Calculated by multiplying list_price and discount_percent.

*Sale Price: Subtracted the discount from the list_price.

*Profit: Subtracted the cost_price from the sale_price to get the profit for each order.

*After the new columns were created, unnecessary columns like list_price, cost_price, and discount_percent were dropped to streamline the dataset.


#Database Integration:

*The cleaned and transformed data was loaded into a SQL Server database using the SQLAlchemy library.

*The table df_orders was created in the database, and the dataset was appended to this table using the to_sql function with the if_exists='append' option.


#SQL Server Connection:

*A connection was established with SQL Server using an ODBC driver.

*The data was successfully loaded into the SQL Server table for further querying and analysis.


#Technologies Used:


#Python Libraries:


*pandas: For data manipulation and analysis.

*SQLAlchemy: For connecting and loading data into SQL Server.

*kaggle: For dataset download.

*Database: SQL Server with an ODBC connection.

*Kaggle Dataset: A retail dataset containing order details, shipping information, and pricing.



#Key Metrics Derived:


*Discount: The absolute discount amount for each order.

*Sale Price: The price after applying the discount.

*Profit: The difference between the sale price and the cost price.


#Potential Use Cases:


*Sales Performance Analysis: The derived metrics (sale price, profit) help in analyzing the profitability of various products and categories.

*Customer Segmentation: The dataset includes shipping and region information, enabling geographical or customer segment analysis.

*Inventory Optimization: Insights into the order quantities, product categories, and sales trends can inform inventory management decisions.



This project demonstrates the end-to-end process of data extraction, cleaning, analysis, and loading into a SQL database for further exploration and reporting.
