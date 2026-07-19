# Online Retail Performance Analysis — Data Analysis Midterm Project

An end-to-end data analysis project on the **Online Retail II** dataset: cleaning a messy, real-world transactional dataset in Excel/Power Query, exploring it to answer concrete business questions, and building an interactive Power BI dashboard with KPIs measured against explicit targets.

## 🔗 Live Dashboard

[View the dashboard on Power BI Service](https://app.powerbi.com/groups/me/reports/6710a21e-b46c-4fb0-bfed-06e91bf39106/8c65d72624e382cfb5a5?experience=power-bi)

## 📊 Project Overview

| | |
|---|---|
| **Dataset** | [Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii) — UCI Machine Learning Repository |
| **Domain** | E-commerce / Retail |
| **Size** | ~1,050,856 transaction rows × 18 columns (after cleaning), covering Dec 2009 – Dec 2011 |
| **Tools** | Microsoft Excel (Power Query, PivotTables), Power BI |
| **Business question** | Which countries, products, and time periods drive the most revenue, and how much of that revenue is affected by cancellations? |

## 📁 Repository Contents

| File | Description |
|---|---|
| `AlyEldeen_Midterm_DatasetDescription.pdf` | Dataset title, source, variable descriptions, and justification |
| `AlyEldeen_Midterm_CleanedDataset.xlsx` | Cleaned dataset (Power Query), with engineered fields (Revenue, Transaction Type, CustomerType, IsOutlier, etc.) |
| `Aly_Midterm_Dashboard.pbix` | Interactive Power BI dashboard (2 pages, 3 KPIs, synced slicers) |
| `AlyEldeen_Midterm_ProjectReport.pdf` | Full project report: data cleaning, EDA, dashboard summary, KPI explanation, business insights |

## 🧹 Data Cleaning Highlights

- Missing `Customer ID` (~22.7% of rows) flagged as **Guest** rather than deleted
- Cancelled/returned orders and non-product rows separated into a `Transaction Type` field (Successful Sale, Cancelled/Returned, Free Gift/Sample, Inventory Loss/Damaged, Accounting Adjustment)
- Outliers flagged (`IsOutlier`) instead of removed, keeping the row count transparent
- Duplicates removed, text standardized, `InvoiceDate` parsed as a proper date/time field
- Engineered features: `Revenue`, `InvoiceYear`, `InvoiceMonth`, `DayOfWeek`, `IsUK`

## 🔑 Key Performance Indicators

| KPI | Target | Actual | Result |
|---|---|---|---|
| Total Orders | 51,820.65 (+5% baseline growth) | 49,353 | -4.76% — below target |
| Total Revenue | 19.87M (+5% baseline growth) | 20.91M | +5.26% — target exceeded |
| Average Order Value | 444.95 (2009–2010 historical baseline) | 423.76 | -4.76% — below baseline |

## 💡 Key Findings

- **Seasonality:** Revenue peaks sharply in Q4 (Nov–Dec), holding in a much narrower band the rest of the year
- **Geographic concentration:** The UK drives ~84% of total revenue
- **Day-of-week pattern:** Thursday generates the highest revenue of the week
- **Customer loyalty:** 75.56% of identified customers are repeat buyers
- **Cancellations:** ~1.85% of transactions were cancelled or returned

Full methodology, decision log, and recommendations are in the [project report](./AlyEldeen_Midterm_ProjectReport.pdf).

## 👤 Author

Aly Eldeen
