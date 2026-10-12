# **Fintech Payment Performance Analysis**
## **One Question Projects — Project 05**

## **Project Overview**
This project simulates a payment performance analysis scenario for a fintech company operating in the digital payments industry, similar to Fawry or Paymob. Using a synthetic dataset of payment transactions, the project evaluates payment performance and investigates patterns associated with transaction failures. The analysis uses Python to examine Payment Success Rate across different payment methods, transaction channels, merchant categories, transaction values, and times of day, aiming to identify segments with elevated failure rates and highlight potential areas for operational improvement.

## **Business Problem**
Payment failures can disrupt customer experiences, reduce completed transactions, and create additional operational friction for payment providers and merchants. However, an overall failure rate alone does not reveal where these problems are concentrated or which transaction characteristics are associated with a higher likelihood of failure. Without a segmented analysis of transaction performance, it can be difficult to identify the areas that require further investigation and operational improvement.

## **Project Goal**
The goal of this project is to evaluate payment performance by measuring the overall Payment Success Rate and comparing transaction outcomes across key operational dimensions. The analysis aims to identify segments with relatively high failure rates, examine the distribution of failure reasons, and generate actionable business insights that can help prioritize further investigation into payment reliability.

## **Project Business Question**
What factors are associated with payment failures, and which transaction segments exhibit the highest failure rates?

## **Dataset Description**
The dataset contains 30,000 payment transactions simulated for a fintech company operating in the digital payments industry. It consists of 10 columns covering transaction details, customer and merchant identifiers, payment methods, transaction channels, merchant categories, transaction amounts, transaction outcomes, and failure reasons.

The dataset supports the analysis of Payment Success Rate across multiple operational dimensions, helping identify transaction segments with elevated failure rates and explore patterns associated with unsuccessful payments.

| Column | Description |
|---|---|
| `transaction_id` | Unique identifier assigned to each payment transaction. |
| `customer_id` | Identifier of the customer initiating the transaction. |
| `merchant_id` | Identifier of the merchant receiving the payment. |
| `transaction_date` | Date and time when the transaction occurred. |
| `payment_method` | Payment method used to complete the transaction. |
| `amount` | Monetary value of the transaction. |
| `channel` | Channel through which the transaction was initiated, such as a mobile app, website, or POS terminal. |
| `merchant_category` | Business category of the merchant. |
| `status` | Final transaction outcome, recorded as Success or Failed. |
| `failure_reason` | Recorded reason for a failed transaction, where available. |

## **EDA & Baseline KPIs**
![baseline_kpis](./charts/0.png)
- The dataset contains **30,000 transactions** generated between **January 1 and March 30, 2026**, involving **7,822 unique customers** and **1,000 merchants**. The total transaction value is **19.56 million**, with an **average transaction amount of 652.08** and a **median of 451.92**.
- Regarding payment performance, **26,337 transactions were successful (87.79%)**, while **3,663 transactions failed (12.21%)**. Although the overall success rate provides a useful performance baseline, it does not reveal whether failures are concentrated in specific payment methods, transaction channels, merchant categories, transaction amounts, or times of day. These dimensions will be examined in the subsequent analysis to identify segments associated with elevated failure rates.
---
![transactions_by_channel](./charts/1.png)
- The **Mobile App** accounts for the largest share of transactions (**44.84%**), followed by **Web (35.18%)** and **POS (19.98%)**, indicating an uneven distribution of transaction volume across channels.
---
![transactions_by_payment_method](./charts/2.png)
- **Credit Card** accounts for the largest share of transactions (**31.75%**), followed by **Debit Card (28.03%)**, **Mobile Wallet (25.43%)**, and **Bank Transfer (14.80%)**, indicating differences in transaction volume across payment methods.
---
![transactions_by_merchant_category](./charts/3.png)
- **Retail** accounts for the largest share of transactions **(22.24%)**, followed by **Food & Beverage (17.82%)**, while the remaining merchant categories each contribute between **10.17% and 15.04%**, indicating a moderate concentration of transaction volume in Retail and Food & Beverage.
---
![transactions_by_hour](./charts/4.png)
- The hourly transaction distribution remains relatively stable throughout the day, with transaction counts ranging from **1,175 to 1,313 per hour** and no substantial fluctuations in overall activity.
---
![transactions_by_day](./charts/5.png)
- The day-of-week transaction distribution is relatively stable, with daily transaction counts ranging from **3,991 on Tuesday** to **4,476 on Sunday**, indicating no substantial variation in transaction volume across the week.