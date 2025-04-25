# COURSE PROYECT Make business decisions based on data

## Resume

This project was developed as part of my Data Analytics training at TripleTen Bootcamp, focusing on data-driven decision-making in a simulated business environment. As an analyst for a large online store, I prioritized marketing hypotheses using the ICE/RICE frameworks to identify high-impact strategies, designed and analyzed an A/B test while evaluating key metrics like conversion rate and revenue per user, and delivered actionable insights to optimize marketing efforts and drive revenue growth.

## Analysis Objective

### Hypothesis Prioritization

- Apply the **ICE framework** to rank hypotheses by potential impact.
- Apply the **RICE framework** to refine prioritization by including user reach.
- Compare **ICE vs. RICE** results and explain key differences.

### A/B Test Analysis

- Preprocess data to handle anomalies (e.g., users in both test groups).
- Visualize:
  - Cumulative revenue by group
  - Average order size by group
  - Conversion rates by group
- Analyze **statistical significance** (p-values) for conversion and order size differences.
- Identify and filter **outliers** using the 95th and 99th percentiles.

### Decision-Making

- Determine the winning A/B test group or conclude no significant difference.
- Provide **actionable recommendations** to optimize revenue.

## Data Sources

Three datasets were used, covering the period from **August 2019**:

- **Hypotheses**: brief descriptions of product improvement ideas, evaluated by Reach, Impact, Confidence, and Effort (on a scale from 1 to 10).
- **Orders**: information on purchases made, including transaction ID, user ID, revenue, and A/B test group.
- **Visits**: daily user session data by A/B test group, showing the number of site visits.



## Methodology & Analysis Approach

The project was developed in two parts:

###  Part 1: Hypothesis Prioritization

The file `hypotheses_us.csv` contains nine ideas aimed at increasing revenue for an online store, each evaluated using four criteria: Reach, Impact, Confidence, and Effort.

- The **ICE framework** (Impact × Confidence ÷ Effort) was applied to rank hypotheses by priority.
- The **RICE framework** (Reach × Impact × Confidence ÷ Effort) was also used to reprioritize them.
- A comparison was made between ICE and RICE results to highlight how prioritization changes when considering audience reach.

###  Part 2: A/B Test Analysis

Using data from `orders_us.csv` and `visits_us.csv`, an A/B test was analyzed to evaluate user behavior and conversion performance:

- Cumulative **revenue** and **average order value** were plotted and compared across groups.
- **Relative differences** between groups were visualized to identify trends and possible effects.
- **Conversion rates** were calculated per day using visit and order data, followed by a comparative analysis.
- Outlier detection was performed using **95th and 99th percentiles** for number of orders and order values.
- Statistical significance was tested (with and without outliers) for both:
  - **Conversion rates**
  - **Average order value**

Based on the analysis, a final decision was made on whether to stop the test, declare a winning group, or continue collecting data.

## Tools & Libraries

The analysis was conducted using **Python**, with the support of the following key libraries:

- **pandas**: for data loading, preprocessing, and manipulation.
- **datetime**: to handle and transform date and time data.
- **numpy**: for numerical operations and efficient array handling.
- **matplotlib.pyplot**: for data visualization and plotting.
- **scipy.stats**: for performing statistical tests and significance analysis.
