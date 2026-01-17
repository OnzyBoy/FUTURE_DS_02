# Platform Advertisement Performance Analysis (Power BI)

## 📊 Project Overview
This project analyzes **multi-platform advertising performance data** to understand how marketing spend across different channels impacts product sales. Using **Power BI**, an interactive dashboard was built to help businesses evaluate **cost efficiency**, **sales performance**, and **return on advertising investment**.

The analysis focuses on answering a key business question:

> *Are advertising budgets across platforms effectively driving product sales, and where should future spending be optimized?*

This project was completed as **Task 2** of the **Future Interns Data Science & Analytics Internship Program**.

---

## 🎯 Business Objectives
The dashboard is designed to help marketing and business teams:

- Understand total advertising spend and total products sold
- Evaluate cost efficiency using **Cost per Product Sold**
- Compare ad spend distribution across platforms
- Identify relationships between ad spend and sales performance
- Support data-driven budget reallocation decisions

---

## 📁 Dataset Information
- **Source:** Kaggle - [Product Adversing Data](https://www.kaggle.com/datasets/singhnavjot2062001/product-advertising-data)
- **Format:** CSV  

### Dataset Columns
| Column Name | Description |
|------------|------------|
| TV | Advertising spend on TV |
| Billboards | Advertising spend on billboards |
| Google_Ads | Advertising spend on Google Ads |
| Social_Media | Advertising spend on social media platforms |
| Influencer_Marketing | Spend on influencer marketing |
| Affiliate_Marketing | Spend on affiliate marketing |
| Product_Sold | Number of products sold |

📌 *Each row represents a marketing scenario where spending across platforms resulted in a given number of product sales.*

---

## 🛠 Tools & Technologies
- **Power BI Desktop** – Data modeling, DAX, and dashboard creation
- **Power Query** – Data preparation and feature engineering
- **DAX (Data Analysis Expressions)** – Business metrics and KPIs
- **Excel / CSV** – Source data format

---

## 🧹 Data Preparation & Feature Engineering
The following steps were performed in **Power Query**:

1. Loaded and validated the dataset
2. Ensured all advertising cost columns were numeric
3. Created a calculated column:

```text
Total_Ad_Cost = 
TV + Billboards + Google_Ads + Social_Media + Influencer_Marketing + Affiliate_Marketing
```

4. Verified data consistency and removed calculation errors
5. Verified data consistency and removed calculation errors

## 📐 Key DAX Measures
```
Total Products Sold =
SUM ( Advertising_Data[Product_Sold] )

Total Ad Spend =
SUM ( Advertising_Data[Total_Ad_Cost] )

Cost per Product =
DIVIDE (
    [Total Ad Spend],
    [Total Products Sold]
)
```

Additional measures were created for individual ad platforms:
- Total TV Ad Cost
- Total Google Ads Cost
- Total Social Media Ad Cost
- Total Billboard Ad Cost
- Total Influencer Marketing Cost
- Total Affiliate Marketing Cost

---

## 📊 Dashboard Components & Visuals
### 1️⃣ KPI Headline Section

Provides an immediate performance snapshot:
- Total Products Sold: 2.1M
- Total Ad Spend: 891.75K
- Cost per Product: 0.42

### 2️⃣ Advertising Cost Distribution (Donut Chart)

Purpose:
- Shows how total ad spend is distributed across platforms.

Insight:
- Advertising budgets are relatively evenly distributed, allowing for fair performance comparison across channels.

### 3️⃣ Ad Spend vs Product Sales (Scatter Plots)

Platforms Analyzed:
- TV
- Google Ads
- Billboards

Purpose:
- To identify correlation between advertising spend and product sales.

Analytics Feature Used:
- Trend lines added to visualize positive relationships

Insight:
- Higher ad spend generally correlates with higher product sales across platforms.

### 4️⃣ Sales Volume Grouping (Binning Analysis)

To improve interpretability:
- The Product_Sold column was grouped into bins (size = 200)
- This transformed dense scatter visuals into meaningful sales tiers

Result:
- An inverted pyramid pattern clearly showing that higher spending tiers align with higher product sales volumes.

--- 

## 🎨 Design & Layout Considerations

- Consistent editorial-style layout
- Neutral beige background for readability
- Unified color palette (orange accents for data emphasis)
-Structured sections using visual containers
-Clear hierarchy: KPIs → Distribution → Performance Analysis

--- 

## 💡 Key Insights & Findings

- Advertising spend shows a positive relationship with product sales
- No single platform dominates budget allocation, enabling optimization opportunities
- Cost per Product Sold (0.42) indicates efficient overall spending
- Grouped sales analysis reveals clear performance tiers tied to spend levels

--- 

## 📊 Dashboard Preview

<img width="1388" height="782" alt="image" src="https://github.com/user-attachments/assets/7c73e97e-a236-470f-acc3-4364f07769f6" />


---

## 👤 Author
**Aristo Ayako**  
Data Analytics & Data Science Intern  

