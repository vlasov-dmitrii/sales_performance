# E-Commerce Sales Performance Analysis

**A comprehensive data analysis portfolio project demonstrating end-to-end analytical capabilities**

---

## Project Overview

This project showcases a complete data analysis workflow for an e-commerce company's sales performance over a 2-year period (2022-2023). The analysis demonstrates proficiency in data cleaning, exploratory data analysis, statistical analysis, data visualization, and business insight generation using Python and SQL.

### Key Technologies
- **Python**: Pandas, NumPy, Matplotlib, Seaborn
- **SQL**: SQLite for database queries and analysis
- **Jupyter Notebook**: Interactive data exploration and analysis
- **Data Visualization**: Charts and dashboards

---

## Dataset Information

**Source**: Mock interview questions e-commerce transaction data  
**Size**: 43,736 transactions (after cleaning)  
**Date Range**: January 1, 2022 - December 31, 2023  
**Records**: Sales transactions across 4 product categories and 5 geographic regions

### Data Schema

```
transactions
├── transaction_id    (string)   - Unique transaction identifier
├── date             (datetime) - Transaction date
├── customer_id      (string)   - Customer identifier
├── product_name     (string)   - Product name
├── category         (string)   - Product category
├── quantity         (int)      - Units purchased
├── unit_price       (float)    - Price per unit
├── total_amount     (float)    - Total transaction amount
├── region           (string)   - Geographic region
├── payment_method   (string)   - Payment method used
└── shipping_cost    (float)    - Shipping charges
```

---

## Project Structure

```
sales-performance-analysis/
│
├── data/
│   ├── ecommerce_sales_raw.csv      # Original dataset with quality issues
│   └── ecommerce_sales_clean.csv    # Cleaned and processed dataset
│
├── notebooks/
│   ├── sales_performance.ipynb      # Main analysis notebook
│   ├── visualization.ipynb          # Visualization generation
│   └── queries.ipynb                # SQL analysis queries
│
├── visualizations/
│   ├── 1_revenue_trend.png
│   ├── 2_category_performance.png
│   ├── 3_regional_distribution.png
│   ├── 4_top_products.png
│   ├── 5_day_of_week.png
│   ├── 6_payment_methods.png
│   ├── 7_quarterly_comparison.png
│   └── 8_heatmap_category_month.png
│
├── ecommerce.db                     # SQLite database
└── README.md                        # Project documentation
```

---

## Analysis Workflow

### 1. Data Quality Assessment

**Issues Identified:**
- Missing values: 875 records (2% of dataset)
  - Region: 438 missing values (1.0%)
  - Payment Method: 437 missing values (1.0%)
- Duplicate records: 50 transactions (0.11%)
- Data validation: Verified date ranges, price constraints, and quantity limits

### 2. Data Cleaning Process

**Steps Implemented:**
- Removed 50 duplicate transactions
- Imputed missing values using mode imputation
- Created additional date-based features:
  - Year, Month, Quarter
  - Day of week, Weekend indicator
  - Month name for visualization
- Engineered new metrics:
  - Total revenue (amount + shipping)
  - Transaction categorization
- Validated data integrity post-cleaning

**Result**: Clean dataset of 43,736 transactions ready for analysis

### 3. Exploratory Data Analysis

#### Business Metrics Summary

| Metric | Value |
|--------|-------|
| Total Revenue | $3,590,832 |
| Total Transactions | 43,736 |
| Average Order Value | $82.10 |
| Unique Customers | 4,001 |
| Transactions per Customer | 10.93 |

#### Category Performance

| Category | Revenue | Share | Avg Revenue |
|----------|---------|-------|-------------|
| Home | $1,170,516 | 32.6% | $106.39 |
| Electronics | $1,141,369 | 31.8% | $77.45 |
| Sports | $890,580 | 24.8% | $81.88 |
| Office | $388,367 | 10.8% | $54.54 |

#### Top 5 Products by Revenue

1. Running Shoes: $591,133 (16.5% of total revenue)
2. Kitchen Knife Set: $506,939 (14.1%)
3. Coffee Maker: $457,405 (12.7%)
4. Wireless Earbuds: $403,147 (11.2%)
5. Bluetooth Speaker: $357,302 (9.9%)

#### Regional Distribution

| Region | Revenue | Transactions | Market Share |
|--------|---------|--------------|--------------|
| Central | $758,734 | 9,266 | 21.1% |
| North | $718,135 | 8,703 | 20.0% |
| South | $712,035 | 8,643 | 19.8% |
| West | $706,624 | 8,582 | 19.7% |
| East | $695,304 | 8,542 | 19.4% |

---

## Key Findings

### 1. Strong Seasonal Patterns

**Q4 Performance Dominance**
- November revenue: $209,209 (51% above monthly average)
- December revenue: $214,716 (highest single month)
- Q4 2023 total: $423,925 (45% higher than Q1-Q3 average)

**Insight**: Strong holiday season impact creates predictable revenue spikes requiring strategic inventory planning.

### 2. Product Revenue Concentration

**High Dependency Risk**
- Top 3 products account for 43.3% of total revenue
- Top 10 products represent 62.1% of revenue
- Significant concentration in premium items (Running Shoes, Kitchen Sets)

**Insight**: Revenue concentration presents risk; diversification strategy recommended.

### 3. Category Insights

**Home Category Leadership**
- Highest average order value ($106.39)
- Strong margin potential
- Lower transaction volume suggests premium positioning

**Electronics Volume Leader**
- Highest transaction count (14,736)
- Lower average order value ($77.45)
- High-volume, moderate-margin category

### 4. Customer Behavior Patterns

**Strong Retention Metrics**
- Average 10.93 transactions per customer
- Consistent purchase behavior across weekdays and weekends
- No significant payment method preference (all ~25%)

**Weekend Analysis**
- Weekend transactions: 34.6% of total volume
- Average order value nearly identical: $82.18 (weekday) vs $81.95 (weekend)

### 5. Geographic Performance

**Balanced Distribution**
- All regions contribute 19-21% of total revenue
- Central region leads slightly ($758,734)
- East region underperforms by $63,430 (8.4% below Central)

**Insight**: Geographic consistency indicates good market coverage; investigate East region performance gap.

---

## Business Recommendations

### Immediate Actions (0-3 Months)

**1. Q4 Inventory Optimization**
- Increase stock levels 50-70% for top performers in October
- Focus on: Running Shoes, Kitchen Sets, Coffee Makers
- Prepare fulfillment capacity for 2x normal volume

**2. Revenue Diversification**
- Develop "next tier" products to reduce concentration risk
- Launch 2-3 new products per quarter
- Target products in $50-$80 price range to fill portfolio gap

**3. East Region Investigation**
- Conduct regional market analysis
- Survey customer satisfaction and preferences
- Consider region-specific marketing campaigns

### Medium-Term Initiatives (3-6 Months)

**4. Home Category Expansion**
- Home has highest AOV but lowest transaction volume
- Opportunity: Increase market share through targeted marketing
- Create product bundles combining home and electronics items

**5. Customer Segmentation Strategy**
- Segment by purchase frequency and lifetime value
- Develop targeted retention programs
- Focus on reactivating low-frequency customers

**6. Seasonal Campaign Calendar**
- Q4 Pre-Holiday Campaign (October): Early bird promotions
- Q1 Recovery Campaign (January): New Year sales
- Summer Engagement (June-August): Maintain momentum

### Long-Term Strategy (6-12 Months)

**7. Advanced Analytics Implementation**
- Customer Lifetime Value (CLV) modeling
- Predictive inventory management
- Churn prediction and prevention models
- Dynamic pricing optimization

**8. Product Portfolio Optimization**
- Evaluate Office category performance (10.8% share)
- Consider expansion in high-performing categories
- Test new price points in $90-$150 range

---

## Technical Skills Demonstrated

### Data Analysis
- Data quality assessment and validation
- Missing value imputation strategies
- Duplicate detection and removal
- Statistical analysis and summarization
- Trend identification and pattern recognition

### Python Programming
- Pandas for data manipulation and aggregation
- NumPy for numerical operations
- Data type handling and transformation
- GroupBy operations and multi-level aggregation

### Data Visualization
- Matplotlib and Seaborn for professional charts
- Time series visualization
- Category comparison charts
- Geographic distribution analysis
- Heatmap creation for multi-dimensional data

### SQL Proficiency
- Database creation and table design
- Complex SELECT queries with aggregations
- JOINs and subqueries
- Window functions for advanced analysis
- Performance optimization

### Business Intelligence
- KPI identification and tracking
- Metric calculation and interpretation
- Business insight generation
- Actionable recommendation development
- Stakeholder-ready reporting

---

## Visualizations

### Revenue Trend Analysis
Time series showing monthly revenue patterns with clear Q4 seasonality spike.

### Category Performance Comparison
Side-by-side analysis of revenue and transaction volume by product category.

### Regional Distribution
Pie chart displaying balanced geographic revenue distribution across 5 regions.

### Top Products Analysis
Horizontal bar chart identifying top 10 revenue-generating products.

### Day of Week Patterns
Revenue comparison showing weekend vs weekday performance.

### Payment Method Distribution
Transaction count analysis across all payment types.

### Quarterly Comparison
Year-over-year quarterly revenue comparison (2022 vs 2023).

### Category-Month Heatmap
Two-dimensional visualization showing seasonal category performance patterns.

---


### Running the Analysis
```bash
# Launch Jupyter Notebook
jupyter notebook

# Open and run notebooks in order:
# 1. sales_performance.ipynb    - Main analysis
# 2. visualization.ipynb         - Generate charts
# 3. queries.ipynb              - SQL analysis
```

---

## Future Enhancements

### Planned Additions

**Predictive Analytics**
- Sales forecasting using time series models (ARIMA, Prophet)
- Customer churn prediction
- Product recommendation engine
- Demand forecasting by category

**Advanced Segmentation**
- RFM (Recency, Frequency, Monetary) analysis
- Customer clustering using K-means
- Cohort analysis for retention tracking
- Customer lifetime value modeling

**Interactive Dashboards**
- Tableau/Power BI dashboard creation
- Real-time KPI monitoring
- Drill-down capabilities for detailed analysis
- Executive summary views

**A/B Testing Framework**
- Promotion effectiveness testing
- Price optimization experiments
- Marketing channel attribution

---