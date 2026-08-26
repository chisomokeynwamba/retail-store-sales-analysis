# Retail Store Sales: Data Cleaning, EDA & Dashboard

## 📊 Project Overview
This project demonstrates an end-to-end data analytics workflow applied to a retail transactions dataset of **12,575 rows** across **11 columns**. The workflow covers data auditing, cleaning, exploratory analysis, and dashboard visualisation — following a structured, evidence-based approach used in quantitative economic research.

---

## 👩‍💻 Analyst Background
* **Profile:** BSc Economics graduate with a Google Data Analytics Professional Certification and hands-on experience in business analysis and data-driven decision-making.
* **Advanced Research Skills:** Conducted time series studies and economic modelling using EViews and statistical tools — covering stationarity testing, cointegration analysis, and long-run forecasting to generate actionable business and financial insights.

---

## 🗂️ Dataset Profile
* **Source:** Kaggle — Retail Store Sales
* **Total Volume:** 12,575 transactions across 11 columns (Transaction ID, Customer ID, Category, Item, Price Per Unit, Quantity, Total Spent, Payment Method, Location, Discount Applied, Date).
* **Categories:** 8 sectors including Beverages, Butchers, Computers and electric accessories, Electric household essentials, Food, Furniture, Milk Products, and Patisserie.
* **Channels & Payments:** Split across Online and In-Store sales channels, using Cash, Digital Wallet, and Credit Card payment methods.

---

## 🧹 Phase 1 — Data Cleaning & Validation
* **File Preservation:** Raw file preserved untouched; all cleaning executed on a separate working copy.
* **Data Inspection:** Conducted `COUNTBLANK` audits across all 11 columns, `ISNUMBER` checks on numeric fields, and Pivot Table audits of all categorical columns.
* **Data Type Validation:** All numeric columns confirmed as true numbers with no text-formatted values found.
* **Categorical Consistency:** Checked Category, Payment Method, and Location for casing and spacing inconsistencies via Pivot Tables — verified as entirely clean.
* **Missing Value Treatment:** Resolved **4,485 blanks** systematically:
  * Financial fields recalculated from mathematical relationships.
  * Item blanks filled as `Unknown`.
  * Discount Applied blanks filled as `FALSE`.
* **Duplicate Check:** Executed `Data → Remove Duplicates` by Transaction ID — resulting in **0 duplicates found**.

### Missing Values Summary
| Column | Blanks | Treatment |
| :--- | :---: | :--- |
| **Item** | 95 | Filled: `Unknown` (cannot be inferred from other columns) |
| **Price Per Unit** | 47 | Recalculated: Total Spent / Quantity |
| **Quantity** | 48 | Recalculated: Total Spent / Price Per Unit |
| **Total Spent** | 48 | Recalculated: Price Per Unit x Quantity |
| **Discount Applied** | 4,199 | Filled: `FALSE` (blank logically means no discount applied) |
| **All other columns** | 0 | Clean — no action required |

---

## 📈 Phase 2 — Exploratory Data Analysis (EDA)
Five core business questions analysed using Pivot Tables:

| # | Business Question | Analytical Finding |
| :---: | :--- | :--- |
| **1** | Which category generates the most revenue? | **Butchers** — 208,118 (highest); **Milk Products** — 180,112 (lowest) |
| **2** | Which sales channel performs better? | **Online** — 791,401 (51%); **In-Store** — 760,670 (49%) |
| **3** | Which payment method is most popular? | **Cash** — 4,310 (34.3%); near-even split across all three methods |
| **4** | Do discounts increase spending? | Discounted avg. spend: **124.30** vs non-discounted: **122.97** (marginal uplift) |
| **5** | Which category sells the most units? | **Furniture** — 8,462 units; **Butchers** — 8,206 units despite leading in revenue |

### 💡 Key Analytical Insight
**Furniture** leads in units sold (8,462) but ranks 7th in revenue, while **Butchers** leads in revenue (208,118) but ranks 7th in units sold. This reveals a fundamental split between volume-driven and value-driven categories — a distinction with direct implications for pricing strategy, stock management, and promotional planning.

---

## 📈 Phase 3 — Excel Dashboard Design
An Excel dashboard was built on a dedicated Dashboard tab featuring 5 dynamic charts:
1. **Revenue by Category** — horizontal bar chart sorted highest to lowest.
2. **Sales by Channel** — pie chart showing Online vs. In-Store split.
3. **Payment Method by Transactions** — horizontal bar chart.
4. **Discount Impact on Revenue** — bar chart comparing discounted vs. non-discounted revenue.
5. **Units Sold by Category** — horizontal bar chart sorted highest to lowest.

---

## 📂 Repository Structure
* `retail_store_sales_RAW.xlsx` — Original untouched dataset.
* `retail_store_sales_CLEANED.xlsx` — Fully cleaned dataset with EDA Pivot Tables and Dashboard.
* `Data_Cleaning_Log.docx` — Full documentation of the cleaning process, EDA findings, and decisions made.
* `screenshots/` — Dashboard and chart visual exports.
* `README.md` — Documentation file.

---

## 🛠️ Tools Used
* **Microsoft Excel** — data cleaning, Pivot Tables, dashboarding, and charting.
* **EViews** — academic research tooling (time series analysis, cointegration modelling).

---

## 📸 Dashboard Preview
*(Insert screenshots of your Excel dashboard and charts here)*
