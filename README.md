# 💳 Moniepoint Transaction Failure & Performance Analytics Dashboard (Power BI)

This project is a two-page Power BI dashboard that gives stakeholders a clear, centralized view of how transactions perform at Moniepoint Microfinance Bank. It covers transaction volume, value, fees, success, failure and reversal rates across channels, states, business categories, customer types and transaction types.

This project turns raw transaction data into an interactive report that helps stakeholders understand why transactions fail, where performance is strongest, and how transaction value changes over time.

---

## 📌 Project Overview

A microfinance bank processes large volumes of transactions every day across USSD, Mobile App and POS. Without a centralized view, it is hard to spot failure patterns, track reversals or see where value is being generated.

This Power BI report was developed to provide insight into:

- 📊 **Key performance indicators:** total transactions, transaction value, fees, success rate, failure rate and reversal rate
- ❌ **Failure analysis:** the main reasons transactions fail, and failure rates by business category, state and month
- 📍 **Regional and channel performance:** how transaction status and success rates differ by state and channel
- 💰 **Value trends:** transaction value by business category, customer type and month

The report supports data-driven decisions on service reliability, channel improvement and customer support.

---

## 🎯 Business Problem

Stakeholders need clear answers to key questions:

- What share of transactions succeed, fail or get reversed?
- Why do transactions fail, and which business categories, states and channels are most affected?
- Which channels, customer types and transaction types generate the most volume and value?
- How do failure rates and transaction value change month by month?

Without a centralized dashboard, these insights stay buried across disconnected transaction records.

This dashboard solves the problem by consolidating transaction data into a single interactive Power BI report.

---

## 📈 Key Metrics and KPIs

| KPI | Value |
|-----|-------|
| Total Transactions | 30K |
| Total Transaction Value | $2.3bn |
| Total Transaction Fees | $10.2M |
| Successful Transactions | 27K |
| Transaction Success Rate | 90.1% |
| Failed Transactions | 2K |
| Transaction Failed Rate | 6.04% |
| Reversed Transactions | 1K |
| Transaction Reversed Rate | 3.86% |

---
## 📊 Dashboard Structure

### Page 1: Transaction Failure & Operational Analysis

<img width="1149" height="553" alt="moine 1" src="https://github.com/user-attachments/assets/2a88c153-d950-4a26-af3b-6f35e3f8a2a0" />

🎯 **Purpose:** "Why do transactions fail, and where?"

🔎 **Filters:** Channel, Transaction_Type, Customer_Type

📌 **KPIs:**
- Total Transactions: 30K
- Failed Transactions: 2K
- Transaction Failed Rate: 6.04%
- Reversed Transactions: 1K
- Transaction Reversed Rate: 3.86%

📊 **Visuals:**
- Stacked bar chart: Transaction Status by State
- Bar chart: Transaction Failed Rate by Business Category
- Line chart: Monthly Transaction Failed
- Column chart: Transaction Failure Reasons
- Donut chart: Transaction Status Distribution
- Column chart: Transaction Success Rate by Channel

### Page 2: Transaction Performance Dashboard

<img width="1057" height="546" alt="moine 2" src="https://github.com/user-attachments/assets/4d732476-066f-4149-bb95-99620d8fc16b" />

🎯 **Purpose:** "How much value are we processing, and where does it come from?"

🔎 **Filters:** Months, State, Transaction_Type

📌 **KPIs:**
- Total Transactions: 30K
- Total Transaction Value: $2.3bn
- Total Transaction Fees: $10.2M
- Successful Transactions: 27K
- Transaction Success Rate: 90.1%

📊 **Visuals:**
- Bar chart: Transaction Value by Business Category
- Column chart: Transaction Value by Customer Type
- Step line chart: Monthly Transaction Value
- Donut chart: Total Transaction by Channel
- Column chart: Transaction by Transaction Type

---
## 🧹 Data Cleaning & Preparation

<img width="1113" height="653" alt="moine 4" src="https://github.com/user-attachments/assets/62568998-735b-436c-8225-01e6a08ef5a2" />

- Standardized category labels (channel, transaction type, customer type, business category) for consistent filtering
- Created status and failure-reason fields to support failure and reversal analysis
- Calculated failure, reversal and success rates as percentages for easier comparison
- Set data types in Power Query, including `Amount` and `Transaction_Fee` as currency, `Transaction_Date` as date and `Transaction_Time` as time
- Extracted first characters from text fields to create consistent codes (see the "Extracted First Characters" step in Power Query)
- Checked column quality in the profiling view: 100% valid, 0% errors and 0% empty on the columns shown

### 🧮 DAX Measures

<img width="278" height="337" alt="moine 3" src="https://github.com/user-attachments/assets/a5774880-a779-4a41-9dc9-e37ff325d440" />

All measures are stored in a dedicated **Measure Table**:

- Total Transaction
- Successful transaction
- Failed transaction
- Reversed transaction
- Total Transaction Value
- Total Transaction Fees
- Transaction Success Rate
- Transaction Failed Rate
- Transaction Reversed Rate
---

## 💡 Key Insights & Business Question Analysis

**What share of transactions succeed, fail or get reversed?**
About 90.11% of transactions succeed, 6.04% fail and 3.86% are reversed. Nine in ten transactions go through, but roughly one in ten still ends in failure or reversal.

**Why do transactions fail, and where?**
Insufficient Funds (487) and Invalid PIN (466) are the top failure reasons, followed by Network Error (438) and Timeout (420). Restaurant has the highest failure rate by business category (6.53%), and Fuel Station has the lowest (5.73%). Lagos leads on successful transactions (10.8K), followed by Abuja (6.7K) and Rivers (4.2K).

**Which channels, customer types and transaction types perform best?**
USSD has the highest success rate (90.5%) and POS the lowest (89.6%). Transaction volume is split almost evenly across Mobile App (33.68%), USSD (33.21%) and POS (33.11%). POS dominates by transaction type (18K), followed by Bank Transfer (6K), Cash Withdrawal (5K) and Bill Payment (1K). Value is also spread evenly across customer types, with Agents slightly ahead ($758.43M).

**How do trends change over time?**
Monthly transaction value stays between about $176M (Feb, lowest) and $195M (Oct, highest). Monthly failure rates move between about 5.4% and 6.6%.

---

## 🚀 Strategic Recommendations

📍 **Reduce Customer-Side Failures**
Add low-balance alerts and balance-check prompts to reduce insufficient-funds failures, and clearer PIN-entry guidance to reduce invalid-PIN failures.

🛠️ **Improve System Reliability**
Investigate network errors and timeouts, starting with POS, which has the lowest success rate.

🏪 **Target High-Failure Categories**
Look into why Restaurant and Fashion have higher failure rates than other business categories.

---

## 🔚 Conclusion

This dashboard turns raw transaction data into a strategic tool for understanding transaction performance. Instead of guessing why transactions fail or where value comes from, stakeholders can now see the reasons, the channels and the regions behind them. That supports smarter decisions on reliability, customer support and channel improvement.

---

## ✨ Key Dashboard Features

- ✅ Two-page layout separating failure analysis from performance analysis
- ✅ KPI cards for volume, value, fees, success rate, failure rate and reversal rate
- ✅ Failure reasons and failure rates by business category, state and month
- ✅ Slicers for channel, transaction type, customer type, month and state
- ✅ Percentage-based metrics for easy comparison across categories

---

## 📁 Files Included

| File | Description |
|------|-------------|
| `[your-dashboard].pbix` | Completed Power BI dashboard |
| `failure-dashboard.png` | Preview of the Transaction Failure & Operational Analysis page |
| `performance-dashboard.png` | Preview of the Transaction Performance Dashboard page |
| `power-query-preview.png` | Screenshot of the Power Query Editor and data profiling |
| `dax-measures.png` | Screenshot of the DAX measures in the Measure Table |
| `README.md` | Project documentation |

---

## 🔧 How to Download and Use

1. Download `[your-dashboard].pbix`.
2. Open the file using Microsoft Power BI Desktop.
3. Use the available filters and slicers to explore transactions by channel, transaction type, customer type, month and state.

---

## 🛠️ Tools and Skills

- Microsoft Power BI
- Power Query
- DAX
- Excel / SQL
- Data analysis
- Dashboard design
- Data visualization

---
