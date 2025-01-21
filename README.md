# A/B Testing Analysis for a Dating App

## Project Overview

This project focuses on analyzing the results of an A/B test conducted to evaluate the effectiveness of a new matching algorithm in a dating app. The goal is to determine whether the new algorithm significantly improves match rates compared to the existing one.

---

## Tech Stack

- **Python**: For data processing and analysis.
- **Pandas**: To manipulate and preprocess the dataset.
- **Scipy**: For statistical testing (chi-squared and t-tests).
- **Matplotlib & Seaborn**: For data visualization and insights presentation.

---

## Logic and Solution Approach

### 1. Data Understanding
The dataset includes logs of user interactions, with each record representing a pair of users. The key columns are:
- `user_id_1`: ID of the first user in the pair.
- `user_id_2`: ID of the second user in the pair.
- `group`: Indicates whether the pair belongs to the control group (0) or test group (1).
- `is_match`: Binary indicator of whether the pair matched (1 for match, 0 for no match).

### 2. Exploratory Data Analysis (EDA)
- Verified dataset structure and identified key statistics, such as the number of records and match rate distribution across groups.
- Visualized match rates and trends using bar plots to compare groups.

### 3. Statistical Testing
- **Chi-squared Test**: Evaluated whether there is a dependency between the group and match outcome.
  - Null Hypothesis (Φ0): No dependency exists.
  - Result: Statistically significant dependency (p < 0.05).

- **T-test**: Compared the average number of matches per user between groups.
  - Null Hypothesis (μ0 = μ1): No difference in average matches.
  - Result: Statistically significant improvement in the test group (p < 0.05).

### 4. Insights and Recommendations
- Generated visualizations to illustrate differences in match rates and user engagement across groups.
- Summarized actionable insights based on statistical findings.

---

## Results

- **Match Rate Comparison**:
  - Control Group (Old Algorithm): ~33%
  - Test Group (New Algorithm): ~78%

- **Statistical Significance**:
  - Chi-squared test confirmed a significant dependency between the group and match outcome.
  - T-test indicated a substantial improvement in average matches per user in the test group.

### Recommendation
The new matching algorithm demonstrates a clear improvement in match rates and user engagement. It is recommended to deploy the new algorithm to all users to enhance the user experience and app performance.
