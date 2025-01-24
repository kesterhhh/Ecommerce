# E-commerce Data Analysis Project

## Objective
The goal of this project is to analyze historical e-commerce data to uncover trends and provide actionable insights that will help improve sales, customer retention, and operational efficiency.

## Problems Identified
- Identifying historical sales trends and top-performing product categories.
- Calculating customer retention rates and identifying returning customers.
- Pinpointing regions with high and low sales performance and understanding the reasons behind these differences.
- Assessing the impact of delivery status on sales and customer satisfaction.
- Analyzing the influence of different shipping options on delivery performance.
- Performing customer segmentation to identify groups based on preferences, behavior, or demographics.

## Target Audience
- **Primary Users**: E-commerce store management team, marketing team, and operations team.
- **Secondary Users**: Data analysts, business analysts, and stakeholders interested in sales performance and customer behavior.

## Use Cases
### Sales Trends Analysis
- **User Story**: As a sales manager, I want to identify historical sales trends to forecast future sales and plan inventory accordingly.
- **Acceptance Criteria**: The dashboard should display monthly, seasonal, and annual sales trends with the ability to filter by product category.
- **Benefits**: Improved inventory management and sales forecasting.

### Customer Retention and Loyalty
- **User Story**: As a marketing analyst, I want to calculate the customer retention rate and identify returning customers to design targeted marketing campaigns.
- **Acceptance Criteria**: The dashboard should show the percentage of returning customers and retention rates over time.
- **Benefits**: Enhanced customer loyalty and targeted marketing efforts.

## Success Criteria
- Accurate identification of sales trends and top-performing product categories.
- Clear insights into customer retention rates and returning customers.
- Detailed analysis of geographical sales performance.
- Comprehensive assessment of delivery status impact on sales and customer satisfaction.
- Effective customer segmentation based on preferences, behavior, or demographics.

## Information Needed
- Historical sales trends (monthly, seasonal, annual).
- Top-performing product categories.
- Customer retention rates and returning customers.
- Geographical sales performance.
- Impact of delivery status on sales and customer satisfaction.
- Influence of different shipping options on delivery performance.
- Customer segmentation insights.

## Data Needed
- **Field Names**: customer_id, customer_full_name, category_name, product_name, customer_segment, customer_city, customer_state, customer_country, customer_region, delivery_status, order_date, order_id, ship_date, shipping_type, order_item_discount, sales_per_order, order_quantity, profit_per_order.

## Data Quality Checks
- Row counts and column counts.
- Checking for duplicates.
- Verifying data types.
- Ensuring no missing values in critical fields.

## Steps Taken in Power Query
1. **Concatenation**: Created a new column by concatenating the following fields:
   ```m
   [customer_full_name] & "" & [category_name] & "" & [product_name] & "" & [customer_segment] & "" & [customer_city] & "_" & [customer_state]
   ```
2. **Grouping**: Grouped data by the new concatenated column to ensure unique customer IDs.
3. **Creating Custom Column**: Added a new custom column with a unique identifier using the formula:
   ```m
   "C_ID_" & Number.ToText(Number.RoundDown(Number.RandomBetween(100000, 999999)))
   ```
4. **Expanding**: Expanded the grouped data to include all necessary fields for analysis.

**Note**: These steps were necessary due to the excessive clashes of supposed unique IDs in the original dataset.

## Key Findings
### Sales Trends
- Identified monthly, seasonal, and annual sales patterns.
- Highlighted top-performing product categories contributing significantly to overall revenue.

### Customer Retention
- Calculated customer retention rate.
- Identified the percentage of returning customers, providing insights for targeted marketing campaigns.

### Geographical Performance
- Pinpointed regions with high and low sales performance.
- Evaluated possible reasons behind sales differences, such as demographics and logistics.

### Delivery and Sales Relationship
- Assessed how delivery status (on-time, delayed, canceled) impacts sales and customer satisfaction in various regions.

### Shipping Type vs. Delivery Performance
- Analyzed how different shipping options (standard, expedited, same-day) influence delivery performance.

### Customer Segmentation
- Performed customer segmentation to identify groups based on preferences, behavior, or demographics.
- Discovered which segments show the most interest in specific products or categories.


## Link to Dashboard
Explore the full interactive dashboard [here](https://app.powerbi.com/view?r=eyJrIjoiYWM1ZjJjN2MtOGUxNi00MDk1LWFlNjUtMWYwNTJjMmIwMGZkIiwidCI6IjUxN2QzNTAyLTI5MDEtNGRlMi1hODdiLTk1YzUwN2E5YTA4OCJ9)

