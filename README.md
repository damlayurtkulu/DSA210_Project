# The Impact of Unemployment Rates on Consumer Spending Behavior in the United States

# Research Question
How do differences in state-level unemployment rates influence multiple aspects of consumer shopping behavior including average spending per transaction, purchase frequency, discount/promo-code usage, and subscription status?

# Motivation
Consumer spending is one of the most important indicators of economic stability.  Households frequently face decreased income security and become more cautious with their financial decisions when unemployment increases.  These changes may have an impact on consumers' spending patterns, frequency of purchases, and reliance on discounts or subscriptions.

The goal of this experiment is to determine whether the US mirrors this larger economic trend: Do people who live in states with greater unemployment rates spend differently for example, by utilizing more discounts and promo codes, shopping less frequently, or spending less per purchase?

Understanding how macroeconomic factors like unemployment shape everyday financial behaviors is the primary motivation behind this study. The findings may offer useful insights for economists studying consumer reactions to economic stress, as well as for businesses and marketing professionals seeking to adapt their strategies in regions with varying economic conditions.

# Data Sources
This project combines two publicly available datasets to enrich the analysis:

1. **Customer Purchase Behavior Dataset**  
   - Source: Kaggle – Customer Purchase Behaviour (shopping_behavior_updated.csv) 
   - Description: Contains demographic and behavioral information about customers in the U.S., including age, gender, location, and purchase amount.
   - Data Set Link: https://www.kaggle.com/datasets/mubeenshehzadi/customer-purchase-behaviour

2. **Unemployment in America per U.S. State Dataset**  
   - Source: Kaggle – Unemployment in America (Unemployment in America Per US State.csv)
   - Description: Provides unemployment rates by state across the United States.
   - Data Set Link: https://www.kaggle.com/datasets/justin2028/unemployment-in-america-per-us-state

The shopping dataset's location column will be mapped to states in the United States, enabling the two datasets to be combined using a common state variable.

# Methodology
1. **Data Cleaning:**  
   - Remove missing or inconsistent entries from both datasets.  
   - Standardize or map shopping-dataset locations to official U.S. state names.
   - Convert unemployment dataset into a state-level summary (e.g., average unemployment rate).

2. **Data Integration (Enrichment):**  
   - Merge datasets on state to associate each consumer record with that state's unemployment rate.
   - Create unemployment rate groupings (e.g., low, medium, high) to compare behavioral differences across economic conditions.

3. **Data Analysis:**   
For each behavioral dimension tied to the research question:
   - Average Spending: Calculate and compare spending tendencies across unemployment groups; apply correlation and regression analysis.
   - Purchase Frequency: Estimate frequency measures and test their relationship with unemployment levels.
   - Discount/Promo Usage: Compare proportions of discount and promo-code usage across unemployment groups.
   - Subscription Status: Examine how subscription adoption varies by unemployment level.
     
4. **Visualization:**  
   - Scatter plots illustrating unemployment vs. spending and unemployment vs. purchase frequency.
   - Bar charts comparing discount usage, promo usage, and subscription rates across unemployment groups.
   - Boxplots and distribution plots for spending and purchase frequency.
   - Correlation heatmaps summarizing relationships among major variables.
  
# Hypotheses

Based on the research question, the following hypotheses will be tested:

- H1 Spending Behavior: Consumers living in states with higher unemployment rates will spend less on average per transaction.
- H2 Purchase Frequency: Higher unemployment rates will be associated with lower purchase frequency, meaning consumers in these states shop less often.
- H3 Discount & Promo Code Usage: Consumers in states with higher unemployment levels will show a greater likelihood of using discounts or promo codes as a cost-saving strategy.
- H4 Subscription Status: Higher unemployment rates will correlate with lower subscription participation, as consumers in economically distressed areas may avoid or cancel subscription-based services.

# Expected Outcome
It is hypothesized that higher unemployment rates will be associated with noticeable shifts in consumer behavior across states. Customers are predicted to spend less per transaction, shop less frequently, rely more on discounts or promo codes, and exhibit lower subscription participation in areas with significant unemployment.
Such patterns would support the idea that financial instability encourages individuals to reduce discretionary spending and adopt more cost saving strategies.

If these correlations prove to be weak or inconsistent, it might indicate that variables other than unemployment like credit availability, local cultural customs, marketing strategies, or pricing variations have a greater impact on consumer purchasing decisions.

# Analysis Results

 - ## H1: Relationship Between Unemployment Rate and Average Purchase Amount

   This hypothesis examined whether higher unemployment rates in U.S. states correspond to a decrease in the average purchase amount per transaction. A Pearson correlation test was performed to measure the linear association between the two variables.
   
   Correlation coefficient: 0.0369
   
   P-value: 0.021
   
   Although the p-value is below 0.05, indicating statistical significance, the actual correlation coefficient is very close to zero. This implies that the relationship between unemployment rate and average spending is extremely weak and practically negligible. In other words, even if the association is statistically detectable, it is far too small to have any real-world significance.
   
   Interpretation: The data does not support the expectation that individuals in high-unemployment states spend less. Average purchase amounts remain nearly constant regardless of unemployment levels.

   ### H1 is not supported.
   
 - ## H2: Relationship Between Unemployment Rate and Purchase Frequency
   This hypothesis proposed that consumers in states with higher unemployment rates shop less frequently. Since purchase frequency was expressed using labels such as “Weekly,” “Monthly,” or “Annually,” these categories were converted into approximate numerical frequencies. Missing values were removed before applying Pearson correlation.
   
   Correlation coefficient: 0.0221
   
   P-value: 0.2027
   
   The correlation is again extremely close to zero, and the p-value is well above 0.05, indicating no statistical significance.
   
   Interpretation: There is no evidence that purchase frequency differs meaningfully based on unemployment rates. Consumers appear to maintain similar shopping routines regardless of the economic conditions of their state.
   
   ### H2 is not supported.
   
 - ## H3: Association Between Unemployment Group and Discount/Promo Code Usage
   To test whether consumers in high-unemployment states rely more on discounts or promo codes, a chi-square test was conducted using unemployment groups (Low, Medium, High) and the “Discount Applied” variable.
   
   Chi-square statistic: 0.4648
   
   P-value: 0.7926
   
   The extremely high p-value indicates no statistically significant relationship between unemployment level and discount usage.
   
   Interpretation: Consumers do not appear more likely to use discounts or promotional codes simply because they live in states with higher unemployment. Discount usage remains nearly identical across all unemployment categories.
   
   ### H3 is not supported.
 - ## H4: Association Between Unemployment Group and Subscription Status

   This hypothesis tested whether subscription-based purchases (e.g., membership or recurring services) differ across unemployment levels. A chi-square test was conducted.
   
   Chi-square statistic: 0.6545
   
   P-value: 0.7209
   
   Again, the p-value is high, indicating no significant association.
   
   Interpretation: Subscription behavior does not change meaningfully across unemployment levels. Consumers in high-unemployment states maintain subscriptions at rates similar to those in low-unemployment states.
   
   ### H4 is not supported.

# Limitations & Future Work
- The datasets are aggregated by state and may not perfectly represent all individual behaviors.  
- Income levels, living costs, and local economic factors are not directly included in this analysis.
- The unemployment dataset provides state-level information; local or city-level economic conditions are not captured.  
- Future work could expand this analysis by incorporating additional economic indicators such as median income, inflation rates, or consumer confidence indices for each state to better contextualize spending behavior. Instead of depending only on static comparisons, another approach would be to examine time-series patterns, which could show how consumer behavior changes as unemployment rises or falls. Additionally, exploring further behavioral dimensions—such as product category preferences, cart size, or repeat-purchase patterns—could provide a more detailed understanding of how economic conditions shape consumer decision-making.

# Tools
- **Python Libraries:** pandas, matplotlib, seaborn  
- **Environment:** Jupyter Notebook / Google Colab

*Prepared by Emine Damla Yurtkulu*  
*Course: DSA210 – Introduction to Data Science*  
*Fall 2025*


