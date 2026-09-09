# E-Commerce Customer Funnel & Revenue Analytics

## Project Overview

This project analyzes e-commerce customer behavior using **SQL and Google BigQuery** to understand how users move through the purchase journey, identify conversion drop-offs, evaluate traffic source performance, and analyze revenue metrics.

The analysis follows the customer journey from initial website interaction to purchase and presents the findings through an interactive analytics dashboard.

The project demonstrates practical data analytics skills including **SQL querying, Common Table Expressions (CTEs), customer funnel analysis, conversion analysis, revenue analysis, customer journey analysis, and data visualization**.

---

## Business Objective

The objective of this project is to answer key business questions such as:

- How many users move through each stage of the purchase funnel?
- At which stage do the most customers drop off?
- What are the conversion rates between funnel stages?
- Which traffic sources bring the most users?
- Which traffic sources generate the most purchases and revenue?
- What is the overall conversion rate from visitor to buyer?
- How much revenue is generated from purchases?
- How long does it take customers to move through the purchase journey?

---

## Customer Funnel

The customer journey was analyzed across the following stages:

```text
Page View
    ↓
Add to Cart
    ↓
Checkout Start
    ↓
Payment Info
    ↓
Purchase
```
## Dataset

The project uses an event-level e-commerce dataset containing customer interactions.
- user_id:	Unique identifier for each user
- event_id:	Unique identifier for each event
- event_date:	Date and time of the customer event
- event_type:	Type of customer interaction
- product_id:	Product associated with the event
- traffic_source:	Source through which the customer arrived
- amount:	Transaction amount associated with purchases

## Analysis Performed
1. Customer Funnel Analysis

Analyzed the number of distinct users progressing through each stage of the e-commerce funnel:
Page Views,
Add to Cart,
Checkout Start,
Payment Info,
Purchases

This analysis helps identify where users drop off before completing a purchase.

2. Conversion Rate Analysis

Calculated conversion rates between each stage of the customer funnel:

View → Cart Conversion Rate
Cart → Checkout Conversion Rate
Checkout → Payment Conversion Rate
Payment → Purchase Conversion Rate
Overall View → Purchase Conversion Rate

Example calculation:

ROUND(stage2_cart * 100 / stage1_views) AS views_to_cart_rate
3. Traffic Source Analysis

Compared different traffic sources based on customer activity and conversion performance.

Metrics analyzed include:

Number of Visitors,
Add to Cart Activity,
Purchases,
Conversion Rates,
Revenue Performance

This helps determine which acquisition channels are driving valuable customer activity.

4. Customer Journey Analysis

Used SQL to analyze the time taken by customers to progress through different stages of their journey.
The analysis includes:
- Time from Page View to Add to Cart
- Time from Add to Cart to Purchase
- Total Customer Journey Time
- Number of Converted Users

SQL functions such as MIN(), TIMESTAMP_DIFF(), and conditional aggregation were used to track customer progression.

5. Revenue Analysis

Calculated important revenue and business performance metrics including:

Total Visitors
Total Buyers
Total Orders
Total Revenue
Average Order Value
Revenue per Buyer
Revenue per Visitor

## Dashboard

The analysis was visualized through an e-commerce analytics dashboard.

The dashboard includes:

Key Performance Indicators
Total Visitors
Total Buyers
Total Orders
Total Revenue
Average Order Value
Overall Conversion Rate
Visualizations
Customer Funnel Analysis
Funnel Conversion Rates
Traffic Source Performance
Revenue by Traffic Source
Revenue Trends
Customer Journey Analysis

## Tools & Technologies
- SQL — Data querying and analysis
- Google BigQuery — Cloud data warehouse and SQL execution
- Julius AI — Dashboard creation and data visualization
- GitHub — Project documentation and version control

  
## Key Skills Demonstrated
SQL Querying
Data Analysis
Customer Funnel Analysis
Conversion Rate Analysis
Revenue Analysis
Customer Journey Analysis
Traffic Source Analysis
Common Table Expressions (CTEs)
Conditional Aggregation
Data Visualization
Business Insights
Key Business Questions Answered

## This project helps answer questions such as:

How many users reach each stage of the purchase funnel?
Where is the largest customer drop-off?
What percentage of visitors eventually make a purchase?
Which traffic source brings the most users?
Which traffic source generates the highest number of purchases?
Which channels generate the most revenue?
What is the average order value?
How long does the average customer journey take?
Future Improvements

## Potential improvements to this project include:

Adding product-level performance analysis
Creating cohort analysis for customer retention
Adding repeat purchase analysis
Performing customer segmentation
Creating automated data refresh pipelines
Connecting the dashboard directly to BigQuery
Adding advanced time-series analysis
Comparing performance across different time periods
