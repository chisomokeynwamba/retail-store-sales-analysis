# retail-store-sales-analysis
Retail Store Sales — Data Cleaning, EDA & Dashboard
Analyst: Chisom Okey-Nwamba
Tool: Microsoft Excel | Dataset: Kaggle — Retail Store Sales | Duration: 2 days

Project Overview
This project demonstrates an end-to-end data analytics workflow applied to a retail transactions dataset of 12,575 rows across 11 columns. The workflow covers data auditing, cleaning, exploratory analysis, and dashboard visualisation — following the same structured, evidence-based approach used in quantitative economic research.

Analyst Background
BSc Economics graduate with a Google Data Analytics Professional Certification and hands-on experience in business analysis and data-driven decision-making. Prior analytical work includes conducting time series studies and economic modelling using Eviews and statistical tools - covering stationarity testing, cointegration analysis,and long run forecasting to generate actionable business and financial insights.

Dataset
Detail	Value
Source	Kaggle — Retail Store Sales
Total Rows	12,575 transactions
Total Columns	11 (Transaction ID, Customer ID, Category, Item, Price Per Unit, Quantity, Total Spent, Payment Method, Location, Discount Applied, Date)
Categories	8 (Beverages, Butchers, Computers and electric accessories, Electric household essentials, Food, Furniture, Milk Products, Patisserie)
Sales Channels	Online and In-Store
Payment Methods	Cash, Digital Wallet, Credit Card

Phase 1 — Data Cleaning
Step	Action	Detail
1	File duplication	Raw file preserved untouched; all cleaning done on a separate working copy
2	Data inspection	COUNTBLANK audit across all 11 columns; ISNUMBER check on all numeric fields; Pivot Table audit of all categorical columns
3	Data type validation	All numeric columns confirmed as true numbers — no text-formatted values found
4	Categorical consistency	Category, Payment Method, and Location checked for casing/spacing inconsistencies via Pivot Table — all clean
5	Missing value treatment	4,485 blanks resolved: financial fields recalculated from mathematical relationships; Item blanks filled as Unknown; Discount Applied blanks filled as FALSE
6	Duplicate check	Data → Remove Duplicates by Transaction ID — 0 duplicates found

Missing Values Summary
Column	Blanks	Treatment
Item	95	Filled: Unknown (cannot be inferred from other columns)
Price Per Unit	47	Recalculated: Total Spent / Quantity
Quantity	48	Recalculated: Total Spent / Price Per Unit
Total Spent	48	Recalculated: Price Per Unit x Quantity
Discount Applied	4,199	Filled: FALSE (blank logically means no discount applied)
All other columns	0	Clean — no action required

Phase 2 — Exploratory Data Analysis
Five business questions were analysed using Pivot Tables:
#	Question	Finding
1	Which category generates the most revenue?	Butchers — 208,118 (highest); Milk Products — 180,112 (lowest)
2	Which sales channel performs better?	Online — 791,401 (51%); In-Store — 760,670 (49%)
3	Which payment method is most popular?	Cash — 4,310 (34.3%); near-even split across all three methods
4	Do discounts increase spending?	Discounted avg. spend: 124.30 vs non-discounted: 122.97 — marginal uplift observed
5	Which category sells the most units?	Furniture — 8,462 units; Butchers — 8,206 units despite highest revenue

Key Analytical Insight
Furniture leads in units sold (8,462) but ranks 7th in revenue, while Butchers leads in revenue (208,118) but ranks 7th in units sold. This reveals a fundamental split between volume-driven and value-driven categories — a distinction with direct implications for pricing strategy, stock management, and promotional planning.

Phase 3 — Dashboard
An Excel dashboard was built on a dedicated Dashboard tab containing 5 charts:
1. Revenue by Category — horizontal bar chart sorted highest to lowest
2. Sales by Channel — pie chart showing Online vs In-Store split
3. Payment Method by Transactions — horizontal bar chart
4. Discount Impact on Revenue — bar chart comparing discounted vs non-discounted revenue
5. Units Sold by Category — horizontal bar chart sorted highest to lowest

Repository Structure
File / Folder	Description
retail_store_sales_RAW.xlsx	Original untouched dataset
retail_store_sales_CLEANED.xlsx	Fully cleaned dataset with EDA Pivot Tables and Dashboard
Data_Cleaning_Log.docx	Full documentation of cleaning process, EDA findings, and decisions made
screenshots/	Dashboard and chart screenshots
README.md	This file

Tools Used
• Microsoft Excel — data cleaning, Pivot Tables, dashboard and charting
• EViews — used in academic research (time series analysis, cointegration modelling)

Contact
GitHub: github.com/chisomokeynwamba
LinkedIn: linkedin.com/in/chisomokeynwamba
