# Europe Real Estate Marketplace Analysis

## 📌 Project Overview
This project provides a comprehensive analysis of the European Real Estate market, focusing on identifying trends, market saturation, and the key factors influencing the time properties spend on the market. This analysis was developed as part of the **FP20 Analytics ZoomCharts Challenge 36**.

## 🛠️ Data Pipeline & Architecture
I implemented a hybrid workflow to ensure a scalable and clean data structure:

### 1. Data Modeling & Preprocessing (Python)
Before importing into Power BI, I used **Python (Pandas)** to handle the heavy lifting of data preparation:
* **Cleaning:** Handled missing values and ensured data type consistency.
* **Feature Engineering:** Created logic for categorizing complex variables.
* **Star Schema Creation:** Deconstructed the flat dataset into a relational structure, generating the foundational logic for Dimension and Fact tables.

### 2. BI Modeling (Power BI)
* **Schema:** Implemented a **Star Schema** with a central `Fact_listings` table connected to `Dim_Date`, `Dim_Property`, and `Dim_Features`.
* **DAX:** Developed advanced measures to calculate Market Speed, Average Price per SQM, and dynamic period-over-period comparisons.

## 📊 Key Insights
* **Market Saturation:** The average **Days On Market (DOM)** is **172 days**, indicating a significant slowdown across the European marketplace.
* **Uniformity:** High DOM is consistent across various property types and features, suggesting a systemic market trend.
* **Decoupled Factors:** Surprisingly, Sale Price, Monthly Rent, and Property Space showed **no significant impact** on market velocity (DOM).

## 🧠 Advanced Categorization
* **Market Speed:** Grouped DOM into 4 categories: (Very Fast, Normal, Slow, Very Slow).
* **Residential Segmentation:** Categorized Bedrooms into logical clusters (1-2 Rooms, 3-4 Rooms, 5-6 Rooms, and Non-Residential).

## 🚀 Recommendations
1. **Analyze Macro Factors:** Investigate external economic conditions (interest rates, local regulations) affecting demand.
2. **Marketing Optimization:** Improve digital visibility and exposure for listings with high DOM.
3. **Strategic Targeting:** Focus on high-demand niche segments to accelerate turnover.

## 💻 Technical Stack
* **Python:** Pandas, NumPy (Data Cleaning & Modeling)
* **Power BI:** Data Visualization & DAX
* **Architecture:** Star Schema (Fact/Dimension Modeling)

## 🔗 Project Links
* **Live Demo:** https://app.powerbi.com/view?r=eyJrIjoiYTJlMzRlNGItNzQ3Ni00NjJiLTlkNjUtN2M4OGE3NzQzMDIyIiwidCI6IjQ2NTRiNmYxLTBlNDctNDU3OS1hOGExLTAyZmU5ZDk0M2M3YiIsImMiOjl9
* **Python notebook:** Check the `/Notebook` folder for the modeling code.

---
## 👨‍💼 Contact Me
I am a Data Professional passionate about the intersection of Data Science and Human Resources (People Analytics).

* **Name:** Eng. Mohammed Ramadan
* **LinkedIn:** https://www.linkedin.com/in/mohamed-ramadan-rah
* **Email:** mohammedramadanqawouq@gmail.com
* **WhatsApp:** https://wa.me/201280779842
