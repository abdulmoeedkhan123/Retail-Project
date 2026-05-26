# Retail Analytics Project

## Overview

This project provides comprehensive customer analytics for retail operations using simulated retail customer data from Databricks. The analytics framework covers four critical business areas:

* **Retail Performance** - Overall business health and KPI tracking
* **Revenue Analysis** - Customer lifetime value and revenue concentration
* **Order Patterns** - Purchase frequency and order behavior analysis
* **Sales Behavior** - Product preferences and cross-selling opportunities

The project leverages Databricks AI/BI dashboards with metric views to deliver interactive, real-time insights into customer segmentation, purchasing patterns, and revenue drivers.

## Project Structure

```
Retail-Project/
├── README.md                          # Project documentation
├── Data/                              # Data storage folder
└── Retail Analytics Dashboard         # Multi-page interactive dashboard
```

## Dashboard

**[Retail Analytics Dashboard](#dashboard-01f1587a7b581be59c5c101b3cf85194)**

This interactive dashboard provides four specialized views for analyzing retail customer data:

### Page 1: Retail Analytics (Overview)

The main landing page provides high-level business intelligence:

* **Key Performance Indicators** - Revenue, orders, average order value, customer counts
* **Regional Sales Distribution** - Geographic performance breakdown
* **Sales Trends** - Time-series analysis of revenue and order patterns
* **Loyalty Segment Analysis** - Performance by customer tier

### Page 2: Revenue to Customer

Deep dive into customer value and revenue distribution:

* **Customer Lifetime Value (CLV)** - Individual customer value rankings with tenure analysis
* **Revenue by Segment** - Total revenue and customer distribution across loyalty tiers
* **Customer Revenue Trends** - Monthly revenue patterns and cumulative growth by segment
* **Revenue Concentration** - Pareto analysis showing top revenue contributors
* **Average Revenue Metrics** - Statistical analysis of revenue per customer by segment

### Page 3: Order to Customer

Analysis of purchasing frequency and order behavior:

* **Order Frequency Distribution** - How often customers place orders
* **Average Order Value (AOV)** - Order value analysis by segment and region with variance metrics
* **Customer Order Patterns** - Temporal patterns (day of week, day of month) by loyalty segment
* **Repeat Customer Metrics** - Retention rates and repeat purchase behavior
* **Order Size Distribution** - Distribution of order values across customer segments

### Page 4: Sales to Customer

Product-level insights and cross-selling opportunities:

* **Top Products by Segment** - Best-selling products for each loyalty tier
* **Product Category Preferences** - Category performance and revenue contribution by segment
* **Customer Purchase Patterns** - Product diversity and category breadth per customer
* **Category Mix Analysis** - Spending distribution across product categories
* **Cross-Sell Opportunities** - Product affinity and bundle recommendations

## Data Source

**Unity Catalog**: `databricks_simulated_retail_customer_data.v01`

### Tables

* **sales** - Transaction-level sales records with product, customer, and order details
* **customers** - Customer master data including demographics and loyalty status
* **sales_orders** - Order-level aggregations and summaries

### Data Characteristics

* **Customer Base**: 25 unique customers
* **Transaction Volume**: 360 total transactions
* **Total Revenue**: $2.7M
* **Time Period**: August 2, 2019 to February 28, 2020 (7 months)
* **Product Categories**: 6 distinct categories
* **Loyalty Segments**: 4 tiers (0 = basic, 3 = premium)

## How to Use

### Viewing the Dashboard

1. Click the [Retail Analytics Dashboard](#dashboard-01f1587a7b581be59c5c101b3cf85194) link above to open the dashboard
2. Navigate between pages using the page selector tabs at the top of the dashboard
3. Apply filters to drill down into specific segments, regions, or time periods
4. Hover over visualizations for detailed tooltips and data points
5. Click on chart elements to cross-filter related visualizations
6. Export data or visualizations using the menu options in each widget

### Working with the Data

The dashboard is powered by SQL-based metric view datasets that provide pre-aggregated, optimized calculations:

**Key Metrics Available**:

* **Revenue Metrics**: Lifetime value, average order value, revenue per order, cumulative revenue
* **Customer Metrics**: Active customers, repeat rate, purchase frequency, customer count
* **Product Metrics**: Purchase count, category revenue, affinity scores, revenue percentage

All metric calculations are performed using Databricks SQL and are refreshed automatically when the underlying data changes.

### Customization

To extend or modify the dashboard:

1. Open the [Retail Analytics Dashboard](#dashboard-01f1587a7b581be59c5c101b3cf85194) in edit mode
2. **Add New Widgets**: Use existing datasets or create new metric views from the source tables
3. **Modify Visualizations**: Change chart types, add filters, or adjust aggregation levels
4. **Create New Pages**: Add specialized views for specific business questions
5. **Configure Filters**: Set up dashboard-level or widget-level filters for dynamic analysis
6. **Schedule Refreshes**: Configure automatic data refresh schedules if using materialized datasets

## Genie Space (Optional)

For conversational analytics and ad-hoc exploration, you can create a Genie space connected to the retail data tables:

**To create a Genie space**:
1. Navigate to the Genie interface in Databricks
2. Connect to catalog `databricks_simulated_retail_customer_data` schema `v01`
3. Select tables: `sales`, `customers`, `sales_orders`

**Example questions to ask**:
* "What are my top 10 customers by total revenue?"
* "Show me monthly sales trends by loyalty segment"
* "Which product categories have the highest repeat purchase rates?"
* "What is the average order value for premium customers?"

## Additional Resources

* **Data Source**: Databricks Sample Data Marketplace - Retail Customer Data
* **Documentation**: [Databricks AI/BI Dashboards](https://docs.databricks.com/en/dashboards/index.html)
* **Metric Views**: [SQL Metric Views Guide](https://docs.databricks.com/en/sql/language-manual/sql-ref-syntax-ddl-create-metric-view.html)
* **Unity Catalog**: [Unity Catalog Documentation](https://docs.databricks.com/en/data-governance/unity-catalog/index.html)

## Notes

* All data is **simulated** and intended for demonstration and training purposes only
* Date range is limited to a **7-month period** (August 2019 - February 2020)
* Loyalty segments are encoded as integers: **0** (basic) to **3** (premium)
* Revenue and transaction metrics are aggregated at daily granularity
* Some aggregations may show zero values for sparse data combinations
* Customer IDs and names are synthetic and do not represent real individuals

---

**Last Updated**: May 27, 2026  
**Dashboard ID**: `01f1587a7b581be59c5c101b3cf85194`  
**Workspace**: Databricks  
**Catalog**: `databricks_simulated_retail_customer_data.v01`
