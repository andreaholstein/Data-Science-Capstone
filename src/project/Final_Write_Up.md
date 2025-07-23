# DSI Group Project Team 3

## Case Study

- A major clothing brand, popular with athletes and young women, is looking to open a new brick-and-mortar store, and hopes to launch a new store promotion. The brand needs to identify the optimal geographical location to open a new store based on where their target shopper demographic is located, and tailoring their promotion to incentivize new and existing shoppers to visit the new store and drive sales conversions.
- Our stakeholders are: the brand's marketing and sales departments, product managers & data analysts, the finance team and senior leadership (operations).
- The outcome of our analysis will help inform the brand's marketing strategies, and product offerings in certain jurisdictions. It will also inform annual budgeting. This project will offer additional insight into customer shopping behaviours, and inform strategies to retain and acquire customers.
- Our project will demonstrate a keen understanding of how to identify business opportunities and apply data-driven decision-making in the retail & commerce sector.

## Business Motivation

- Analyzing customer demographics, we will identify the optimal location for a new store, and tailor their launch promotion to target new and existing customers based on those criteria.

## Dataset Used

- [Dataset from Kaggle](https://www.kaggle.com/datasets/datascientistanna/customers-dataset)

## Project Overview (Table of Contents)

### Requirements:

This project uses the following Python libraries:

- NumPy: For fast matrix operations.
- pandas: For analysing and getting insights from datasets.
- matplotlib: For creating graphs and plots.
- seaborn: For creating graphs and plots.

Additionally, we used Jupyter notebooks to run all the code, and our dataset is--as mentioned above--from Kaggle.

### Methodology:

- (Adi's Comments) Methodology: Outline the specific steps you’ll take—e.g. geocoding customer addresses, calculating catchment areas, scoring locations by foot traffic or demographic fit—and any algorithms or other libraries/datasets you will use.

### Review of Raw Data and Exploratory Data Analysis:

- Understanding the Raw Data
  - List features and data types
- Understanding the Features
- Correlation between features

### Conclusion of reviewing the raw data and EDA:

- How many states are there?
- How many of each gender?
- What categories are there?
- What season has the most spending?
- How many customers have subscriptions?
- What items are sold?

### Assumptions, Limiting Conditions, Data Risks:

(Adi's Comments) Data risks & assumptions: You note bias and initial assumptions—consider specifying how you’ll test for sampling bias (e.g., comparing dataset demographics to census data) and how you’ll handle missing or sparse location data.

- Our inital dataset was not suitable for our business problem. This resulted in us sourcing another dataset from Kaggle.
- At the beginning, we believed we could assume who the target demographic of our brand is - our challenge was to perform our analysis agnostic of that assumption to see if our hypothesis aligns with our conclusion.
- We had concerns that the data may be biased: we did in fact identify a considerable class imbalance between the sexes of the respondents in our dataset which we balanced, and performed our analyses on this updated dataset.
- Some of our initial data analysis proved redundant as we learned more about the process. For instance, we initially thought we might need to create smaller samples to perform our analysis on, thinking our dataset might be too large and performance-demanding. However, that proved to not be necessary, and so we performed our analyses on the full dataset.

### Data Cleaning:

For data cleaning, we first performed validation on the dataset to check for missing data, nulls, or invalid data types. We also ran checks to check for typos in the string data, and renamed the column headers in our datafram for more legibility.

### Data Cleaning Conclusions:

All-in-all, our dataset was very clean, and no data needed to be dropped or imputed to correct for missing information.

We identified a class imbalance issue in our dataset, where the data was skewed heavily toward male values: we balanced this by oversampling female values until parity between the sexes of the respondents was reached.

### Analytics:

- age groups (filtering)
- gender and purchase amount
- purchase amount by location
- previous purchases by location
- category by purchase amount (insight into high-purchase categories to prioritize product inventory)
- category by purchase amount by location - inform what promotions to run

## Final Conclusions:

- (Adi's Comments) Evaluation criteria: Define how you’ll judge “optimal” location—will you use distance buffers, drive-time analysis, or demographic thresholds? Mention your metrics or scoring rubric.

## Other requirements

### Team Videos:

-

### Team Work Structure:

- ## Worked together on:
- ## Worked dependently on:

### Reproducibility:

- Project includes one fully reproducible feature
- Reproduction instructions are clear and include
  - Data access
  - Software/environment dependencies
  - File structure
