# CO₂ Emissions by Vehicle — Power BI Root Cause Analysis
End-to-end Power BI dashboard project applying AI visuals (Key Influencers &amp; Decomposition Tree) to analyze vehicle CO₂ emissions and uncover root causes


**Objective:** Identify the drivers behind vehicle CO₂ emissions and build an interactive Power BI report using **Key Influencers** and **Decomposition Tree** visuals to explain *why* emissions increase or decrease.

## ❓ Questions Answered

What factors most strongly influence CO₂ emissions?
→ Key influencers identified: Powertrain type, Engine size, Fuel type, and Transmission.

How does engine size impact CO₂ emissions?
→ Scatter plot shows a direct positive relationship between engine size (cm³) and average CO₂ emissions.

Which powertrain and transmission combinations contribute most to emissions?
→ Internal combustion engines (ICE), especially with automatic transmission, dominate CO₂ output.

## 📊 Report Contents
1. **Card:** Total vehicles analyzed  
2. **Key Influencers:** CO₂ (Analyze) explained by Transmission, Engine Size (cm³), Fuel Type, Powertrain  
3. **Scatter Plot:** *Engine Size (cm³)* vs **Average CO₂**  
4. **Top Segments:** Groups of attributes most associated with higher/lower emissions  
5. **Clustered Bar (example):** CO₂ by **Powertrain** (Y) with **Transmission** as Legend  
6. **Fuel Type Pie/Donut:** Top 3 fuel types comprising >90% of total CO₂  
7. **Decomposition Tree (AI):** Drill path to lowest average CO₂ for **Powertrain = HEV**

> **Note:** Engine Size bins are created for the Decomposition Tree (e.g., 5 equal-sized bins) to improve usability.

## 🧠 Key Insights (from this analysis)
- **Engine size** shows a strong positive relationship with average CO₂ (confirmed by Key Influencers and scatter).
- **Powertrain + Transmission** combinations meaningfully shift emission levels (Top Segments).
- A small set of **fuel types** accounts for the vast majority of total CO₂.
- Using AI splits in the **Decomposition Tree**, the **lowest average CO₂** within **HEV** is found by selecting *Low value* across remaining attributes after choosing Powertrain = HEV.

*(Replace with your own specific callouts if you have exact values in your report.)*

## 🧱 Data & Fields
- **Target (Analyze):** `CO2 emission`
- **Explainers (Explain by):** `Engine Size (cm3)`, `Powertrain`, `Transmission`, `Fuel Type`
- **Index:** `car_id` (used only for counting; not analytically meaningful)

## 🛠️ How to Use
1. Open `Root Cause Analysis.pbix` in **Power BI Desktop**.
2. On Page 1, explore **Key Influencers**, **Segments**, scatter, and fuel-type chart.
3. On Page 2, drill through the **Decomposition Tree** (try Powertrain → HEV → *Low value*).

## 💡 Techniques Used
- **Power BI AI visuals:** Key Influencers, Decomposition Tree  
- **Data modeling & binning:** Engine-size bin groups for better explainability  
- **Visual analytics:** Scatter (Avg CO₂), categorical comparisons (bar/pie)  
- **Storytelling:** From drivers → segments → drilldown to lowest-emission configs

---

**Author:** James Miller  
**Tools:** Power BI Desktop
