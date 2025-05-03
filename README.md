# Market-Basket-Analysis
![image](https://github.com/user-attachments/assets/b956acd2-1a86-405e-bc99-d8ff5dfc4b54)
## Overview
For this project, I'm analyzing shopping patterns for a retail company to uncover which products customers frequently buy together. This market basket analysis reveals valuable insights into customer behavior that can help the company enhance customer satisfaction, make more strategic decisions, and boost sales.

## Tools
- Python
- Jupyter Notebook
#### Python Libraries used
Pandas - Data cleaning and preprocessing
mlxtend - Basket Analysis
matplotlib - Visualization
seaborn - Visualization
#### ML Algorithm used
Apriori algorithm

## Steps
### 1. Data Preparation
- Imported necessary libraries
- Checked for null values, none were found
- Removed duplicates
- Changed the date column from string to datetime and member number from int to string
- Feature engineering: generated day, month, and year feature from date

### 2. Exploratory Data Analysis
- Count of unique customers
- Count of unique items
- Average visits per customer
- Top 10 most bought items
- 10 least bought items
- Count of items bought every month
- count of products bought yearly and percentage increase

### 3. Market Basket Analysis
- Grouped member number and date to get the items bought by a particular member (basket). I then made a list of lists out of the baskets and calculated the support metrics for each item.
- I then encoded the list of baskets and converted into a dataframe
- Applied apriori algorithm into the dataframe to get fequent itemsets, to get this, minimum support is set at 0.005 in order to get itemsets that appear in at least 0.5% transactions
- Created rules using association_rules function, using lift as it provides the measure of strength of association of items
- Sorted the results by zhangs metric as it identifies  strong associations as it incorporates confidence rule and support.

### 4. Visualization
- Histogram showing frequencies of the number of items per customer
- Histogram showing frequencies of the number of average visits per customer
- Bar chart showing  top 10. customers in terms of no. of items bought
- Bar chart showing top 10. most bought items
- Bar chart showing 10 least bought items
- Line plot showing trends for across the years
- Heatmap of antecedents and consequents using zhangs metric

### Communication and Insights
**Exploratory Data Analysis**
- The total number of unique customers is 3898
- The total number of unique items bought is 167
- The average number of visits per customer is 4
- The total number of customers who have visited the store less than 4 times is 1849 which is 47.43% of the total customers
- 57.52% of the customers have visited the store more than 4 times
- The total number of sales increased by 10.85% between 2014 and 2015
- The month with the highest cummulative sales is August while December has the least

**Market Basket Analysis**
- Whole milk, other vegetable, yogurt, soda, and rolls/buns are the most frequently bought items
- Frankfurters and other vegetables are likely to  be bought together. With a lift of 0.1, it means that customers who buy frankfurters are more likely to buy other vegetables compared to those who do not buy them.
- Sausages and yogurt are frequently bought together

**Recommendations**
- Most customers buy goods in small quantities, the store could offer bulk discounts to encourage customers to buy in bulk
- A good number of customers have been to the store less than 4 times. The store should investigate the cause for this, whether it's just customer churn or just less frequent buyers.
- There is seems to be significant low sales across the months. The store could utilize seasonal trends to inform promotional campaigns.
- Place frequently bought together items adjacent to each other for easier visibility. For example, sausage and yogurt, frankfurter and other vegetables

