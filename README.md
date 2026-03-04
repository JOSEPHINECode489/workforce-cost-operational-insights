                                       Workforce Cost & Operational Insights

                                Power BI | Star Schema | DAX | Time Intelligence
               Project Overview

This Business Intelligence project demonstrates the design and implementation of a scalable workforce cost analytics solution using Power BI. The solution incorporates dimensional modelling, DAX-based performance measures, and time intelligence to deliver structured operational insights.

                Business Objective

To provide leadership with structured insights into workforce cost distribution using scalable dimensional modelling and performance-driven metrics.

                 Data Model Architecture

The solution was built using a star schema structure:

Central Fact Table: Fact_workforce

Dimension Tables:

Dim_Date

Dim_Department

Dim_City

Relationships:

One-to-many cardinality

Single-direction filtering

Dedicated Date dimension for time intelligence optimisation

<img width="1920" height="1080" alt="Screenshot (213)" src="https://github.com/user-attachments/assets/ab49e748-1128-41ba-a8df-b2f9774f2836" />


                 📊 Key DAX Measures
Total Salary = SUM(Fact_workforce[Salary])
Headcount = DISTINCTCOUNT(Fact_workforce[EmployeeID])
Average Salary = AVERAGE(Fact_workforce[Salary])
Salary YTD = TOTALYTD(SUM(Fact_workforce[Salary]), Dim_Date[Date])

                    
                    Dashboard Overview
<img width="1920" height="1080" alt="Screenshot (212)" src="https://github.com/user-attachments/assets/e2cf2510-f68a-4c5a-bc1b-f8d11acbc5cf" />


                  
                   Key Insights

January recorded a peak salary expenditure before declining through March.

Department 2 has the highest allocation of workforce costs.

Bristol represents the largest salary distribution across cities.


                  
                  Data Governance & Best Practices

Structured dimensional modelling

Proper key relationship validation

Dedicated Date table for time intelligence

Performance-optimised filtering logic
