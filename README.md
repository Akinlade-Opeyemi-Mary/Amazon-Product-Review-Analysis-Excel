# Amazon-Product-Review-Analysis-Excel
📊 Excel Case Study  Analyzing Amazon product reviews to uncover insights on pricing, discounts, ratings, and customer engagement. Includes pivot tables, data cleaning, and an interactive Excel dashboard

# 📘 INTRODUCTION

In the fast-paced world of e-commerce, customer reviews and pricing strategies play a crucial role in influencing buyer behavior. Sellers on platforms like **Amazon** must continuously analyze feedback, ratings, and product performance to stay competitive and improve sales outcomes.

This case study places me in the role of a **Junior Data Analyst** at *RetailTech Insights*, a company focused on delivering data-driven insights to online retailers. Leveraging Microsoft Excel, I explored a dataset of over **1,400 Amazon products** to uncover trends in ratings, review counts, pricing, and discounts.

The primary focus of this analysis was to answer key business questions, such as:

- 🏷️ Which product categories are performing best?  
- 📉 What is the relationship between discounts and customer ratings?  
- 💰 How are products distributed across pricing ranges?  
- 🎯 Where should sellers concentrate their efforts to boost engagement and revenue?

# 🏢 BACKGROUND

As a **Junior Data Analyst** at *RetailTech Insights*, a fictional e-commerce analytics company, I was tasked with analyzing product review data scraped from Amazon. This project simulates a real-world business analytics workflow from raw data preparation to visual dashboard delivery with the goal of guiding product strategy and performance evaluation for online sellers.

The analysis focuses on interpreting product metrics such as ratings, discount levels, review volume, and pricing. It aims to help businesses understand customer feedback trends, evaluate which products and categories are performing well, and discover how pricing and discount strategies influence customer behavior. Additionally, it highlights areas where marketing and promotional efforts can be optimized to improve sales performance.

This hands-on case study reflects the type of product intelligence work commonly required by e-commerce teams to remain competitive, data-driven, and customer focused in a saturated marketplace.

# 🎯 Objectives

This analysis focused on generating actionable insights for e-commerce sellers using Amazon product review data. The key objectives were:

1. Determine the average discount percentage across different product categories.  
2. Identify how many products are listed within each category.  
3. Analyze the total number of customer reviews per product category.  
4. Find out which products have the highest average customer ratings.  
5. Compare the average actual price versus the discounted price across categories.  
6. Identify products with the highest number of reviews.  
7. Determine how many products offer discounts of 50% or more.  
8. Analyze the distribution of product ratings (e.g., 3.0, 4.0, 5.0, etc.).  
9. Calculate the total potential revenue per category using actual price and rating count.  
10. Classify products into price range buckets (e.g., under ₹200, ₹200–₹500, over ₹500) and count how many fall into each.  
11. Explore how discount levels correlate with customer ratings.  
12. Identify how many products have fewer than 1,000 reviews.  
13. Highlight which categories contain the highest-discounted products.  
14. Rank the top five products based on a combination of rating and review volume.

These objectives guided the creation of pivot tables, calculated columns, and visual dashboards that support better product positioning, pricing decisions, and customer engagement strategies.

# 📂 SOURCES

**Dataset Origin**:  
This dataset was provided by Digital Skills Africa / The Incubator Hub as part of the Excel capstone project. https://canvas.instructure.com/courses/11955369/files/folder/DSA%20Capstone%20Project%20Files?preview=302721273

**Dataset Overview**:  
The dataset contains **1,465 rows** and **20 columns**, with each row representing a unique product and its aggregated review data.

**Primary Columns Included**:

- `Product_Id`: Unique identifier for each product  
- `Product_Name`: Name or title of the product  
- `Category`: The product category (e.g., Electronics, Books, Clothing)  
- `Discounted_Price`: Current price after discount  
- `Actual_Price`: Original price before discount  
- `Discount Percentage`: Calculated % off between actual and discounted price  
- `Rating`: Average customer rating  
- `Rating_Count`: Total number of ratings  
- `Price Bucket Range`: Custom-calculated field grouping products by price (e.g., <₹200, ₹200–₹500, >₹500)  
- `Discount >=50`: Flag for products with 50% or more discount (TRUE/FALSE)  
- `Potential Revenue`: Estimated revenue = Actual_Price × Rating_Count  
- `Average Rating`: Calculated average rating across product categories  
- `About_Product`: Short description of the product  
- `User_Id`: ID of the reviewer  
- `Username`: Name or alias of the reviewer  
- `Review_Id`: Unique identifier for each review  
- `Review_Title`: Title of the customer review  
- `Review_Content`: Full content/body of the customer review  
- `Img_Link`: Image link for the product (optional)  
- `Product_Link`: Link to the Amazon product page

This structured dataset enabled deep exploration of consumer behavior, discount strategies, and category-level performance for better decision-making and dashboard storytelling.

## 🛠 Tools Used for the Analysis

The entire analysis was conducted in **Microsoft Excel**, leveraging its data exploration, transformation, and visualization features to derive meaningful business insights from Amazon product review data.

- **Pivot Tables** were used extensively to summarize average discounts by category, count products, total review volumes, analyze rating distributions, and compare actual vs discounted prices.

- **Calculated Columns** were created to derive custom metrics such as:
  - `Discount Percentage`
  - `Revenue` (Actual Price × Rating Count)
  - `Price Bucket Range` (e.g., <₹200, ₹200–₹500, >₹500)
  - `Discount ≥ 50%` (Boolean flag)

- **Sorting & Filtering** enabled quick identification of top-rated products, most-reviewed items, and products with extreme discount values.

- **Excel Functions** like `IF()`, `COUNTIF()`, `AVERAGE()`, and basic arithmetic were used for conditional logic and data transformation.

- **Charts & Graphs** (including bar charts, pivot charts, and line chart) were used to visualize relationships such as between rating and discount level and display product rating distributions.

- **Dashboard Features** like slicers, formatted cards, and conditional formatting were used to design an interactive and visually engaging report.

Together, these tools provided a full pipeline from raw data interpretation to business-focused storytelling using Excel.

# 📈 ANALYSIS

### 🔍 Question 1: What is the average discount percentage by product category?

#### 📌 Approach:
To answer this, I used a **Pivot Table** where:
- `Product Category` was placed in the **Rows**
- `Discount Percentage` was placed in the **Values** and summarized as **Average**

#### 📈 Result:
Below is a snapshot of the average discount across different product categories:

![Alt text](https://github.com/Akinlade-Opeyemi-Mary/Amazon-Product-Review-Analysis-Excel/blob/615e0caaaccbc0bcfe1ccbbf39e1b17b4ff6064a/AVERAGE%20PRODUCT%20CATEGORY.JPG)

> 💡 **Insight:**  
> Categories such as *Mobile Accessories, Earpads, Internal Hard Drives,* and *OTG Adapters* have average discounts of over **70–90%**, indicating heavy promotional pricing strategies.  
> This may be an effort to boost visibility or clear out overstocked items.  
> On the other hand, essential or high-end products (e.g., laptops, ink cartridges, home appliances) tend to have much **lower discounts (10–30%)**, possibly to retain premium value.

#### 🎯 Business Implication:
- Sellers may focus high discounts on mobile and headphone accessories to attract price-sensitive customers.
- Categories with lower discounts may rely on **brand strength** or **differentiated features**, not price competition.

