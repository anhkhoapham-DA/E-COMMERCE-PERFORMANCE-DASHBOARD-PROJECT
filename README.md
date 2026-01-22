# E-COMMERCE-PERFORMANCE-DASHBOARD-PROJECT
1.BACKGROUND
- This project simulates a real-world scenario for a fashion retailer on Amazon India, specializing in ethnic wear (Kurtas, Sets). While the brand saw steady traction in early 2022, the stakeholders flagged a critical performance slump during Q2 (April - June).

2.OBJECTIVES
This dashboard serves a dual purpose: acting as an Operational Tracker for daily business health and a Diagnostic Instrument to investigate the underlying causes of the Q2 performance slump.

Phase 1: Operational Monitoring (The "What")
  - Track High-Level KPIs: Monitor real-time fluctuations in Total Revenue, Order Volume, and Average Order Value (AOV) to detect anomalies immediately.
  - Logistics Oversight: Assess the efficiency of the supply chain by tracking Delivery Status (Shipped, Cancelled, Pending) across different courier partners
  - Inventory Health: Identify "Best-Sellers" vs. "Slow-Movers" to optimize stock levels for the upcoming festive season.

 Phase 2: Root Cause Discovery (The "Why")
  - Diagnose the Revenue Dip: Drill down into the June data to determine if the sales drop was caused by high cancellation rate, low marketing spend, or stock unavailability.
  - Pinpoint Cancellation Drivers: Correlate Cancellation Rates with specific dimensions (e.g., Is the cancellation rate higher for Merchant-fulfilled orders vs. Amazon-fulfilled? Is it specific to certain cities?).

3.WORKFLOW
The project execution followed a structured end-to-end BI development lifecycle:

Phase 1: Requirement Analysis & Design
  - Problem Definition: Identified the core business objective — diagnosing the Q2 revenue dip and operational inefficiencies.
  - Dashboard Prototyping: Planned the layout using a grid system, defining the specific KPIs and charts required for each of the 4 report pages (Growth, Product, Customer, Logistics).

Phase 2: Data Pre-processing (Excel)
  - Initial Sanitation: Conducted a preliminary check on the raw dataset (CSV/Excel) to handle missing values and correct data types.
  - Standardization: Formatted Date columns to ISO standards and normalized Currency fields to ensure consistency before ingestion.

Phase 3: ETL & Data Modeling (Power Query-Power BI)
  - Data Transformation: Used Power Query Editor to filter out irrelevant columns, keeping only the fields necessary for analysis to optimize file performance.
  - Schema Design (Star Schema)

Phase 4: Analytics Engine (DAX-Power BI)
  - Measure Creation: Wrote DAX formulas to calculate dynamic metrics instead of using static calculated columns.
  - Key Measures: Total Revenue, Total Orders, Average Order Value (AOV).
  - Logic Measures: Profit Margin, Profit Markup, Cancellation Rate %.

Phase 5: Visualization & Storytelling(Power BI)
  - Visual Implementation: Built interactive charts (Bar, Line, Donut, Maps) tailored to answer specific business questions.
  - UX/UI Design: Implemented page navigation buttons, slicers for filtering (Time, Shipping Type, Category), and tooltips to enhance user experience.

4.INSIGHTS
Page 1: Growth & Financial Health
<img width="1928" height="1098" alt="Ảnh chụp màn hình 2026-01-22 120448" src="https://github.com/user-attachments/assets/0b569e23-653c-405b-9661-3784ceed898e" />
🔍The Price-Volume Trade-off (Inverse Correlation):
  - A distinct pattern emerged in Q2: Order Volume showed a consistent month-over-month decline (April > May > June), while Profit Margins and Markups steadily increased, peaking in June.
  - Insight: This suggests the business prioritized per-unit profitability over volume in June, likely by reducing discounts or increasing base prices.
  - Cancellation Rate Spike:June recorded a noticeably higher Cancellation Rate compared to April.
  - Correlation: The spike in cancellations coincides with the peak in profit margins. This indicates that customers may be experiencing "Sticker Shock" (reacting negatively to higher prices) or post-purchase regret, leading to immediate order withdrawals.
  - Hypothesis - The "Promotion Void": The combination of High Margins + Low Volume + High Cancellations strongly suggests that the lack of promotional campaigns (fewer active Promotion IDs) or aggressive pricing in June dampened demand. The market showed high Price Sensitivity, meaning customers are waiting for the return of discounts/coupons before purchasing.

