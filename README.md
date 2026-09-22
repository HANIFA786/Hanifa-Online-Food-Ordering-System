# Hanifa-Online-Food-Ordering-System
# 🍔 Online Food Ordering System — Power BI Dashboard

An interactive Power BI dashboard analyzing customer demographics, ordering behavior, and feedback for an online food delivery service. Built to uncover who orders, from where, how often, and how satisfied they are — supporting data-driven decisions around customer targeting, retention, and service improvement.

## 📌 Project Overview

- **Type:** Business Intelligence Dashboard (Power BI Template)
- **File:** `Hanifa_DA-VSP-002.pbit`
- **Data Source:** `online food delivery dataset (1).csv`
- **Tool Used:** Power BI Desktop (Power Query + DAX + Data Visualization)
- **Layout:** Single-page interactive report (1920×1080)

## 🎯 Objective

To analyze an online food delivery dataset and build a single-page interactive dashboard that answers:

- Who are the customers ordering food online? (age, gender, marital status, occupation, education)
- What income and family-size segments order the most?
- How frequently do customers purchase, and how does that vary by demographic?
- Where are customers geographically located (city/pin-code level)?
- What is the order outcome and customer feedback pattern?

## 🗂️ Dataset

A single table, **`online food delivery dataset (1)`**, containing:

| Column | Type | Description |
|---|---|---|
| Age | Integer | Customer's age |
| Gender | Text | Customer's gender |
| Marital Status | Text | Marital status of the customer |
| Occupation | Text | Customer's occupation |
| Monthly Income | Text | Income bracket |
| Educational Qualifications | Text | Highest qualification |
| Family size | Integer | Number of family members |
| Customer Type | Text | New vs. returning customer |
| latitude / longitude | Decimal | Geographic coordinates of the customer |
| Pin code | Integer | Delivery area pin code |
| Output | Text | Order outcome (e.g., order placed / not placed) |
| Feedback | Text | Customer feedback on the order |
| Column1 | Text | Unique row/order identifier |

## ⚙️ Data Preparation (Power Query)

- Loaded raw CSV via `Csv.Document`
- Promoted the first row to headers
- Applied correct data types to each column (`Age` → Integer, text fields → Text, etc.)

## 📐 DAX Measures

```DAX
total sales = ...
total orders = [total sales]
Average Purchase Frequency = DIVIDE([Total Orders], DISTINCT('online food delivery dataset (1)'[Column1]))
```

## 📊 Dashboard Visuals

| Visual | Purpose |
|---|---|
| **KPI Card** | Quick summary of Age / Customer Type |
| **Waterfall Chart** | Feedback vs. Order Output breakdown |
| **Treemap** | Gender × Monthly Income × Age distribution |
| **Bar Chart** | Age distribution by Gender |
| **Shape Map** | Geographic spread of customers (lat/long) |
| **Slicer** | Filter by Customer Type |
| **Pie Chart** | Educational Qualification vs. Customer Type share |
| **Clustered Bar Chart** | Average Purchase Frequency by Gender & Customer Type |
| **Donut Chart** | Marital Status distribution |
| **Funnel Chart** | Marital Status vs. Pin Code funnel |
| **Gauge** | Family Size indicator |

## 🔍 Key Insights Explored

- Demographic profile of the customer base (age, gender, marital status, education, occupation)
- Purchase frequency trends across customer segments
- Geographic concentration of orders
- Correlation between feedback and order outcomes

## 🛠️ How to Use

1. Open `Hanifa_DA-VSP-002.pbit` in **Power BI Desktop**.
2. When prompted, connect it to the source CSV (`online food delivery dataset (1).csv`) on your local machine, or update the data source path via **Transform Data → Data Source Settings**.
3. Click **Refresh** to load the latest data.
4. Interact with the slicer and visuals to explore different customer segments.

## 🧰 Tech Stack

- **Power BI Desktop** — dashboard design & visualization
- **Power Query (M)** — data cleaning & transformation
- **DAX** — custom measures for sales, orders, and purchase frequency

## 👩‍💻 Author

**Hanifa Begum**
Data Analyst | SQL · Python · Power BI · Advanced Excel

---
*Part of a portfolio of data analytics projects demonstrating end-to-end skills in data cleaning, modeling, and visualization.*
