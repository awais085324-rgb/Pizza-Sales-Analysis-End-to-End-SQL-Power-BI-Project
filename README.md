# Precision Analytics: Solving Data Discrepancies in Pizza Retail Reporting
## 📌 Project Overview: Solving the "Trust Gap" in BI
In many business environments, stakeholders often hesitate to act on dashboard insights due to a lack of trust in the underlying data logic. A dashboard is only as good as the accuracy of its calculations.

**The Challenge:** 
The objective was to analyze 12 months of pizza sales data to identify growth opportunities. However, the primary challenge wasn't just visualizing the trends—it was ensuring absolute data integrity across the analytical pipeline.

**The Solution:**
I implemented a dual-validation framework. Before a single visualization was built in Power BI, I developed a comprehensive suite of SQL queries to extract and calculate every KPI manually. This created a "Source of Truth" ledger used to audit and cross-verify the DAX measures in the final dashboard.

## 🛠️ The Strategic Approach
**1. Identifying the Business Questions**

The business needed answers to three critical questions:

**Operational Efficiency:** When are the peak periods that require more staffing?

**Product Performance:** Which pizza categories drive the highest revenue vs. volume?

**Customer Behavior:** What is the average order value (AOV) and how can we increase it?

**2. The SQL Audit (Data Confirmation Layer)**

To solve the problem of potential calculation errors in the visualization layer, I wrote complex SQL scripts to define:

**Revenue Logic: **Validating total sales against quantity and unit price.

**Date Intelligence:** Using DATENAME and GROUP BY to isolate peak daily and monthly order volumes.

**Market Share:** Calculating the Percentage of Total Sales (PCT) per category using subqueries to ensure the math held up under various filters.

**3. Power BI Transformation (The Action Layer)**

Once the SQL results matched the raw data, I translated that logic into Power BI.

**Dynamic Filtering: **Allowed stakeholders to slice data by category and date.

**Visual Storytelling:** Transformed raw numbers into Daily/Monthly trend charts and Category Distribution maps.

## 📈 Impact & Results
By validating the data through SQL first:

Eliminated Discrepancies: Ensured 100% accuracy between the database and the executive report.

Actionable Insights: Identified that weekends (Fridays/Saturdays) and the month of July are peak performance periods, allowing for optimized inventory planning.

Menu Optimization: Highlighted underperforming pizza sizes and categories to inform future promotional strategies.
<img width="1446" height="818" alt="Screenshot 2026-05-14 084930" src="https://github.com/user-attachments/assets/fe0ebfd8-2158-47af-bfb5-b32c3eb5b255" />
