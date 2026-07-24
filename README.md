# FinSight: Finance Analytics Dashboard

## Project Overview
A financial organization required a centralized analytical solution to monitor overall financial transactions, customer behavior, and transaction performance across different business segments. The objective of this interactive Power BI dashboard is to help stakeholders monitor KPIs in real time, identify high-performing customer segments, and track operational fees and taxes to improve financial decision-making.

![Main Dashboard](Preview_Dashboard/Overview_Analysis.png)

## Key Financial Metrics (KPIs)
* **Total Amount:** Displays the total transaction amount processed with a Year-over-Year (YoY) growth comparison.
* **Total Transactions:** Tracks the overall transaction volume and yearly changes.
* **Average Transaction Value:** Calculates the average monetary amount per transaction.
* **Total Fees & Taxes:** Monitors total fees collected and total tax generated from all operations.

## Business Insights & Visualizations
* **Trend Analysis:** Analyzes monthly transaction amount trends to identify seasonal spikes or drops throughout the year.
* **Operational Efficiency:** Compares transaction amounts based on their status (Success, Failed, Pending) to measure the transaction success rate.
* **Customer Segmentation:** Evaluates the contribution of different customer groups (Retail, Premium, SME, Corporate, Wealth) to identify the most valuable segments.
* **Geographical Performance:** Compares state-wise transaction amounts to pinpoint top-performing regions.
* **Transaction Type Profitability:** Uses a detailed matrix to understand performance and profitability across various categories like Loan EMI, Bill Payment, and Investment.
* **Demographic Analysis:** Breaks down transaction amount contributions based on customer gender.

## Technical Implementation & Data Modeling

![Data Model](Preview_Dashboard/data_model.png)

* **Star Schema Design:** Architected a clean Star Schema connecting the central `finance_transactions` fact table to the `customers` and `Calendar Table` dimension tables via one-to-many relationships. This structured data model ensures efficient data retrieval and responsive dynamic filtering across the dashboard.
* **Custom Calendar Table:** Built a dedicated, continuous Date table to establish a solid foundation for Time Intelligence logic. This step was critical to bypass standard auto-date hierarchies, enabling accurate and lightweight calculations for all YoY performance metrics.
* **Data Transformation:** Cleaned and standardized the raw financial dataset in Power Query, ensuring consistent formatting for transaction statuses, categorical segments, and currency columns before loading them into the model.

## Interactive Features
* **Dynamic Filtering:** Allows users to dynamically slice data by Year, Dynamic Measure, Occupation, and Category for tailored business analysis.
* **Drill-Down Capabilities:** Includes a detailed grid view dashboard to inspect underlying transactional records at a granular level.

![Drill Down View](Preview_Dashboard/Transactions.png)
