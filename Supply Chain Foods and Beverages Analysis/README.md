# 📊 End-to-End Foods & Beverages Supply Chain Performance Analysis
An interactive, impact-driven **Power BI Business Intelligence Dashboard** designed to monitor, analyze, and optimize an end-to-end Food & Beverage Supply Chain dataset. 

This repository contains a full star-schema data model built from multi-table operational layers to deliver advanced diagnostics covering commercial sales, logistics throughput, warehouse operations, product shelf life risks, and customer return behaviors.

---

## 🚀 Executive Highlights & Key Findings
* **Commercial Scale:** Analyzed **2K+ Total Orders** across **42 Products**, generating **$605.61K in Revenue** with a **$208.35K Gross Profit (34.4% Margin)** and **$397.26K COGS**.
* **Logistics Efficiency:** Maintained a strong **92.55% OTIF (On-Time In-Full) Rate**, demonstrating a highly stable and reliable fulfillment cycle.
* **Volume Distribution:** Handled a massive cargo throughput of **4M+ Total Shipped Units**, maintaining an average running inventory of **3.16M Units** at a **1.11 Stock Movement Rate**.
* **Operational Hotspots Identified:**
  * **The Freshness Dilemma:** Short shelf-life subcategories like **Yogurt (32 days)** and **Milk (38 days)** suffer from the highest spoilage rates (**0.75% and 0.73%** respectively), causing **8.177K Expired Units (0.14% Expired Rate)**.
  * **The Return Bottleneck:** The **Bakery** category exhibits extreme structural return risk (approaching **0.05%**), while high-throughput categories like **Beverages** remain completely safe and highly optimized.
  * **Serial Returner Accounts:** Customer **C060** generated the highest returns (**28 units**), closely linked to localized cold-chain or handling issues, while Customer **C074** represents a high-risk relationship due to elevated returns relative to their buying volume (**33 units bought vs. 26 returned**).

---

## 🛠️ Tech Stack & Skills Demonstrated
* **Business Intelligence:** Power BI Desktop
* **Data Modeling:** Power Query (M Language), Star Schema Design, Dimension vs. Fact Table architecture.
* **Advanced Analytics:** DAX (Data Analysis Expressions) for complex dynamic measures and KPIs.
* **UI/UX Design:** High-contrast dark executive theme using corporate golden accents, custom navigation panels, custom KPI indicators, and responsive tooltips.

---

## 📐 Data Model & Architecture (Star Schema)
The architecture completely isolates historical operational transactions from dimensional lookups to maximize performance, storage efficiency, and **Columnar Compression** via Power BI's VertiPaq engine.

### 📥 Fact Tables (Operational Transaction Layers)
1. **`Fact_Orders`**: The core operational engine storing revenue, cost, margins, and line-level flags for OTIF, stockouts, returns, waste, quality, and marketing promotions.
2. **`Inventory_Snapshots`**: Tracks running inventory balances, monthly stock movements, and warehouse availability indices.

### 🗂️ Dimension Tables (Granular Lookup Hierarchies)
* **`Dim_Product`**: Contains granular descriptive fields for categories, subcategories, custom storage parameters, and shelf-life constraints.
* **`Dim_Customer`**: Profiles buyers across customer segments (e.g., Retail, Retail Chain, HoReCa, Distributors) and geographic locations.
* **`Dim_Supplier`**: Houses risk profiles, reliability indexes, and standard transportation lead times.
* **`Dim_Warehouse`**: Identifies warehouse locations, processing capabilities, storage capacity thresholds, and cold-storage availability flags.
* **`Dim_Channel`**: Segments the order generation mediums.
* **`Dim_Date`**: Full calendar day dimension supporting advanced Time Intelligence DAX expressions.

---

## 💾 DAX Measure & Calculation Layer
A clean compilation of core calculated metrics optimized for dynamic filtering across the dashboard viewports:

| Metric Name | Calculation Logic (DAX) | Strategic Business Purpose |
| :--- | :--- | :--- |
| **Total Revenue** | `Revenue = SUM ( Fact_Orders[Revenue] )` | Quantifies market footprint across categories and channels. |
| **Gross Profit** | `Gross Profit = SUM ( Fact_Orders[GrossProfit] )` | Isolates pure profitability by filtering out baseline COGS. |
| **OTIF Rate** | `OTIF Rate = AVERAGE ( Fact_Orders[OTIF_Flag] )` | Evaluates overall delivery reliability (Time & Quantity combined). |
| **Return Rate** | `Return Rate = DIVIDE ( SUM ( Fact_Orders[ReturnQty] ), SUM ( Fact_Orders[OrderQty] ) )` | Diagnostic indicator for product quality or logistics handling errors. |
| **Stock Movement Rate** | `Stock Movement Rate = 
    DIVIDE(
        SUM(Inventory_Snapshots[ShippedQty]),
        [Avg Inventory Units],
        0
    )` | his KPI operationally reflects product rotation velocity and capacity utilization, which is vital in the F&B industry to prevent stock stagnation and expiration risks. |

---

## 🎛️ Dashboard Structure & Interface Architecture
The report features 4 dedicated analytical lenses designed to streamline cross-departmental alignment:

### 🌟 1. Executive Overview
* **Target Audience:** C-Suite & VP of Supply Chain.
* **Visual Focus:** High-level scorecard metrics (Revenue, Gross Profit, COGS, OTIF) mapped across strategic timelines, distribution channels, and regional customer clusters.

### 🚚 2. Logistics Insights
* **Target Audience:** Logistics Managers & Operations Specialists.
* **Visual Focus:** Breakdown of volume dynamics via **Ordered QTY by Channel** (identifying *Retail* as the primary driver with 111K units). Analyzes *Shipment Volume vs. Return Risk* via multi-axis scatter plots to track structural vulnerabilities (e.g., isolating *Bakery* risks vs. highly efficient *Beverage* routing).

### ⏳ 3. Manufacturing & Shelf Life
* **Target Audience:** Inventory Control & Production Planning.
* **Visual Focus:** Explores manufacturing cost allocations alongside product storage tolerances via **Average Shelf Life Days by Subcategory**. Identifies severe operational risks in short-cycle lines (*Yogurt* and *Milk*) to prioritize **First-Expired, First-Out (FEFO)** warehouse rotations.

### 👥 4. Customer Insights
* **Target Audience:** Accounts Management & Commercial Operations.
* **Visual Focus:** Connects behavioral patterns with corporate bottom lines by isolating **Customers Who Returned the Most Products** (identifying account *C060* and *C074*) against **Top Buyers** (account *C036*). Integrates customer category segments with a **Customer Transactions by Promotion Status** analysis to track promotional elasticity.

---

## 📈 Strategic Business Recommendations
1. **Enforce FEFO in Cold Chain Operations:** Due to high expiration rates in *Yogurt* and *Milk* subcategories, deploy automated **FEFO (First-Expired, First-Out)** picking protocols within cold-storage facilities to lower the current **8.177K Expired QTY** drain.
2. **Audit Bakery Logistical Controls:** Investigate the manufacturing quality checks or distribution transport protocols for the *Bakery* line to eliminate the systemic high-return rates appearing in scatter plot anomalies.
3. **Targeted Customer Account Interventions:** Initiate operational alignment meetings with accounts **C060** and **C074** to review delivery acceptance criteria, reducing unnecessary handling costs and minimizing transit-based return spikes.

---

## ⚙️ How to Open and Interact with the Dashboard
1. Ensure **Power BI Desktop** (latest version) is installed on your workstation.
2. Clone this repository to your local system:
   ```bash
   git clone [https://github.com/yourusername/supply-chain-food-beverage-analysis.git](https://github.com/yourusername/supply-chain-food-beverage-analysis.git)
