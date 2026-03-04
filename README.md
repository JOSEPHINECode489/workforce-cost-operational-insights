                                       Workforce Cost & Operational Insights

                                Power BI | Star Schema | DAX | Time Intelligence
               Project Overview

This project demonstrates a Business Intelligence solution designed to monitor workforce cost allocation, departmental expenditure, geographic distribution, and monthly salary trends to support operational planning and cost control.

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

                 📊 Key DAX Measures
Total Salary = SUM(Fact_workforce[Salary])
Headcount = DISTINCTCOUNT(Fact_workforce[EmployeeID])
Average Salary = AVERAGE(Fact_workforce[Salary])
Salary YTD = TOTALYTD(SUM(Fact_workforce[Salary]), Dim_Date[Date])

                   Key Insights

January recorded a peak salary expenditure before declining through March.

Department 2 has the highest allocation of workforce costs.

Bristol represents the largest salary distribution across cities.


                  Data Governance & Best Practices

Structured dimensional modelling

Proper key relationship validation

Dedicated Date table for time intelligence

Performance-optimised filtering logic
