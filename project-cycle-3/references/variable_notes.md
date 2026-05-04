# Variable Notes and Method Reference

## Project Cycle

Project Cycle 3 focuses on two-sample inference using the `YRBS_2007.csv` dataset.

## Selected Research Question

Is the proportion of current alcohol use different between male and female students?

This research question compares two independent groups: male students and female students.

## Variables Used

### Group Variable

Original variable name:

`WhatIsYourSex`

This variable is used to define the two comparison groups.

Recoding:

- Code 1 = Female
- Code 2 = Male

Final recoded variable name:

`sex_group`

Final categories:

- Female
- Male

### Response Variable

Original variable name:

`CurrentAlcoholUse`

This variable is used to measure whether a student currently used alcohol.

According to the project instructions, the coding rule is:

- Code 1 = did not currently use alcohol
- Codes 2 to 7 = currently used alcohol

Final recoded variable name:

`current_alcohol_use`

Final coding:

- 0 = did not currently use alcohol
- 1 = currently used alcohol

## Data Cleaning Rules

Only the two variables needed for this research question were selected:

- `WhatIsYourSex`
- `CurrentAlcoholUse`

Rows with missing values in either variable were removed.

Only valid codes were kept:

- `WhatIsYourSex`: 1 or 2
- `CurrentAlcoholUse`: 1, 2, 3, 4, 5, 6, or 7

After cleaning and recoding, the final dataset included only:

- `sex_group`
- `current_alcohol_use`

## Statistical Method

Because the response variable is binary, this project compares two proportions.

The statistical method used is:

Two-proportion z-test

Welch's two-sample t-test was not used because Welch's t-test is used for comparing two means of a quantitative response variable. In this project, the response variable is binary, so the appropriate method is a two-proportion z-test.

## Parameter Definitions

Let \( p_m \) be the proportion of male students who currently used alcohol.

Let \( p_f \) be the proportion of female students who currently used alcohol.

The estimated difference is calculated as:

\[
\hat{p}_m - \hat{p}_f
\]

## Hypotheses

Null hypothesis:

\[
H_0: p_m - p_f = 0
\]

Alternative hypothesis:

\[
H_A: p_m - p_f \neq 0
\]

This is a two-sided test because the research question asks whether the proportions are different between male and female students.

## Confidence Interval

A 95% confidence interval was calculated for the difference in proportions:

\[
p_m - p_f
\]

The confidence interval helps estimate the range of plausible values for the true difference in current alcohol use proportions between male and female students.

## Assumptions

The response variable is binary because each student is classified as either currently using alcohol or not currently using alcohol.

The two groups are male and female students, and they are treated as independent groups.

The sample sizes are large enough for a two-proportion z-test because both groups have many observations and both success and failure counts are large.

The data come from an observational survey, so the result can show an association between sex and current alcohol use, but it cannot prove causation.

## Interpretation Rule

If the p-value is less than 0.05, we reject the null hypothesis and conclude that there is statistically significant evidence that the current alcohol use proportions are different between male and female students.

If the p-value is greater than or equal to 0.05, we fail to reject the null hypothesis and conclude that there is not enough statistical evidence that the current alcohol use proportions are different between male and female students.