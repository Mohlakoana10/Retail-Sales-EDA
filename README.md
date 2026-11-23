# Retail Sales Analysis - EDA Project

## 📊 Project Overview
Exploratory Data Analysis of 1,000 retail transactions to understand what drives revenue, who the customers are, and where the business should focus.

**Key Question:** What drives revenue in this retail store - Category, Gender, Age, Quantity, or Time?

## 🗂️ Dataset
- **Source:** Retail Sales Dataset
- **Period:** 2023-01-01 to 2024-01-01
- **Rows:** 1,000 transactions
- **Columns:** Transaction ID, Date, Customer ID, Gender, Age, Product Category, Quantity, Price per Unit, Total Amount
- **Data Quality:** No missing values, no duplicates. 1,000 transactions = 1,000 unique customers.

## 🛠️ Tools Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

## 🔍 Key Findings

### 1. Overall Performance
- **Total Revenue:** 456,000
- **Average Sale:** 456.0
- **Median Sale:** 135.0
- **Transactions:** 1,000

> Revenue is right-skewed - mean (456) > median (135). Most sales are small, a few large sales pull the average up.

### 2. Product Category - Balanced, No Dominant Winner
| Category | Transactions | Total Revenue | Avg Sale |
| :--- | :--- | :--- | :--- |
| Electronics | 342 | 156,905 | 458.79 |
| Clothing | 351 | 155,580 | 443.25 |
| Beauty | 307 | 143,515 | 467.48 |

- **Electronics** leads on total revenue (156,905)
- **Clothing** leads on volume (351 transactions)
- **Beauty** leads on average sale (467.48) despite fewest transactions

### 3. Gender - No Meaningful Difference
| Gender | Transactions | Total Revenue | Avg Sale |
| :--- | :--- | :--- | :--- |
| Female | 510 | 232,840 | 456.55 |
| Male | 490 | 223,160 | 455.43 |

> Female total is slightly higher only because there are 20 more Female customers. Average spend per visit is virtually identical (difference of 1.12). Gender does not drive spending.

### 4. Monthly Trend - Volatile, No Growth Trend
- **Peak:** May 2023 - 53,150
- **Lowest full month:** September 2023 - 23,620
- Revenue fluctuates between 23k - 53k with no steady growth.

> Note: Jan 2024 (1,530) excluded - only 1 day of data (2024-01-01).

### 5. Customer Age - Uniform Distribution
- Range: 18 - 64 years, Mean: 41.4
- Distribution is flat across all ages, no dominant segment.

### 6. Quantity vs Total Amount - Price Beats Quantity
> Buying more items does NOT mean spending more. Price per Unit drives revenue. A single high-priced item can be worth more than 4 low-priced items.

## 💡 Business Recommendations
1. **Don't drop any category:** Revenue is balanced. Focus on cross-selling.
2. **Promote Beauty:** Highest average sale (467.48). Opportunity to increase basket value.
3. **Don't split marketing by gender:** Spend per visit is identical.
4. **Focus on retention:** 1,000 customers bought only once. Biggest opportunity is a 2nd purchase.
5. **Replicate May:** Investigate what drove the May peak (53,150) and repeat it.
6. **Investigate September dip:** Lowest month (23,620).
7. **Sell value, not volume:** Push higher-value items.

## ▶️ How to Run
1. Clone this repo
2. Install: `pip install pandas matplotlib seaborn`
3. Open `Retail_Sales_EDA.ipynb` in Jupyter / Google Colab
4. Run all cells

---
**Author:** Mohlakoana Mokoena
