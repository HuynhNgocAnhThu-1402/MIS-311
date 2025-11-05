**1. Overview**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This project analyzes the **“Supermarket Sale”** dataset, which contains sales transaction records from three supermarket branches located in New York, Los Angeles, and Chicago (USA). It includes details about products, customers,  and sales information, enabling insights into customer behavior and branch performance.

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
 
**Data Sources**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Although the original source is unspecified, the dataset likely represents sample supermarket transaction data used for educational purposes. It reflects common structures found in real retail sales systems and public learning resources. Comparable data is often adapted from the following open platforms:

- Kaggle: Retail and supermarket sales datasets for data analytics practice.

- UCI Machine Learning Repository: Business and marketing datasets for academic study.
  
- Open educational resources: Sample data provided for teaching statistics and business analytics.

**2. Data cleaning**

**2.1. Data Formatting**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;All columns were formatted with appropriate data types to ensure data consistency and avoid calculation errors. Specifically, Sale_ID, Branch, City, Customer_Type, Product_Name, and Product_Category were set to Text format, as they represent categorical data. The Quantity column was formatted as Number (0 decimal places), and Total_Price was formatted as Currency (2 decimal places). Although Sale_ID contains numeric characters, it was formatted as Text because it acts as a unique identifier rather than a numerical value.

**2.2. Checked for missing values**

**Step 1:** Select all data → go to Home → Find & Select → Go To Special → Blanks.

Excel highlights all blank cells.

<img width="512" height="269" alt="F1" src="https://github.com/user-attachments/assets/73e8d4dc-a221-4fe7-8613-8450032cbd5d" />

_**Figure 1: Missing values (row 20 - column: quantity)**_

<img width="512" height="116" alt="F2" src="https://github.com/user-attachments/assets/00f2897f-86fb-4441-a057-4f9211d397e7" />

_**Figure 2: Missing values (row 30, 31, 32, 35 - column customer_type & product_category)**_

![F3](https://github.com/user-attachments/assets/7698404c-bdcd-4de2-bc1f-bf958e1dccd8)

_**Figure 3: Missing values (row 44, 49, 61 column customer_type, product_category & qiantity)**_

![F4](https://github.com/user-attachments/assets/27f78339-1aec-40a7-b148-c8ee329e146b)

_**Figure 4: Missing values (row 68, 87 - column product_category)**_

![F5](https://github.com/user-attachments/assets/006c4c6e-88bb-46eb-9e93-34fef0fd9778)

_**Figure 5: Missing value (row 99 - column product_category)**_

A total of 12 missing values were identified in the dataset across three columns. Missing entries were found in:

- **quantity column:** rows 20, 44, 61

- **customer_type column:** rows 31, 35, 44

- **product_category column:** rows 30, 32, 49, 68, 87, 99

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;These missing values represented incomplete sales information, such as unknown quantities, customer types, or product categories. Such gaps could lead to inaccurate descriptive statistics and biased insights.

**Step 2:** Delete rows that contain missing data (Right-click → Delete → Entire Row or Ctrl -).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;A total of 12 missing values were detected in key columns such as quantity, customer_type, and product_category. Because these fields contain essential information for calculating sales and understanding customer behavior, filling them with estimated values could distort the analysis. Therefore, the missing records were removed to maintain data accuracy and reliability for further descriptive analysis.

**2.3. Checked for duplicate records**

**Step 1:** Select the whole table (ctrl A)

**Step 2:** Go to Data → Remove Duplicates.

**Step 3:** Tick all columns → OK.

![F6](https://github.com/user-attachments/assets/1d8bfb36-b454-4b95-9c4f-8e8036e3fc46)

_**Figure 5: Duplicate values**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;After handling missing values, a duplicate check was performed using Excel’s Remove Duplicates function. Three identical rows were found and deleted, resulting in 239 unique records. The cleaned dataset now contains 8 columns with no missing or duplicate values, ensuring consistency and reliability for descriptive analysis and visualization.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;After cleaning, the dataset contains 239 valid records, with no missing or duplicate values, ready for accurate analysis.

**3. Descriptive Statistics**

![F7](https://github.com/user-attachments/assets/8f5902f9-3c01-4891-9dfd-a50c03d93e99)

_**Figure 6: Summary statistics**_

**Quantity**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Customers usually buy around 10 items per transaction, showing a stable and moderate shopping pattern. This consistency helps the supermarket predict product demand and manage inventory more effectively.

**Total Price**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The average spending per transaction is about USD 127, though some customers spend much higher amounts. This indicates the presence of high-value customers who contribute significantly to total revenue,a key group for targeted promotions or loyalty programs.

![F8](https://github.com/user-attachments/assets/0afecf50-e6df-4315-af15-f58f21109a26)

**Figure 7:  Box Plot of Total Price per Transaction**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The box plot illustrates the distribution of total spending per transaction. The median value is approximately USD 106.59, while the mean is slightly higher at USD 127.04, suggesting a right-skewed distribution. Most transactions fall within the range of USD 40 to 200, as indicated by the interquartile range (IQR), while the minimum and maximum values are USD 2.18 and USD 427.14, respectively. This implies that most customers make moderate purchases, but a few high-value transactions significantly raise the overall average.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Overall, this distribution supports the findings from descriptive statistics and highlights variability in customer spending behavior, an important aspect to consider before moving on to deeper business insights.

![F8](https://github.com/user-attachments/assets/6ba1e1da-2f96-444a-a7e7-8b010d401c33)

_**Figure 8: Distribution of quantity per transaction**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The histogram above shows how many products customers usually buy in one transaction. Most customers purchase between 8 and 11 items, which is the largest group with about 55 transactions. Buying 1–4 items and 15–18 items is also quite common (around 50–55 transactions), while only a few customers buy more than 18 items (about 30 transactions). This means most customers make medium-sized purchases instead of very small or very large ones. Overall, the chart shows that the number of products per purchase is fairly balanced, so customer buying behavior is quite consistent.

After understanding the overall distribution, the next step focuses on identifying key business insights

**3.1. Insight 1: Total Sales Revenue by Branch**

![F9](https://github.com/user-attachments/assets/5315ca76-1be8-4483-9548-f5d3f92b7c17)

_**Figure 9: Total Sales Revenue by Branch**_

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Branch A generated about 2.4 times more revenue than Branch B (USD 21,427 vs. USD 8,935). This suggests stronger sales performance, possibly due to better location, a larger customer base, or more effective marketing. The company should consider expanding operations or investing more in Branch A’s area to maximize overall business growth.

**3.2. Insight 2: Average Spending by Customer Type**

![F10](https://github.com/user-attachments/assets/bf0ea589-4d29-4acc-b3a3-c3d8fb330f44)

**Figure 10: Average Spending by Customer Type**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Member customers spend about 22% more than normal customers on average (USD 138.69 vs. USD 113.83). This shows that the membership program successfully encourages higher spending and customer loyalty. Maintaining and expanding this program could further increase total revenue and long-term customer retention.
