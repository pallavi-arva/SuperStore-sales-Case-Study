1. Data Cleaning & PII Governance
Privacy First (PII): Implemented data masking by dropping sensitive Customer Name columns and generating a Customer Name Masked column using initials to comply with data protection regulations.

Format Standardization: Standardized Postal Codes to a 5-digit string format with leading zeros and converted state abbreviations (e.g., "CA") to full names (e.g., "California") for consistent regional analysis.

Type Casting: Converted financial and quantity columns from string objects to high-precision float and int types.

2. Feature Engineering & Logic Modeling
Logistics Logic: Derived Days to Ship and engineered a Shipping Urgency classification (Immediate, Urgent, Standard).

Financial Metrics: Engineered new features including Original Price, Total Sales, Total Profit, Discount Price, and Total Discount.

Temporal Features: Calculated "Days Since Last Order" to track customer churn and engagement frequency.

Customer-Centric Aggregation: Created a secondary dataset of customer-level metrics (Total Sales, Qty, Discount) and merged them back into the main pipeline to enrich the granular transaction data.

3. Advanced Statistical Processing
Robust Outlier Removal: Built a custom reusable function to detect and remove extreme outliers using the 3*IQR Rule, ensuring the model's integrity while preserving high-variance business data.

Quintile Segmentation: Applied statistical quintiles to divide customers into five equal groups based on Sales and Profit, creating a Cross-Grid Heatmap to identify the most valuable "Power Users."

4. Data Visualization & Insights Dashboard
Product Performance: Visualized the Top 10 Most Profitable and Top 10 Loss-Making products.

Correlation Analysis: Developed scatter plots with regression lines to analyze the relationship between Discounts vs. Profitability and Sales vs. Profit.

Logistics Impact: Analyzed the distribution of shipping modes across regions using Pivot Tables and Violin Plots to see if "Faster Shipping" actually correlates with higher profit margins.

Geospatial Intelligence: Mapped state-wise profitability using label-encoded correlation matrices and regional bar charts.

Key Deliverables:

Cleaned & Masked Dataset: A privacy-compliant dataset ready for modeling.

Outlier Function: A modular Python function for automated data cleaning.

Interactive Insights: A series of visualizations including Heatmaps, Joint Plots, and Year-over-Year (YoY) growth charts.
