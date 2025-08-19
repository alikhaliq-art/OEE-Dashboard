<img width="1200" height="644" alt="image" src="https://github.com/user-attachments/assets/04c8dd71-c7ff-4785-bfd9-616a9dc60bac" />

# 📊 OEE Dashboard – Power Query & Power BI

## 🚀 Overview
This project provides a **dynamic OEE (Overall Equipment Effectiveness) dashboard** built with **Power Query** for data transformation and **Power BI** for visualization.  
The dashboard helps monitor **Availability, Performance, and Quality** KPIs across production lines, enabling better decision-making and productivity improvements.

---

## 📂 Project Workflow
1. **Data Source**  
   - Production data extracted from Excel files (e.g., machine logs, shift data, downtime records).  
   - Consolidated into a structured dataset.

2. **Data Transformation (Power Query)**  
   - Clean and reshape raw data.  
   - Create calculated columns for:  
     - **Availability** = Operating Time ÷ Planned Production Time  
     - **Performance** = (Ideal Cycle Time × Total Count) ÷ Operating Time  
     - **Quality** = Good Count ÷ Total Count  
     - **OEE** = Availability × Performance × Quality  

3. **Data Model (Power BI)**  
   - Relationships defined between fact tables (production, downtime, quality) and dimension tables (date, shift, machine).  
   - DAX measures created for OEE metrics.

4. **Visualization (Power BI)**  
   - KPI cards for OEE, Availability, Performance, and Quality.  
   - Trend charts (daily, weekly, monthly).  
   - Downtime Pareto analysis.  
   - Drill-through reports for machine-level analysis.  
   - Filters for date, shift, and machine.

---

## 📊 Dashboard Features
- ✅ Real-time OEE monitoring  
- ✅ Interactive slicers (Machine, Date, Shift)  
- ✅ Downtime root cause analysis  
- ✅ Comparison between planned vs actual production  
- ✅ Export capability for reporting  

---

## ⚙️ Technologies Used
- **Power Query (M Language)** → Data cleaning & transformation  
- **Power BI (DAX)** → Measures & dashboard creation  
- **Excel/CSV** → Data input  

---

## 📌 How to Use
1. Clone or download this repository.  
2. Open the `.pbix` file in **Power BI Desktop**.  
3. Update data source paths in **Power Query** if required.  
4. Refresh the dataset to load the latest production data.  
5. Publish the report to **Power BI Service** for sharing with stakeholders.  

---

## 📈 Example OEE Formulae
```DAX
Availability = DIVIDE([Operating Time], [Planned Production Time])
Performance = DIVIDE(([Ideal Cycle Time] * [Total Count]), [Operating Time])
Quality = DIVIDE([Good Count], [Total Count])
OEE = [Availability] * [Performance] * [Quality]
📅 Future Enhancements
Add predictive analytics for downtime.

Integrate IoT/machine sensors for real-time data.

Automate data refresh via Power BI Gateway.

👨‍💻 Author
Developed by Muhammad Ali Khaliq – Data Analyst | BI Developer
