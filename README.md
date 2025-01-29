# Sites-Energy-Consumption-Analysis

## Project Overview

This project aims to analyze energy consumption data from network sites to uncover useful insights about energy usage, cost-saving opportunities, and determining the best thresholds for shutting down cells during low-demand periods. The objective is to optimize energy consumption and reduce costs while maintaining operational efficiency.

## Dataset

The project utilizes two primary datasets:

1. **Energy Dataset**: Contains energy consumption information for network sites, with data recorded every half hour in 2013. Each record includes the following columns:
   - `DateTime`: Timestamp for each half-hour period.
   - `Site_id`: Unique identifier for the site.
   - `Cell_id`: Unique identifier for the cell at the site.
   - `Region`: Geographical location of the site.
   - `KWH/hh`: Energy consumption in kilowatt-hours (KWH) for each half-hour period.

2. **Demand Dataset**: Contains energy consumption demand recorded at half-hour intervals with the following columns:
   - `DemandDateTime`: Timestamp for each half-hour period.
   - `Demand`: Energy consumption demand for the corresponding time.

## Methodology

1. **Data Exploration**: The data was thoroughly explored to identify potential issues such as duplicated columns, incorrect data types, null values, outliers, and missing records.
   
2. **Challenges Identified**: Several challenges were faced, including inconsistencies in naming conventions, duplicate rows, incorrect DateTime formats, extreme values, outliers in the energy column, and missing data. Solutions were applied to clean the data.

3. **Pre-Processing**: 
   - Corrected inconsistent names and duplicate rows.
   - Handled missing and extreme values using imputation and median values.
   - Created new columns for further analysis, such as day, month, weekend, and time categories.

4. **Dashboard**

![Image](https://github.com/user-attachments/assets/da02caae-22f5-4380-8cb5-e7d7e474d06b)
![Image](https://github.com/user-attachments/assets/6e1bc894-0061-4d19-aedd-9c7b152b63f7)
![Image](https://github.com/user-attachments/assets/c89c8bdd-5e9e-44cf-920b-631241137670)
![Image](https://github.com/user-attachments/assets/dcca66ef-cc3d-45e8-a17b-4f26c8d7375f)

5. **Hypothesis Testing**: Multiple hypotheses were tested to identify whether there were differences in energy consumption across sites, regions, and times of day. Results showed significant differences in all categories, prompting further optimization.

6. **Optimal Shutdown Thresholds**: Three potential thresholds for cell shutdown during low-demand periods were identified, with different levels of cost and energy savings. These thresholds are:
   - **0.065 (25th Percentile)**: Best for maximizing savings.
   - **0.051 (Most Frequent Value in Low Demand)**: Best for a stable approach.
   - **0.057 (Lowest Median in Sites)**: A balanced solution.

## Business Insights

1. **Regional and Site-Based Energy Consumption**: Energy consumption varies significantly between regions and sites. Focus energy-saving measures on high-consumption regions (e.g., Region C and Site C) to maximize savings.

2. **Time-Based Energy Usage**: Higher energy usage occurs during peak times, with opportunities for savings during low-demand periods. Scheduling shutdowns during these times can reduce costs.

3. **Cost vs. Demand Dynamics**: Energy costs align with demand levels, with the highest costs during high demand and the lowest during low demand. Optimizing energy usage during high-cost periods by shutting down low-priority cells can lead to savings.

4. **Threshold Selection for Savings**: Different thresholds for cell shutdown yield varying levels of savings. Businesses can choose a threshold that aligns with their priorities for maximizing savings, minimal disruption, or a balanced trade-off.

## Tools and Libraries Used

- **Python**: For data cleaning, analysis, and visualization.
- **Pandas**: Data manipulation and analysis.
- **Matplotlib/Seaborn**: Visualization libraries for plotting trends.
- **Hypothesis Testing**: To analyze the statistical differences across sites, regions, and times of day.

