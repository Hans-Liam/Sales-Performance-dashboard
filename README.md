# Sales Performance Analysis for Superstore

## Table of Contents

- [Introduction](#introduction)
- [Business Problem](#business-problem)
- [Business Questions](#business-questions)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Data Cleaning and Transformation](#data-cleaning-and-transformation)
- [Data Modeling](#data-modeling)
- [Dashboard](#dashboard)
- [Key Insights & Business Recommendations](#key-insights--business-recommendations)
- [Stakeholders](#stakeholders)
- [Limitations](#limitations)
- [Conclusion](#conclusion)

---

## Introduction

### Business Context

A US-based superstore needs a clearer view of its sales and profitability performance across products, regions, customers, and time.

This analysis uses transaction-level sales data from **2014–2017** to identify revenue drivers, profitability gaps, customer contributions, and seasonal patterns, with the goal of translating those findings into actionable recommendations.

Management needs a consolidated view of business performance to answer questions such as:

- How much revenue is the business generating?
- Which products and categories drive sales?
- Which regions contribute the most revenue and profit?
- Are high-sales categories also the most profitable?
- Which customer segments contribute most to revenue?
- How does sales performance change throughout the year?

I analyzed **9,994 transaction records** covering 2014–2017 to identify sales and profitability patterns and translate the findings into actionable recommendations.

### Why This Matters

Strong revenue does not necessarily mean strong profitability.

A business can generate significant sales while underperforming on profit because of differences in product mix, regional performance, pricing, or discounting.

The objective of this analysis was therefore not simply to determine where sales are highest, but to understand **where revenue and profitability align and where they do not**.

---

## Business Problem

The business lacked a consolidated view of sales performance that would allow stakeholders to quickly identify:

- Revenue and profit performance
- Sales trends over time
- High-performing products and categories
- Regional sales and profitability
- Customer contribution
- Potential gaps between revenue and profitability

### The Central Question

> **Where is the business generating sales, where is it generating profit, and where should management focus its attention?**

---

## Business Questions

The analysis was designed around the following questions.

### Sales Performance

- How much revenue is being generated?
- How is sales performance changing over time?
- Which months generate the most sales?
- Which product categories and sub-categories generate the most revenue?
- Which regions contribute the most sales?

### Profitability

- How much profit is being generated?
- Are there areas where strong sales do not translate into strong profit?
- Are the highest-selling categories also the most profitable?
- Which categories contribute most to profit?
- Which regions generate the most profit?

### Customers

- Which customer segments contribute most to sales?
- Which customers generate the most revenue?
- How are sales distributed across customer segments?

### Operations & Trends

- How many units are being sold?
- What is the average order value?
- Are there noticeable monthly patterns?
- How does performance vary across years and periods?

---

## Data Source

The primary dataset used for this project is the **Sample Superstore** dataset obtained from Kaggle:

**Source:** [Sample Superstore Dataset](https://www.kaggle.com/datasets/naveenkumar20bps1137/sample-superstore/data)

The dataset contains transaction-level information covering **2014–2017**.

### Dataset Dimensions

- **9,994 rows**
- **19 columns**

> **Note:** This is a portfolio analysis using a publicly available sample dataset. The business context described in this project represents a simulated stakeholder scenario rather than an engagement with the actual company.

---

## Tools Used

- **Microsoft Excel** — Data analysis and dashboard development
- **Power Query** — Data cleaning and transformation
- **PivotTables** — Aggregation and exploratory analysis
- **PivotCharts** — Data visualization
- **Excel Slicers & Timelines** — Interactive filtering
- **Excel Formulas** — Data validation and calculated metrics

---

## Data Cleaning and Transformation

The raw dataset was first inspected to understand its structure, data types, missing values, inconsistencies, and potential errors.

The preparation process included:

- Reviewing the structure and completeness of the dataset
- Checking for duplicate records
- Validating Row IDs
- Identifying incorrect and inconsistent values
- Checking quantity-related inconsistencies
- Standardizing data for analysis
- Separating and validating yearly records
- Creating fields required for time-based analysis
- Preparing the cleaned dataset for PivotTable analysis

### Data Validation

An important part of the process was validating the transaction data rather than immediately building visualizations from the raw file.

For example, inconsistencies identified in quantity values were investigated and corrected using Excel-based validation and `SUMIF` calculations.

This helped ensure that the dashboard metrics were based on a validated dataset.

---

## Data Modeling

The cleaned transaction data was structured into an **Excel Table** and used as the analysis source for PivotTables and PivotCharts.

The dashboard uses several calculated metrics, including:

- **Total Revenue**
- **Total Profit**
- **Quantity Sold**
- **Average Order Value**

These KPIs provide a high-level view of performance, while the underlying charts allow stakeholders to investigate the drivers behind them.

---

## Dashboard

The final dashboard was divided into two analytical views.

### Page 1 — Executive Sales Performance

![Executive Sales Performance Dashboard](https://github.com/Hans-Liam/Sales-Performance-dashboard/blob/26193cffd588c5150899fb722deb142931ba7491/Sales_Performance_Analysis_P1.png)

The first page focuses on:

- Revenue
- Profit
- Quantity Sold
- Average Order Value
- Monthly Sales
- Sales by Sub-category
- Sales by Region
- Monthly Profit
- Top 10 Products
- Regional Profit

Interactive filters allow stakeholders to explore performance by:

- Region
- Year
- Quarter
- Month
- Day
- Customer Segment
- Category
- Segment

---

### Page 2 — Customer & Profitability Analysis

![Customer and Profitability Analysis Dashboard](https://github.com/Hans-Liam/Sales-Performance-dashboard/blob/26193cffd588c5150899fb722deb142931ba7491/Sales_Performance_Analysis_P2.png)

The second page focuses on:

- Sales by Segment
- Sales by Customer Retention
- Sales Contribution by Category
- Profit by Customer Segment
- Top 10 Customers
- Profit Contribution by Category

This page was designed to move beyond the question:

> **"How much did we sell?"**

toward:

> **"Where is the money coming from, and where is the profit coming from?"**

---

# Key Insights & Business Recommendations

The analysis identified several important patterns across **sales, profitability, regional performance, customers, and seasonality**.

### 1. High Sales Do Not Always Translate Into High Profit

**What I found**

The business generated **$2.30M in sales and $286.41K in profit**. However, profitability varies significantly by category.

Technology generated **36.4% of total sales but contributed 50.79% of total profit**, while Furniture generated **32.3% of sales but only 6.45% of profit**.

**What this means**

Furniture generates substantial revenue but contributes relatively little to overall profit. This shows that increasing sales alone does not necessarily improve financial performance.

**Recommended action**

Management should investigate Furniture at the **product and sub-category level**, focusing on pricing, discounts, product costs, and individual product profitability.

The business should also identify what makes Technology more profitable and determine whether similar strategies can be applied elsewhere.

---

### 2. The West Region Leads Performance, While Central Requires Attention

**What I found**

The West generated the highest sales at approximately **$725K**, followed by:

- East — $678K
- Central — $501K
- South — $392K

The West also generated the highest profit at approximately **$108K**.

However, Central generated **$501K in sales but only $40K in profit**, giving it the weakest profit-to-sales performance among the four regions.

**What this means**

The West performs strongly on both revenue and profitability, while Central generates considerable revenue without converting it into comparable profit.

**Recommended action**

Management should examine the Central region's:

- Product mix
- Customer composition
- Sub-category performance
- Discounting patterns
- Product-level profitability

The West could also be examined to identify practices that may help improve performance in weaker regions.

---

### 3. Sales and Profit Show Clear Seasonal Fluctuations

**What I found**

Sales vary considerably throughout the year. Sales peak around:

- **November — $352K**
- **December — $325K**
- **September — $308K**

January and February are considerably weaker.

Profit also fluctuates throughout the year, increasing from approximately **$9K in January to $43K in December**, although several months experience noticeable declines.

**What this means**

Demand and profitability are not evenly distributed throughout the year. Certain periods represent significantly greater sales opportunities than others.

**Recommended action**

Management should use these historical patterns when planning:

- Inventory
- Staffing
- Sales targets
- Promotional campaigns
- Resource allocation

Further analysis could determine whether these seasonal patterns are consistent across categories and regions.

---

### 4. Consumer Customers Generate the Most Revenue

**What I found**

Consumer customers generated approximately **$1.16M in sales**, making them the largest customer segment.

Sales by segment were approximately:

- Consumer — $1.16M
- Corporate — $706K
- Home Office — $429K

Consumer also generated the most total profit at approximately **$134K**. However, Corporate has a slightly higher profit-to-sales ratio.

**What this means**

Consumer customers are currently the largest source of revenue and profit, but having the largest sales volume does not necessarily mean having the highest profitability efficiency.

**Recommended action**

Management should evaluate customer segments using both **revenue and profitability**, rather than sales alone.

Further analysis of purchasing behavior, product mix, and discounts could reveal opportunities to increase the profitability of the largest customer segment.

---

### 5. A Small Group of Customers Contributes Significantly to Sales

**What I found**

The Top 10 Customers dashboard shows individual customers generating approximately **$12K–$25K in sales**, with the leading customer contributing around **$25K**.

**What this means**

Some customers make substantially larger contributions to revenue than others, making them important accounts to understand and retain.

**Recommended action**

Management should investigate the purchasing patterns and profitability of high-value customers and consider targeted **retention and account-development strategies**.

A future analysis could calculate what percentage of total revenue comes from the Top 10 customers to quantify customer concentration.

---

### 6. Technology and Office Supplies Account for Most of the Company's Profit

**What I found**

Technology contributes **50.79% of total profit**, while Office Supplies contributes **42.77%**.

Together, they account for more than **90% of total profit contribution**, while Furniture contributes only **6.45%**.

**What this means**

The company's profitability is heavily concentrated in Technology and Office Supplies.

**Recommended action**

Management should identify the **products and sub-categories driving profitability** within Technology and Office Supplies and protect their availability and performance.

At the same time, Furniture should receive a deeper profitability review rather than simply being evaluated based on its strong sales volume.

---

## Overall Business Takeaway

The most important conclusion from the analysis is:

> **The business should not evaluate performance based on sales alone.**

The dashboard shows a clear difference between **where the company generates revenue and where it generates profit**.

Technology is a strong example: it produces only about one-third of sales but more than half of profit. Furniture presents the opposite situation, generating almost one-third of sales while contributing only a small fraction of profit.

Similarly, the West region leads in both sales and profit, while Central produces significant sales but comparatively weak profit.

### Recommended Priority

The analysis suggests that management should shift its focus from simply increasing sales toward **understanding and improving the profitability of existing sales**.

---

# Stakeholders

The dashboard was designed to provide different stakeholders with a consolidated view of sales and profitability performance.

### Sales Management

Can use the dashboard to monitor:

- Overall sales performance
- Monthly sales trends
- Regional performance
- Category and sub-category performance
- Customer segment contribution

### Finance Team

Can use the analysis to:

- Monitor profitability
- Compare revenue and profit contribution
- Identify categories with weak profitability
- Investigate regional differences in profit performance

### Regional Managers

Can use the regional analysis to:

- Compare sales performance across regions
- Monitor regional profitability
- Identify underperforming areas
- Investigate differences in product and customer mix

### Product & Category Managers

Can use the category and sub-category analysis to:

- Identify high-performing products
- Compare category revenue and profitability
- Investigate products contributing strongly to sales
- Identify categories requiring further profitability analysis

### Senior Management

Can use the executive dashboard to obtain a high-level overview of:

- Revenue
- Profit
- Quantity Sold
- Average Order Value
- Regional performance
- Category performance
- Customer contribution

The dashboard provides a starting point for identifying areas that require deeper investigation and supporting data-informed decision-making.

---

# Limitations

Although the analysis provides useful insights into sales and profitability, several limitations should be considered.

### 1. Sample Dataset

The analysis uses the **Sample Superstore dataset obtained from Kaggle**.

The dataset is intended primarily for analytics practice and therefore does not represent a complete picture of a real company's operations.

### 2. Limited Business Context

The dataset contains transaction-level sales information but does not provide several factors that could influence business performance, such as:

- Marketing expenditure
- Supplier costs
- Employee costs
- Inventory levels
- Customer acquisition costs
- Competitor pricing
- Operating expenses

As a result, the analysis focuses primarily on **sales and transaction-level profitability** rather than overall business profitability.

### 3. Historical Analysis

The analysis covers transactions from **2014 to 2017**.

The identified trends describe historical performance and should not automatically be interpreted as forecasts of future performance.

Further analysis using more recent data would be required before making current business decisions.

### 4. Limited Explanation of Causality

The dashboard identifies relationships and patterns within the data but does not necessarily explain why those patterns occurred.

For example, the analysis identifies Furniture as a category with relatively low profit contribution, but the available data does not by itself establish whether pricing, discounting, product costs, or another factor is responsible.

These areas therefore require further investigation before specific corrective actions are implemented.

### 5. Customer Activity and Churn Definition

The analysis extends beyond customer-level sales by using transaction history to evaluate customer activity. Metrics such as first and last order dates, days since last order, purchase frequency, consecutive years of activity, and average days between orders were used to segment customers based on their observed purchasing behavior.

However, the dataset does not contain an explicit customer churn indicator, customer acquisition cost, marketing interactions, or customer lifetime value information.

Therefore, customer categories such as **New, Lapsed, Retained, Regular, and Potential** are analytical classifications based on the criteria defined for this project rather than confirmed business classifications.

A more comprehensive customer retention analysis would require additional customer lifecycle and behavioral data.

---

# Conclusion

This project transformed **9,994 transaction records covering 2014–2017** into an interactive Excel dashboard for analyzing sales and profitability performance.

The analysis found that the business generated **$2.30M in sales and $286.41K in profit**, but performance varies considerably across categories, regions, customers, and time.

The most significant finding is that **sales contribution does not necessarily correspond to profit contribution**.

Technology generated **36.4% of sales but 50.79% of profit**, while Furniture generated **32.3% of sales but only 6.45% of profit**.

Similarly, the West region led both sales and profit, while Central generated substantial sales but comparatively weak profit.

These findings demonstrate why business performance should be evaluated using **multiple KPIs rather than sales alone**.

The analysis therefore recommends that management focus on **understanding the drivers of profitability**, particularly within Furniture and the Central region, while protecting the performance of high-profit categories such as Technology.

Overall, the project demonstrates how **Excel, Power Query, PivotTables, PivotCharts, and interactive dashboards** can be used to transform raw transaction data into a structured analysis that supports business decision-making.

> **The goal is not simply to know how much the business sells, but to understand where its revenue comes from, where its profit comes from, and where further investigation is needed.**
