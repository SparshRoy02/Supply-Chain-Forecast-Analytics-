## Supply Chain & Profitability Analytics (2019–2022)

### Project Overview

This project presents an interactive **Supply Chain & Profitability Analytics Dashboard** built using **Power BI** to analyze business performance across four years (2019–2022).

The dashboard transforms raw supply chain data into **actionable insights**, enabling stakeholders to monitor revenue growth, evaluate profitability, and identify cost inefficiencies across regions and product segments.

---

### Problem Statement

Organizations often experience rapid revenue growth but fail to maintain profitability due to:

* Lack of visibility into **cost drivers (COGS, operational expenses)**
* Inability to track **profitability trends over time**
* Difficulty in comparing **actual performance vs benchmark (BM)**
* Limited insights into **region-wise and product-wise performance**

As a result, businesses face **hidden losses despite increasing sales**, leading to poor strategic decisions.

---

### Purpose of the Dashboard

This dashboard is designed to solve the above challenges by:

* Providing **year-wise (2019–2022) performance comparison**
* Identifying **profit leakage and cost inefficiencies**
* Enabling **benchmark vs actual (BM vs Selection) analysis**
* Supporting **data-driven decision-making for sustainable growth**

---

### Dashboard Views (4-Year Analysis)

#### 2019 – Baseline Performance

* Net Sales: **$111.37M**
* GM%: **41.20%**
* Net Profit %: **2.21%**

**Insight:**
A stable and profitable baseline year with controlled costs and healthy margins.

---

#### 2020 – Revenue Growth with Declining Profitability

* Net Sales: **$267.98M  +140%**
* GM%: **37.10%**
* Net Profit %: **-0.85%**

**Insight:**
Significant revenue growth but profitability turned negative due to increased costs — early indication of inefficiency.

---

#### 2021 – Aggressive Scaling with Heavy Losses

* Net Sales: **$823.85M  +207%**
* GM%: **36.49%**
* Net Profit %: **-6.63%**

**Insight:**
Business scaled rapidly, but operational expenses surged, leading to substantial losses.

---

#### 2022 – Peak Revenue but Maximum Loss

* Net Sales: **$3.74B  +353%**
* GM%: **38.08%**
* Net Profit %: **-13.98%**

**Insight:**
Despite achieving peak revenue and slight margin improvement, excessive operational costs resulted in critical losses.

---

### Key Business Insights

* Revenue increased **~33x from $111M (2019) to $3.74B (2022)**
* Net Profit % dropped from **+2.21% → -13.98%**
* Operational expenses are the **primary driver of losses**
* APAC and North America are the **top-performing regions**
* Notebooks and Peripherals are **high-revenue segments**
* High growth does not guarantee profitability → **cost control is critical**

---

### Data Model

The dashboard follows a **Star Schema Data Model**:

#### Fact Table

* Sales Data (Revenue, Cost, Profit Metrics)

#### Dimension Tables

* Region
* Product Segment
* Customer
* Date (Year, Month, Quarter)

---

### Key Metrics & KPIs

* Net Sales
* Gross Margin (GM)
* Gross Margin %
* Net Profit
* Net Profit %
* Cost of Goods Sold (COGS)
* Operational Expenses
* Benchmark (BM) Comparison
* Year-over-Year (YoY) Growth

---

### Tools & Technologies

* Power BI
* DAX (Data Analysis Expressions)
* Microsoft Excel / CSV

---

### Key DAX Measures

```DAX
Net Sales = SUM(Sales[Net Sales])

Gross Margin = [Net Sales] - [COGS]

GM % = DIVIDE([Gross Margin], [Net Sales], 0)

Net Profit = [Gross Margin] - [Operational Expense]

Net Profit % = DIVIDE([Net Profit], [Net Sales], 0)

YoY Growth % =
DIVIDE(
    [Net Sales] - CALCULATE([Net Sales], SAMEPERIODLASTYEAR(Date[Date])),
    CALCULATE([Net Sales], SAMEPERIODLASTYEAR(Date[Date]))
)
```

---

### Features of the Dashboard

* Year-wise comparison (2019–2022)
* Monthly trend analysis (Net Sales over time)
* Benchmark vs Actual comparison
* Region-wise performance breakdown
* Product segment analysis
* KPI cards for quick insights
* Interactive filters (Region, Customer, Segment)
* Profit & Loss statement visualization

---

### Project Structure

```
Supply-Chain-Analytics-Dashboard
│
├── Data
│    ├── dim_customer.csv
│    ├── dim_market.csv
│    ├── dim_product.csv
│    └── fact_sales_monthly.zip
│
├── Dashboard
│     └── Supply_Chain_Dashboard.pdf
│
└── README.md
```

---

### Business Conclusion

Although the company demonstrates **exceptional revenue growth**, the continuous decline in profitability highlights a major issue in **cost management and operational efficiency**.

 The dashboard clearly shows that:

* Growth is **not sustainable without cost control**
* Increasing operational expenses are eroding profits
* Strategic decisions must focus on **efficiency, not just expansion**

---

### Future Enhancements

* Predictive analytics (Sales forecasting using time series models)
* Integration with real-time data sources
* Advanced analytics using Python (Pandas, ML models)
* Customer segmentation & churn analysis

---

### Final Note

This project demonstrates the ability to not only build dashboards but also extract meaningful business insights, identify critical problems, and support strategic decision-making using data.
