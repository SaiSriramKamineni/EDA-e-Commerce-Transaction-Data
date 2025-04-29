# 🛒 E-Commerce Retail Dataset Analysis

## 📋 Table of Contents
1. [About the Project](#about-the-project)
2. [Dataset Description](#dataset-description)
3. [Tech Stack](#tech-stack)
4. [Data Preprocessing](#data-preprocessing)
5. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
6. [Visualizations](#visualizations)
7. [Key Insights](#key-insights)
8. [Conclusion](#conclusion)

---

## 📌 About the Project
This project involves analyzing an e-commerce retail dataset to extract business insights and prepare for further applications like customer segmentation, product recommendations, and sales forecasting.

The dataset contains over 540,000 transaction records from an online retailer based in the UK, selling gift-related items from 2010 to 2011.

---

## 📦 Dataset Description
The dataset `data.csv` includes the following columns:

| Column Name  | Description                                                       |
|--------------|-------------------------------------------------------------------|
| InvoiceNo    | Unique invoice number. 'C' prefix indicates a cancellation.      |
| StockCode    | Product/item code                                                 |
| Description  | Item name                                                         |
| Quantity     | Number of items purchased                                         |
| InvoiceDate  | Date and time of the transaction                                  |
| UnitPrice    | Price per item                                                    |
| CustomerID   | Unique customer ID                                                |
| Country      | Country of the customer                                           |

**Total rows:** 541,909  
**Total columns:** 8

---

## 🛠️ Tech Stack
- Python (Pandas, NumPy, Matplotlib, Seaborn, Plotly)
- Jupyter Notebook
- Markdown for documentation

---

## 🧹 Data Preprocessing
### ✅ Steps Taken:
- Loaded the dataset with ISO-8859-1 encoding.
- Checked and summarized data types and missing values:
  - CustomerID has ~25% missing values.
  - Description has ~0.26% missing values.
- Dropped missing rows using `dropna()`.
- Removed duplicates (found 5,225).
- Converted `InvoiceDate` to datetime format.
- Removed canceled transactions (marked by 'C' in `InvoiceNo`).
- Filtered special StockCodes like POST, D, M, etc.
- Checked for negative `Quantity` indicating returns/refunds.

---

## 📊 Exploratory Data Analysis (EDA)

1. **Basic Stats**
   - **Total Products:** 3,684
   - **Total Transactions:** 22,190
   - **Total Unique Customers:** 4,372
   - **Countries involved:** 37

2. **Order Patterns**
   - Found 16.47% of transactions were canceled.
   - Detected returns through negative quantity values.
   - Discovered special StockCodes for discounts, postage, carriage, etc.

3. **Basket Size**
   - Number of products per invoice varies significantly (1 to over 80 items).

---

## 📈 Visualizations

| Visualization    | Description                                             |
|------------------|---------------------------------------------------------|
| 🌍 Choropleth Map | Orders per country                                     |
| 🔥 Bar Chart      | Top 10 countries by order volume                       |
| 📦 Histogram      | Distribution of number of products per transaction     |
| 🥧 Pie Chart      | Canceled vs non-canceled orders                        |
| 🔁 Count Plot     | Returned vs normal items                               |
| 🛒 Bar Chart      | Top 10 most sold products                              |
| 📅 Time Series    | Monthly trend of product sales                         |
| ☁️ Word Cloud     | Common words in product descriptions                   |
| 🧯 Heatmap        | Visual representation of missing data                  |

---

## 📌 Key Insights
- **United Kingdom** had the highest number of transactions (~89%).
- ~16.5% of total orders were canceled.
- Some product codes indicate services (e.g., postage, discounts).
- A few products (e.g., bags, lanterns) dominate sales.
- Returns are common for certain items and may indicate quality issues or customer dissatisfaction.

---

## 🧾 Conclusion
This project successfully performed an in-depth exploratory analysis of a retail transaction dataset. We cleaned, transformed, and visualized the data, identifying key patterns such as:
- Customer behavior across countries
- Popular products
- Cancelation and return patterns
- Seasonal sales trends

These insights can be used for:
- Inventory planning
- Targeted marketing
- Customer segmentation
- Sales forecasting

---

