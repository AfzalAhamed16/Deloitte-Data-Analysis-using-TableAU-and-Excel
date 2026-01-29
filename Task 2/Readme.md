# Gender Pay Equality Classification – Forensic Technology

This project focuses on analyzing employee compensation data to classify the level of gender pay equality across different job roles and factory locations. The objective is to categorize equality scores into meaningful classes for easier interpretation and investigation.

---

## Business Problem

Daikibo Industrials received multiple internal complaints regarding gender inequality in salaries.  
The Forensic Technology team developed an algorithm to calculate an **Equality Score** for each job role at every factory location.

The Equality Score:
- Ranges between **-100 and +100**
- **0** represents ideal equality  
- Higher absolute values indicate greater inequality  

The goal is to classify these scores into clear categories for analysis.

---

## Tools Used

- Microsoft Excel  
- Conditional logic using formulas  

---

## Dataset Description

The dataset contains the following columns:

- Factory  
- Job Role  
- Equality Score  

A new column was created:

- Equality Class  

---

## Classification Logic

A 4th column (**Equality Class**) was created based on the Equality Score using the following rules:

- **Fair** → Equality Score between **-10 and +10**  
- **Unfair** → Equality Score less than **-10 or greater than +10**  
- **Highly Discriminative** → Equality Score less than **-20 or greater than +20**

Excel formula used:
=IF(ABS(C2)<=10,"Fair",IF(ABS(C2)<=20,"Unfair","Highly Discriminative"))


This formula dynamically assigns a class based on the absolute value of the Equality Score.

---

## Output

The final Excel file contains:

- Factory  
- Job Role  
- Equality Score  
- Equality Class (Fair / Unfair / Highly Discriminative)  

This allows quick identification of job roles and locations with potential discrimination risks.

---

## Use Case

This project demonstrates:

- Logical classification using Excel formulas  
- Handling of real-world business rules  
- Data preparation for forensic and compliance analysis  
- Converting raw numerical metrics into actionable categories  

---
