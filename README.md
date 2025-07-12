# ✅ Preprocessing and Visualization of Restaurant Data

## 📌 Project Overview
This project involves preprocessing and visualizing transactional data from a restaurant's point-of-sale system. The objective is to analyze customer purchases, item-level sales trends, and invoice-level revenue metrics using Python and visualization libraries.

---

## 🗃️ Dataset Information
- **Source:** Excel file (`Restaurant.xlsx`) uploaded to Google Colab
- **Format:** `.xlsx`
- **Columns Identified:**
  - `DATE`: Transaction date
  - `INVOICE_NO`: Unique invoice number
  - `ITEM`: Name of the item sold
  - `QUANTITY`: Number of units sold
  - `SUB_TOTAL`: Item total before tax or discount
  - `AMOUNT`: Final amount paid

---

## 📊 Data Preprocessing
- Loaded Excel data using `pandas.read_excel()`
- Viewed sample records using `.head()`
- Checked data types and null values using `.info()` and `.isnull().sum()`
- Filtered specific dates and invoices for targeted analysis

---

## 📉 Data Analysis and Visualizations

### 🔹 Specific Date Filtering
- Filtered data for:
  - `01.10.23`: Calculated **average transaction amount**
  - `INVOICE_NO = 117`: Calculated **total transaction value**
  - `2.10.2023`: Isolated for visual summaries

### 🔸 Aggregation & Insights
- **Top 5 Items by Revenue:**  
  Used `groupby('ITEM')['SUB_TOTAL'].sum()`  
  → Visualized with `seaborn.barplot()`

- **Least 5 Items by Quantity Sold:**  
  Used `groupby('ITEM')['QUANTITY'].sum()`  
  → Visualized with `seaborn.barplot()`

- **Top 5 Invoices by Total Amount:**  
  Used `groupby('INVOICE_NO')['AMOUNT'].sum()`

---

## 🔍 Key Insights
- Identified high-revenue generating items.
- Found underperforming items in terms of quantity sold.
- Tracked big-bill customers based on invoice totals.
- Computed specific stats like:
  - Average spend per customer on a specific day.
  - Total amount in a particular invoice.

---

## 📌 Tools & Libraries Used
- `Pandas`: Data loading and aggregation
- `NumPy`: Numerical operations
- `Seaborn`: Data visualization (`barplot`)
- `Matplotlib`: (Optional for future visuals)

---

## 📷 Sample Visualizations

> Add your saved plots to the GitHub project under an `images/` folder and link them here:

```markdown
![Top 5 Items by Subtotal](images/top_items.png)
![Least 5 Sold Items](images/least_items.png)
