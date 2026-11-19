# Module-End-Evaluation---Excell
The assignment includes data cleaning using power query, using excel functions, descriptive analysis, xlookup, vlookup, creating pivot tables, graphs, slicers, KEPs etc. With these creating Data Visualization Dashboard.

1.	Imported the file ‘Ecommerce_sales_dataset’ to Power Query for Cleaning.
2.	Selected all four sheets to Transform Data.

Customer_Dim sheet

3.	Found Error in the Customer_ID column. Edited it using Replace value.
4.	In the Name column I cleaned it using TRIM, CLEAN, CAPITALIZE EACH WORD, and only some of the names were having Prefix (Mr., Ms., Mrs., Dr.) so cleaned it with Relace Value.
5.	Age and Gender columns are fine.
6.	Column City cleaned using TRIM, CLEAN and CAPITALIZE EACH WORD.
7.	State Column is fine.
8.	Relace value in the column Country from ‘United States of America’ and ‘usa’ to ‘USA’.
9.	In the Column Loyality_Level remove null values with ‘Unknown’.

Product_Dim sheet

10.	Replace Value ‘P-‘ with ‘PROD’.
11.	Cleaned using TRIM and CLEAN Columns- Product_name, Category, Sub_Category and Brand.
12.	In the Cost column found the AVERAGE and replaced it with ‘null’ values. Changed character to Currency.
13.	In the Stock column found the AVERAGE and replaced it with ‘null’ values. Changed character to Whole Number.

Sales_fact sheet

14.	Sales_ID, Order_date, Customer_ID, Product_ID and Store_ID columns have no errors.
15.	Replace null Value of Quanity column with the median.
16.	Created a  custom column Unit_price_cleaned to remove null values in Unite Price, giving following eqation-
if [Unit_Price] = null then
    ([Total_Amount] + ([Total_Amount] * [Discount])) / [Quantity]
else
    [Unit_Price])
17.	Found that Sales_ID SALES52 have both Discount and Unit Price as ‘null’. Hence Replace value of Sales_ID - SALES52 with the AVERAGE of the Discount.
18.	Deleting Column Unit_Price.
19.	Found there are null values in Total_Amount. Hence Creating custom column Total_Amount_Cleaned and used following equation-
=([Unit_Price] * [Quantity]) * (1 - [Discount])
20.	Found no errors in Payment_mode column.


Store_dim sheet

21.	Used first row as header.
22.	TRIM and CLEAN all the columns.

23.	Close & Load all the sheets.

24.	Back to Excel.

25.	In Sales_fact and Prroduct_dim sheets formatting Cost, Unit Price and Total Amount column to Currency type and Discount column to Percentage.
In Excel
26.	Creating a new sheet with the information of 4 tables named Complete_data - using VLOOKUP, XLOOKUP and INDEX & MATCH.
27.	Created a sheet Calculation for using SUM, SUMIF, COUNTIF function.
28.	In the sheet Product_Dim created a column Stock with 3-digit value to use TEXT function.
29.	For Descrptive Staistics created Column in sheet Complete_data
30.	Created sheet Pivote Table and Graphs and inserted Pivot Tables, Graphs and Slicers.
31.	Created Sheet Data Visulisation and copied graphs from above sheet and made relations between all Graphs, Slicers and KEP.
    
Summary

The dashboard presents an overview of store sales performance across categories, regions, store types, payment methods, and time.
Overall Performance
•	Total Sales Amount: ₹21,70,952.02
•	The business has generated over ₹21.7 lakh in total sales across all regions, categories, and store types.
Category-wise Sales
•	Sports and Electronics are the highest-performing categories, each contributing approximately ₹5 lakh+ in sales.
•	Home products also perform strongly, generating around ₹4.2 lakh.
•	Clothing contributes about ₹3.8 lakh.
•	Beauty records the lowest sales, at approximately ₹3.2 lakh.
Insight: Sports and Electronics drive the majority of revenue and should remain key focus areas for inventory and promotional efforts.
Insight: North, South, and East regions perform almost equally and contribute significantly to total revenue. The West region underperforms considerably and may require targeted marketing or operational improvements.
Store Type-wise Sales
•	Flagship Stores: 58% of sales (₹12.66 lakh)
•	Outlet Stores: 29% of sales
•	Online Stores: 13% of sales
Insight: Flagship stores are the primary revenue source, generating more than half of all sales. Online sales contribute the smallest share, suggesting potential opportunities for digital growth.
Payment Mode Analysis
•	PayPal: 35%
•	Credit Card: 33%
•	COD (Cash on Delivery): 32%
Insight: Payment methods are evenly distributed, with PayPal having a slight preference among customers. No single payment method dominates the market.
Sales Trend Over Time
•	Monthly sales fluctuate between approximately ₹40,000 and ₹1,10,000.
•	Sales remain relatively stable throughout the observed period (2023-2025), with occasional peaks above ₹1 lakh.
•	A noticeable decline appears at the final data point in the timeline.
Insight: The business demonstrates consistent sales performance over time, though the recent drop should be investigated to determine whether it reflects seasonality, market conditions, or incomplete data.
Conclusion
The store shows strong overall performance with ₹21.7 lakh in total sales. Revenue is primarily driven by Sports and Electronics categories, Flagship stores, and the North, South, and East regions. The West region and Online channel represent the greatest opportunities for improvement and future growth. Payment preferences are balanced across all major methods, indicating flexibility in customer purchasing behaviour.
