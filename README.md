**1. Overview**

This project analyzes the “Supermarket Sale” dataset, which contains sales transaction records from three supermarket branches located in New York, Los Angeles, and Chicago (USA). It includes details about products, customers,  and sales information, enabling insights into customer behavior and branch performance.
**- Dataset Size:** 253 rows × 8 columns
**- Final Size (after cleaning):** 239 rows × 8 columns
**- Missing Values:** 12 missing values (1 out of 11 row has 2 missing values) removed due to incomplete data

**Columns:**
- sale_id: Unique sale transaction ID
- branch: Supermarket branch (A, B)
- city: City location (New York, Los Angeles, Chicago)
- customer_type: Member or Normal customer
- product_name: Name of product
- product _category: Product category (e.g., Fruits, Stationery, Beverages)
- quantity: Number of units sold
- total_price: Total sales value (USD)
- 
**Data Sources**
Although the original source is unspecified, the dataset likely represents sample supermarket transaction data used for educational purposes. It reflects common structures found in real retail sales systems and public learning resources. Comparable data is often adapted from the following open platforms:
Kaggle: Retail and supermarket sales datasets for data analytics practice.
UCI Machine Learning Repository: Business and marketing datasets for academic study.
Open educational resources: Sample data provided for teaching statistics and business analytics.

**2. Data cleaning**

**2.1. Data Formatting**
All columns were formatted with appropriate data types to ensure data consistency and avoid calculation errors. Specifically, Sale_ID, Branch, City, Customer_Type, Product_Name, and Product_Category were set to Text format, as they represent categorical data. The Quantity column was formatted as Number (0 decimal places), and Total_Price was formatted as Currency (2 decimal places). Although Sale_ID contains numeric characters, it was formatted as Text because it acts as a unique identifier rather than a numerical value.

**2.2. Checked for missing values**
**Step 1:** Select all data → go to Home → Find & Select → Go To Special → Blanks.
Excel highlights all blank cells.
![Bắc cực quang - hiện tượng thiên nhiên kì vĩ nhất thế giới](https://github.com/user-attachments/assets/4280a628-0059-4306-9b8f-8847f47bad1c)

_**Figure 1: Missing values (row 20 - column: quantity)**_


_**Figure 2: Missing values (row 30, 31, 32, 35 - column customer_type & product_category)**_


_

