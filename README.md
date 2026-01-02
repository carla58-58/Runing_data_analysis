# Runing_data_analysis

# Ultra-Marathon Running Data Analysis

**View the interactive notebook on Google Colab:**  
[Open in Google Colab](https://colab.research.google.com/drive/1G-fN6EwIXIJuQK-ECDRe3mx67HP7lXHv?usp=sharing)

## 1. Project Overview

**Objective:**  
Explore and analyze ultra-marathon race data (50km and 50mi races in the USA) to understand athlete performance, demographic trends, and seasonal effects.

**Key Business Questions:**
- How do gender and age impact ultra-marathon performance?
- Which age groups perform best in long-distance races?
- Are there seasonal trends affecting athlete speed?
- How stable is athlete performance over time?
- What relationships exist between age, speed, and event size?

**Dataset:**  
- **Source:** TWO_CENTURIES_OF_UM_RACES.csv  
- **Features:** race date, race name, distance, number of finishers, athlete ID, gender, age, performance, average speed

## 2. Data Loading & Initial Inspection

- Loaded data from `TWO_CENTURIES_OF_UM_RACES.csv`
- Inspected shape, columns, data types, and previewed the first few rows to understand the dataset structure

## 3. Data Cleaning

- **Filtering:**  
  - Selected USA races of 50km or 50mi distance for the year 2018
  - Removed country codes from race names

- **Feature Engineering:**  
  - Calculated athlete age from event year and year of birth
  - Cleaned performance time entries

- **Missing Values:**  
  - Dropped rows with missing or invalid values in key columns

- **Duplicates:**  
  - Removed duplicate rows to ensure data integrity

- **Data Types:**  
  - Converted columns to appropriate data types for analysis

- **Column Renaming & Reordering:**  
  - Renamed columns for clarity and reordered for readability

## 4. Exploratory Data Analysis (EDA)

- **Summary Statistics:**  
  - Calculated mean, median, standard deviation, and counts for average speed by gender and race length

- **Age and Speed Distributions:**  
  - Plotted histograms of athlete age and average speed, segmented by gender and race length

- **Boxplots & Violin Plots:**  
  - Visualized speed distributions by gender, race length, and age group

- **Regression Analysis:**  
  - Explored the relationship between age and speed for each gender

## 5. Statistical Testing

- **T-Test:**  
  - Compared average speeds between male and female athletes in 50mi races

- **ANOVA:**  
  - Assessed differences in average speed across age groups for 50mi races

## 6. Seasonal Analysis

- Extracted race month and assigned each race to a season (Winter, Spring, Summer, Fall)
- Analyzed average speed by season and visualized with boxplots

## 7. Trend Analysis

- Extracted year from race date
- Plotted yearly trends in athlete average speed (if data from multiple years available)

## 8. Correlation Analysis

- Computed and visualized correlations between athlete age, average speed, and number of finishers

## 9. Key Findings & Conclusion

- Male athletes consistently achieve higher average speeds than females in both 50km and 50mi races; this difference is statistically significant.
- Athletes aged 30–49 perform best in 50mi races; average speed declines with age.
- 50km races yield higher average speeds than 50mi races, regardless of gender.
- Performance is slightly lower in summer, with winter generally seeing higher speeds.
- Participation is highest among males, followed by females.
- Yearly trends show average athlete speed remains relatively stable over time.
- Age and speed are moderately negatively correlated; race size has little effect on individual speed.
- Visualizations confirm these trends and highlight differences across demographic groups.

## 10. Export Cleaned Data

- Saved the cleaned and processed dataset to `cleaned_ultramarathon_data.csv` for future use or sharing

## 11. Technologies Used

- Data Processing: Pandas, NumPy
- Visualization: Seaborn, Matplotlib
- Statistics: SciPy (t-tests, ANOVA)
- Environment: Google Colab (Jupyter)


