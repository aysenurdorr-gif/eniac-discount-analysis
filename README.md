# ENIAC Discount & Pricing Analysis

## 📌 Overview
This project analyzes e-commerce transaction data from ENIAC (an online marketplace specializing in Apple products and Apple-compatible accessories) to evaluate the market dynamics, brand performance, and the dual impact of discount strategies on revenue and sales volume.

This was a collaborative team project. While data extraction, cleaning, and the macro-level brand/category pricing analysis were done together, my individual focus was leading the **smartphone category discount-timing analysis** to evaluate the relationship between strategic timing and financial impact.

## 🙋 My Contribution (Smartphone Strategic Timing Analysis)
I owned the **"Smartphone Analysis: Strategic Timing vs. Discount Impact"** portion of the project. Using smartphones as a core case study, I analyzed the historical correlation between average discount percentages, total revenue, and units sold over a 14-month period. 

### Key Insights from My Analysis:
* **The Q4 Surge (Holiday Season):** Identified a massive revenue and volume peak in late 2017 (Nov–Dec), where sales volume surged to nearly 400 units and revenue approached €250,000. Interestingly, this peak was achieved with a moderate average discount (~7-8%), proving that seasonal demand, rather than aggressive discounting, was the primary driver.
* **The August Promotional Spikes:** Discovered a sharp volume and revenue spike in August 2017 driven directly by an aggressive discount peak (~10.5%). This confirms high price sensitivity among Spanish consumers during specific off-season promotional windows.
* **Diminishing Returns (Late Q1 2018):** Noted that a sharp increase in discounts in March/April 2018 failed to generate proportional revenue or volume lifts, indicating potential market saturation or ineffective late-cycle discount timing.

To ensure the integrity of these insights, I personally navigated severe data quality issues, including standardizing mixed decimal separators, handling missing values ($NaN$), isolating misclassified product outliers, and filtering out incomplete orders.

## 🛠️ Method (Team Collaboration)
* **Data Extraction & Load:** Loaded raw transactional datasets (~270,000 rows) using Pandas to inspect data structures, schema discrepancies, and missing values.
* **Data Cleaning & Engineering:** * Handled missing values ($NaN$) that hindered calculation loops.
  * Standardized inconsistent decimal separators across pricing fields.
  * Merged product metadata with order-line datasets.
  * Handled product placement errors by re-categorizing misaligned items that created data outliers.
  * Generated time-based features (year, month, order_month) for trend analysis.
* **Exploratory Data Analysis (EDA):** Segmented top-performing brands (Apple, Pack, OWC) and categories (Storage, Smartphone) using Pandas `groupby` aggregations to cross-reference list prices against actual selling prices.
* **Data Visualization:** Built scannable bar charts and dual-axis line plots using Seaborn and Matplotlib to visualize revenue distributions, average unit prices, and discount trends over time.

## 📊 Key Findings
* **Market Context:** Operating in the rapidly growing Spanish e-commerce market (projected 37M buyers by 2025), where 75% of consumers search for better deals, making an optimized discount strategy vital.
* **Brand & Category Dominance:** Apple heavily dominates both product count (over 2,000 products) and revenue generation (approaching €2.8M). Storage and Smartphones represent the highest-grossing product categories.
* **The Discounting Dilemma:** Top-selling discounted items are heavily anchored around core Apple ecosystem needs (e.g., iPhone AppleCare Protection Plans, Lightning Cables, and AirPods). 
* **Overall Conclusion:** Discounting acts as a double-edged sword. While it successfully clears inventory and drives volume during promotional spikes (like August), seasonal demand shifts (like Q4) generate revenue without requiring margin-killing discounts. 

## ⚠️ Data Limitations
* **Lack of True Cost Data:** The actual cost of goods sold (COGS) was unavailable, meaning profit margins could not be precisely calculated. Discount impacts were estimated based on list vs. selling price assumptions.
* **Data Volatility:** Out of ~270,000 initial rows of data, only 50,000–60,000 rows representing fully completed orders could be utilized to maintain analysis accuracy.

## 🛠️ Tools Used
Python • Pandas • Matplotlib • Seaborn • Jupyter Notebook • Git & GitHub
