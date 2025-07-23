#Title 

#Introduction - done 

#Business Case - Done

#Dataset Used - Done (Update)

#Project Overview (Table of Contents)

Requirements: (All)
- This project uses the following Python libraries
- (Adi's Comments)Tech stack: List the tools, languages, and frameworks (Python, Jupyter, mapping libraries, dashboard platform) along with what you’ll deliver (heatmaps, interactive map, slide deck) and a roadmap of the 5 day sprint.


NumPy : For fast matrix operations.
pandas : For analysing and getting insights from datasets.
matplotlib : For creating graphs and plots
seaborn : 

Methodology (All) 
- (Adi's Comments) Methodology: Outline the specific steps you’ll take—e.g. geocoding customer addresses, calculating catchment areas, scoring locations by foot traffic or demographic fit—and any algorithms or other libraries/datasets you will use.


Review of Raw Data and Exploratory Data Analysis (Joanne)
- Understanding the Raw Data
The dataset contains 18 features: Unnamed:0 (int64), Customer ID (int64), Age (int64), Gender (object), Item Purchased (object), Category (object), Purchase Amount (USD) (int64), Location (object), Color (object), Season (object), Review Rating (float64), Subscription Status (object), Shipping Type (object), Discount Applied (object), Promo Code Used (object), Previous Purchases (int64), Payment Method (object), and Frequency of Purchases (object). This mix of numerical and categorical data provides insights into customer demographics, purchasing behavior, and preferences.
- Understanding the Features
Features capture customer details (e.g., Age, Gender, Location), purchase specifics (e.g., Item Purchased, Category, Purchase Amount), and engagement metrics (e.g., Subscription Status, Previous Purchases). Categorical features like Color, Season, and Shipping Type allow segmentation, while numerical features like Review Rating and Purchase Amount enable quantitative analysis of trends and correlations.
- Correlation between features 
Purchase Amount (USD) shows weak correlations with Age and Review Rating, suggesting no strong linear relationship. Subscription Status and Promo Code Used are highly correlated, indicating subscribers frequently use discounts, which could influence spending patterns.

Conclusion of reviewing the raw data and EDA (Joanne)
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

Assumptions, Limiting Conditions, Data Risks (Joanna)
(Adi's Comments) Data risks & assumptions: You note bias and initial assumptions—consider specifying how you’ll test for sampling bias (e.g., comparing dataset demographics to census data) and how you’ll handle missing or sparse location data.
The dataset assumes representative sampling of customer purchases but may contain biases due to uneven gender distribution or sparse location data, potentially skewing demographic insights. To address sampling bias, compare dataset demographics (e.g., age, gender) to U.S. census data; sparse location data should be handled by grouping low-sample regions or imputing missing values cautiously to avoid distorting geographic trends. Data risks include potential inconsistencies in categorical entries (e.g., typos in Color or Item Purchased) and incomplete records, which could affect analysis reliability.

Data Cleaning (Andrea and Joanne )
- Column titles 
- Check for nulls 
- Check data types 
- Class imbalance (Joanne)
The dataset exhibits a significant gender imbalance, with 2652 males and 1248 females, as observed in the EDA. The class_imbalance.ipynb script attempts to address this by oversampling the minority class (Female) to match the majority class (Male), creating a balanced dataset with equal gender representation.

Data Cleaning Conclusions (Andrea and Joanne)
- Impact of the class imbalance 
The gender imbalance (2652 males vs. 1248 females) may bias predictive models toward male customers, potentially skewing insights into purchasing behavior. Oversampling the female class, as implemented in the updated script, balances the dataset, improving model fairness and ensuring equitable representation in analyses.
- Dropping any data?


Analytics (Dianne, Ayshe, Mirian, Crystal)
- age groups (filtering)
- gender and purchase amount
- purchase amount by location
- previous purchases by location
- category by purchase amount (insight into high-purchase categories to prioritize product inventory)
- category by purchase amount by location - inform what promotions to run

Final Conclusions (All)
- (Adi's Comments) Evaluation criteria: Define how you’ll judge “optimal” location—will you use distance buffers, drive-time analysis, or demographic thresholds? Mention your metrics or scoring rubric.

Other requirements

Team Videos (All)
- 

Team Work Structure (All)
- Worked together on:
    - 
- Worked dependently on:
    - 


Reproducibility (All)
- Project includes one fully reproducible feature 
- Reproduction instructions are clear and include 
    - Data access
    - Software/environment dependencies 
    - File structure 


