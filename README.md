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

- **General & DNF Rates:** Retention metrics and participant volume by distance.

<img width="2767" height="1600" alt="1General" src="https://github.com/user-attachments/assets/c8e20db5-02a3-4b83-b2ea-29503b9ca7ee" />

<img width="2767" height="1600" alt="1DNFRate" src="https://github.com/user-attachments/assets/2dcbb202-ef58-44c9-a988-c95a9e8475dd" />

> **Key Insight:** The general dashboard reveals a direct correlation between race distance and DNF rates. It visually highlights how the premier 100M category experiences the most significant attrition, emphasizing the rigorous nature of the endurance event.

- **Rankings & Gaps:** Position matrix and gap analysis compared to the average time.

<img width="1945" height="1600" alt="2Ranking" src="https://github.com/user-attachments/assets/c011204f-411e-41d2-bca0-df1d3256afd8" />

<img width="2299" height="1600" alt="2Gap1" src="https://github.com/user-attachments/assets/1219ccd7-e08c-45aa-b076-6d2d386ae14f" />

<img width="1735" height="1600" alt="2gap2" src="https://github.com/user-attachments/assets/9f0671fe-1b20-4db2-9ce8-78691f78bccf" />


> **Key Insight:** The ranking matrix uses conditional formatting (★) to instantly identify demographic leaders across different segments. This is paired with an area chart that measures the exact gap in minutes between the category winner and the group's average finish time, quantifying elite dominance.


- **Python Elite Distribution:** Stripplots highlighting the top 10% of runners.

<img width="1156" height="768" alt="3Phyton" src="https://github.com/user-attachments/assets/0624d806-2398-43b2-8ae0-a737c55b9042" />

> **Key Insight:** Integrating Python scripts (Seaborn/Matplotlib) into Power BI to isolate and visualize the distribution of the top decile (top 10%) of the fastest runners by distance.



<!--
*(Proximamente Screenshots: `![View Name](path/to/image.png)`)*


