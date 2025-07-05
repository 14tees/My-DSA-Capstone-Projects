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






📘 
### **Documentation: Palmora Group HR Analysis Case Study** ###
👤 **Role**
HR Analytics Expert
Hired by CHRO of Palmora Group to uncover insights around gender inequality, pay gaps, and regulatory compliance.

🎯 **Objective**
Analyze HR data to:

Explore gender distribution, pay gap, and regional patterns

Clean and transform the data to remove null values and exited staff

Assign bonuses based on performance ratings

Deliver interactive visual insights using Power BI

📁 **Data Cleaning & Preparation**
🧹 Data Cleaning Steps (in Excel or Power BI Power Query Editor)
Task	Action
1. Handle Missing Genders	Replace null/blank gender values with "Undisclosed"
2. Remove Exited Employees	Filter out rows with null or 0 salary
3. Remove Null Departments	Filter out rows where Department = NULL or is blank
4. Bonus Rules	Merge bonus rules dataset with main HR dataset using performance rating
5. Add Computed Fields	- Bonus Amount = Salary × Bonus %
- Total Compensation = Salary + Bonus
- Salary Band (bin) using Power BI binning

📊 **Analysis Areas & Power BI Visualizations**
1️⃣ Gender Distribution
Visuals: Donut Chart, Stacked Column Chart

Breakdowns:

Overall Gender Split

Gender Distribution by Region

Gender Distribution by Department

2️⃣ Performance Ratings by Gender
Visuals: Clustered Column Chart or Box Plot

Breakdowns:

Average Performance Rating by Gender

Rating Distribution by Gender

3️⃣ Salary Structure & Gender Pay Gap
Visuals:

Line Chart (Average Salary by Gender)

Matrix/Table (Avg Salary by Gender & Department)

Decomposition Tree (Drill down Pay Gap by Region > Dept)

💡 Insights to Derive:
Compare male vs female average salary in:

Overall organization

Each region

Each department

4️⃣ Minimum Wage Compliance
Visuals:

Column Chart (Employees by Salary Band)

KPI Card for % Employees < $90,000

Regional Bar Chart (Compliance rate per region)

💡 Insights to Derive:
Number of employees earning below $90,000

Region(s) with the most non-compliant salaries

5️⃣ Bonus Allocation Analysis
Steps:

Join performance rating data with bonus rules

Compute:

Bonus Amount = Salary × Bonus %

Total Compensation = Salary + Bonus

Aggregate:

Total Bonus per Region

Total Company-wide Bonus Allocation

Visuals:

Stacked Column Chart (Total Payout by Region)

Card Visual (Total Bonus Cost)

Matrix/Table of Individual Bonuses

🖼️ **Power BI Report Page Layout**
📄 Page 1: Executive Summary
KPI Cards:

Avg Gender Pay Gap

Compliance with $90k Policy

Total Bonus Budget

Donut: Gender Split

Bar: Employees by Region

📄 Page 2: Gender Pay & Ratings
Matrix: Avg Salary by Gender, Dept, Region

Bar: Rating by Gender

📄 Page 3: Salary Band Analysis

Clustered Bar: Salary Band by Region

KPI: Employees < $90k

📄 Page 4: Bonus Analysis
Table: Bonus per Employee

Column: Total Bonus by Region

KPI: Total Compensation Cost

🧠 **Recommendations Based on Insights**
Implement a salary review in regions/departments with large gender pay gaps.

Increase transparency in performance rating criteria to eliminate unconscious bias.

Ensure all salaries comply with the $90k minimum wage regulation.

Create an annual budget cap for bonuses to manage expenses effectively.

📎 **Deliverables**
Power BI .pbix report file

Documentation of assumptions, transformations, and KPIs 

