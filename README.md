# Online-Retail-Customer-Segmentation-RFM
End-to-End Customer Analytics project using SQL, Python (K-Means), and Power BI to segment online retail customers and predict churn.
# Online Retail Customer Segmentation & Churn Prediction Dashboard

## Project Overview
This project provides an end-to-end analysis solution for an online retail business to segment its customers based on their purchasing behavior. By understanding customer segments, the business can tailor marketing strategies, improve customer retention, and optimize revenue.

This dashboard identifies 4 distinct customer segments: **Best Customers**, **At Risk (Churn Danger)**, **Loyal Customers**, and **New / Low Spenders**.

## Data Source
*   The original dataset used is the [Online Retail II dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II) from the UCI Machine Learning Repository.
*   The raw data was processed to generate actionable metrics.

## Tech Stack & Workflow

### Phase 1: Data Acquisition & Preprocessing (SQL)
*   Used **MySQL** to clean and prepare the raw transactional data.
*   Calculated key performance indicators (KPIs) and prepared the base for RFM analysis.
*   **📂 File:** [`sql/Online_Retail_RFM_Queries.sql`](sql/Online_Retail_RFM_Queries.sql)

### Phase 2: Feature Engineering & Churn Tagging (SQL)
*   Engineered **RFM (Recency, Frequency, Monetary)** scoring using advanced SQL window functions.
*   Implemented logic to tag customers as "Churned" based on inactivity periods.
*   **📂 File:** Same as Phase 1.

### Phase 3: Exploratory Data Analysis & Clean-up (Python)
*   Used **Python** and **Pandas** to explore the data distribution.
*   Removed outliers and standardized features.
*   **📂 File:** [`python/Customer_Segmentation_Notebook.ipynb`](python/Customer_Segmentation_Notebook.ipynb)

### Phase 4: Machine Learning - K-Means Clustering (Python)
*   Applied the **K-Means Clustering** algorithm (Scikit-Learn).
*   Selected the optimal number of clusters (4).
*   Assigned human-readable labels to each segment (e.g., "Best Customer").
*   **📂 File:** Same as Phase 3.

### Phase 5: Power BI Dashboarding
*   Integrated the output from Python (`final_customer_analytics.csv`) into **Power BI**.
*   Built an interactive executive dashboard visualizing:
    *   Total Customers (362)
    *   Segment Distribution (Bar Chart)
    *   Revenue vs. Recency by Segment (Scatter Chart)
    *   Interactive filtering based on segments.
*   **📂 Files:**
    *   [`power_bi/Customer_Intelligence_Dashboard.pbix`](power_bi/Customer_Intelligence_Dashboard.pbix)
    *   [`power_bi/dashboard_screenshot.png`](power_bi/dashboard_screenshot.png)

## Dashboard Screenshot
![Dashboard Screenshot](power_bi/dashboard_screenshot.png)

## Key Insights
1.  **High-Risk Segment:** The "At Risk" segment (blue on the scatter chart) has high monetary value but hasn't purchased recently. This is a critical area for immediate re-engagement campaigns.
2.  **Loyal Customers:** The "Loyal Customers" are a strong asset with high frequency.
3.  **New / Low Spenders:** These need targeted offers to increase their spend.

## How to Run This Project
1.  Clone the repository.
2.  Run the SQL script to create and process the data.
3.  Execute the Python notebook to perform the clustering.
4.  Open the Power BI file and refresh the data connection.

## Future Improvements
*   Implement automatic churn prediction model.
*   Add time-series analysis for segment migration.
