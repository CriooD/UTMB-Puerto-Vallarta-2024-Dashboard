# UTMB - Puerto Vallarta 2024 Power BI Dashboard

## Description

This repository contains the Power BI dashboard and documentation used to visually analyze the UTMB Puerto Vallarta 2024 race results. This proyect demostrates practical business intelligence techniques, including the use of DAX for dynamic measures, data modeling to handle long time time formats, and the integration of Python scripts to generate statistical visualizations of runner performance and DNF rates.   

## Languages Used

- <b> DAX </b>
- <b> Python </b>

## Environment Used

- Power BI Desktop

## Key Power BI Concepts Used

- **DAX Measures & Variables** (Functions like CALCULATE and DIVIDE for dynamic rates)
- **Data Modeling & Time Formatting** (Mathematical conversion from HH:MM:SS to numerical values)
- **Python Visuals Integration** (Using native libraries in PBI like Pandas and Seaborn)
- **Conditional Formatting** (Implementing matrices with ranking icons ★)

## Data Quality & Modeling Notes
Real-world ultramarathon data presents specific challenges, so the following decisions were made in the data model:

- **Times over 24 hours**: Power BI has native limitations with extended durations. A variable model in DAX was implemented to isolate hours, minutes, and seconds, ensuring accurate calculations for averages and gaps.
  
- **Dynamic DNF rates**: To avoid division-by-zero errors when interacting with slicers, the Finishers vs. DNF logic was safely structured. This allows dynamic filtering by gender and category without breaking the visuals.

## Business Questions Analyzed
1. **Top 10 fastest finish times (per race and by gender)**
2. **DNF (drop-out) rate by race/distance and by gender**
3. **Countries with the most participants (Top 10 nationalities)**
4. **Gap between the overall category winner and the category average (Area chart with support table)**\
  4.1 Gap between the race category winner and the race category average
5. **Visual ranking within each race + age category + gender (Matrix with ★ indicators)**
6. **Top 10% fastest finishers within each category (Elite isolated with Python)**
7. **Complete data coverage across all race and age combinations, explicitly displaying 0 for categories with no finishers.**

> *Note: This Power BI file is fed by the clean datasets previously processed through the SQL project.*

## Dashboard Views

<!--
*(Proximamente Screenshots: `![View Name](path/to/image.png)`)*



- **General & DNF Rates:** Retention metrics and participant volume by distance.
- **Rankings & Gaps:** Position matrix and gap analysis compared to the average time.
- **Python Elite Distribution:** Stripplots highlighting the top 10% of runners.
