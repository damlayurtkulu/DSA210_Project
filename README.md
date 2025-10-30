# The Impact of Unemployment Rates on Consumer Spending Behavior in the United States

# Research Question
Do individuals in states with higher unemployment rates spend less on average?

# Motivation
One of the most important measures of a nation's economic health is consumer spending. Household income and confidence frequently fall when unemployment increases, which may result in less spending.  
The purpose of this project is to investigate whether the US exhibits this pattern: *Do residents in states with greater unemployment rates, on average, spend less money?  

Understanding how macroeconomic variables, including unemployment, impact routine financial behavior is the driving force behind this study. Economists and marketing experts that research customer behavior in various economic environments may find value in the findings.

# Data Sources
This project combines two publicly available datasets to enrich the analysis:

1. **Customer Purchase Behavior Dataset**  
   - Source: Kaggle – Customer Purchase Behaviour (shopping_behavior_updated.csv) 
   - Description: Contains demographic and behavioral information about customers in the U.S., including age, gender, location, and purchase amount.

2. **Unemployment in America per U.S. State Dataset**  
   - Source: Kaggle – Unemployment in America (Unemployment in America Per US State.csv)
   - Description: Provides unemployment rates by state across the United States.

The shopping dataset's location column will be mapped to states in the United States, enabling the two datasets to be combined using a common state variable.

# Methodology
1. **Data Cleaning:**  
   - Remove missing or inconsistent entries from both datasets.  
   - Standardize the location names in the shopping dataset to match the state names in the unemployment dataset.

2. **Data Integration (Enrichment):**  
   - Merge both datasets by the state column to attach each customer record with that state’s unemployment rate.

3. **Data Analysis:**  
   - Calculate the average purchase amount per state.  
   - Explore the relationship between unemployment rate and spending behavior using correlation analysis and scatter plots.  
   - Investigate whether higher unemployment rates are associated with lower consumer spending.

4. **Visualization:**  
   - Plot graphs such as scatter plots and bar charts to illustrate trends and relationships between variables.

# Expected Outcome
It is hypothesized that higher unemployment rates will correlate with lower average spending amounts across states.  
This would support the idea that because of financial instability or lower income, customers in economically distressed places typically spend less.

If the association is weak or positive, it may indicate that variables other than unemployment alone, such the use of credit, cultural practices, or regional price disparities, are more important.

# Limitations & Future Work
- The datasets are aggregated by state and may not perfectly represent all individual behaviors.  
- Income levels, living costs, and local economic factors are not directly included in this analysis.  
- Future work could expand the dataset by including average income per state or inflation-adjusted spending to strengthen the results.

# Tools
- **Python Libraries:** pandas, matplotlib, seaborn  
- **Environment:** Jupyter Notebook / Google Colab

*Prepared by Emine Damla Yurtkulu*  
*Course: DSA210 – Introduction to Data Science*  
*Fall 2025*


