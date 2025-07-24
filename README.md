# DSI Group Project Team 3

## 📦 Case Study

A major clothing brand — popular among athletes and young women — is planning to open a new brick-and-mortar store and launch a store-specific promotion. To maximize success, the brand seeks to:

- Identify the **optimal geographical location** for the new store, based on customer demographics and purchasing behavior  
- Design a **targeted promotion** to attract both new and existing shoppers and drive **sales conversions**

### 🎯 Stakeholders

- **Marketing & Sales teams** — to tailor promotions and campaigns  
- **Product Managers & Data Analysts** — to refine regional product strategies  
- **Finance Team** — to support budgeting and ROI forecasting  
- **Senior Leadership (Operations)** — to inform expansion and investment decisions

### 💡 Project Impact

Our analysis aims to:

- Guide **marketing strategies** and regional **product offerings**  
- Support **annual budgeting** and financial planning  
- Provide deeper insight into **customer shopping behavior**  
- Inform tactics to **retain existing customers** and **acquire new ones**

This project showcases the power of **data-driven decision-making** in the retail and commerce sector, with a focus on identifying actionable business opportunities through rigorous analysis.

## 💼 Business Motivation

By analyzing customer demographics and purchase behaviors, this project aims to:

- Identify the **optimal location** for a new physical store
- Design a **tailored launch promotion** that effectively targets both **new and existing customers**
- Align promotional strategies with the brand’s core demographic to **maximize foot traffic** and **drive sales conversions**

## The Dataset

- [Shop Customer Dataset from Kaggle](https://www.kaggle.com/datasets/sahilislam007/shopping-trends-and-customer-behaviour-dataset)

## ⚠️ Challenges on the Horizon

- While we may have initial assumptions about our brand’s target demographic, a key challenge is to conduct our analysis **objectively** to validate (or challenge) those assumptions with data.
- The **initial dataset** provided was not aligned with our business goals, prompting us to source a more suitable dataset from **Kaggle**.
- The data may carry **inherent biases** 

## 👩‍💼The Team:

- Andrea Holstein - [GitHub](https://www.github.com/andreaholstein/) - [LinkedIn](https://www.linkedin.com/in/andrea-holstein/)
- Joanne Leung - [Github](https://github.com/code-me-matcha)
- Mirian Quispe Sarmiento - [Github](https://github.com/KiraLei)
- Crystal Chow - [Github](https://github.com/taltalchow)
- Dianne Dumalag - [Github](https://github.com/ddumalag)
- Aysegul Bozkurt - [Github](https://github.com/ayseboz)

### 💻Requirements:

This project uses the following Python libraries:

- NumPy: For efficient numerical computations and array/matrix operations.

- Pandas: For data cleaning, transformation, and insightful analysis of structured datasets.

- Matplotlib.pyplot: For creating static visualizations like line charts, bar graphs, and scatter plots.

- Seaborn: For enhancing matplotlib plots with advanced statistical graphics and improved aesthetics.

- SciPy: For advanced scientific computing, including optimization, statistics, and signal processing.

- Scikit-learn machine learning utilities (used for resampling, e.g., class balancing)

- Plotly Express (import plotly.express as px) — interactive visualizations

Additionally, we used Jupyter notebooks to run all the code, and our dataset is--as mentioned above--from Kaggle.

### 📊Methodology:

To evaluate potential store locations and customer behavior patterns, the following multi-step methodology was applied:

1. Data Preprocessing & Cleaning

- Loaded and cleaned the customer dataset using Pandas.
- Handled missing values, standardized column names, and transformed categorical features where necessary.

2. Exploratory Data Analysis (EDA)

- Used Seaborn, Matplotlib, and Plotly Express to explore customer distribution by age, gender, location, and purchasing behavior.
- Identified key metrics such as total spending, repeat purchases, and product category trends across different regions.

3. Dealing with Class Imbalance

- Applied resampling techniques to balance customer classes when modeling or analyzing groups

4. Visualization Dashboards

- Bar Charts – For comparing category-level totals (e.g., product categories, locations).
- Heatmaps – For visualizing customer concentration across locations
- Count Plots – To show distribution of customers by gender and other discrete features
- Pie Charts – Used to represent proportional data such as the total purchase distribution by product category.
- Area Plots – Included to track cumulative or continuous trends over categories.
- Scatter Plots – For bubble charts showing relationships between customer count, repeat purchases, and total spend.

5. Geographic Analysis

- Heatmaps and bubble charts use to represent store location potential and customer behavior density.

## 🌍Review of Raw Data and Exploratory Data Analysis

- **Understanding the Raw Data**  
  The dataset contains 18 features:  
  *Unnamed:0* (int64), *Customer ID* (int64), *Age* (int64), *Gender* (object), *Item Purchased* (object), *Category* (object), *Purchase Amount (USD)* (int64), *Location* (object), *Color* (object), *Season* (object), *Review Rating* (float64), *Subscription Status* (object), *Shipping Type* (object), *Discount Applied* (object), *Promo Code Used* (object), *Previous Purchases* (int64), *Payment Method* (object), and *Frequency of Purchases* (object).  
  This mix of numerical and categorical data provides insights into customer demographics, purchasing behavior, and preferences.

- **Understanding the Features**  
  Features capture customer details (e.g., Age, Gender, Location), purchase specifics (e.g., Item Purchased, Category, Purchase Amount), and engagement metrics (e.g., Subscription Status, Previous Purchases). Categorical features like Color, Season, and Shipping Type allow segmentation, while numerical features like Review Rating and Purchase Amount enable quantitative analysis of trends and correlations.

- **Correlation between Features**  
  Purchase Amount (USD) shows weak correlations with Age and Review Rating, suggesting no strong linear relationship. Subscription Status and Promo Code Used are highly correlated, indicating subscribers frequently use discounts, which could influence spending patterns.


### 🌟Conclusion of reviewing the raw data and EDA:

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

### 🧩Assumptions, Limiting Conditions, Data Risks:

The dataset assumes representative sampling of customer purchases but may contain biases due to uneven gender distribution or sparse location data, potentially skewing demographic insights. To address sampling bias, compare dataset demographics (e.g., age, gender) to U.S. census data; sparse location data should be handled by grouping low-sample regions or imputing missing values cautiously to avoid distorting geographic trends. Data risks include potential inconsistencies in categorical entries (e.g., typos in Color or Item Purchased) and incomplete records, which could affect analysis reliability.

- Our inital dataset was not suitable for our business problem. This resulted in us sourcing another dataset from Kaggle.
- At the beginning, we believed we could assume who the target demographic of our brand is - our challenge was to perform our analysis agnostic of that assumption to see if our hypothesis aligns with our conclusion.
- We had concerns that the data may be biased: we did in fact identify a considerable class imbalance between the sexes of the respondents in our dataset which we balanced, and performed our analyses on this updated dataset.
- Some of our initial data analysis proved redundant as we learned more about the process. For instance, we initially thought we might need to create smaller samples to perform our analysis on, thinking our dataset might be too large and performance-demanding. However, that proved to not be necessary, and so we performed our analyses on the full dataset.

### 🧹Data Cleaning:

For data cleaning, we first performed validation on the dataset to check for missing data, nulls, or invalid data types. We also ran checks to check for typos in the string data, and renamed the column headers in our dataframe for more legibility.

The dataset exhibits a significant gender imbalance, with 2652 males and 1248 females, as observed in the EDA. The class_imbalance.ipynb script attempts to address this by oversampling the minority class (Female) to match the majority class (Male), creating a balanced dataset with equal gender representation.

### ✅Data Cleaning Conclusions:

All-in-all, our dataset was very clean, and no data needed to be dropped or imputed to correct for missing information.

We identified a class imbalance issue in our dataset, where the data was skewed heavily toward male values (2652 males vs. 1248 females). Concerned that this would potentially skewing insights into purchasing behavior, we balanced this by oversampling the female class, as implemented in the updated script, balances the dataset, improving model fairness and ensuring equitable representation in analyses.

---

## 🔍 Analytics

We conducted a multi-faceted analysis to uncover purchasing behavior trends across customer demographics, locations, and categories. Below is a summary of key findings and their strategic implications:

---

### 1. 📊 Age Group & Gender Insights

**(Average Purchase Amount by Age Group and Gender)**

* Customers in their **20s and 30s** represent the highest concentration, forming our **core demographic**.
* Average purchase value peaks in the **30s and 40s** age groups.
* **Female customers** consistently spend slightly more than males across most age groups.
* Spending drops significantly after age 60.

**Strategic takeaway:**

* Prioritize product design and loyalty programs for customers aged **20–39**.
* Target high-spending **female** audiences for premium marketing.

---

### 2. 🌍 Geographic Spending Patterns

**(Top 30 Locations – Average Spend by State and Gender)**

* States like **Alaska, North Dakota, Pennsylvania, Arkansas, and Michigan** show the highest average spending.
* Female customers in these states contribute significantly to purchase totals.

**Strategic takeaway:**

* Focus **premium product campaigns** in Alaska and Pennsylvania.
* Launch **female-centric promotions** in high-spend regions.

---

### 3. 🗂 Category Performance

**(Purchase Amount by Category)**

* A pie chart analysis revealed **Clothing** as the top revenue-generating category.
* This category should be a **stocking priority** and central to future campaigns.
* Product category performance also varies by location, aiding localized inventory planning.

---

### 4. 📌 Top Performing Locations

**(Total Purchase Amount & Number of Previous Purchases)**

We visualized the **Top 10 Locations** using two key metrics:

#### ➤ Graph 1: Total Purchase Amount by Location

* Highlights the **highest-grossing regions**.

#### ➤ Graph 2: Number of Previous Purchases by Location

* Measures **customer loyalty and engagement**.

**Why Top 10?**

* ✅ **Clarity**: Avoids clutter from visualizing all regions.
* ✅ **Efficiency**: Speeds up stakeholder decision-making.
* ✅ **ROI Focus**: Concentrates on regions with strongest returns.

**Strategic Value:**

* Guides **store placement** and **inventory prioritization**.
* Identifies **high-value and loyal customers** for targeted marketing.

---

### 5. 📦 Spending Behavior in Key States

**(Montana & Alabama Deep Dive)**

* **Montana**: Highest total purchase revenue.
* **Alabama**: Highest number of previous purchases and average spend per customer.
* Clothing was the top category in both states.

**Strategic takeaway:**

* **Montana** is a high-value market.
* **Alabama** indicates strong customer loyalty—ideal for retention programs.

---

### 6. 🧠 Customer Density vs. Repeat Purchases

**(Bubble Chart: Age-Gender-Location Analysis)**

A bubble chart combined three metrics: **customer count**, **repeat purchases**, and **total spend**.

Key insights:

* **Montana**: Top revenue and customer count, moderate loyalty.
* **Illinois**: Balanced across all metrics – strong expansion candidate.
* **California**: Large customer base but low loyalty – good testing ground for loyalty programs.

**Strategic takeaway:**

* Prioritize store placement in areas with **high density, loyalty, and spend**.
* Deploy targeted promotions in regions with high potential but low engagement.

---

## 📊 Results

We found that while **Montana** generated the most revenue overall, **Alabama** customers made more repeat purchases and had a higher average spend. In terms of product categories, **Clothing** significantly outperformed **Accessories**, **Footwear**, and **Outerwear** in total sales.

* In **Montana**, the top sellers were: socks, pants, and jeans.
* In **Alabama**, the most popular items included: pants, shirts, skirts, and jeans.

---

## 🧠 Final Conclusions

* The most attractive store locations combine:

  * A **large customer base**
  * **High loyalty** (repeat purchases)
  * **Strong total spending**

* These locations appear as **large, dark bubbles in the upper-right** quadrant of the scatter plot — ideal candidates for expansion.

### Key Insights:

* **Montana** leads in **total revenue** but has moderate repeat purchases.
* **Alabama** has **high loyalty** and **above-average spending per purchase**, suggesting strong customer relationships.
* **Illinois** shows a **well-balanced profile**, making it a solid candidate for store growth.
* **California** has the **largest customer base**, but lower loyalty — making it suitable for **targeted loyalty programs** before expansion.
* Locations with:

  * **High customers but low loyalty** = opportunity for **promotions or retention strategies**.
  * **High loyalty but fewer customers** = potential for **niche or digital-first store formats**.

### Location-Specific Observations:

* **Montana**: High volume + maxed-out revenue = strong expansion target.
* **Alabama**: Loyal, high-spending base = potential for deeper customer engagement.
* **California**: Volume-rich but loyalty-lagging = needs retention focus.

### Location Analysis Summary:

We identified:

* **Top 10 locations by Total Purchase Amount** → Where the most **revenue** comes from.
* **Top 10 locations by Number of Previous Purchases** → Where our most **frequent and engaged** customers are.

By comparing these two metrics, we gain insight into:

* Which locations offer **high value and frequency**,
* How to tailor **inventory**, **marketing**, and **customer loyalty** strategies.

These insights support **strategic decisions** around:

* Expansion opportunities,
* Targeted advertising,
* Inventory planning, and
* Loyalty program optimization across geographic areas.

### 🧭 Strategic Recommendations:

* 🏬 Focus expansion efforts on locations with high spending and moderate-to-high loyalty

* 💳 Launch retention programs in high-traffic but low-loyalty regions like California

* 📦 Align inventory and product mixes with region-specific preferences (e.g., socks in Montana)

* 📣 Use targeted advertising based on spending patterns and loyalty clusters

* 🔁 Prioritize repeat customer growth over one-time volume in saturated markets

### 📌 Bottom Line:

* Montana, Alabama, and Illinois represent the strongest candidates for store expansion.
* California and similar markets should be prioritized for loyalty-building campaigns before scaling physical presence.

---

## Team Reflections

**⏳Ayshe's Reflection**

- **What did I learn?**  
  In this project, I focused on analyzing customer behavior across age, gender, and location. I created visualizations such as bar charts and a bubble plot to highlight purchasing trends and identify strategic locations for potential store expansion based on customer count and repeat purchases. This work helped me strengthen my skills in Python-based data visualization and exploratory analysis. 

- **What challenges did I face? and How did I overcome those challenges?**  
  One of the challenges I encountered was a Git merge conflict while pushing changes to the shared repository. With help from a teammate and learning support, I gained a better understanding of version control and how to resolve collaboration issues in Git. 

- **If I had more time, what would I add?**  
  If I had more time, I would have incorporated advanced visualization techniques to map potential store openings geographically and provide a more location-intelligent analysis on the US map. 

- **What strength do I bring to a team?**  
  Overall, I bring analytical thinking, a willingness to learn, and a collaborative attitude to team environments. This project reinforced the importance of communication, clear versioning, and visual storytelling in delivering impactful data insights.


**📚Crystal's Reflection**

- **What did I learn?**  
  I learned how to clean and analyze real customer data to find useful information for business decisions. I also improved my skills using Python tools like pandas and matplotlib to create charts and explain results clearly.

- **What challenges did I face?**   
  The data was not perfect — some parts were missing and some groups had more data than others, making it hard to get accurate answers. Also, working with the team online sometimes made communication and sharing work a little tricky.

- **How did I overcome those challenges?**   
  We fixed the data problems by balancing the groups and carefully cleaning mistakes. For teamwork, we used Git and communicated often to ensure everyone’s work fit together well.

- **If I had more time, what would I add?**   
  I would add better maps and tools to explore the best store locations, and create an interactive dashboard so the team and stakeholders can easily explore the data.

- **What strength do I bring to a team?**  
  I am careful with details and like to make sure the data is correct. I also communicate clearly and work well with others to finish the project on time.

**💪Dianne's Reflection**

- **What did you learn?**  
  Through this project, I improved my understanding of Git, including version control, branching strategies, and resolving merge conflicts. I also learned approaches for task assignments and team coordination. Additionally, I developed a better ability to explore and analyze data.

- **What challenges did you face?** 
  One of the biggest challenges was navigating Git, particularly when dealing with merge conflicts and troubleshooting errors. Another challenge was bringing all the pieces of the project together. It required condensing and reconciling everyone’s contributions into a cohesive final report.

- **How did you overcome those challenges?**  
  We overcame these challenges through teamwork and communication. When issues came up, we collaborated to troubleshoot, shared knowledge, and supported each other. This collaborative approach made it possible to finalize the project efficiently and with a tight timeline despite some obstacles.

- **If you had more time, what would you add?** 
  With more time, I would focus on creating more polished and meaningful visualizations, trying to incorporate interactive elements. I would also dedicate more time to exploratory data analysis (EDA) to identify which features were most relevant, ensuring that the resulting insights were as impactful as possible.

- **What strengths did you bring to the team environment?**  
  I was available for all meetings as my schedule allowed it. Despite not having met in person, I tried to keep the work friendly and professional.


### Reproducibility

All project code, data, and documentation are publicly accessible in our GitHub repository. The README includes detailed instructions on data access, software dependencies, and environment setup to enable full reproduction of the analysis and results.

---

