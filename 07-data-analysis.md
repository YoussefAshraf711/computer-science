[العربي](./07-data-analysis_ar.md)

# <a name="-7-data-analysis"></a>📈 Chapter 7: Data Analysis

## 1. What is it?

Data Analysis is the process of inspecting, cleaning, transforming, and modeling data with the goal of discovering useful information, drawing conclusions, and supporting decision-making. This discipline primarily answers two questions: "What happened?" and "Why did it happen?".

If the data engineer builds the data highways, and the data scientist predicts the future, the data analyst is the "detective" who studies the evidence (current and historical data) to understand what happened and present a clear report to management.

## 2. What does the specialist do?

A data analyst is the bridge between raw data and business leaders. Their daily tasks include:
 * Understanding business requirements: Sitting with different departments (like marketing, sales) to understand what they need to know from the data.
 * Querying and collecting data: Writing complex SQL queries to pull the required data from databases and data warehouses.
 * Cleaning and preparing data: Dealing with missing data, errors, and inconsistent formats to make it ready for analysis.
 * Statistical analysis: Applying basic statistical concepts to discover trends, patterns, and correlations in the data.
 * Data Visualization: Creating clear and attractive charts and graphs to present the findings.
 * Building reports and dashboards: Assembling charts and key performance indicators into an interactive dashboard to help management track performance and make decisions.

## 3. Sub-domains

 * Business Intelligence Analyst: Focuses heavily on building and maintaining interactive dashboards to monitor company performance.
 * Product Analyst: Analyzes user behavior within a digital product (app or website) to understand how it's used and provide recommendations for improvement.
 * Marketing Analyst: Analyzes the performance of marketing campaigns, customer behavior, and market trends.
 * Financial Analyst: Analyzes the company's financial data to support investment and budget decisions.

## 4. Expanded Key Concepts

 * Types of Analysis:
     * `Descriptive Analytics`: Describes what happened in the past (e.g., "Our total sales were $1 million last month").
     * `Diagnostic Analytics`: Investigates why something happened (e.g., "Sales decreased because a competitor launched a new product").
 * `KPI (Key Performance Indicator)`: A measurable value that demonstrates how effectively a company is achieving key business objectives (e.g., customer retention rate).
 * `Metric`: A specific measurement to track a particular aspect of performance (e.g., daily website visitors).
 * `Data Visualization`: The graphical representation of information. Using charts, graphs, and maps to see and understand trends, outliers, and patterns in data.
 * `Dashboard`: A dashboard that combines several visualizations and KPIs on a single screen to provide a comprehensive and quick overview.
 * `SQL`: Structured Query Language, the primary tool for a data analyst to pull data from relational databases.
 * Statistical Concepts: Mean, Median, Standard Deviation, and Correlation.

## 5. Expanded Tools & Technologies

 * Business Intelligence and Visualization Tools: Tableau, Microsoft Power BI, Looker.
 * Spreadsheet Software: Microsoft Excel, Google Sheets (indispensable for quick analyses and ad-hoc tasks).
 * Query Language: SQL (in-depth).
 * Programming Languages (for advanced analysis): Python (with Pandas, NumPy, Matplotlib, Seaborn libraries), R.
 * Data Sources: They connect to various databases like PostgreSQL, MySQL and data warehouses like BigQuery, Snowflake.

## 6. In-Depth Workflow

Project: The marketing team wants to understand the performance of their latest email campaign.

 1. Scoping Questions: The analyst sits with the marketing team. The main questions are: What is the open rate? What is the click-through rate (CTR)? Did the campaign lead to an increase in sales? Which customer segment was most engaged?
 2. Data Collection: The analyst writes SQL queries to pull data from multiple sources in the company's data warehouse:
     * From the marketing tool's database: A table containing every email sent, who opened it, and who clicked a link.
     * From the sales database: A table with all transactions, including timestamp and user ID.
 3. Data Cleaning and Preparation: The analyst joins the two tables using `user_id`. They might find inconsistent data (like different email formats) and clean it. They calculate new metrics, like CTR = (Total Clicks / Total Emails Sent) * 100.
 4. Analysis:
     * They calculate the overall open rate and CTR.
     * They analyze sales data for the week following the campaign and compare it to the week before to see if there was a "lift" in sales.
     * They segment the results by customer demographics (age, location) to see which group was most engaged.
 5. Visualization and Reporting: The analyst uses Tableau to create a dashboard:
     * KPI cards showing key metrics (open rate, CTR, sales lift).
     * A bar chart showing the CTR for different customer segments.
     * A time-series chart showing sales before, during, and after the campaign.
 6. Communicating Results: The analyst presents the dashboard to the marketing team, concluding that: "The campaign achieved a 25% open rate and a 5% CTR, leading to a 10% increase in sales. The highest engagement was from the 25-35 age group in urban areas."

## 7. Common Job Roles

 * Data Analyst
 * Business Intelligence (BI) Analyst
 * Marketing Analyst
 * Financial Analyst
 * Product Analyst

## 8. A-Z Glossary
<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`A/B Testing`** | Testing two different versions of something (like a webpage) to see which one performs better. |
| **`Ad-hoc Analysis`** | A one-time analysis performed to answer a specific, sudden business question. |
| **`Aggregation`** | Grouping data, such as calculating the SUM or AVG of a set of rows. |
| **`BI`** | Business Intelligence, refers to the technologies and applications for collecting and analyzing business data. |
| **`Churn Rate`** | The percentage of customers who stopped using a service during a specific period. |
| **`Cohort Analysis`** | Analyzing the behavior of a group of users who share a common characteristic over time. |
| **`Conversion Rate`** | The percentage of users who completed a desired goal (like a purchase or registration). |
| **`Correlation`** | A statistical measure that shows how two variables are related to each other. |
| **`CTR`** | Click-Through Rate, the ratio of clicks to the number of impressions. |
| **`Dashboard`** | A dashboard that visually displays key metrics and visualizations. |
| **`Data Mining`** | The process of discovering patterns in large data sets. |
| **`Funnel Analysis`** | Visualizing and tracking the steps users go through to complete a specific goal. |
| **`Join`** | An operation in `SQL` to combine rows from two or more tables based on a related column. |
| **`KPI`** | Key Performance Indicator, a vital metric for tracking business goals. |
| **`LTV (Lifetime Value)`** | The total expected revenue from a single customer throughout their relationship with the company. |
| **`Segmentation`** | Dividing a customer base into groups based on shared characteristics. |
| **`SQL`** | Structured Query Language, the primary language for talking to relational databases. |
| **`Time Series Analysis`** | Analyzing data points collected at successive time intervals. |

</details>

[⬆️ Back to Table of Contents](README.md)