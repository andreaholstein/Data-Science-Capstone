#Title 

#Introduction - done 

#Business Case - Done

#Dataset Used - Done (Update)

#Project Overview (Table of Contents)

Requirements: (All)
- This project uses the following Python libraries
- (Adi's Comments)Tech stack: List the tools, languages, and frameworks (Python, Jupyter, mapping libraries, dashboard platform) along with what you’ll deliver (heatmaps, interactive map, slide deck) and a roadmap of the 5 day sprint.

This project uses the following Python libraries

*NumPy: For efficient numerical computations and array/matrix operations.

*Pandas: For data cleaning, transformation, and insightful analysis of structured datasets.

*Matplotlib.pyplot: For creating static visualizations like line charts, bar graphs, and scatter plots.

*Seaborn: For enhancing matplotlib plots with advanced statistical graphics and improved aesthetics.

*SciPy: For advanced scientific computing, including optimization, statistics, and signal processing.

*Scikit-learn machine learning utilities (used for resampling, e.g., class balancing)

*Plotly Express (import plotly.express as px) — interactive visualizations
 

Methodology (All) 
- (Adi's Comments) Methodology: Outline the specific steps you’ll take—e.g. geocoding customer addresses, calculating catchment areas, scoring locations by foot traffic or demographic fit—and any algorithms or other libraries/datasets you will use.


To evaluate potential store locations and customer behavior patterns, the following multi-step methodology was applied:
 1- Data Preprocessing & Cleaning
    *Loaded and cleaned the customer dataset using Pandas.
    *Handled missing values, standardized column names, and transformed categorical features where necessary.

 2- Exploratory Data Analysis (EDA)
    *Used Seaborn, Matplotlib, and Plotly Express to explore customer distribution by age, gender, location, and purchasing behavior.
    *Identified key metrics such as total spending, repeat purchases, and product category trends across different regions.

 3-Dealing with Class Imbalance
    *Applied resampling techniques to balance customer classes when modeling or analyzing groups

 4- Visualization Dashboards
    *Bar Charts – For comparing category-level totals (e.g., product categories, locations).
    *Heatmaps – For visualizing customer concentration across locations
    *Count Plots – To show distribution of customers by gender and other discrete features 
    *Pie Charts – Used to represent proportional data such as the total purchase distribution by product category.
    *Area Plots – Included to track cumulative or continuous trends over categories.
    *Scatter Plots – For bubble charts showing relationships between customer count, repeat purchases, and total spend.
  
 5- Geographic Analysis
    *Heatmaps and bubble charts use to represent store location potential and customer behavior density.
 


Review of Raw Data and Exploratory Data Analysis (Joanne)
- Understanding the Raw Data
    - List features and data types
- Understanding the Features
- Correlation between features 

Conclusion of reviewing the raw data and EDA (Joanne)
- How many states are there?
- How many of each gender?
- What categories are there?
- What season has the most spending?
- How many customers have subscriptions?
- What items are sold?

Assumptions, Limiting Conditions, Data Risks (Joanna)
(Adi's Comments) Data risks & assumptions: You note bias and initial assumptions—consider specifying how you’ll test for sampling bias (e.g., comparing dataset demographics to census data) and how you’ll handle missing or sparse location data.

Data Cleaning (Andrea and Joanne )
- Column titles 
- Check for nulls 
- Check data types 
- Class imbalance (Joanne)

Data Cleaning Conclusions (Andrea and Joanne)
- Impact of the class imbalance 
- Dropping any data?


Analytics (Dianne, Ayshe, Mirian, Crystal)
- age groups (filtering) (Average Purchase Amount by Age Group and Gender)
            *This chart displays the distribution of customers across different age groups, categorized into defined age bins (e.g., 20s, 30s, etc.). The bars represent the number of customers in each group, with quantity labels added for clarity.
            *The 20s and 30s age groups have the highest concentration of customers, indicating that younger adults form the core of our customer base.
            *The number of customers gradually declines with age, with fewer customers aged 60 and above.
            *The <20 age group is relatively small, suggesting limited engagement from teenagers.
            *The majority of our customers fall between the ages of 20 to 39, making this a key demographic for campaigns, product design, and customer loyalty programs.
- gender and purchase amount (Average Purchase Amount by Gender) (Top 30 Locations)
            *This bar chart illustrates the average amount spent per purchase, segmented by both age group and gender. The age groups are evenly categorized by decades (e.g., 20s, 30s, 40s), and the comparison between genders provides insights into customer value across different demographics.
            *Customers in their 30s and 40s tend to spend the most on average, regardless of gender.
            *In many age groups, female customers spend slightly more on average than male customers.
            *After age 60, average purchase amounts decline for both genders, suggesting reduced spending or more conservative purchasing habits in older customers.
            *Alaska, North Dakota, Pennsylvania, Arkansas, Michigan; These states show the highest average purchase amounts, especially from female customers.
                -Premium targeting: Alaska and Pennsylvania are promising regions for premium offerings.
                -Female-focused marketing: Consider campaigns that target female demographics in high-spending states.

- purchase amount by location
- previous purchases by location
- category by purchase amount (insight into high-purchase categories to prioritize product inventory)
- category by purchase amount by location - inform what promotions to run

Final Conclusions (All)
- (Adi's Comments) Evaluation criteria: Define how you’ll judge “optimal” location—will you use distance buffers, drive-time analysis, or demographic thresholds? Mention your metrics or scoring rubric.

    #The most attractive locations for opening a new store are those with a high number of customers, strong loyalty, and large total spending. 
    #These are visualized as large, dark bubbles in the upper-right of the plot.
    #Locations in the top-right quadrant with large, dark bubbles are strong candidates for store expansion. 
    # These regions combine:large and loyal customer base High total spending
    #Locations with a large customer base but low repeat purchases may benefit from targeted loyalty programs or promotions before committing to physical expansion.
    #Locations with high repeat purchase rates but smaller customer counts suggest untapped potential — perhaps a niche market or underserved area worth exploring with a   smaller-format store or digital presence.
    #Montana stands out due to maxed-out total purchase and customer volume, even with moderate loyalty.
    #Illinois is a well-balanced candidate with strong scores across the board.
    #California has the largest customer base, but relatively lower repeat purchases, so may need loyalty incentives.

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


