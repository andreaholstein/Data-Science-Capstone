# DSI Group Project Team 3

## Case Study

- A major clothing brand, popular with athletes and young women, is looking to open a new brick-and-mortar store, and hopes to launch a new store promotion. The brand needs to identify the optimal geographical location to open a new store based on where their target shopper demographic is located, and tailoring their promotion to incentivize new and existing shoppers to visit the new store and drive sales conversions.
- Our stakeholders are: the brand's marketing and sales departments, product managers & data analysts, the finance team and senior leadership (operations).
- The outcome of our analysis will help inform the brand's marketing strategies, and product offerings in certain jurisdictions. It will also inform annual budgeting. This project will offer additional insight into customer shopping behaviours, and inform strategies to retain and acquire customers.
- Our project will demonstrate a keen understanding of how to identify business opportunities and apply data-driven decision-making in the retail & commerce sector.

## Business Motivation

- Analyzing customer demographics, we will identify the optimal location for a new store, and tailor their launch promotion to target new and existing customers based on those criteria.

## Dataset Used

- [Shop Customer Data Dataset from Kaggle](https://www.kaggle.com/datasets/datascientistanna/customers-dataset)

## Project Overview (Table of Contents)

### Requirements:

This project uses the following Python libraries:

\*NumPy: For efficient numerical computations and array/matrix operations.

\*Pandas: For data cleaning, transformation, and insightful analysis of structured datasets.

\*Matplotlib.pyplot: For creating static visualizations like line charts, bar graphs, and scatter plots.

\*Seaborn: For enhancing matplotlib plots with advanced statistical graphics and improved aesthetics.

\*SciPy: For advanced scientific computing, including optimization, statistics, and signal processing.

\*Scikit-learn machine learning utilities (used for resampling, e.g., class balancing)

\*Plotly Express (import plotly.express as px) — interactive visualizations

Additionally, we used Jupyter notebooks to run all the code, and our dataset is--as mentioned above--from Kaggle.

### Methodology:

- (Adi's Comments) Methodology: Outline the specific steps you’ll take—e.g. geocoding customer addresses, calculating catchment areas, scoring locations by foot traffic or demographic fit—and any algorithms or other libraries/datasets you will use.

To evaluate potential store locations and customer behavior patterns, the following multi-step methodology was applied:
1- Data Preprocessing & Cleaning
*Loaded and cleaned the customer dataset using Pandas.
*Handled missing values, standardized column names, and transformed categorical features where necessary.

2- Exploratory Data Analysis (EDA)
*Used Seaborn, Matplotlib, and Plotly Express to explore customer distribution by age, gender, location, and purchasing behavior.
*Identified key metrics such as total spending, repeat purchases, and product category trends across different regions.

3-Dealing with Class Imbalance
\*Applied resampling techniques to balance customer classes when modeling or analyzing groups

4- Visualization Dashboards
*Bar Charts – For comparing category-level totals (e.g., product categories, locations).
*Heatmaps – For visualizing customer concentration across locations
*Count Plots – To show distribution of customers by gender and other discrete features
*Pie Charts – Used to represent proportional data such as the total purchase distribution by product category.
*Area Plots – Included to track cumulative or continuous trends over categories.
*Scatter Plots – For bubble charts showing relationships between customer count, repeat purchases, and total spend.

5- Geographic Analysis
\*Heatmaps and bubble charts use to represent store location potential and customer behavior density.

### Review of Raw Data and Exploratory Data Analysis:

- Understanding the Raw Data
  The dataset contains 18 features: Unnamed:0 (int64), Customer ID (int64), Age (int64), Gender (object), Item Purchased (object), Category (object), Purchase Amount (USD) (int64), Location (object), Color (object), Season (object), Review Rating (float64), Subscription Status (object), Shipping Type (object), Discount Applied (object), Promo Code Used (object), Previous Purchases (int64), Payment Method (object), and Frequency of Purchases (object). This mix of numerical and categorical data provides insights into customer demographics, purchasing behavior, and preferences.
- Understanding the Features
  Features capture customer details (e.g., Age, Gender, Location), purchase specifics (e.g., Item Purchased, Category, Purchase Amount), and engagement metrics (e.g., Subscription Status, Previous Purchases). Categorical features like Color, Season, and Shipping Type allow segmentation, while numerical features like Review Rating and Purchase Amount enable quantitative analysis of trends and correlations.
- Correlation between features
  Purchase Amount (USD) shows weak correlations with Age and Review Rating, suggesting no strong linear relationship. Subscription Status and Promo Code Used are highly correlated, indicating subscribers frequently use discounts, which could influence spending patterns.

### Conclusion of reviewing the raw data and EDA:

- How many states are there?
  There are 50 unique states in the dataset
- How many of each gender?
  The dataset includes 2652 males and 1248 females
- What categories are there?
  There are 4 product categories - Clothing, Accessories, Footwear, Outerwear. Clothing is the category with the most purchases
- What season has the most spending?
  Fall has the highest spending
- How many customers have subscriptions?
  1053 customers have subscriptions
- What items are sold?
  25 unique items are sold, including Blouse, Sweater, Jeans, Handbag, etc.

### Assumptions, Limiting Conditions, Data Risks:

(Adi's Comments) Data risks & assumptions: You note bias and initial assumptions—consider specifying how you’ll test for sampling bias (e.g., comparing dataset demographics to census data) and how you’ll handle missing or sparse location data.
The dataset assumes representative sampling of customer purchases but may contain biases due to uneven gender distribution or sparse location data, potentially skewing demographic insights. To address sampling bias, compare dataset demographics (e.g., age, gender) to U.S. census data; sparse location data should be handled by grouping low-sample regions or imputing missing values cautiously to avoid distorting geographic trends. Data risks include potential inconsistencies in categorical entries (e.g., typos in Color or Item Purchased) and incomplete records, which could affect analysis reliability.

- Our inital dataset was not suitable for our business problem. This resulted in us sourcing another dataset from Kaggle.
- At the beginning, we believed we could assume who the target demographic of our brand is - our challenge was to perform our analysis agnostic of that assumption to see if our hypothesis aligns with our conclusion.
- We had concerns that the data may be biased: we did in fact identify a considerable class imbalance between the sexes of the respondents in our dataset which we balanced, and performed our analyses on this updated dataset.
- Some of our initial data analysis proved redundant as we learned more about the process. For instance, we initially thought we might need to create smaller samples to perform our analysis on, thinking our dataset might be too large and performance-demanding. However, that proved to not be necessary, and so we performed our analyses on the full dataset.

### Data Cleaning:

For data cleaning, we first performed validation on the dataset to check for missing data, nulls, or invalid data types. We also ran checks to check for typos in the string data, and renamed the column headers in our dataframe for more legibility.

The dataset exhibits a significant gender imbalance, with 2652 males and 1248 females, as observed in the EDA. The class_imbalance.ipynb script attempts to address this by oversampling the minority class (Female) to match the majority class (Male), creating a balanced dataset with equal gender representation.

### Data Cleaning Conclusions:

All-in-all, our dataset was very clean, and no data needed to be dropped or imputed to correct for missing information.

We identified a class imbalance issue in our dataset, where the data was skewed heavily toward male values (2652 males vs. 1248 females). Concerned that this would potentially skewing insights into purchasing behavior, we balanced this by oversampling the female class, as implemented in the updated script, balances the dataset, improving model fairness and ensuring equitable representation in analyses.

### Analytics:

- age groups (filtering) (Average Purchase Amount by Age Group and Gender)
  *This chart displays the distribution of customers across different age groups, categorized into defined age bins (e.g., 20s, 30s, etc.). The bars represent the number of customers in each group, with quantity labels added for clarity.
  *The 20s and 30s age groups have the highest concentration of customers, indicating that younger adults form the core of our customer base.
  *The number of customers gradually declines with age, with fewer customers aged 60 and above.
  *The <20 age group is relatively small, suggesting limited engagement from teenagers.
  \*The majority of our customers fall between the ages of 20 to 39, making this a key demographic for campaigns, product design, and customer loyalty programs.
- gender and purchase amount (Average Purchase Amount by Gender) (Top 30 Locations)
  *This bar chart illustrates the average amount spent per purchase, segmented by both age group and gender. The age groups are evenly categorized by decades (e.g., 20s, 30s, 40s), and the comparison between genders provides insights into customer value across different demographics.
  *Customers in their 30s and 40s tend to spend the most on average, regardless of gender.
  *In many age groups, female customers spend slightly more on average than male customers.
  *After age 60, average purchase amounts decline for both genders, suggesting reduced spending or more conservative purchasing habits in older customers.
  \*Alaska, North Dakota, Pennsylvania, Arkansas, Michigan; These states show the highest average purchase amounts, especially from female customers.
  -Premium targeting: Alaska and Pennsylvania are promising regions for premium offerings.
  -Female-focused marketing: Consider campaigns that target female demographics in high-spending states.

- purchase amount by location
- previous purchases by location
- category by purchase amount (insight into high-purchase categories to prioritize product inventory)
- category by purchase amount by location - inform what promotions to run

## Final Conclusions:

- (Adi's Comments) Evaluation criteria: Define how you’ll judge “optimal” location—will you use distance buffers, drive-time analysis, or demographic thresholds? Mention your metrics or scoring rubric.

- The most attractive locations for opening a new store are those with a high number of customers, strong loyalty, and large total spending.
- These are visualized as large, dark bubbles in the upper-right of the plot.
- Locations in the top-right quadrant with large, dark bubbles are strong candidates for store expansion.

### These regions combine:large and loyal customer base High total spending

- Locations with a large customer base but low repeat purchases may benefit from targeted loyalty programs or promotions before committing to physical expansion.
- Locations with high repeat purchase rates but smaller customer counts suggest untapped potential — perhaps a niche market or underserved area worth exploring with a smaller-format store or digital presence.
- Montana stands out due to maxed-out total purchase and customer volume, even with moderate loyalty.
- Illinois is a well-balanced candidate with strong scores across the board.
- California has the largest customer base, but relatively lower repeat purchases, so may need loyalty incentives.

## Other requirements

### Team Videos:

-

### Team Work Structure:

- ## Worked together on:
- ## Worked dependently on:

### Reproducibility:
