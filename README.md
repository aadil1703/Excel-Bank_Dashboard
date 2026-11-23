# Aarohan Bank — Banking Performance Intelligence (FY 2025)

A comprehensive, multi-sheet synthetic banking dataset and executive dashboard designed for **Excel practice, financial data analysis, and portfolio projects**. This workbook models a full fiscal year (FY 2025) of retail and commercial banking operations across 12 Indian branches.

---

## 📊 Executive Summary (FY 2025 KPIs)

| Metric | Value | Notes |
| :--- | :--- | :--- |
| **Total Deposits (Txns)** | ₹1,32,57,583.54 | Sum of successful deposit transactions |
| **Total Withdrawals (Txns)** | ₹57,61,919.36 | Sum of successful withdrawal & ATM withdrawal transactions |
| **Loan Outstanding** | ₹23,37,39,305.09 | Total active principal across all loan types |
| **NPA Ratio** | 2.27% | Non-Performing Assets share of total outstanding loans |
| **Total Transactions** | 1,800 | Across all channels and statuses |
| **Successful Txn Rate** | 95.83% | Percentage of transactions marked `Successful` |
| **Active Customers** | 257 | Customers with `Active` account status (out of 300 total) |
| **Operating Profit** | -₹95,87,420.62 | Aggregate branch operating profit across all 4 regions |

---

## 🗂️ Workbook Structure & Data Dictionary

The workbook consists of an executive summary view alongside four relational data tables and a metadata reference sheet:

### 1. Executive Summary / Dashboard
* **KPI Cards:** High-level FY 2025 performance metrics.
* **Monthly Transaction Flow:** Month-over-month deposits (₹), withdrawals (₹), and successful transaction counts.
* **Operating Profit by Region:** Profitability breakdown across **West, North, South, and East**.
* **Loan Portfolio by Type:** Outstanding principal split across **Home, Personal, Vehicle, Education, and Business Loans**.

### 2. `Transactions` (1,800 Records)
Granular daily transaction logs spanning January 1, 2025 to December 31, 2025.
* `Transaction_ID`: Unique identifier (`TXN000001` – `TXN001800`).
* `Transaction_Date`: Date of transaction in FY 2025.
* `Customer_ID` & `Customer_Name`: Foreign key linking to the `Customers` table.
* `Branch_ID`, `City`, `Region`: Branch location metadata.
* `Transaction_Type`: *Deposit, Withdrawal, UPI Payment, Card Payment, Fund Transfer, ATM Withdrawal*.
* `Channel`: *Mobile Banking, Internet Banking, Branch, ATM, POS*.
* `Amount_INR`: Transaction value in Indian Rupees (₹).
* `Status`: *Successful, Failed, Pending*.

### 3. `Customers` (300 Records)
Demographic and account segmentation profiles (`CUST0001` – `CUST0300`).
* `Age`: Customer age.
* `Customer_Segment`: *Retail, Premium, Business, Student*.
* `Join_Date`: Account onboarding date.
* `Customer_Status`: *Active* or *Dormant*.

### 4. `Loans` (420 Records)
Active loan book (`LN00001` – `LN00420`) with risk and delinquency tracking.
* `Loan_Type`: *Home Loan, Personal Loan, Vehicle Loan, Education Loan, Business Loan*.
* `Disbursement_Date`: Date the loan was issued.
* `Sanctioned_Amount_INR` & `Outstanding_Amount_INR`: Original loan principal vs. current remaining balance.
* `Interest_Rate_%` & `Tenure_Months`: Loan pricing and repayment duration.
* `Days_Past_Due` (DPD): Number of days overdue.
* `Loan_Status`: Risk classification based on DPD bands (*Standard*, *SMA* [Special Mention Account], *NPA* [Non-Performing Asset]).

### 5. `Branch Performance` (144 Records)
Monthly financial P&L statements for all 12 branches (`BR001` – `BR012`) across 12 months.
* **Branches Covered:** Ahmedabad, Mumbai, Pune, Surat (West); Delhi, Jaipur, Lucknow (North); Bengaluru, Chennai, Hyderabad (South); Kolkata, Bhubaneswar (East).
* `Deposits_INR` & `Advances_INR`: Monthly branch deposit mobilization and loan advances.
* `Interest_Income_INR`, `Fee_Income_INR`, `Operating_Expenses_INR`: Core revenue and cost drivers.
* `Operating_Profit_INR`: Calculated as $\text{Interest Income} + \text{Fee Income} - \text{Operating Expenses}$.

---

## ⚠️ Disclaimer
*This is a **fictional, synthetic dataset** created exclusively for educational, Excel learning, and data analytics portfolio purposes. Any resemblance to real banking institutions or individuals is coincidental.*
