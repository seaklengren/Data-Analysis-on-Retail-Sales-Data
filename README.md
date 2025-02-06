# **Retail Sales Analysis Report**  

## **1. Problem Statement**  
The objective of this project is to analyze a retail sales dataset to uncover trends, patterns, and actionable insights that can enhance business strategies. The analysis involves **data cleaning, exploratory data analysis (EDA), feature engineering, and advanced analytics** using **Python, Pandas, and other relevant data analysis libraries**.  

## **2. Dataset Overview**  
The dataset used for this analysis is **Online Retail II**, which contains transaction records for a UK-based online retailer from **December 1, 2009, to December 9, 2011**. The company specializes in unique all-occasion giftware, with many customers being wholesalers.  

**Source:** [Online Retail II Dataset](https://archive.ics.uci.edu/dataset/502/online+retail+ii)  

### **Dataset Attributes**  
- **InvoiceNo** – Unique transaction ID  
- **StockCode** – Product identifier  
- **Description** – Product name  
- **Quantity** – Number of products purchased  
- **InvoiceDate** – Date of transaction  
- **Price** – Unit price of the product  
- **CustomerID** – Unique customer identifier  
- **Country** – Country where the customer is located  

---

## **3. Data Cleaning and Preparation**  
### **Initial Inspection**  
- The dataset contains **525,461 rows** and **8 columns**.  
- Used `df.info()` to examine data types and identify missing values.  

### **Handling Missing Values**  
- The **Description** and **CustomerID** columns contain missing values.  
- Missing values in **Description** were replaced with `"Unknown"`.  
- Missing values in **CustomerID** were replaced with `0` (indicating an unidentified customer).  

### **Handling Duplicates**  
- Used `df.duplicated().sum()` to identify duplicate entries.  
- Removed all duplicate rows using `df.drop_duplicates()`.  

### **Final Validation**  
- Used `df.info()` to ensure all missing values were handled and data types were appropriate for analysis.  

---

## **4. Exploratory Data Analysis (EDA)**  
### **Descriptive Statistics**  
- Used `df.describe()` to generate summary statistics.  

### **Key Insights from EDA**  
1. **Sales Distribution Across Countries**  
   - Identified the top-performing countries based on total sales.  
2. **Price Distribution by Stock Code**  
   - Analyzed price variations across different product categories.  
3. **Top-Selling Products**  
   - Identified the **top 5 stock codes** by quantity sold.  
4. **Customer Frequency Analysis**  
   - Determined the **top 10 most frequent customers** based on transaction counts.  
5. **Transaction Frequency Trends**  
   - Analyzed transaction patterns over time.  

---

## **5. Feature Engineering**  
### **New Variables Created**  
1. **Total Sales Calculation**  
   ```python
   df['Total Sales'] = df['Quantity'] * df['Price']

---  

## **6.  Advanced Analytics**  
### **Investigated the relationship between Quantity and Price**  
            Quantity     Price
Quantity    1.000000  -0.001941
Price      -0.001941   1.000000

---

**7.  Keys Insights**
Top Countries by Sales: Belgium, Channel Islands, Australia, Austria, and Cyprus (See Figure 1).
Top Stock Codes by Price: 10002, 11001, 10135, 10133, and 10125 (See Figure 2).
Most Popular Product: StockCode 10002 had the highest quantity sold (See Figure 3).
Top Customers: Customer ID 14911 accounted for 18.8% of the top 10 customers, followed by ID 17841 (16.5%) (See Figure 4).
Most Popular Price Points: Products priced at $1.25 and $0.85 were the most frequently purchased (See Figure 5).
No Clear Price-Quantity Relationship: There is no strong correlation between price and quantity (See Figure 6).

---
**8.  Recommendations**
Expand Marketing in High-Sales Countries

Focus marketing efforts on Belgium, Channel Islands, Australia, Austria, and Cyprus to increase market share and revenue.
Ensure Stock Availability for High-Demand Products

StockCode 10002 is the best-selling product. Ensure adequate inventory to meet demand and avoid stockouts.
Price Optimization Strategy

The most popular products are priced at $1.25 and $0.85. Introduce more products within this price range to cater to customer affordability.
Avoid excessive stocking of high-priced items, as they may not sell as well.
Customer Loyalty Program

Customer ID 14911 contributes significantly to sales. Implement loyalty programs, exclusive offers, or personalized discounts to retain high-value customers.
Test Different Pricing Strategies

Although no strong correlation exists between price and quantity, experimenting with discounts, bundling, or seasonal pricing strategies may uncover hidden sales opportunities.
---
## 9. Appendix**

### Sale Price Distribution Across Different Countries
![Sale Price Distribution](image.png)  
**Figure 1:** Sale Price Distribution Across Different Countries  

### Price Distribution by Different Stock Codes
![Price Distribution by Stock Code](image-1.png)  
**Figure 2:** Price Distribution by Different Stock Codes  

### Top 5 Stock Codes by Quantity Sold
![Top 5 Stock Codes](image-2.png)  
**Figure 3:** Top 5 Stock Codes by Quantity Sold  

### Top 10 Most Frequent Customers
![Top 10 Customers](image-3.png)  
**Figure 4:** Top 10 Most Frequent Customers  

### Frequency of Transactions
![Transaction Frequency](image-4.png)  
**Figure 5:** Frequency of Transactions  

### Relationship Between Quantity and Price
![Quantity vs Price](image-5.png)  
**Figure 6:** Relationship Between Quantity and Price  

