# 🍎 Fruits Sales Analytics Dashboard

> A multi-page Power BI dashboard built to track and analyze fruit retail sales performance across stores, categories, brands, and customers — enabling data-driven decisions in FMCG and grocery retail.

---

## 📌 Problem Statement

Retail fruit businesses often face challenges like:
- Identifying which stores and product categories consistently drive revenue
- Tracking cumulative sales growth over time (YTD trends)
- Understanding average vs. total sales to spot outlier months or locations
- Finding the top-performing stores without sifting through raw spreadsheets

This dashboard consolidates all that into a clean, navigable analytics tool.

---

## 🖥️ Dashboard Pages

| Page | Description |
|------|-------------|
| **Fruit Sales** | Cover / landing page with summary context |
| **Sum / Average** | Side-by-side line charts for Total Sales and Average Sales by Year & Month |
| **Sales Analysis** | Running totals, YTD sales trend, average sales by customer, and Top 5 Stores by Revenue |

---

## 🔍 Key Features

- **7 interactive slicers** — filter by Customer Name, Brand, Category, Product, Store Name, Store Location, and Date
- **Running Total measure** — track cumulative revenue growth over time
- **YTD Sales** — year-to-date performance line charts
- **Top 5 Stores ranking** — dynamically ranked by total sales
- **Average vs. Total** — compare mean and sum side-by-side to identify high-variance periods

---

## 🛠️ Tech Stack

| Tool | Usage |
|------|-------|
| **Power BI Desktop** | Dashboard development and visualization |
| **DAX** | Running Total, YTD Sales, Average Sales, Sum of Sales measures |
| **Power Query (M)** | Data shaping and date table generation |

---

## 📊 Key DAX Measures

```dax
Running Total = CALCULATE([Sum of Sales], FILTER(ALL('Date'), 'Date'[Date] <= MAX('Date'[Date])))

TotalYTD Sales = TOTALYTD([Sum of Sales], 'Date'[Date])

Average Sales = AVERAGEX(VALUES('Sales'[Customer Name]), [Sum of Sales])
```

---

## 📊 Dataset Fields

`Customer Name` · `BrandName` · `CategoryName` · `ProductName` · `Store Name` · `Store Location` · `Date` · `Sales`

---

## 💡 Business Impact

- Helps **retail managers** identify which stores are underperforming relative to average
- Enables **category managers** to reallocate inventory toward high-velocity brands and products
- Supports **sales forecasting** with running total and YTD trend visibility
- Drives **promotional planning** by pinpointing seasonal sales dips or spikes

---

## 📁 File

| File | Description |
|------|-------------|
| `Fruits_Sales_Dashboard.pbix` | Power BI report file |

---

## 🚀 How to Use

1. Download `Fruits_Sales_Dashboard.pbix`
2. Open in **Power BI Desktop**
3. Navigate through the 3 pages using the page tabs at the bottom
4. Use slicers to filter by store, brand, category, or date range

---

## 👤 Author

**Tejas Bafna** — Data Analyst | Power BI Developer  
📧 tejasbafna311@gmail.com · [LinkedIn](www.linkedin.com/in/tejas-bafna) ·
