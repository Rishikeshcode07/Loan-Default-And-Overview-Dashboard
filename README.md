# Loan Default Risk & Borrower Profile Dashboard

### Dashboard Link : [https://app.powerbi.com/groups/me/reports/your-custom-report-url-here](https://app.powerbi.com/groups/me/reports/95ef714f-1d25-4fb9-b8d5-998a410d1189/95bbb9c9f6b118039b94?experience=power-bi)

## Situation (Problem Statement)

Financial institutions and lending businesses face a critical risk vector: borrower defaults. Managing a multi-billion dollar loan portfolio requires an accurate, granular comprehension of borrower profiles, credit behaviors, and microeconomic dependencies. Traditionally, risk assessment models evaluate applications using standalone data metrics (like a static credit score or individual income brackets) in isolation. 

However, evaluating risk without a unified platform leads to severe informational gaps. Risk managers struggle to quickly answer complex queries, such as: 
* How does the default rate trend over multiple years alongside macroscopic shifts in general loan amounts?
* Do specific combinations of demographics (like age bracket combined with mortgage status and dependents) yield significantly higher defaults?
* Which loan purposes exhibit the highest baseline loss metrics?

Without a centralized, multi-dimensional business intelligence platform, lenders face unexpected credit defaults, unoptimized capital allocations, and an inability to dynamically adjust lending criteria to shifting risk profiles.

## Task

The core objective of this project was to architect and build a robust, multi-page Power BI environment serving as a **Credit Risk and Demographics Command Center**. The project focused on three key analytical pillars:
1.  **Loan Default & Macro Overview:** Map out baseline metrics across loan purposes, employment categories, age bands, and multi-year historical default cycles.
2.  **Applicant Demographics & Financial Profiles:** Intersect credit risk categories with education levels, marital status, dependent status, and active property mortgages.
3.  **Advanced Financial Risk Metrics:** Calculate and visualize highly sensitive dynamic indicators, including Year-over-Year (YoY) shifts in loan volumes, YoY growth in defaults, and multi-layered decomposition of overall funding allocation.

The end-product is designed to give executive leadership and senior risk analysts an immediate, interactive window into portfolio exposure, helping optimize credit screening rules and mitigate balance-sheet losses.

## Action (Steps Followed)

The execution phase was structurally segmented across data normalization, modeling, and deep visual engineering.

### Page 1: Data Architecture & Portfolio Overviews

![image alt](https://github.com/user-attachments/assets/7612d4c6-ed7c-4b6b-87a8-7dc9e1715138)

*   **Step 1:** Ingested the master dataset into Power BI Desktop, configuring column distribution profiling against the complete dataset via Power Query to minimize anomalous strings or missing default indicators.
*   **Step 2:** Formatted and engineered the historical timeline fields to support robust multi-year analytical trend lines (covering the historical timeframe from 2013 to 2018).
*   **Step 3:** Built a step-down area chart titled **"Loan Amount by Purpose"** to visually rank the massive capital deployment across Home, Business, Education, Auto, and Other sectors.
*   **Step 4:** Engineered a custom distribution step-chart showing **"Average Income by Employment ID"** to map the economic variance between Full-time, Self-employed, Part-time, and Unemployed groups.
*   **Step 5:** Built a step-down default matrix titled **"Default Rate (%) by Employment Type"** to visually highlight how credit loss cascades based on a borrower's employment standing.
*   **Step 6:** Developed custom time-series area charts to plot **"Average Loan Amount by Age Group"** (Adults, Middle Age Adults, Senior Citizens) alongside the dynamic **"Default Rate (%) by Year"** timeline.

### Page 2: Demographic & Credit Slicing

![image alt](https://github.com/user-attachments/assets/9abb55f7-f624-425d-bf40-9b5b2f578685)

*   **Step 7:** Dedicated a second reporting interface explicitly to borrower profiles. Created an area chart titled **"Median Loan Amount by Credit Score Category"** ranging from Low to High indicators.
*   **Step 8:** Formulated a multi-tiered Donut Chart tracking **"Average Loan Amt (High Credit) by Age Groups and Marital Status"**, parsing capital allocation among cross-sections of Adults, Middle Age Adults, and Senior Citizens.
*   **Step 9:** Designed a localized trend chart mapping **"Total Loan (Adults) by Credit Score Bins"** to observe credit tier concentration among the younger borrower demographic.
*   **Step 10:** Constructed a comparative multi-bar chart titled **"Loan (Middle Age Adults) by Have Mortgage/Dependents"** that splits volume according to boolean factors (`True`/`False` for Dependents).
*   **Step 11:** Plotted a clean step-down area chart titled **"Number of Loans by Education Type"** to categorize borrower distribution by their highest completed academic level.

### Page 3: Advanced Risk & Decomposition Analytics

![image alt](https://github.com/user-attachments/assets/8f25f26a-ba77-485a-9b33-62b9c01eb5eb)

*   **Step 12:** Implemented advanced time-intelligence calculations to plot **"YoY Loan Amount Change by Year"** and **"YoY Default Loans Changes by Year"**, providing explicit velocity metrics on how fast portfolio exposure is moving.
*   **Step 13:** Created an advanced visual matrix tracking **"YoY Loan Amount by Credit Score Bins and Marital Status"**, tracing capital fluctuations across cross-sections of Divorced, Married, and Single individuals.
*   **Step 14:** Configured an interactive **Decomposition Tree** tracking the **"Sum of Loan Amount"**, enabling deep drill-down actions from broader Income Brackets (High, Medium, Low Income) directly down into specific Employment Types (Full-time, Part-time, Self-employed).

## Result (Insights & Data Inferences)

The finalized dashboard delivers rich, multi-layered data insights across your portfolio's performance:

### [1] Portfolio Allocations & Baseline Inferences
*   **Core Capital Drivers:** Loan volume is heavily front-loaded into foundational assets. "Home" loans represent the largest share of the portfolio at **6,545M**, closely followed by "Business" ventures at **6,522M** and "Education" at **6,511M**.
*   **Income Dynamics:** Full-time professionals maintain the highest average income baseline at **82,890**, outperforming the self-employed tier (**82,447**) and part-time staff (**82,389**).
*   **The Academic Split:** Borrowers holding a Bachelor's degree represent the largest segment by volume with **64,366 active loans**, continuously scaling down through High School (**63,903**), Master's (**63,541**), and PhD candidates (**63,537**).

### [2] Critical Risk & Default Correlations
*   **Employment Risk Correlation:** There is an inverse relationship between career stability and default velocity. Unemployed borrowers display the highest default rate at **3.4%**, which decreases to **3.0%** for Part-time workers, **2.9%** for Self-employed individuals, and a portfolio low of **2.4%** for Full-time employees.
*   **Age and Exposure Matrix:** Younger borrowers ("Adults") hold a significantly larger financial weight per loan, maintaining a high average loan amount baseline of **127,789**, which smoothly tapers off down to **127,459** for Middle Age Adults and drops to **127,355** for Senior Citizens.

### [3] Credit Tier and Demographics Slicing
*   **Credit Tier Disparities:** The median loan amount for "Low" credit score tiers sits high at **128,397**, whereas premium "High" credit tier applicants maintain a more conservative median loan footprint of **127,149**.
*   **Socio-Demographic Balance:** Middle-aged adults display remarkably uniform credit consumption. Whether evaluating those with active mortgages and dependents or those without, capital distribution stands firmly stabilized at a balanced **3.1bn** across all standard household structures.

### [4] Historical YoY Trends & Portfolio Volatility
*   **Historical Cyclicality:** The portfolio experienced an extended, severe macroeconomic default wave. Default rates surged from a historic low of **11.50%** in 2014, climbing up to an extreme peak of **11.70% (2015)** and **11.75% (2016)**, before correcting back down to **11.50% in 2017** and slightly rebounding to **11.60% by 2018**.
*   **YoY Momentum Swings:** Portfolio expansion experienced severe volatility. YoY Loan Amount changes plummeted to a negative growth rate of **-1.53072** in 2014 before radically spiking to a positive expansion of **1.30071** in 2015. Concurrently, YoY Default growth rates tracked this shift, hitting a massive contraction of **-2.6** in 2014 before accelerating sharply into positive default growth of **2.7** by 2015.
*   **Portfolio Tree Decomposition:** Out of a massive global portfolio footprint (**Sum of Loan Amount = 325.79bn**), the High Income bracket commands the lion's share at **217.32bn**. Drill-down analysis shows this segment is primarily driven by Full-time high earners, who account for **54.44bn** of that total allocation.

## Future Enhancements

To further advance the analytical capabilities of this reporting ecosystem, subsequent iterations will focus on:
*   **Predictive Machine Learning Integration:** Deploying a binary classification model (such as logistic regression or random forests) inside Power BI to assign a predictive "Default Probability Score" to new applicants during ingestion.
*   **LGD & EAD Modeling:** Expanding basic default tracking into advanced metrics, including Loss Given Default (LGD) and Exposure at Default (EAD), to calculate true monetary risk buffers.
*   **Dynamic Scenario Slicers:** Integrating What-If parameter sliders to simulate how a 1% or 2% shift in structural unemployment might impact total portfolio default rates and corporate cash flows.

## How to Interact

*   **Multi-Page Navigation:** Use the tab panels to toggle seamlessly between the primary *Loan Default Overview*, *Applicant Demographics Profile*, and *Financial Risk Metrics* pages.
*   **Decomposition Exploration:** On the Financial Risk tab, expand or collapse the blue node indicators on the Income Bracket tree to view real-time calculations across various employment tiers.
*   **Interactive Tooltips:** Hover your cursor over any interactive data point on the multi-year timeline curves to see exact growth indicators across specific reporting years.
