# A/B Testing Analysis: Evaluating a New Website Landing Page
For a detailed explanation of the business problem, methodology, findings, and recommendations, please visit the project documentation:

🔗 [View Full Case Study](https://viridian-mulberry-00a.notion.site/A-B-Testing-Analysis-3a033087556280559091c23978548beb)
## Project Overview

This project analyzes the results of an A/B test conducted to determine whether a new landing page can improve user conversion rates compared to the existing page.

Users were randomly assigned to one of two groups:

* **Control Group**: Viewed the existing landing page (old_page)
* **Treatment Group**: Viewed the redesigned landing page (new_page)

The objective of this analysis is to determine whether the new page leads to a statistically significant improvement in conversions.

---

## Business Problem

The company introduced a new landing page with the expectation that it would increase user conversions.

Before deploying the new page to all users, an A/B test was conducted to answer the following question:
1. Should the new website version be implemented for all users?
2. Should the company retain the existing website version?
3. Should the experiment continue to collect more data if the current results are not statistically strong enough to support a confident decision?


---

## Dataset

The dataset contains user-level information from the experiment, including:

| Column    | Description                                           |
| --------- | ----------------------------------------------------- |
| id        | Unique identifier for each user                       |
| time      | Timestamp of user activity                            |
| con_treat | Experiment group (control or treatment)               |
| page      | Landing page version viewed by the user               |
| converted | Conversion outcome (1 = converted, 0 = not converted) |
| country   | User's country                                        |


---

## Data Cleaning

The following preprocessing steps were performed:

* Removed users assigned to an inconsistent page-group combination.
* Removed duplicate user records.
* Verified the integrity of the experiment groups.

---

## Methodology

The analysis was conducted using the following steps:

1. Data Cleaning and Validation
2. Exploratory Data Analysis (EDA)
3. Conversion Rate Comparison
4. Two-Proportion Z-Test
5. Confidence Interval Estimation
6. Effect Size Calculation (Cohen's h)
7. Statistical Power Analysis
8. Sample Size Estimation

### Hypotheses

Null Hypothesis (H₀):

> The conversion rate of the control group is equal to the conversion rate of the treatment group.

Alternative Hypothesis (H₁):

> The conversion rates of the two groups are different.

---

## Results

### Conversion Rate

| Group     | Conversion Rate |
| --------- | --------------: |
| Control   |          12.03% |
| Treatment |          11.88% |

The control group achieved a slightly higher conversion rate than the treatment group.

---

### Two-Proportion Z-Test

| Metric      | Value |
| ----------- | ----: |
| Z-statistic | 1.208 |
| P-value     | 0.227 |

Since the p-value is greater than 0.05, the null hypothesis cannot be rejected.

There is insufficient statistical evidence to conclude that the new landing page performs differently from the old landing page.

---

### Confidence Interval

The 95% confidence interval for the difference in conversion rates includes zero.

This suggests that the observed difference may be due to random variation rather than a true treatment effect.

---

### Effect Size

| Metric    |  Value |
| --------- | -----: |
| Cohen's h | 0.0045 |

The observed effect size is extremely small, indicating a negligible practical difference between the two page versions.

---

### Power Analysis

| Metric            |  Value |
| ----------------- | -----: |
| Statistical Power | 22.68% |
| Recommended Power |    80% |

The experiment achieved a relatively low statistical power, indicating a limited ability to detect such a small effect.

---

### Required Sample Size

| Metric                         |   Value |
| ------------------------------ | ------: |
| Required Sample Size per Group | 780,971 |

To reliably detect an effect of the observed magnitude with 80% statistical power, approximately 780,971 users would be required in each group.

---

## Key Findings

* The control group showed a slightly higher conversion rate than the treatment group.
* The observed difference was not statistically significant.
* The confidence interval included zero.
* The observed effect size was extremely small.
* The experiment achieved only 22.68% statistical power.
* Detecting such a small effect would require a substantially larger sample size.

---

## Conclusion

Based on the current results:

- There is insufficient evidence to recommend replacing the existing landing page with the new version.
- There is also insufficient evidence to conclude that the new page performs worse than the existing page.
- Since the experiment is underpowered, extending the experiment and collecting additional data may help provide stronger statistical evidence before making a final business decision.

At this stage, retaining the existing landing page while continuing the experiment would be the most appropriate data-driven approach.


