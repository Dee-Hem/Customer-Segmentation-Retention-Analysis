# Energy House — Customer Segmentation & Retention Analysis

An Excel-based customer analytics project analyzing purchase behavior, retention, and revenue concentration across a simulated Nigerian e-commerce dataset — built for the BoyCode Africa Data Analysis program.

## 📌 Business Problem

Management needed to understand who the company's customers are, how frequently they buy, and which customer groups actually drive value — so retention and acquisition efforts can be focused on the right people instead of spread evenly across everyone.

## 📊 Dataset

Simulated Nigerian e-commerce transaction data:
- **1,812** raw order records
- **568** unique customers
- **10** regions
- **6** acquisition channels
- Multiple product categories

*Data is synthetic, created for educational/portfolio purposes.*

## 🧹 Data Preparation

- Removed duplicate records
- Handled missing values, including ~314 blank `Customer_Rating` fields (largely tied to Cancelled/Returned orders with no completed experience to rate) — deliberately left blank rather than imputed, since filling with 0 or an average would distort rating-based analysis
- Corrected data types in Power Query (e.g., `Customer_Rating` converted to numeric with true nulls) so PivotTable aggregations calculate correctly

## 🔍 Analysis

Built a customer-level summary table (Power Query Group By) aggregating each customer's:
- Total orders
- Total quantity
- Total revenue
- Total profit
- Average order value
- Average rating

**Segmentation rule:**
- **New** — 1 order
- **Returning** — 2–3 orders
- **Loyal** — 4+ orders

PivotTables were used to compare segments by revenue/profit, and to analyze repeat-purchase behavior by region and acquisition channel.

**Excel techniques used:** Power Query (Group By, Custom Columns), PivotTables/PivotCharts, structured table references, `SUMIFS`/`COUNTIFS`/`AVERAGEIFS`, conditional filtering for high-value vs. low-value/high-frequency segments, interactive slicers.

## 📈 Key Findings

- 568 unique customers placed 1,812 orders; overall repeat purchase rate is **85%** (customers with 2+ orders)
- **Loyal customers generate ~₦146M of ₦188.4M total revenue (≈78%)**, despite being a minority of the customer base — a small group drives most of the business
- Average Order Value varies by segment: Returning customers show the highest AOV (₦54,364), ahead of Loyal (₦51,541) and New (₦49,909)
- Repeat-purchase rate varies meaningfully by region and acquisition channel
- A distinct group orders frequently (4+ orders) but at low basket value — "loyal in behavior, not yet high-value" — a separate growth opportunity from top spenders

## 💡 Recommendations

1. **Protect and grow the Loyal segment** — introduce loyalty incentives targeted at customers approaching the 4-order threshold
2. **Investigate regional retention gaps** — prioritize the lowest-repeat regions for follow-up on delivery, service, or availability issues before increasing marketing spend there
3. **Reallocate acquisition spend** — shift budget toward channels with higher repeat-customer share rather than optimizing purely for signup volume

> ⚠️ **Limitations:** These findings are descriptive, not causal. Correlations between region, channel, segment, and repeat behavior do not prove that any one factor *causes* retention — other unmeasured variables (delivery infrastructure, income levels, customer tenure) may explain the patterns. Recommendations involving reallocated spend should be validated with a controlled test (e.g., A/B testing) before scaling.

## 📷 Dashboard

<img width="643" height="503" alt="brave_screenshot" src="https://github.com/user-attachments/assets/07b3c418-8eee-4473-903a-dfaa54cb6b03" />


## 🛠️ Tools

Microsoft Excel — Power Query, PivotTables, PivotCharts, structured formulas

## 👤 Author

**Olumide Adeleke**
Computer Science student | BoyCode Africa Data Analysis Program
