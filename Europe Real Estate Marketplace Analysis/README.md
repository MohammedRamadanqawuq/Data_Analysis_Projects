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

## 🖼️ Dashboard Preview
Visualizing the insights: Here’s a look at the multi-page Power BI report designed for this analysis, showcasing the market trends and deep dives.

| Landing_Page | Overview |
|---|---|
| ![Landing_Page](Screenshots/Landing_Page.png) | ![Overview](Screenshots/Overview.png) |

| Days_on_market_overview | Deep_Days_on_market_overview |
|---|---|
| ![Days_on_market_overview](Screenshots/Days_on_market_overview.png) | ![Deep_Days_on_market_overview](Screenshots/Deep_Days_on_market_overview.png) |

| Amenities | Deep_Amenities_Analysis |
|---|---|
| ![Amenities](Screenshots/Amenities.png) | ![Deep_Amenities_Analysis](Screenshots/Deep_Amenities_Analysis.png) |

## 🔗 Project Links
* **[Live Report Demo](https://app.powerbi.com/view?r=eyJrIjoiYTJlMzRlNGItNzQ3Ni00NjJiLTlkNjUtN2M4OGE3NzQzMDIyIiwidCI6IjQ2NTRiNmYxLTBlNDctNDU3OS1hOGExLTAyZmU5ZDk0M2M3YiIsImMiOjl9)** - Interactive Power BI Dashboard.
* **[Python Notebook](https://github.com/MohammedRamadanqawuq/Data_Analysis_Projects/blob/main/Europe%20Real%20Estate%20Marketplace%20Analysis/Notebook/Real_Estate_Project.ipynb)** - Modeling and Data Transformation logic.

---
## 👨‍💼 Contact Me
I am a Data Professional passionate about the Data Analysis Field.

* **Name:** Eng. Mohammed Ramadan
* **LinkedIn:** [Mohammed Ramadan Qawouq](https://www.linkedin.com/in/mohamed-ramadan-rah)
* **Email:** [mohammedramadanqawouq@gmail.com](mailto:mohammedramadanqawouq@gmail.com)
* **WhatsApp:** [Chat with me](https://wa.me/201280779842)
