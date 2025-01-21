# A/B Testing Analysis Project

## Table of Contents
- [Project Overview](#project-overview)
- [Tools and Technologies Used](#tools-and-technologies-used)
- [Metrics Analyzed](#metrics-analyzed)
- [SQL Code](#SQL-code)
- [Python Code](#python-code)
- [CSV File Format](#CSV-file-format)
- [Results and Recommendations](#results-and-recommendations)
- [Tableau Dashboard](#tableau-dashboard)
- [Database Model](#database-model)

---

## Project Overview
This project analyzes A/B testing results using statistical methods implemented in Python and visualizes key conversion metrics in a Tableau dashboard. The main goal was to identify the impact of changes on user behavior and conversion rates to inform business decisions. All results are publicly available on Tableau Public: [A/B Testing Dashboard](https://public.tableau.com/views/ABTests_17336680632730/ABtest?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).

---

## Tools and Technologies Used
- **Google BigQuery**: Used for data storage and querying using SQL.
- **Python in Google Colab**: Employed for statistical analysis and data processing using the following libraries:
  - `pandas`
  - `numpy`
  - `statsmodels.api`
  - `google.colab.drive`
- **Tableau**: Created an interactive dashboard to visualize the A/B test results.
- **CSV**: Results were saved in a structured CSV format for easy sharing and interpretation.

---

## Metrics Analyzed
We focused on the following conversion metrics:
1. Add Payment Info / Session
2. Add Shipping Info / Session
3. Begin Checkout / Session
4. New Accounts / Session

---

## SQL Code
The SQL code used for querying data from Google BigQuery is included in this repository under the `sql` folder.

---

## Python Code
The Python scripts, executed in Google Colab, included the following functionalities:
- Data retrieval using `pandas`.
- Statistical testing using `statsmodels.api`.
- Integration with Google Drive for file storage and management.

---

### CSV File Format
The processed results were saved in a CSV file with the following columns:
- **Test**: A/B test identifier.
- **Metric**: The metric being analyzed.
- **Numerator_1**: Count of events in Group 1.
- **Denominator_1**: Total sessions in Group 1.
- **Group1_Conversion_Rate**: Conversion rate for Group 1.
- **Numerator_2**: Count of events in Group 2.
- **Denominator_2**: Total sessions in Group 2.
- **Group2_Conversion_Rate**: Conversion rate for Group 2.
- **Metric Changes, %**: Percentage change between Group 1 and Group 2.
- **Z-Stat**: Z-statistic from the hypothesis test.
- **P-Value**: P-value indicating statistical significance.
- **Significant**: Whether the result is statistically significant (True/False).

---

## Results and Recommendations
1. **Test #1**:
   - **Significant Improvement**: Add Payment Info, Add Shipping Info, and Begin Checkout.
   - **No Significant Result**: New Accounts metric showed a slight decline.
   - **Recommendation**: Implement changes with caution and investigate the decline in New Accounts.

2. **Test #2**:
   - No statistically significant results for any metric.
   - **Recommendation**: Continue testing to gather more data.

3. **Test #3**:
   - **Significant Decline**: Begin Checkout metric.
   - **Recommendation**: Do not implement the changes.

4. **Test #4**:
   - **Significant Decline**: Begin Checkout and New Accounts metrics.
   - **No Significant Result**: Declines in Add Payment Info and Add Shipping Info metrics.
   - **Recommendation**: Retain the original version without the tested changes.

---

## Tableau Dashboard
The Tableau dashboard provides an interactive visualization of the A/B testing results, including metric performance and statistical significance. Explore the dashboard [here](https://public.tableau.com/views/ABTests_17336680632730/ABtest?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link).

--- 

## Database Model

The database model used in this project is provided as a PNG file. Refer to database_model.png for an overview of the data structure.

---
