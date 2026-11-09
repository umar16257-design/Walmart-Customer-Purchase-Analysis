# Walmart Customer Purchase Analysis – CLT & Confidence Intervals

## Project Overview

This project analyzes Walmart customer purchase data to understand customer spending behaviour and identify purchasing patterns across different demographic segments.

The primary focus is on applying statistical concepts, particularly the **Central Limit Theorem (CLT)** and **Confidence Intervals**, to estimate average customer spending and compare purchasing behaviour across gender, marital status, and age groups.

The analysis aims to translate statistical findings into actionable business recommendations that can help Walmart improve customer engagement, product positioning, and sales strategies.

## Business Objectives

- Understand customer purchasing behaviour across demographic segments.
- Identify customer groups contributing the most to purchase volume and revenue.
- Analyse spending patterns across gender, age, marital status, occupation, and city categories.
- Apply the Central Limit Theorem to understand the distribution of sample means.
- Calculate confidence intervals at 90%, 95%, and 99% confidence levels.
- Compare average customer spending across different demographic groups.
- Develop data-driven recommendations for improving business performance.

## Dataset Overview

The dataset contains **550,068 purchase records** and covers customer demographics, product categories, and purchase amounts.

Key attributes include:

| Column | Description |
|---|---|
| User_ID | Unique customer identifier |
| Product_ID | Product identifier |
| Gender | Customer gender |
| Age | Customer age group |
| Occupation | Customer occupation category |
| City_Category | City classification (A, B, C) |
| Stay_In_Current_City_Years | Years spent in the current city |
| Marital_Status | Customer marital status |
| Product_Category | Product category |
| Purchase | Purchase amount |

**Dataset observations:**
- 550,068 purchase records.
- 5,891 unique customers.
- 3,631 unique product IDs.
- 20 product categories.
- 21 occupation categories.
- 7 age groups.
- No missing values identified during initial data inspection.

## Tools & Technologies

- **Python**
- **Pandas & NumPy** – Data manipulation and numerical analysis
- **Matplotlib & Seaborn** – Data visualization
- **Jupyter Notebook** – Analysis and experimentation
- **Statistics** – Sampling, Central Limit Theorem, and Confidence Intervals

## Project Workflow

### 1. Data Loading & Inspection
- Imported the required Python libraries.
- Loaded the Walmart dataset.
- Examined dataset dimensions, data types, and statistical summaries.
- Checked for missing values and duplicate identifiers.
- Converted categorical attributes stored as integers into appropriate categorical data types.

### 2. Exploratory Data Analysis (EDA)

**Univariate Analysis**
- Examined customer demographics and purchase distributions.
- Analysed purchase frequency across gender, age, occupation, and city categories.
- Identified frequently purchased product categories.
- Used histograms and boxplots to understand purchase distributions and outliers.

**Bivariate Analysis**
- Compared purchase behaviour across gender and age groups.
- Examined spending patterns across marital status and city categories.
- Analysed customer spending across different product categories.

**Multivariate Analysis**
- Explored purchasing patterns across multiple demographic attributes.
- Compared male and female spending behaviour across age, city category, and marital status.
- Examined relationships between numerical variables.

### 3. Customer-Level Spending Analysis

Aggregated transaction-level purchase amounts by customer to calculate total spending per customer.

This enabled comparisons of customer-level spending across:
- Gender
- Marital status
- Age groups

### 4. Central Limit Theorem (CLT)

Applied the Central Limit Theorem by repeatedly drawing random samples with replacement and calculating their sample means.

The experiments included:
- Sample size of 1,000 and 1,500 for gender-based comparisons.
- Sample size of 1,000 for marital-status comparisons.
- Sample size of 200 for age-group comparisons.
- 1,000 sampling repetitions.

**Key observation:** The distributions of sample means appeared approximately normal, and the average of the sample means was close to the corresponding population mean.

### 5. Confidence Interval Analysis

Calculated confidence intervals at three confidence levels:

- 90% Confidence Interval
- 95% Confidence Interval
- 99% Confidence Interval

The analysis compared average customer spending across gender, marital status, and age groups.

It also examined how changing sample size and confidence level affects the interval width.

## Key Findings

### Customer Demographics & Purchasing Behaviour

- Customers aged **26–35 account for approximately 40% of purchase transactions**.
- Customers aged **18–45 contribute approximately 78% of purchase transactions**.
- Male customers account for approximately 75% of purchase transactions.
- Single customers contribute approximately 60% of purchase transactions.
- City Category B contributes approximately 42% of purchase transactions, despite representing around 29% of customers.
- Product Categories 1, 5, and 8 have the highest purchase frequency.
- Customers who have lived in their current city for one year contribute approximately 35% of purchase transactions.

### Spending Patterns

- Male customers contribute approximately 76% of the total purchase amount, while female customers contribute approximately 23%.
- Single customers contribute approximately 59% of total purchase value, compared with 41% from married customers.
- City Category C contributes approximately 32.65% of total purchase value.
- Purchase amounts are most frequently concentrated between 5,000 and 10,000.
- Product Category 10 contains relatively higher-value purchases.
- Purchase behaviour is broadly similar across demographic groups, although some differences in spending levels are observed.

### Central Limit Theorem

- Repeated sampling produced approximately normal distributions of sample means for gender and marital-status groups.
- The sample means were close to the corresponding population means.
- Similar behaviour was observed across the age groups analysed.

### Confidence Interval Findings

At a 99% confidence level with a sample size of 1,000, the estimated intervals for average customer-level spending were:

| Customer Segment | Lower Limit | Upper Limit |
|---|---:|---:|
| Male | 923,266.28 | 926,586.95 |
| Female | 710,554.95 | 713,331.90 |
| Married | 841,128.63 | 845,157.14 |
| Unmarried | 877,928.80 | 882,759.52 |

**Key observations:**
- The male and female confidence intervals do not overlap.
- Unmarried customers have a higher estimated average spending level than married customers.
- Increasing sample size generally reduces the width of confidence intervals.
- Increasing the confidence level from 90% to 99% increases the interval width.

## Business Recommendations

Based on the analysis, the following recommendations were identified:

1. **Customer Retention:** Focus on retaining high-value customers and strengthening engagement with customer segments contributing significantly to sales.
2. **Product Focus:** Prioritize Product Categories 1, 5, and 8, which have the highest purchase frequency.
3. **Customer Segmentation:** Develop targeted campaigns for customers aged 26–35, who contribute a substantial share of purchases.
4. **Female Customer Engagement:** Explore female-focused marketing initiatives and investigate product preferences to understand the difference in observed spending.
5. **City-Level Strategy:** Focus on City Category B's relatively high purchase activity and investigate the higher-value purchasing behaviour observed in City Category C.
6. **Product Portfolio Review:** Review the performance of lower-contributing categories such as 19, 20, and 13 before making assortment decisions.
7. **Customer Loyalty:** Consider targeted loyalty programmes and offers for high-value customers.
8. **Product Positioning:** Maintain the quality and availability of frequently purchased products.
9. **Pricing & Promotion:** Evaluate the demand for products in the 5,000–10,000 purchase range.

## Key Learnings

Through this project, I strengthened my understanding of:

- Exploratory Data Analysis and customer segmentation.
- Univariate, bivariate, and multivariate analysis.
- Sampling techniques and sampling distributions.
- Central Limit Theorem and its practical applications.
- Confidence Interval estimation at different confidence levels.
- The impact of sample size on confidence interval width.
- Applying statistical concepts to real-world business problems.
- Translating analytical findings into business recommendations.

## Repository Structure

```text
Walmart-Case-Study/
│
├── Walmart_Case_Study_Confidence_Interval_and_CLT.ipynb
├── walmart_data.csv
└── README.md
```

*Note: The dataset file should be included in the repository only if its distribution is permitted.*

## Conclusion

This project demonstrates how statistical techniques can be used alongside exploratory data analysis to understand customer purchasing behaviour.

By applying the Central Limit Theorem and Confidence Intervals, the analysis provides a structured way to estimate average customer spending and compare demographic segments.

The findings can help Walmart make more informed decisions around customer retention, product prioritization, and targeted marketing strategies.

---

## Author

**Umar Reyaz**

Data Analyst | Data Science & AI/ML Enthusiast

- **LinkedIn:** https://www.linkedin.com/in/umar-reyaz-55a164272
- **GitHub:** https://github.com/umar16257-design
- **Email:** umar16257@gmail.com
