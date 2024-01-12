# Will a Customer Accept the Coupon? - Data Analysis Readme

## Context

Imagine driving through town, and a coupon is delivered to your cell phone for a restaurant, bar, or coffee house near your location. The goal of this project is to determine the factors influencing whether a driver accepts a coupon under various driving scenarios.

## Data Overview

The dataset is sourced from the UCI Machine Learning repository and gathered through an Amazon Mechanical Turk survey. It includes user attributes, contextual attributes, and coupon attributes. The target variable 'Y' indicates whether the driver accepted the coupon (Y=1) or not (Y=0).

## Deliverables

The final product is a brief report highlighting differences between drivers who accepted and those who didn't. The analysis involves utilizing visualization techniques, probability distributions, and Python programming.

## Key Problems Investigated

1. **Missing Data Handling:** Investigate and handle missing or problematic data.
2. **Acceptance Proportion:** Determine the proportion of total observations that accepted the coupon.
3. **Coupon Visualization:** Use a bar plot to visualize the distribution of coupon types.
4. **Temperature Histogram:** Visualize the distribution of the 'temperature' column using a histogram.
5. **Bar Coupons Analysis:** Analyze acceptance rates for bar-related coupons and explore factors influencing acceptance.

## Analysis Steps

1. **Data Preparation:**
    - Read in the `coupons.csv` file.
    - Investigate and handle missing data by dropping the 'car' column and replacing other missing values with 'unknown'.

2. **Coupon Acceptance Overview:**
    - Calculate the proportion of total observations that accepted the coupon.
    - Visualize coupon types using a bar plot.

3. **Temperature Analysis:**
    - Create a histogram to visualize the distribution of the 'temperature' column.

4. **Bar Coupons Analysis:**
    - Create a DataFrame containing only bar-related coupons.
    - Analyze the acceptance rate for bar coupons and compare rates for different scenarios:
        - Bar frequency (3 or fewer times vs. more than 3 times a month).
        - Age groups.
        - Presence of passengers and their characteristics.

## Hypotheses

- The 'Bar' column has a significant impact on the acceptance rate for bar-related coupons.
- A combination of factors (columns) may yield higher acceptance rates than individual columns alone.

## Conclusion of Bar Coupon Analysis

Based on the analysis, the 'Bar' column strongly influences the acceptance rate for bar-related coupons. Drivers who went to bars three or more times a month had a significantly higher approval rate than those who went less. Further investigation into multiple columns reveals potential combinations that result in higher acceptance rates, providing insights for targeting specific customer groups with coupon offers.

# Independent Investigation - Coffee House Coupon Analysis

## Objective
The primary objective of this Python code is to conduct a comprehensive analysis driver attributes contributing to accpetance of Coffee House coupons. By exploring various coupon groups, the aim is to discern patterns and factors influencing acceptance rates. The analysis involves data manipulation, approval rate calculations, and visualization to provide insight into drivers who are more likely to accept Coffe House Coupons.

## Code Overview

### 1. Analyzing Coupon Types
**Purpose:** Understand the distribution of various coupon types to identify the prevalence of Coffee House coupons in the dataset.

### 2. Coffee House Coupon DataFrame Creation
**Purpose:** Isolate data specific to Coffee House coupons for in-depth analysis.

### 3. Creating Approval Rates DataFrame
**Purpose:** Prepare a structured framework for recording approval rates associated with different columns values.

### 4. Loop for Approval Rate Calculation
**Purpose:** Systematically compute approval rates for all column values to identify influential factors.

### 5. Scatter Plot Visualization
**Purpose:** Visualize approval rates to gain insights into patterns and trends across different column values.

### 6. Box Plot Analysis
**Purpose:** Identify and visually represent columns with the highest approval rates to focus on key features.

### 7. Additional Queries and Population Analysis
**Purpose:** Explore specific queries and analyze their impact on approval rates to uncover actionable insights.

1. **Scatter Plot:** The scatter plot visualizes approval rates for different column values, providing an overview of influential factors.

2. **Box Plot:** The box plot highlights columns with the highest approval rates, aiding in the identification of key features.

3. **Population Analysis:** The analysis of specific queries, such as "time in ['10AM', '2PM'] and CoffeeHouse in ['4~8', '1~3','gt8'] and passanger in ['Friend(s)', 'Partner', 'Kid(s)']", reveals a high acceptance rate of 0.7893 with a population size of 636.

## Conclusion

This analysis demonstrates that leveraging combinations of values across multiple columns can lead to higher approval rates than analyzing individual columns in isolation. The findings suggest the potential development of an algorithm to identify optimal column/value queries for maximizing acceptance rates. The identified population with a high acceptance rate provides a valuable insight for targeted coupon offerings.

