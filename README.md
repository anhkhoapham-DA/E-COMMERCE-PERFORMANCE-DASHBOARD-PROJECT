# E-COMMERCE-PERFORMANCE-DASHBOARD-PROJECT
1.BACKGROUND
- This project simulates a real-world scenario for a fashion retailer on Amazon India, specializing in ethnic wear (Kurtas, Sets). While the brand saw steady traction in early 2022, the stakeholders flagged a critical performance slump during Q2 (April - June).

2.OBJECTIVES
- This dashboard serves a dual purpose: acting as an Operational Tracker for daily business health and a Diagnostic Instrument to investigate the underlying causes of the Q2 performance slump and provide analytical insights to support decision-making and optimize business profitability.

3.WORKFLOW
- The project execution followed a structured end-to-end BI development lifecycle:

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

<img width="1935" height="1092" alt="Ảnh chụp màn hình 2026-01-22 122257" src="https://github.com/user-attachments/assets/7052f2da-56a6-41aa-9c1c-15115a93fcc6" />

The Price-Volume Trade-off (Inverse Correlation):
  - A distinct pattern emerged in Q2: Order Volume showed a consistent month-over-month decline (April > May > June), while profit margin and markup steadily increased, peaking in June at 38.36% (profit markup) and 27.72% (profit margins).
  - Insight: This suggests the business prioritized per-unit profitability over volume in June, likely by reducing discounts or increasing base prices.
  - Cancellation Rate Spike: June recorded a steadily higher Cancellation Rate (5.14%) compared to April (4.82%).
  -> Correlation: The spike in cancellations coincides with the peak in profit margin. This indicates that customers may be experiencing "Sticker Shock" (reacting negatively to higher prices) or post-purchase regret, leading to immediate order withdrawals.
  -> Hypothesis - The "Promotion Void": The combination of High Margins + Low Volume + High Cancellations strongly suggests that the lack of promotional campaigns (fewer active Promotion IDs) or aggressive pricing in June dampened demand. The market showed high Price Sensitivity, meaning customers are waiting for the return of discounts/coupons before purchasing.

Page 2: Product Performance

<img width="1939" height="1090" alt="Ảnh chụp màn hình 2026-01-22 121748" src="https://github.com/user-attachments/assets/3832a140-10f6-4c51-8333-26bb2f994122" />

  - Pricing Misalignment (The "Dupatta" Anomaly): The Dupatta category exhibits an extremely high profit markup (52.28%) & margin (34.33%) despite having a low production cost. However, it recorded a negligible sales volume of only 3 units for the entire quarter
  - Volume Drivers vs. Margin: In contrast, core categories like Sets, Kurtas, and Western Dresses show a balanced "High Volume - Moderate Margin" profile. These items are priced competitively, acting as the primary revenue engines (Cash Cows) for the business.
 -> Insight: This indicates a "Prohibitive Pricing" strategy. The product is overpriced relative to its perceived value, killing demand despite its high-profit potential.
  - The Quality-Churn Correlation: The Average Product Rating remained consistently low throughout Q2.
  -> Root Cause Discovery: There is a strong correlation between these low ratings and the declining Order Volume / rising Cancellation Rate observed in Page 1.
  -> Conclusion: The revenue dip is not solely due to seasonal trends but is likely driven by poor product quality or negative customer reviews, triggering a "Crisis of Confidence" among buyers. Immediate Quality Control (QC) intervention is required.

Page 3: Customer Intelligence & Targeting

<img width="1932" height="1081" alt="Ảnh chụp màn hình 2026-01-22 121803" src="https://github.com/user-attachments/assets/48ce2a85-fd61-43ce-8ffa-c6c3208d1dd8" />

  - The "Power User" Segment (Adults): The Adult age group is the undisputed backbone of the business, contributing 57.61% of total customers.
  -> Strategy: Marketing budget allocation should follow the Pareto Principle, focusing 80% of retention efforts (Loyalty Programs, Email Marketing) on this specific demographic to maximize Customer Lifetime Value (CLV).
  - Generational Product Mapping: A clear divergence in style preference was observed across age groups: Young Adults: Show a strong affinity for Western Dresses & Tops, indicating a trend-driven fashion sense. Adults: Primarily purchase Sets (Kurta + Bottom), prioritizing complete outfits/value bundles. Middle-Aged: Prefer standalone Kurtas, likely for daily comfort or traditional wear.
  - Actionable Insight: The website/app interface should implement Personalized Recommendations based on user age data (e.g., hiding Western wear for Middle-aged users) to increase conversion rates.
  - The "Sunday Effect" (Shopping Habits): Sunday emerged as the peak trading day with the highest traffic and order volume.
  - Operational Shift: This behavior suggests customers shop during leisure time. Therefore, Marketing Campaigns (Push Notifications/Newsletters) should be scheduled for Saturday evenings or Sunday mornings to capture this intent. Additionally, Customer Support bandwidth should be maximized on weekends.

Page 4: Logistics Performance Analysis (Focusing on Shipping & Fulfilment)

<img width="1578" height="879" alt="Ảnh chụp màn hình 2026-01-22 213838" src="https://github.com/user-attachments/assets/0ea5c55a-489e-4a63-853f-1f682bd7d52b" />

  - Profitability Dynamics (Amazon vs. Merchant): Amazon is the dominant profit contributor, consistently generating ~3x more value than Merchant fulfillment. However, the total profit decline in June was driven by a sharp 30% drop in Merchant performance (20M to 14M), while Amazon remained relatively stable.
  - Insight: While Amazon is the financial backbone, the volatility in Merchant Fulfillment is currently dragging down overall growth. Operations must stabilize Merchant capacity to prevent it from eroding the gains made by the primary Amazon channel.
  - Geographic Dependency (Maharashtra & Karnataka): The heatmap identifies Maharashtra and Karnataka as the overwhelming volume drivers for the business.
  - Risk & Strategy: These two states represent a critical "Single Point of Failure." Logistics planning must ensure multiple courier partners and warehouse redundancy in these specific regions to prevent localized disruptions from crippling total output.
  - Cost Optimization (Shipping Types): Expedited Shipping accounts for 70.22% of all orders, significantly driving up logistics costs compared to Standard delivery (29.78%).
