# Bank-Customer-Data-Exploratory-Data-Analysis-EDA
Project Overview
This project involves the development of an interactive Banking Risk Analytics Dashboard using Power BI. The goal is to help financial institutions minimize lending risk by analyzing customer behavior, engagement patterns, and financial metrics before approving loans.

🎯 Problem Statement
Understand how data is used in banking and financial services to reduce the risk of loan default.
The dashboard provides decision-makers with insights into whether an applicant is likely to repay a loan or pose a financial risk.

💡 Solution
The dashboard helps banking personnel and analysts:

Evaluate the financial profile of clients.

Analyze engagement timelines and income bands.

Assess loan, deposit, and credit behavior.

Track key banking metrics through KPIs.

Make informed lending decisions using calculated metrics.

🗂️ About the Dataset
The dataset contains interlinked tables:

Clients - Banking

Banking Relationship

Investment Advisor

Gender

Period

🔑 The tables are connected using primary and foreign keys.

🔧 Data Preparation
Performed in Power BI using Power Query and DAX:

Created Engagement Timeframe column based on client tenure.

Added Engagement Days by calculating days since account joining.

Categorized Estimated Income into bands (Low, Mid, High) using binning.

Defined a Processing Fees column based on fee structure (e.g., 5% for high fees).

🧮 DAX Measures & Calculated Columns
🔢 Key Calculations
Measure	Description
Bank Deposit	SUM('Clients - Banking'[Bank Deposits])
Total Clients	DISTINCTCOUNT('Clients - Banking'[Client ID])
Total Loan	Sum of Bank Loan, Business Lending, and Credit Cards Balance
Total Deposit	Sum of all deposit types (savings, checking, foreign currency, etc.)
Total Fees	SUMX(Table, Loan * Processing Fee)
Engagement Days	DATEDIFF('Joined Bank', TODAY(), DAY)

⚙️ Functions Used:
SUM, SUMX, DISTINCTCOUNT

DATEDIFF for engagement

SWITCH for conditional calculations

📊 Key KPIs in Dashboard
✅ Total Clients

💰 Total Loan (Loan + Business Lending + Credit Card Balances)

🏦 Total Deposit (Deposit + Savings + Foreign Currency + Checking)

💸 Total Fees

💳 Credit Card Balance

📆 Engagement Days

📈 Visualizations
The Power BI dashboard includes:

Home Page: Executive snapshot of banking performance

Loan Analysis Page: Deep dive into loan and credit trends

Deposit Analysis Page: Track deposits across account types

Summary Page: Consolidated KPIs and trends

✅ Conclusion
Power BI dashboards provide a powerful way to visualize banking operations and financial risk. This project demonstrates how banks can:

Monitor client financial behavior

Identify high-risk applicants

Track overall banking performance with real-time KPIs

🚀 Future Work
Predictive analytics to classify high-risk clients using ML

Integration with real-time banking systems

Expand analysis to include branch performance and geographic trends

📁 Repository Structure
bash
Copy
Edit
banking-risk-analytics/
├── Banking Report.pdf         # Project documentation
├── Banking Dataset (.csv)     # (Add if public or synthetic)
├── Power BI File (.pbix)      # Dashboard file
├── Screenshots/               # Dashboard visuals
└── README.md                  # This file
