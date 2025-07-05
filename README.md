# My-DSA-Capstone-Projects
This is a documentation on how I worked on my DSA Project Question
## QUESTION 1 & 3
📘
### **Amazon Product Review Analysis – Documentation Report** ###

👤 **Role**
Junior Data Analyst, RetailTech Insights

📝 **Objective**
To analyze Amazon product and review data in order to generate insights that support product improvement, marketing strategy, and customer engagement initiatives.

📂 **Dataset Overview**
File: Amazon case study.xlsx

Rows: 1,348

Columns: 23

Data Sources:

Product details (name, category, prices, ratings)

Customer engagement (user IDs, reviews, titles)

Computed fields (discount %, potential revenue)

🧮**Data Cleaning & Preparation**
Loaded dataset into Excel

Verified:

No missing values in key columns (product_id, category, discount_percentage, rating_count).

Columns like rating_count and discount_percentage were converted to numeric formats.

Created calculated fields:

Total Revenue = actual_price × rating_count

High Discount = IF(discount_percentage ≥ 0.5, "Yes", "No")

Rating + Review Score = rating + (rating_count / MAX(rating_count))

📊 **Pivot Table Construction (Excel)**
Task	Description	Pivot Table Setup
1. Average Discount by Category	To identify pricing strategy by category	Main Category as Rows, discount_percentage as Values (Average)
2. Product Count by Category	Understand product distribution	Main Category as Rows, product_id as Values (Count)
3. Total Reviews by Category	Analyze customer engagement	Main Category as Rows, rating_count as Values (Sum)
4. Average Prices	Compare actual vs. discounted price	Main Category as Rows, actual_price & discounted_price as Values (Average)
5. Products by Price Range	Group product tiers	Price Range Bucket as Rows, product_id as Values (Count)
6. Review Distribution	Rating trend analysis	rating as Rows, product_id as Values (Count)

🥇 **Insight-Based Analysis**
Insight Task	Approach Taken
Highest Rated Products	Sorted data by rating (descending)
Most Reviewed Products	Sorted data by rating_count
Products with 50%+ Discount	Used =COUNTIF(discount_percentage, ">=0.5")
Products <1,000 Reviews	Used filter or COUNTIF(rating_count, "<1000")
Highest Discounted Categories	Sorted pivot with average discounts
Top 5 Products (Rating + Reviews)	Created a new column with combined score and sorted

📈 **Dashboard Development**
Tools Used: Microsoft Excel
Sheets Created:

Raw Data: Cleaned original dataset

Pivot Tables: Contained all analysis tasks

Dashboard: Presented summaries and visuals

Dashboard Components:
Element	Description
KPI Tiles	Total Products, Total Reviews, Avg Discount, Revenue
Charts	Bar (Avg Discount by Category), Pie (Product Count), Column (Reviews by Category), Scatter (Rating vs Discount)
Slicers	Used for Main Category and Price Range Bucket
Interactive Elements	All visuals are linked to slicers for dynamic filtering

🎯 **Key Findings**
Electronics and Computers & Accessories had the highest product count and total reviews.

Categories like Home Improvement showed the highest average discount.

Top-rated products were not necessarily the most reviewed.

Many products received heavy discounts (≥ 50%), which can affect pricing strategies.

A significant number of products had <1,000 reviews, suggesting improvement areas for promotion or visibility.

📁 **Deliverables**
Amazon case study.xlsx (with Raw Data, Analysis, and Dashboard sheets)

Pivot Tables for 14 analysis tasks

Interactive Dashboard with slicers and KPI metrics


💡 **Recommendations**
Focus on top-rated but under-reviewed products to increase awareness.

Use discount strategy smartly to drive engagement without undervaluing product categories.

Encourage verified reviews to boost product credibility.
