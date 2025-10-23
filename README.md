## 📊 Power BI Project: Sample Superstore Analysis

### 🧾 Overview

This Power BI report analyzes sales performance, profitability, and customer behavior using the **Sample Superstore** dataset. The dashboard provides insights into regional trends, product performance, shipping efficiency, and customer segmentation to support data-driven decision-making.

---

### 📂 Dataset Information

**Source File:**
`Sample - Superstore.csv`

**Description:**
The dataset contains transactional sales records for a retail company operating across multiple regions in the United States.

**Key Columns:**

| Column Name   | Description                                               |
| ------------- | --------------------------------------------------------- |
| Order ID      | Unique identifier for each order                          |
| Order Date    | Date when the order was placed                            |
| Ship Date     | Date when the order was shipped                           |
| Ship Mode     | Shipping method (e.g., First Class, Standard Class)       |
| Customer ID   | Unique identifier for each customer                       |
| Customer Name | Name of the customer                                      |
| Segment       | Customer segment (Consumer, Corporate, Home Office)       |
| Country       | Country of the transaction                                |
| City          | City where the sale occurred                              |
| State         | State where the sale occurred                             |
| Region        | Geographic region (Central, East, South, West)            |
| Product ID    | Unique product identifier                                 |
| Category      | Product category (Furniture, Office Supplies, Technology) |
| Sub-Category  | Product sub-category                                      |
| Product Name  | Name of the product                                       |
| Sales         | Total sales amount                                        |
| Quantity      | Number of items sold                                      |
| Discount      | Discount applied on the order                             |
| Profit        | Profit earned on the order                                |

---

### 🧠 Data Model

The model uses a **single fact table** (`Orders`) with calculated columns and measures for analysis.

**Key Measures (DAX):**

* **Total Sales** = SUM(Orders[Sales])
* **Total Profit** = SUM(Orders[Profit])
* **Profit Margin** = DIVIDE([Total Profit], [Total Sales])
* **Total Quantity Sold** = SUM(Orders[Quantity])
* **Average Discount** = AVERAGE(Orders[Discount])

---

### 📈 Report Pages

1. **Sales Overview**

   * KPIs: Total Sales, Profit, Quantity, and Discount
   * Charts: Sales by Region, Category, and Sub-Category
   * Slicer: Year and Region

2. **Profit Analysis**

   * Visuals: Profit by State, Profit Margin by Category
   * Highlight: Most and least profitable products

3. **Customer Insights**

   * Customer segmentation by Segment and Region
   * Top 10 customers by sales and profit

4. **Shipping Performance**

   * Delivery timelines by Ship Mode
   * Late shipments vs. total orders

5. **Product Performance**

   * Sub-category level breakdowns
   * Trend analysis by month and category

---

### ⚙️ Data Source Settings

* **Type:** CSV file
* **Location:** Local file (`C:\Users\Above James\Desktop\Data Analysis Folder\Sample - Superstore.csv`)
* **Connection Mode:** Import (loaded into Power BI model)

---

### 🚀 Usage Instructions

1. Open the `.pbix` file in **Power BI Desktop**.
2. Ensure the data source path points to the correct CSV location.
3. Click **Refresh** to update the dataset.
4. Explore insights through interactive visuals and slicers.

---

### 📚 Insights & Findings (Typical)

* The **West region** often leads in total sales.
* **Technology** category yields the highest profit margins.
* **Furniture** tends to have low profitability due to higher discounts.
* **Standard Class** shipping mode is the most used but has longer delivery times.

---

### 🧩 Future Improvements

* Add **forecasting visuals** for sales trends.
* Integrate **geospatial mapping** using ArcGIS.
* Include **dynamic parameter filters** for date and category.


