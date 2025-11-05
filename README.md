# 1. Overview

This project analyzes the **“Supermarket Sales”** dataset, which contains detailed sales transaction records from three supermarket branches in New York, Los Angeles, and Chicago (USA).  
It includes information about products, customers, and total sales value — enabling insights into customer behavior and branch performance.

- **Dataset Size:** 253 rows × 8 columns  
- **Final Size (after cleaning):** 239 rows × 8 columns  

---

### **Columns**
- **sale_id** – Unique transaction ID  
- **branch** – Supermarket branch (A, B)  
- **city** – City (New York, Los Angeles, Chicago)  
- **customer_type** – Member or Normal  
- **product_name** – Product name  
- **product_category** – Category (e.g., Fruits, Stationery, Beverages)  
- **quantity** – Number of units sold  
- **total_price** – Total value of transaction (USD)

---

# 2. Data Cleaning

The dataset was cleaned to ensure accuracy and consistency.

**Steps performed:**
1. Checked and removed **12 missing values** across key columns (`quantity`, `customer_type`, `product_category`).  
2. Removed **3 duplicate records** using Excel’s “Remove Duplicates” feature.  
3. Verified correct data types:  
   - Text: `sale_id`, `branch`, `city`, `customer_type`, `product_name`, `product_category`  
   - Number: `quantity`  
   - Currency: `total_price`  

✅ *Final dataset:* 239 valid rows, ready for analysis.

---

# 3. Descriptive Statistics and Insights

### **Descriptive Overview**
- Average quantity per transaction: **10.78 items**  
- Average total spending per transaction: **USD 127.04**  
- Spending distribution shows right-skewness → a few customers spend much higher than average.  

---

### **Insight 1: Total Sales by Branch**
Branch A generated **USD 21,427**, nearly double Branch B (**USD 8,935**).  
→ *Branch A shows stronger performance, likely due to location or customer base advantages.*

---

### **Insight 2: Average Spending by Customer Type**
Members spend **~22% more** than normal customers (**USD 138.69 vs. 113.83**).  
→ *The membership program effectively increases spending and customer loyalty.*

---

# 4. Files in this Repository
| File Name | Description |
|------------|-------------|
| `MIS311_Portfolio.pdf` | Full report document |
| `Supermarket_Sale_cleaned.xlsx` | Cleaned dataset |
| `charts/` | Visualizations used in the report |

---

# 5. Author
👩 **Huynh Ngoc Anh Thu**  
📚 MIS 311 – Introduction to Business Analytics, EIU  
📧 *[optional: your email address]*
