# Daikibo Telemetry Data Analysis using Tableau

This project presents an interactive data analysis of machine telemetry collected from Daikibo’s factories. The analysis was performed using Tableau to identify locations with the highest machine downtime and the device types responsible for frequent failures.

---

## Business Problem

Daikibo collects telemetry data from machines deployed in four factories:

- Daikibo Factory Meiyo (Tokyo, Japan)  
- Daikibo Factory Seiko (Osaka, Japan)  
- Daikibo Berlin (Berlin, Germany)  
- Daikibo Shenzhen (Shenzhen, China)  

Each factory contains 9 machine types that send a status message every 10 minutes. The data was collected for one month (May 2021) and provided as a single unified JSON file.

The business objectives were:

1. Identify which factory experienced the most machine downtime.  
2. Determine which machine types failed most frequently in that factory.

---

## Tools & Technologies

- Tableau Public / Tableau Desktop  
- JSON data source  
- Calculated fields  
- Interactive dashboards  

---

## Data Preparation

- Imported the telemetry JSON dataset into Tableau.  
- Created a calculated measure named **Unhealthy**: IF [status] = "unhealthy" THEN 10 ELSE 0 END


Each unhealthy status represents 10 minutes of potential downtime.

---

## Visualizations

Two bar charts were created:

1. **Down Time per Factory**  
 Displays the total downtime (in minutes) for each factory.

2. **Down Time per Device Type**  
 Displays downtime aggregated by machine type.

---

## Dashboard Design

- Both charts were combined into a single interactive dashboard.  
- The “Down Time per Factory” chart is configured as a filter.  
- Selecting a factory dynamically updates the “Down Time per Device Type” chart to show only machine failures for the selected factory.  
- This enables drill-down analysis from factory level to device level.

---

## Key Insight

- The factory with the highest overall downtime is highlighted using the dashboard filter.  
- For that factory, the machine types contributing the most to downtime can be clearly identified using the second chart.

---

## Output

The final deliverable is an interactive Tableau dashboard that visualizes:

- Downtime per factory  
- Downtime per device type  
- Relationship between factory and machine failures  

A screenshot of the final dashboard is included in this repository.

---

## Use Case

This project demonstrates:

- Practical data analysis using Tableau  
- Use of calculated fields for business metrics  
- Interactive dashboard creation  
- Root cause analysis of machine failures  
