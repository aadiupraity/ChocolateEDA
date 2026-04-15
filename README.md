# Chocolate Sales Exploratory Data Analysis (EDA)

## Project Overview
This project analyzes a synthetic retail dataset representing chocolate sales across multiple stores, customers, and products during 2023–2024. The goal was to integrate data from a **Star Schema** (Sales, Products, Stores, Customers, and Calendar) to uncover actionable business insights regarding profitability, customer behavior, and retail performance.

## Dataset Structure
The analysis was performed on five interconnected tables:
- **Sales (Fact):** Transaction-level data (Revenue, Profit, Quantity, Discounts).
- **Products:** Product metadata (Cocoa %, Weight, Brand, Category).
- **Stores:** Geographic and store type information.
- **Customers:** Demographic data and loyalty status.
- **Calendar:** Time-based attributes for trend analysis.

## Tech Stack
- **Language:** Python 3.x
- **Libraries:** Pandas (Data Manipulation), NumPy (Numerical Analysis), Matplotlib & Seaborn (Data Visualization).
- **Environment:** Jupyter Notebook.

## Key Analysis & Methodology
1.  **Data Integration:** Merged five disparate tables into a unified master dataframe for holistic analysis.
2.  **Profitability Deep-Dive:** Identified "Hero" products by grouping revenue and profit by product category and cocoa intensity.
3.  **Customer Segmentation:** Used `pd.cut` to bin customers into age groups and analyzed spending habits by loyalty status.
4.  **Discount Impact Study:** Investigated the correlation between discount levels and total profit to assess pricing efficiency.
5.  **Temporal Trends:** Resampled sales data by month and day-of-week to identify seasonal patterns.

## Key Insights
* **Premium Drivers:** Products with **70–90% cocoa** (specifically Truffles and Pralines) are the primary profit drivers.
* **Discount Strategy:** High discounts (20%+) showed diminishing returns; they did not significantly boost volume compared to 10% discounts, leading to unnecessary margin erosion.
* **Stable Demand:** The dataset shows consistent demand year-round with minimal seasonality, suggesting chocolate acts as a "staple luxury" for this demographic.
* **Loyalty Potential:** Loyalty members account for ~50% of transactions, but their average transaction value is similar to non-members, indicating an opportunity for more aggressive loyalty incentives.

## Future Work
- **K-Means Clustering:** Implement machine learning to group customers into behavioral segments (e.g., Champions vs. At-Risk).
- **Predictive Modeling:** Build a regression model to forecast next month's sales based on historical trends.

## Project Structure
```text
├── Chocolate_EDA.ipynb   # Main analysis notebook
├── data/                 # Folder containing CSV files (Sales, Products, etc.)
└── README.md             # Project documentation
