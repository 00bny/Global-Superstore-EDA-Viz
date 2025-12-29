# Global Superstore Performance Analytics

[![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=flat&logo=pandas)](https://pandas.pydata.org/)
[![Tableau](https://img.shields.io/badge/Tableau-Visualization-E97627?style=flat&logo=tableau)](https://public.tableau.com/)
[![Notion](https://img.shields.io/badge/Notion-Full_Report-000000?style=flat&logo=notion)](https://www.notion.so/EDA-Visualization-Project-Global-Superstore-2cb3e65290b9805d9205c6cff0104212)

## 📖 Executive Summary
This project delivers an end-to-end business intelligence solution for **Global Superstore**, a large-scale retail dataset. The objective was to transform raw transaction data into actionable strategies regarding sales performance, profitability, and supply chain efficiency.

By leveraging **Python for comprehensive data preparation (Cleaning, Feature Engineering, EDA) and Tableau for interactive storytelling**, this project identifies key drivers of profit and potential revenue leakages (e.g., excessive discounts or high shipping costs).

## 🔗 Project Deliverables
- **📊 Interactive Dashboard (Tableau):** [View Live Dashboard](https://public.tableau.com/views/GlobalSuperstorePerformanceAnalyticsExecutiveProductCustomer/Dashboard1ExecutivePerf_?:language=th-TH&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
- **📝 Strategic Insight Report (Notion):** [Read Full Analysis](https://www.notion.so/EDA-Visualization-Project-Global-Superstore-2cb3e65290b9805d9205c6cff0104212)

## 🔍 Business Problem & Objectives
The Global Superstore needed a clear view of its operations to answer critical business questions:
1.  **Profitability:** Which products and regions are driving profit, and where are margins slipping?
2.  **Customer Behavior:** Who are the high-value customers, and how does segmentation affect buying patterns?
3.  **Operational Efficiency:** How does shipping mode impact delivery times and costs?

## 📈 Dashboard Overview
The Tableau solution is divided into three analytical views to serve different stakeholders:

### 1. Executive Performance View (Overview)
*Target Audience: Senior Management*
- **Key Features:** High-level KPIs (Total Sales, Total Profit, Profit Margin, YoY Growth).
- **Function:** Provides a snapshot of business health, tracking monthly trends to identify seasonality and overall growth trajectory.
<img width="1262" height="813" alt="Screenshot 2568-12-29 at 17 26 56" src="https://github.com/user-attachments/assets/3cc4d1c3-ae51-42b0-893f-0d88fc138e9f" />

### 2. Product & Sales Intelligence
*Target Audience: Sales Managers & Marketing*
- **Key Features:** Granular analysis of Categories and Sub-Categories. Includes a scatter plot analyzing the correlation between **Discount** and **Profit**.
- **Function:** Identifies "Loss Leaders" (high sales, negative profit) and determines optimal discount strategies to prevent margin erosion.
<img width="1262" height="813" alt="Product   Sales Intelligence" src="https://github.com/user-attachments/assets/82cee426-a3af-4457-9bb9-2e5c1c523fd8" />

### 3. Customer & Shipping Analytics
*Target Audience: Operations & Logistics Team*
- **Key Features:** Customer segmentation analysis, Top 10 High-Value Customers, and Shipping Mode performance (Cost vs. Speed).
- **Function:** Optimizes logistics by highlighting expensive shipping routes and analyzes customer retention through purchasing frequency.
<img width="1262" height="813" alt="Customer   Shipping Analytics" src="https://github.com/user-attachments/assets/034f3e13-500e-483c-9562-e3879deed7df" />

## 💡 Key Insights & Strategic Recommendations
Based on the data analysis, the following actionable insights were derived:

### 1. The "Discount Trap"
- **Observation:** Several sub-categories (e.g., Tables) show high sales volume but negative profit margins due to excessive discounting (>30%).
- **Recommendation:** **Restructure the discounting policy.** Implement a "Discount Threshold" alert system to prevent discounts from eroding the entire profit margin on low-margin goods.

### 2. Seasonal Peaks
- **Observation:** Sales consistently peak in Q4 (Nov-Dec), following a typical retail seasonality pattern.
- **Recommendation:** **Optimize Inventory for Q4.** Increase stock levels for high-performing categories (Technology) in Q3 to prevent stockouts during the peak season.

### 3. Shipping Inefficiencies
- **Observation:** Certain regions incur disproportionately high shipping costs when using "Same Day" delivery, without significantly increasing order value.
- **Recommendation:** **Review Logistics Contracts.** Encourage customers to choose "Standard Class" by offering incentives, or renegotiate rates for express shipping in high-cost regions.

## 🛠️ Technical Workflow

### Step 1: Data Cleaning & Feature Engineering
*Notebook: `data_cleaning_and_feature_engineering.ipynb`*
- **Data Validation:** Handled missing values and standardized data types (Date parsing, Numeric conversion).
- **Feature Creation:**
    - `ShipDays`: Calculated delivery duration (`Ship Date` - `Order Date`).
    - `ProfitMargin`: Calculated profitability ratio (`Profit` / `Sales`).
    - `Order_Year/Month`: Extracted for time-series aggregation.
- **Export:** Generated `Global_Superstore_Cleaned.csv` for optimized Tableau performance.

### Step 2: Exploratory Data Analysis (EDA)
*Notebook: `EDA.ipynb`*
- Conducted statistical analysis using **Pandas** and **Matplotlib**.
- Analyzed distributions of `ShipDays` and identified outliers in `Sales`.
- Segmented data by Region and Category to find preliminary patterns before visualization.

### Step 3: Dashboard Implementation
- Designed the layout in **Tableau** focusing on User Experience (UX).
- Implemented dynamic filters (Year, Region, Category) to allow users to drill down into the data.

## 📂 File Structure

| File Name | Description |
| :--- | :--- |
| `data_cleaning_and_feature_engineering.ipynb` | Notebook for data cleaning and feature extraction. |
| `EDA.ipynb` | Notebook for exploratory data analysis and statistical summaries. |
| `Global_Superstore_Cleaned.csv` | Processed dataset ready for analysis. |
| `README.md` | Project documentation. |

## 💻 Tech Stack
- **Language**: Python
- **Libraries**: Pandas, NumPy, Matplotlib
- **BI Tool**: Tableau
- **Documentation**: Notion

## 👤 Author
Benyapa Prakunhungsit
