# Excel Dashboard Suite: Customer Service, Finance & Orders
### A Data-Driven Exploration in Dashboard Design

A suite of three interactive Excel dashboards — **Customer Service**, **Finance**, and **Orders Management** — built to showcase how spreadsheet tools can transform raw business data into actionable insights. By combining KPI tracking, time-series analysis, and interactive filtering, the dashboards deliver a 360-degree view of a food chain's operations, covering sales performance, customer satisfaction, and financial trends. The project leverages advanced Excel features including PivotTables, PivotCharts, Slicers, and Conditional Formatting to produce clean, user-friendly, and data-driven decision support.

![Dashboard Overview](Images/dashboard-overview.png)

---

## 📂 Repository Structure

```
Excel-Dashboard-Suite/
│
├── Images/
│   ├── dashboard-overview.png
│   ├── customer-service-dashboard.png
│   ├── finance-dashboard.png
│   └── orders-dashboard.png
│
├── Customer_Service_Dashboard.xlsx
├── Finance_Dashboard.xlsx
├── Orders_Management_Dashboard.xlsx
├── README.md
└── .gitattributes
```

---

## 🗂️ Project Overview

The **Excel Dashboard Suite** aims to:

- **Monitor Sales Operations** — Track total orders, revenue, average order value, discounts, and product-level performance through the Orders Management Dashboard
- **Evaluate Customer Experience** — Analyze customer interactions, satisfaction (CSAT) scores, agent efficiency, and workload distribution using the Customer Service Dashboard
- **Assess Financial Performance** — Examine sales distribution, revenue trends, regional performance, and identify underperforming products with the Finance Dashboard
- **Enable Strategic Decisions** — Provide stakeholders with a 360-degree view of business operations, turning raw transactional data into actionable insights for optimization and growth

---

## 🗃️ Dataset Structure

The project is built on three interlinked datasets capturing customer interactions, financial transactions, and order-level details. Together they provide a holistic view of customer service performance, sales trends, and operational efficiency.

### Customer Service Dataset
Captures customer support interactions to analyze service quality and agent performance.

| Field | Description |
|---|---|
| `Customer_ID`, `Order_ID` | Unique identifiers linking service tickets to customers and orders |
| `Contact_Date`, `Contact_Day`, `Contact_Date_Month` | Temporal details for tracking patterns in service requests |
| `Contact_Type` | Nature of the interaction — Query, Request, or Complaint |
| `Is_it_for_an_Order` | Binary flag indicating whether the contact relates to an order |
| `Ticket_ID` | Unique support ticket reference |
| `Agent_Handled` | Agent assigned to the case |
| `Rating_Given` | Customer satisfaction rating (scale 1–10) |

### Finance Dataset
Tracks financial outcomes of sales transactions to monitor revenue, discounts, and regional performance.

| Field | Description |
|---|---|
| `Order_ID`, `Product_ID` | Transactional identifiers for mapping orders to products |
| `Sale_Date` | Date of purchase |
| `Amount_in_Sales` | Gross sales value |
| `Discounted_Value` | Net revenue after discounts |
| `Region` | Geographical market segmentation (North, South, East, etc.) |

### Orders Dataset
Provides detailed order-level insights for operational analysis.

| Field | Description |
|---|---|
| `Order_ID`, `Product_ID` | Core identifiers linking orders with products |
| `Product_Name`, `Order_Type` | Item description and sales channel (Online vs. Physical Visit) |
| `Price_of_One_Product` | Unit price of the product |
| `Agent` | Staff member responsible for processing the sale |
| `No_of_Products_in_one_Sale` | Quantity purchased per order |
| `Discount` | Percentage discount applied |
| `Revenue_before_discount`, `Revenue_after_discount`, `Discount_Amount` | Calculated revenue and discount impact fields |

---

## 🛠️ Dashboard Development & Analytical Workflow

### 1. Formulated Targeted Business Questions
Defined key operational questions for each dashboard to guide the analysis. For example, in the Orders Dashboard I evaluated the relationship between discount strategy and profitability, while in the Customer Service Dashboard I focused on identifying the root causes of complaints.

### 2. Data Preparation & Feature Engineering
- Cleaned and standardized all three datasets to ensure accuracy and consistency
- Engineered new calculated fields such as discrete sales buckets (e.g., ₹300–₹500) to analyze purchasing patterns
- Created agent-specific performance metrics including Average CSAT per agent

### 3. Pivot-Based Analysis & Visualization
- Leveraged PivotTables and PivotCharts to aggregate raw data and answer each business question
- Created time-series trends for daily revenue, broke down CSAT scores by agent and contact type, and compared product-level sales performance

### 4. Interactive Dashboard Construction
- Assembled three distinct dashboards (Orders, Customer Service, Finance), each tailored to its functional audience
- Incorporated Slicers for dynamic filtering by Agent, Region, and Order Type
- Applied a clean, minimalist design with a consistent pastel color palette to enhance readability for non-technical stakeholders

### 5. Insight Generation & Reporting
- Synthesized the visual analysis into actionable insights documented directly on the dashboards
- Key findings included pinpointing underperforming products, linking order-related issues to customer complaints, and framing a methodology to evaluate discount ROI on a per-agent basis

---

## 📊 Dashboard Previews

### Customer Service Dashboard
Tracks customer support volume, interaction types, agent-level CSAT scores, and weekly contact patterns. Enables managers to identify coaching opportunities and optimize staffing.

![Customer Service Dashboard](Images/customer-service-dashboard.png)

---

### Finance Dashboard
Visualizes revenue distribution by region, sales trends over time, product-level financial performance, and the impact of discounting on net revenue.

![Finance Dashboard](Images/finance-dashboard.png)

---

### Orders Management Dashboard
Monitors total orders, average order value, product sales volumes, discount application rates, and sales channel distribution (Online vs. Physical Visit).

![Orders Management Dashboard](Images/orders-dashboard.png)

---

## 💡 Key Insights

### Financial & Product Performance
- **Underperforming Products:** PIZB0005 (₹10,677 revenue, ₹628 avg. sales) and PIZB0006 (₹5,077 revenue, ₹564 avg. sales) were identified as significant underperformers — candidates for strategic review or discontinuation
- **Revenue Concentration:** 73% of sales occur within the ₹500–₹900 range, highlighting this as the core pricing sweet spot for retention and upselling
- **Volume vs. Value Discrepancy:** While the *Large Paneer Tikka Pizzabun* drove high order volumes, the standard *Paneer Tikka Pizzabun* generated higher total revenue — underscoring the distinction between popularity and profitability
- **Sales Trend Decline:** Despite stable average ticket sizes (~₹5,000), overall sales volumes declined after July, reflecting possible product mix shifts or increased discounting pressure

### Customer Service Drivers & Agent Performance
- **Interaction Mix:** Requests (53%) and Queries (38%) dominate customer contact, while Complaints remain limited at 9%
- **Non-Order Related Issues:** A substantial portion of queries and complaints are unrelated to orders, indicating friction in pre-sales information and general support
- **Agent CSAT Gap:** Adrien Martin (7.3) outperformed peers Albain Forestier and Roch Cousineau (both 6.9), highlighting clear training and coaching opportunities
- **Service Quality by Contact Type:** Requests achieved the highest CSAT (7.2) vs. Queries (6.9) and Complaints (6.6) — dissatisfaction is most pronounced in complaint handling

### Operational & Weekly Trends
- **Order & Revenue Profile:** Across 794 orders, the business generated ₹2,38,246 in total revenue — average revenue per order ₹300.06, average discount ₹251.92
- **Volatile Daily Sales:** Revenue and order volumes showed sharp, sporadic peaks in late June and mid-July, indicating demand volatility and opportunities for smoothing strategies
- **Product Winners & Laggards:** Paneer Tikka and Large Paneer Tikka Pizzabuns each drove over ₹54,000 in revenue, while Aloo Shots Pizzabun lagged at ₹10,046
- **Weekly Customer Trends:** Interactions peaked on Mondays and declined through the week; CSAT peaked midweek (Wednesday avg. 7.4) — suggesting workload redistribution and Monday handling improvements as quick wins

---

## ⭐ Project Highlights

- Developed a **comprehensive suite of three interactive Excel dashboards** (Orders, Customer Service, Finance) providing a 360° view of business operations
- Adopted a **question-driven analytical approach**, leveraging PivotTables, PivotCharts, Slicers, and Conditional Formatting to transform raw data into actionable intelligence
- Engineered **custom KPIs and calculated fields** — including sales buckets, agent-level CSAT, and average revenue per order — to uncover hidden performance drivers
- Identified **critical business insights** such as the divergence between high-volume vs. high-revenue products, underperforming product lines, and regional sales disparities
- Implemented a **clean, user-centric design** with interactive filtering and a minimalist pastel theme, ensuring accessibility and clarity for non-technical stakeholders
- Delivered a **scalable decision-making framework** offering insights on staffing optimization, discount strategy ROI, and customer satisfaction improvement

This project demonstrates how Microsoft Excel can be leveraged to build a cohesive suite of interactive dashboards, transforming raw and siloed operational data into integrated business intelligence that delivers actionable insights and drives strategic decision-making across sales, finance, and customer service operations.

---

## 🧰 Tools & Techniques

| Tool / Feature | Usage |
|---|---|
| Microsoft Excel | Primary platform for all dashboards |
| PivotTables | Multi-dimensional data aggregation |
| PivotCharts | Linked dynamic visualizations |
| Slicers | Interactive cross-filtering across dashboards |
| Conditional Formatting | At-a-glance KPI status indicators |
| Calculated Fields | Custom metrics — CSAT avg, sales buckets, discount ROI |
| Excel Tables | Structured data ranges enabling auto-refresh |

---

## 🚀 How to Use

1. **Download** the `.xlsx` files from this repository (or clone the repo)
2. **Open** in Microsoft Excel 2016 or later for full Slicer and PivotChart support
3. Navigate to the **Dashboard** tab in each workbook for the summary view
4. Use the **Slicers** to filter by Agent, Region, Product, or Order Type — all charts update dynamically
5. Explore the underlying **data and pivot sheets** for detailed drill-down analysis

---

*Built with Microsoft Excel · Food Chain Operations Dataset*
