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

## 1. What is the average discount percentage by product category?

### 📌 Approach:
This analysis was conducted using a **Pivot Table** in Excel:
- `Product Category` was added to **Rows**
- `Discount Percentage` was added to **Values**, summarized as **Average**

### 📈 Result:
A snapshot of the pivot output shows the **average discount percentage** applied across all product categories.

![Alt text](https://github.com/Akinlade-Opeyemi-Mary/Amazon-Product-Review-Analysis-Excel/blob/ec96f0d1637f6bca0e3c207ee41117cef726e746/AVERAGE%20PRODUCT%20CATEGORY.JPG)
### 💡 Insight:
- Categories like **Mobile Accessories**, **Earpads**, **Internal Hard Drives**, and **OTG Adapters** show **extremely high average discounts** (70%–90%), indicating **heavy promotional efforts**.  
  These may be clearance strategies, loss leaders, or tactics to boost listing visibility.

- Conversely, **premium and essential items** such as **Laptops**, **Ink Cartridges**, and **Home Appliances** show **lower average discounts** (10%–30%), suggesting efforts to **preserve brand value** and maintain **profit margins**.

### 🎯 Business Implication:
- Heavy discounting could be leveraged to **drive traffic** or **clear excess stock**.
- Low-discount categories likely represent **core revenue drivers** with **stable demand** and **pricing power**.

---

## 2. How many products are listed under each product category?

### 📌 Approach:
Used an **Excel Pivot Table** where:
- `Product Category` was added to **Rows**
- `Product Name` was counted in **Values** (Count)

### 📈 Result:
A snapshot of the pivot output shows the **average discount percentage** applied across all product categories.

![Alt text](https://github.com/Akinlade-Opeyemi-Mary/Amazon-Product-Review-Analysis-Excel/blob/b7a2e01a7f5598e2f8cb1c6a9bad60ede23f704d/category.JPG)


### 🔍 Key Findings:
- **Top category**:
  - `USB Cables` – **233 products**

- Other high-volume categories:
  - **Smartwatches** – 76 products  
  - **Smartphones** – 68 products  
  - **Smart Televisions** – 63 products  
  - **In-Ear Headphones** – 52 products

- **Low-volume or niche categories** (1–3 products each):
  - **Traditional Laptops**, **Earpads**, **Air Purifiers**, **Memory**, **Webcams**, etc.

### 💡 Insight:
- The data shows a **strong market focus** on **accessories and smart devices**, suggesting **high demand** or **low barrier to entry** in these segments.
- Categories with **very few listings** may represent:
  - **Untapped niches**
  - **Supply gaps**
  - Or **emerging demand areas**

### 🎯 Business Implication:
- Sellers can focus on **expanding inventory** in trending categories like smart accessories.
- Niche categories offer opportunities for **early positioning** or **product diversification**.

## 3. What is the total number of reviews per product category?

### 📌 Approach:
Used an **Excel Pivot Table** where:
- `Product Category` was added to **Rows**
- `Review_Id` was counted in **Values** (Count)

### 📈 Result:
A snapshot of column chart displaying the **top 10 categories by total review count** for clearer interpretation.

![Alt text](https://github.com/Akinlade-Opeyemi-Mary/Amazon-Product-Review-Analysis-Excel/blob/bc76dd4370a9d7d259fe8d1afc9e611cab7bf4e4/total%20product%20by%20Category.JPG)

### 🔍 Key Findings:
- **Top-reviewed categories:**
  - USB Cables – 233 reviews  
  - Smartwatches – 76 reviews  
  - Smartphones – 68 reviews  
  - Smart Televisions – 63 reviews  
  - In-Ear Headphones – 52 reviews  
  - Remote Controls – 49 reviews  

- **Low-volume or niche categories (1–3 reviews each):**
  - Traditional Laptops  
  - Earpads  
  - External SSDs  
  - Webcams  
  - Camera Batteries  
  - And more...

### 💡 Insight:
The data indicates a **high concentration of user reviews in mobile and smart tech accessories**, reflecting:
- Strong customer interest  
- Frequent usage  
- Higher online engagement

Categories with fewer reviews may:
- Reflect **lower visibility** or **newer products**
- Indicate **smaller customer bases**
- Signal **niche opportunities** for sellers to build early product leadership

#### 🎯 Business Implication:
- High-review categories are ideal for:
  - **Targeted promotions**
  - **Product bundling**
  - **Inventory scaling**

- Low-review categories present opportunities to:
  - **Launch awareness campaigns**
  - **Encourage user-generated reviews**
  - **Explore emerging demand or underserved needs**
 
  ---    

## 4. Which products have the highest average ratings?

📌 **Approach**:  
Used Excel sorting on the dataset where:
- Grouped by **Product Name**
- Calculated the **Average Rating**
- Sorted in descending order to extract the **top-rated products**

📈 **Result**:  
Below are the top 6 highest-rated products based on **average customer ratings**:

| Product Name | Average Rating |
|--------------|----------------|
| Syncwire LTG to USB Cable for Fast Charging Compatible with Phone 5/5C/5S/6/6S/7/8/X/XR/XS Max/11/12/13 Series and Pad Air/Mini, Pod & Other Devices (1.1 Meter, White) | 5.00 |
| REDTECH USB-C to Lightning Cable 3.3FT, [Apple MFi Certified] Lightning to Type C Fast Charging Cord Compatible with iPhone 14/13/13 Pro/Max/12/11/X/XS/XR/8, Supports Power Delivery - White | 5.00 |
| Amazon Basics Wireless Mouse – 2.4 GHz Connection, 1600 DPI, Type-C Adapter, 12-Month Battery Life | 5.00 |
| Swiffer Instant Electric Water Heater Faucet Tap Home-Kitchen Instantaneous Water Heater Tankless for Tap, LED Electric Head Water Heaters Tail Gallon Comfort (3000W) (Pack of 1) | 4.80 |
| Oratech Coffee Frother Electric, Coffee Beater, Froth Maker, Coffee Blender (6 Month Warranty, Multicolour) | 4.80 |
| Instant Pot Air Fryer, Vortex 2QT, 360° EvenCrisp™ Technology, 4-in-1 Appliance: Air Fry, Roast, Bake, Reheat (Black) | 4.80 |

🔍 **Key Findings**:
- **Perfect Ratings (5.00)**:  
  - 3 products achieved perfect scores:  
    - Syncwire LTG USB Cable  
    - REDTECH Lightning Cable  
    - Amazon Basics Wireless Mouse

- **High Ratings (4.80)**:  
  - Top-rated **home and kitchen appliances** include:  
    - Water heater tap  
    - Electric coffee frother  
    - Air fryer

---

💡 **Insight**:
- Tech **accessories** and **peripherals** are consistently top-rated, indicating **strong product quality** and **user satisfaction**.
- **Small kitchen gadgets** with high ratings reflect:
  - **Efficient design**
  - **Frequent usage**
  - **Trust in utility brands**

---

🎯 **Business Implication**:
- Products with **5-star consistency** are:
  - Excellent for **highlighting in promotions**
  - Strong candidates for **bundling**
  - Effective in **recommendation systems**

- Sellers of **top-rated home gadgets** can:
  - Use **positive reviews** in advertising
  - Run **testiimonial-driven campaigns**
  - Emphasize **key features and use cases**

- Ongoing **review analysis** helps businesses:
  - Maintain **high-quality offerings**
  - Identify **trending categories**
  - Capitalize on **consumer trust**
    

## 5. What is the average actual price vs the discounted price by category?

📌 **Approach**:  
Used Excel Pivot Table to:
- Add **Product Category** to Rows
- Compute **Average of Actual Price** and **Average of Discounted Price** in Values
- Sorted by highest Average Actual Price to highlight premium categories and discount patterns

📈 **Result**:  
The table below displays the **top 30 categories** with the highest average actual and discounted prices:

| Product Category | Avg Actual Price | Avg Discounted Price |
|------------------|------------------|------------------------|
| Home&Kitchen → Heating, Cooling & Air Quality → Split-System Air Conditioners | $75,990.00 | $42,990.00 |
| Computers&Accessories → Laptops → Traditional Laptops | $59,890.00 | $37,247.00 |
| Home&Kitchen → Vacuum & Floor Care → Robotic Vacuums | $44,949.50 | $23,449.50 |
| Electronics → Televisions → Smart Televisions | $40,132.84 | $24,840.19 |
| Computers&Accessories → Tablets | $37,999.00 | $26,999.00 |
| Computers&Accessories → External Solid State Drives | $32,000.00 | $10,389.00 |
| Home&Kitchen → Air Purifiers → HEPA Air Purifiers | $27,113.25 | $11,917.00 |
| Home&Kitchen → Cold Press Juicers | $23,999.00 | $12,609.00 |
| Electronics → Smartphones | $20,593.40 | $15,754.44 |
| Electronics → Projectors | $18,293.33 | $9,990.00 |
| Computers&Accessories → Monitors | $16,430.00 | $8,199.00 |
| Home&Kitchen → Water Purifiers | $15,618.83 | $7,015.25 |
| Electronics → Televisions → Standard Televisions | $15,329.67 | $7,180.83 |
| Electronics → Soundbar Speakers | $12,499.00 | $4,999.00 |
| Home&Kitchen → Air Fryers | $12,116.80 | $6,276.40 |
| Home&Kitchen → Storage Water Heaters | $11,738.17 | $6,323.33 |
| Home&Kitchen → Stand Mixers | $11,495.00 | $5,999.00 |

 Table showing average actual and discounted prices by category (top 20 categories)

---

💡 **Insight**:
- **High-priced tech** (e.g., SSDs, laptops, monitors) experience significant **discounting margins**, often up to **60–70% off**.
- Categories like **USB adapters**, **gaming peripherals**, and **webcams** show moderate discounts, potentially indicating **high demand with less price elasticity**.
- **Basic accessories** (e.g., cable protectors, dust covers, lamps) retain **low actual prices** with **deep markdowns**, possibly to drive **impulse or bulk purchases**.
- **Laptop and PC accessory segments** consistently show **pricing sensitivity**, revealing ample room for bundling, pricing strategies, or value packaging.

## 6. Which products have the highest number of reviews?

📌 **Approach**:  
Using Excel:
- Grouped by **Product Name**
- Summed the **Rating_Count** field
- Sorted the results in descending order
- Extracted the **Top 10** most-reviewed products

📈 **Result**:

| Product Name | Total Number of Reviews |
|--------------|--------------------------|
| 3M Scotch Double Sided Heavy Duty Tape (1m holds 4.5Kgs) – for wall hanging and indoor use | 14,778 |
| 3M Post-it Sticky Note Cube (4 colors x 50 sheets) – 3"x3" | 7,429 |
| Acer 55” I Series 4K Ultra HD Android Smart LED TV (AR55AR2851UDFL) | 4,703 |
| Acer 43” I Series 4K Ultra HD Android Smart LED TV (AR43AR2851UDFL) | 4,703 |
| Acer 50” I Series 4K Ultra HD Android Smart LED TV (AR50AR2851UDFL) | 4,703 |
| Acer 32” I Series HD Ready Android Smart LED TV (AR32AR2841HDFL) | 4,703 |
| Acer 40” P Series Full HD Android Smart LED TV (AR40AR2841FDFL) | 4,702 |
| Abode Kitchen Measuring Cup & Spoon Set – For Cooking/Baking (Black) | 4,074 |
| HDMI 2.1 Cable – 10k/8k/4k Ultra High Speed Certified for TV/PS5/Xbox | 3,664 |
| Acer 55” H Series 4K Ultra HD Android Smart LED TV (AR55AR2851UDPRO) | 1,611 |

 Table listing the top 10 most-reviewed products based on total rating count, ranging from 1.6k to 14k+ reviews.

---

💡 **Insight**:  
- **3M office supplies** dominate the top with overwhelming review volumes, likely due to low cost, broad utility, and repeated purchases.
- **Acer Smart TVs** appear **6 times** in the top 10, showing **strong customer engagement** across multiple size segments.
- The presence of **kitchen essentials** and **tech accessories** (like HDMI cables) emphasizes the popularity of **functional, everyday-use products**.

## 7. How many products have a discount of 50% or more?

📌 **Approach**:  
- Calculated **discount percentage** using:  
  `(Actual Price - Discounted Price) / Actual Price * 100`
- Created a **Pivot Table** to group by Product Name and compute the average discount percentage.
- Filtered the results to include only products with **≥ 50% discount**.

📈 **Result**:  
 A pivot table image below for a detailed view of products with 50% or more discounts.

![Alt text](https://github.com/Akinlade-Opeyemi-Mary/Amazon-Product-Review-Analysis-Excel/blob/00cd0acb3356217b06eeb1da90ee61a0f19ba525/50%20%2B.JPG)

🔍 **Key Findings**:
- Multiple **home appliances** and **tech accessories** are offered at **steep discounts** (50% and above).
- Brands like **AGARO**, **Amazon Basics**, and **Akiara** frequently appear, suggesting aggressive pricing strategies.
- High-discount items span across **room heaters, sewing machines, HDMI cables, speakers, and kettles**.

💡 **Insight**:
- These heavy-discounted products could be part of **seasonal sales** or **inventory clearance**.
- Customers looking for value buys are likely drawn to these high-discount categories, which can be leveraged in targeted promotions or bundle deals.

## 8. What is the distribution of product ratings?

📌 **Approach**:
- Used a Pivot Table in Excel to group by product `Rating`.
- Counted the number of products for each rating.
- Sorted ratings in descending order to analyze distribution patterns.

📈 **Result**:
The chart below shows how product ratings are distributed across the dataset.

![Alt text](https://github.com/Akinlade-Opeyemi-Mary/Amazon-Product-Review-Analysis-Excel/blob/129c3b26e1e4bbcfff72f97dfdd84ab18a0328d0/rate%20distrubrution.JPG)

🔍 **Key Findings**:
- Most products are rated between **4.0 and 4.3**, indicating generally **positive customer feedback**.
- The **peak rating** is **4.1**, with **244 products**.
- Very few products have ratings below 3.5 or above 4.6.
- Only **3 products** received a **perfect 5.0 rating**, suggesting customers are conservative with full scores.

💡 **Insight**:
- The concentration around the **4-star range** shows overall customer satisfaction but leaves room for improvement.
- Products rated below **3.5** might need review attention, product fixes, or reconsideration in promotional strategy.

### 9. What is the total potential revenue by category?

📌 **Approach**:
- Computed **total potential revenue** using:
  
  \[
  \text{Potential Revenue} = \text{Actual Price} \times \text{Rating Count}
  \]

- Grouped the data by product category
- Summarized the top 10 categories by **highest potential revenue**

📈 **Result**:
Top 10 categories by total potential revenue:

| Product Category | Total Potential Revenue (₦) |
|------------------|-----------------------------|
| Smartphones | ₦38,500,723,825 |
| Smart Televisions | ₦26,237,061,348 |
| Smartwatches | ₦13,274,477,088 |
| In-Ear Headphones | ₦7,891,731,253 |
| USB Cables | ₦2,989,269,763 |
| MicroSD Memory Cards | ₦2,615,837,993 |
| Mixer Grinders | ₦1,641,979,238 |
| Power Banks | ₦1,597,847,790 |
| On-Ear Headphones | ₦1,585,622,750 |
| HDMI Cables | ₦1,569,588,545 |

🔍 **Key Findings**:
- **Smartphones and Smart TVs** dominate the potential revenue chart, accounting for over ₦64 billion combined.
- Accessories like **USB cables**, **headphones**, and **power banks** also contribute significantly due to high volume and steady demand.
- **Kitchen appliances** like **mixer grinders** and **high-capacity cables** show strong purchase intent.

💡 **Insight**:
- These top categories are ideal for **targeted advertising**, **flash sales**, or **bundle deals** to convert high potential revenue into actual earnings.
- The combination of **unit cost × popularity** drives these figures — suggesting focus should remain on both **product visibility** and **value-for-money messaging**.


