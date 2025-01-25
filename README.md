---

# E-commerce Data Analysis Project

## Objective
The goal of this project is to analyze historical e-commerce data to uncover trends and provide actionable insights that will improve sales, customer retention, and operational efficiency.

---

## Problems Identified
- Analyzing historical sales trends and identifying top-performing product categories.
- Understanding customer retention rates and recognizing returning customers.
- Pinpointing regions with high and low sales performance and investigating the reasons behind these differences.
- Evaluating the impact of delivery status on sales and customer satisfaction.
- Exploring how shipping options affect delivery performance and customer experience.
- Segmenting customers to identify patterns in preferences, behavior, or demographics.

---

## Target Audience
- **Primary Users**: E-commerce management, marketing, and operations teams.
- **Secondary Users**: Data analysts, business analysts, and stakeholders focused on sales performance and customer behavior.

---

## Use Cases
### Sales Trends Analysis
- **User Story**: As a sales manager, I want to track historical sales trends to plan inventory and optimize future sales campaigns.
- **Acceptance Criteria**: The dashboard should show monthly, seasonal, and annual trends by category with filtering capabilities.
- **Benefits**: Improved forecasting and inventory management.

### Customer Retention and Loyalty
- **User Story**: As a marketing analyst, I want insights on returning customers to design loyalty programs and targeted campaigns.
- **Acceptance Criteria**: The dashboard must display customer retention rates and trends over time.
- **Benefits**: Enhanced marketing ROI and customer loyalty.

### Regional Performance Evaluation
- **User Story**: As an operations manager, I need to assess regional sales performance to allocate resources efficiently.
- **Acceptance Criteria**: The dashboard highlights sales and delivery performance by region.
- **Benefits**: Optimized regional operations and logistics.

---

## Success Criteria
- Clear identification of sales trends and product performance.
- Insights into customer retention rates and behaviors.
- Comprehensive regional performance analysis.
- Assessment of delivery and shipping efficiency.
- Effective segmentation of customers for targeted strategies.

---

## Data Needed
- **Fields**: customer_id, customer_full_name, category_name, product_name, customer_segment, customer_city, customer_state, customer_country, customer_region, delivery_status, order_date, order_id, ship_date, shipping_type, order_item_discount, sales_per_order, order_quantity, profit_per_order.

---

## Steps Taken in Power Query
1. **Concatenation**: Created a composite key for unique identification:
   ```m
   [customer_full_name] & "_" & [category_name] & "_" & [product_name] & "_" & [customer_segment] & "_" & [customer_city] & "_" & [customer_state]
   ```
2. **Grouping**: Grouped data by the composite key to resolve ID clashes.
3. **Unique Identifier**: Generated unique IDs using:
   ```m
   "C_ID_" & Number.ToText(Number.RoundDown(Number.RandomBetween(100000, 999999)))
   ```
4. **Expansion**: Expanded grouped data for detailed analysis.

---

## Key Findings
### Sales Trends
- Sales reached $25.23 million, with top-performing categories being office supplies (60.14%), furniture (21.63%), and technology (18.23%).
- Seasonal trends reveal potential peak periods to optimize inventory and marketing efforts.

### Customer Retention
- Customer retention is at 14.27%, with a clear opportunity to improve through loyalty programs and personalized campaigns.

### Regional Performance
- Central and East regions show the highest on-time delivery rates, with tight competition between them. These regions also have consistent sales performance, indicating reliable operations.

### Delivery and Sales
- Delivery delays significantly impact customer satisfaction and sales, emphasizing the need for better logistics.

### Shipping and Delivery
- Standard shipping dominates but shows room for improvement in speed and reliability. Expedited and same-day shipping could enhance the customer experience.

### Customer Segmentation
- Consumers account for 51.75% of sales, followed by corporate customers at 30.32%. These segments can be leveraged for targeted campaigns.

---

## Recommendations
1. **Improve Customer Retention**: Implement loyalty programs and targeted campaigns for returning customers to boost retention from the current 14.27%.
2. **Optimize Delivery Performance**: Focus on enhancing delivery efficiency in lagging regions to match Central and East's success.
3. **Expand Product Marketing**: Promote high-demand categories (office supplies) while exploring growth in furniture and technology.
4. **Enhance Shipping Options**: Invest in faster shipping methods to attract customers willing to pay for convenience.
5. **Leverage Segmentation Insights**: Use consumer and corporate segmentation to design more effective marketing campaigns.

---

## Conclusions
- The analysis highlights significant opportunities to improve customer satisfaction, operational efficiency, and sales strategies.
- Regional and segment-specific insights offer actionable pathways for targeted interventions.
- Data-driven decisions will enable the business to adapt to customer needs, streamline operations, and maximize profitability.

---

## Link to Dashboard
Explore the full interactive dashboard [here](https://app.powerbi.com/view?r=eyJrIjoiYWM1ZjJjN2MtOGUxNi00MDk1LWFlNjUtMWYwNTJjMmIwMGZkIiwidCI6IjUxN2QzNTAyLTI5MDEtNGRlMi1hODdiLTk1YzUwN2E5YTA4OCJ9).

---
