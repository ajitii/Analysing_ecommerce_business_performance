# Analyzing eCommerce Business Performance

## Overview
This project provides a comprehensive analysis of eCommerce business performance by examining critical factors such as customer growth, product quality, and payment types. Utilizing SQL for data analysis and visualization tools for presenting findings, this project aims to offer actionable insights that can help optimize business strategies.

## Table of Contents
- 1.Project Background
- 2.Dataset
- 3.Installation
- 4.Usage
- 5.Analysis Methods
- 6.Results and Insights
- 7.Visualizations
- 8.Future Improvements
- 9.Contributing
- 10.License
- 11.Acknowledgments

## Project Background
Measuring business performance is essential for any eCommerce company to assess market trends, understand customer behavior, and identify new opportunities. This project utilizes a dataset consisting of 100,000 orders made at various marketplaces in Brazil from 2016 to 2018.

## Dataset
The dataset used for this analysis is sourced from Rakamin Academy. It includes:

- Order Status: The current status of each order.
- Price: The total cost of the purchase.
- Payment Method: Types of payment made by customers.
- Customer Demographics: Information regarding customer locations and preferences.
- Product Attributes: Information about the products purchased.
- Customer Reviews: Feedback provided by customers.

## Dataset Structure
Column Name	Description
- order_id	Unique identifier for each order
- product_category	Category of the product
- customer_id	Unique identifier for each customer
- payment_type	Method of payment used
- order_status	Status of the order
- order_date	Date when the order was placed
- revenue	Revenue generated from the sale

## Installation
Prerequisites
- SQL Database: PostgreSQL or similar relational database system
- Python (optional for data visualization)
- Visualization Tools: Google Data Studio or Tableau (for generating interactive dashboards)

# Setup Database
- Create a new PostgreSQL database.
- Import the CSV files from the dataset folder into your database following the structure defined above.
- Make sure to create the appropriate tables and relationships as described.

![image](https://user-images.githubusercontent.com/77976107/173325369-97674007-82ba-42e1-92eb-52c7bd6bcf59.png)
<br>Figure 1. Data Relationship

![image](https://user-images.githubusercontent.com/77976107/173325708-61b334a7-d55b-466c-9055-39ea48c60869.png)
<br>Figure 2. Entity Relationship Diagram


## Usage
- 1.Open your SQL environment (e.g., pgAdmin, MySQL).
- 2.Run the provided SQL scripts located in the Query folder to analyze the dataset.
- 3.Generate insights on customer behavior, product quality, and payment types.

# Sample Queries
- Top Selling Products:

sql:
- SELECT product_category, SUM(revenue) AS total_revenue
- FROM orders
- GROUP BY product_category
- ORDER BY total_revenue DESC;

- Customer Growth Over Time:

- sql:
- SELECT DATE_TRUNC('month', order_date) AS month, COUNT(DISTINCT customer_id) AS new_customers
- FROM orders
- GROUP BY month
- ORDER BY month;

## Analysis Methods
This project employs the following analysis methods:

- Descriptive Statistics: To summarize the main characteristics of the data.
- Trend Analysis: To track changes in customer growth and sales over time.
- Cohort Analysis: To evaluate customer behavior segments based on purchase patterns.
- Data Visualization: Utilizing Google Data Studio for interactive dashboards.

## Results and Insights
Key Insights
- Customer Growth: Analyze the trends in new customer acquisition across different timeframes.
- Revenue Generation: Identify product categories with the highest and lowest sales performance.
- Payment Preferences: Evaluate shifts in payment methods over the years, identifying opportunities for targeted marketing.

## Visualizations
Effective visualizations are crucial in understanding the data. Below are some example visualizations that could be included in this project:

1. Customer Growth Over Time
![image](https://user-images.githubusercontent.com/77976107/173325968-5e8e23a5-59f4-4450-aed8-551590d00883.png)

2. Top Selling Product Categories
![image](https://user-images.githubusercontent.com/77976107/173326674-9c184bc8-cc65-4b69-a7d9-1d97dc33f94f.png)

3. Payment Method Preferences
![image](https://user-images.githubusercontent.com/77976107/173327174-1d594f7c-c2e6-4bb6-9c3b-b8503e9b2fbb.png)

## Future Improvements
- Enhance Documentation: Provide more elaborate explanations of each analysis step.
- Add Predictive Analytics: Incorporate machine learning models to forecast future sales trends.
- Expand Dataset: Include more recent data to assess ongoing trends and patterns.
- User Interface: Develop a web interface or app for easier data interaction and exploration.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## License
## Acknowledgments
Rakamin Academy for providing the dataset.
Tools and resources used for data visualization like Google Data Studio and Tableau.















