General Ledger Analysis (Excel)

Project Overview

This project is a full end-to-end General Ledger analysis built entirely in Microsoft Excel. The dataset represents 30 months of financial transactions (January 2023 – June 2025) for a fictional company operating across multiple departments, cost centers, and currencies.

The goal was to clean raw transactional data, build a multi-currency conversion model, and deliver two interactive dashboards — one focused on financial performance and one on operational activity — complete with insights and recommendations that a business could act on.

Dataset Description

	∙	2,000 transactions spanning January 2023 to June 2025
	∙	6 departments: Finance, HR, IT, Marketing, Operations, Sales
	∙	5 cost centers: CC100, CC200, CC300, CC400, CC500
	∙	5 currencies: USD, GBP, EUR, AUD, CAD
	∙	Account types: Revenue and Expense
	∙	All transaction values converted to Nigerian Naira (₦) using a custom FX rate table
  
  Tools Used
  
	∙	Microsoft Excel
	∙	Power Query (data cleaning, transformation, and merging)
	∙	Pivot Tables and PivotCharts
	∙	Slicers and KPI Cards
  
  Data Cleaning Process
  
  (Power Query)
The raw dataset was loaded into Power Query before any analysis began. The following cleaning steps were carried out:
General Cleaning
	∙	Removed blank rows and duplicate entries
	∙	Standardized column headers and data types
	∙	Corrected inconsistent date formats and ensured all dates were recognized as date values
	∙	Trimmed whitespace from text fields across all columns
Calculated Columns Created
	∙	Revenue Column — flagged and extracted all transactions where the account type was revenue
	∙	Expense Column — flagged and extracted all transactions where the account type was expense
	∙	Amount Column — consolidated transaction values into a single amount field for consistent calculation
	∙	Year Column — extracted the year from the transaction date column to enable year-based slicers on both dashboards
FX Rate Table — Built and Merged
Because the dataset contained transactions in five different currencies, a separate FX Rate Table was built manually mapping each currency (USD, GBP, EUR, AUD, CAD) to its Nigerian Naira equivalent.
This table was then merged into the main dataset in Power Query using a matching join on the currency column. Once merged, an Amount in Naira calculated column was created by multiplying each transaction’s original amount by its corresponding Naira exchange rate. This ensured every transaction — regardless of original currency — could be analyzed in a single consistent currency across both dashboards.

Dashboard 1 — Financial Performance

KPI Cards
	∙	Total Revenue: ₦2,736,911,726
	∙	Total Expenses: ₦1,635,447,714
	∙	Net Profit: ₦1,101,464,012
	∙	Profit Margin: 40%
	∙	Gross Profit Margin: 80%
	∙	Expense Ratio: 60%
  
Charts Built
	∙	Monthly Profit Trend — Line chart tracking revenue, expenses, and net profit month by month across 30 months
	∙	Revenue vs Expense by Department — Clustered bar chart comparing revenue and expense per department
	∙	Revenue Breakdown — Pie/donut chart showing contribution of each revenue stream
	∙	Expense Breakdown — Pie/donut chart showing contribution of each expense category
	∙	Transaction Distribution — Chart showing the split between revenue and expense transactions
  
Slicers

	∙	Year slicer (2023, 2024, 2025)
	∙	Department slicer
	∙	Account type slicer
  
  Dashboard 2 — Operations & Activity
KPI Cards

	∙	Total Transactions: 2,000
	∙	Average Transaction Value: ₦2,186,180
	∙	Active Departments: 6
	∙	Active Cost Centers: 5
  
Charts Built

	∙	Monthly Transaction Trend — Line chart showing transaction volume per month across 30 months
	∙	Cost Center Spend — Bar chart comparing total spend across all five cost centers
	∙	Transaction Value by Department — Bar chart showing total transaction value per department
	∙	Transaction Count by Department — Bar chart showing number of transactions per department
	∙	Total Activity Value Trend — Area/line chart showing total monthly activity value over time
	∙	Currency Distribution — Pie chart showing the percentage split of transactions across all five currencies
  
Slicers

	∙	Year slicer
	∙	Department slicer
	∙	Currency slicer
	∙	Cost center slicer
  
  Analysis Questions This Project Answers
  
	1.	Is the business profitable and how does its margin compare to industry benchmarks?
	2.	Which month recorded a loss and what caused it?
	3.	Which department generates the most revenue relative to its expenses?
	4.	Which department carries the highest expense burden?
	5.	How dependent is the business on its current revenue streams?
	6.	Which expense categories are the hardest to cut and why?
	7.	Is business activity growing year on year?
	8.	Which cost center is spending the most?
	9.	Which department processes the most transactions and which handles the highest value?
	10.	How exposed is the business to foreign exchange risk?
  
  Insights
  
Financial Performance

The business generated ₦2.74B in revenue against ₦1.64B in expenses, delivering ₦1.10B in net profit at a 40% margin — exceeding the typical 20–30% industry benchmark. The 80% Gross Profit Margin dropping to 40% net reveals that operating expenses consume exactly half of gross profit. At 60%, the Expense Ratio means ₦0.60 is spent per ₦1 earned, leaving a thin buffer for unexpected costs.
Revenue peaked at ₦128.7M in December 2023, suggesting strong seasonal demand. September 2024 was the only loss-making month at -₦1.94M, driven by Travel and Payroll spikes in Operations and Marketing. Net profit fluctuates sharply month to month, indicating revenue and expense cycles are misaligned.
Finance is the star performer, generating ₦504.9M revenue against only ₦269.7M in expenses — the best ratio across all departments. HR carries the worst expense ratio at 72.6% (₦315.4M expenses vs ₦434.6M revenue). Operations has the lowest revenue and lowest expenses, suggesting underinvestment.
Online Sales (₦1.41B, 51.6%) narrowly leads Sales Revenue (₦1.33B, 48.4%) by only ₦85.8M — a closing gap that signals Sales Revenue is catching up. The business depends entirely on two income streams with no diversification buffer.
COGS (₦549.9M), Travel (₦544.8M), and Payroll (₦540.8M) are almost equally distributed, making cost reduction harder as there is no single dominant expense to target. Revenue transactions (52%) outnumber expense transactions (38%), confirming the business processes more income-generating activity than cost activity — a healthy operational signal.

Operations & Activity

The business processed exactly 2,000 transactions across 30 months, averaging ₦2,186,180 per transaction across 6 active departments and 5 cost centers. The balanced spread signals a well-distributed operational structure with no single department or cost center dominating activity.
Transaction volumes fluctuated between 48 and 82 per month, peaking at 82 in mid-2024 and dropping as low as 48 in early 2023. 2024 recorded the highest annual volume at 839 transactions — a 10.8% increase over 2023’s 757, confirming growing business activity year-on-year.
CC100 leads spending at ₦343.7M while CC300 is the lowest at ₦301.3M — a ₦42.4M gap. The relatively close spend distribution suggests balanced cost allocation with no runaway cost center.
Finance leads total transaction value at ₦504.9M while Operations records the lowest at ₦441.4M. Despite similar transaction counts, Finance handles significantly higher-value transactions on average. HR processes the most transactions at 352 while IT and Operations tie at the lowest with 317 each.
All five currencies are evenly distributed — USD (20.40%), GBP (20.65%), EUR (20.05%), AUD (19.10%), and CAD (19.80%) — with no single currency dominating. This confirms truly diversified multi-currency operations with minimal foreign exchange concentration risk.

Recommendations

The business should focus on cutting unnecessary costs, diversifying revenue, and investing in underleveraged departments to protect its 40% profit margin and sustain the growth recorded in 2024.
	∙	Build a seasonal sales strategy around December demand
	∙	Cap Travel and Payroll costs in Operations and Marketing to prevent repeat loss months
	∙	Reduce HR’s expense ratio from 72.6% by reviewing staffing costs relative to revenue
	∙	Diversify revenue beyond two streams to reduce income concentration risk
	∙	Push the Expense Ratio below 55% — every 5% reduction adds approximately ₦136M annually
	∙	Review CC100 as the highest spending cost center for reduction opportunities
	∙	Automate HR transactions given their high frequency and lower value
	∙	Invest in IT and Operations — both show untapped growth potential
	∙	Sustain the strategies that drove 2024’s 10.8% activity growth
	∙	Maintain even currency spread across all five currencies to keep foreign exchange risk low
  
  Author
  
Jane Chisom Raymond
Accounting Graduate | BI Analytics Enthusiast
GitHub: github.com/Janechisom
#LearningInPublic
