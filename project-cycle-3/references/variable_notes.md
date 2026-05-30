# Variable Notes and Method Reference

## Project Cycle

Project Cycle 3 focuses on two-sample inference using the `YRBS_2007.csv` dataset.

## Main Research Question

Is the proportion of current alcohol use different between male and female students?

This research question compares two independent groups:

- Male students
- Female students

---

# Main Analysis: Gender and Current Alcohol Use

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

## Main Data Cleaning Rules

Only the two variables needed for the main research question were selected:

- `WhatIsYourSex`
- `CurrentAlcoholUse`

Rows with missing values in either variable were removed.

Only valid codes were kept:

- `WhatIsYourSex`: 1 or 2
- `CurrentAlcoholUse`: 1, 2, 3, 4, 5, 6, or 7

After cleaning and recoding, the final dataset included only:

- `sex_group`
- `current_alcohol_use`

## Main Statistical Method

Because the response variable is binary, this project compares two proportions.

The statistical method used is:

Two-proportion z-test

Welch's two-sample t-test was not used because Welch's t-test is used for comparing two means of a quantitative response variable. In this project, the response variable is binary, so the appropriate method is a two-proportion z-test.

## Main Parameter Definitions

Let p_m be the proportion of male students who currently used alcohol.

Let p_f be the proportion of female students who currently used alcohol.

The estimated difference is calculated as:

sample male proportion - sample female proportion

In this project, the estimated difference was calculated as:

Male proportion - Female proportion

## Main Hypotheses

Null hypothesis:

H0: p_m - p_f = 0

Alternative hypothesis:

HA: p_m - p_f ≠ 0

This is a two-sided test because the research question asks whether the proportions are different between male and female students.

## Main Confidence Interval

A 95% confidence interval was calculated for the difference in proportions:

p_m - p_f

The confidence interval helps estimate the range of plausible values for the true difference in current alcohol use proportions between male and female students.

## Main Assumptions

The response variable is binary because each student is classified as either currently using alcohol or not currently using alcohol.

The two groups are male and female students, and they are treated as independent groups.

The sample sizes are large enough for a two-proportion z-test because both groups have many observations and both success and failure counts are large.

The data come from an observational survey, so the result can show an association between sex and current alcohol use, but it cannot prove causation.

## Main Interpretation Rule

If the p-value is less than 0.05, we reject the null hypothesis and conclude that there is statistically significant evidence that the current alcohol use proportions are different between male and female students.

If the p-value is greater than or equal to 0.05, we fail to reject the null hypothesis and conclude that there is not enough statistical evidence that the current alcohol use proportions are different between male and female students.

---

# Extension Analysis: Other Risk Behaviors

## Extension Research Question

Is the proportion of current alcohol use different between students with other risk behaviors and students without other risk behaviors?

This extension compares two groups:

- Students with other risk behaviors
- Students without other risk behaviors

This is an exploratory extension using the same two-sample inference framework.

## Extension Variables Used

### Extension Response Variable

Original variable name:

`CurrentAlcoholUse`

This variable is used to measure whether a student currently used alcohol.

Recoding:

- Code 1 = did not currently use alcohol
- Codes 2 to 7 = currently used alcohol

Final recoded variable name:

`current_alcohol_use`

Final coding:

- 0 = did not currently use alcohol
- 1 = currently used alcohol

### Composite Group Variables

The composite group variable was created using two original variables:

- `CurrentCigaretteUse`
- `PhysicalFighting`

---

## Current Cigarette Use Recoding

Original variable name:

`CurrentCigaretteUse`

This variable is used to measure whether a student currently used cigarettes.

Recoding:

- Code 1 = did not currently use cigarettes
- Codes 2 to 7 = currently used cigarettes

Final recoded variable name:

`current_cigarette_use`

Final coding:

- 0 = did not currently use cigarettes
- 1 = currently used cigarettes

## Physical Fighting Recoding

Original variable name:

`PhysicalFighting`

This variable is used to measure whether a student had a physical fight.

Recoding:

- Code 1 = did not have a physical fight
- Codes 2 to 8 = had at least one physical fight

Final recoded variable name:

`physical_fighting`

Final coding:

- 0 = did not have a physical fight
- 1 = had at least one physical fight

## Composite Risk Behavior Group Definition

The final composite group variable was:

`risk_behavior_group`

The group was defined as:

- `Other risk behavior`: students who currently used cigarettes or had at least one physical fight
- `No other risk behavior`: students who did not currently use cigarettes and did not have a physical fight

In logical form:

Other risk behavior = current cigarette use = 1 OR physical fighting = 1

No other risk behavior = current cigarette use = 0 AND physical fighting = 0

## Extension Data Cleaning Rules

Only the variables needed for the extension analysis were selected:

- `CurrentAlcoholUse`
- `CurrentCigaretteUse`
- `PhysicalFighting`

Rows with missing values in any of these variables were removed.

Only valid codes were kept:

- `CurrentAlcoholUse`: codes 1 to 7
- `CurrentCigaretteUse`: codes 1 to 7
- `PhysicalFighting`: codes 1 to 8

After cleaning, the extension dataset included 12,075 observations.

## Extension Statistical Method

Because the response variable is binary, the extension compares two proportions.

The statistical method used is:

Two-proportion z-test

The difference in proportions was calculated as:

sample risk group proportion - sample no-risk group proportion

In this extension, the estimated difference was calculated as:

Other risk behavior group proportion - No other risk behavior group proportion

where:

- p_risk is the proportion of current alcohol use among students with other risk behaviors
- p_no_risk is the proportion of current alcohol use among students without other risk behaviors

Welch's two-sample t-test was not used because the response variable is binary, not quantitative.

## Extension Hypotheses

Null hypothesis:

H0: p_risk - p_no_risk = 0

Alternative hypothesis:

HA: p_risk - p_no_risk ≠ 0

This is a two-sided test because the extension asks whether the current alcohol use proportions are different between the two risk behavior groups.

## Extension Confidence Interval

A 95% confidence interval was calculated for the difference in proportions:

p_risk - p_no_risk

The confidence interval helps estimate the range of plausible values for the true difference in current alcohol use proportions between students with and without other risk behaviors.

## Extension Assumptions

The response variable is binary because each student is classified as either currently using alcohol or not currently using alcohol.

The two groups are students with other risk behaviors and students without other risk behaviors.

The sample sizes are large enough for a two-proportion z-test because both groups have many observations and both success and failure counts are large.

The composite risk behavior group is an exploratory definition created for this extension analysis.

The data come from an observational survey, so the result can show an association between other risk behaviors and current alcohol use, but it cannot prove causation.

## Extension Interpretation Rule

If the p-value is less than 0.05, we reject the null hypothesis and conclude that there is statistically significant evidence that the current alcohol use proportions are different between students with and without other risk behaviors.

If the p-value is greater than or equal to 0.05, we fail to reject the null hypothesis and conclude that there is not enough statistical evidence that the current alcohol use proportions are different between students with and without other risk behaviors.

## Important Interpretation Note

The main analysis compares current alcohol use between male and female students.

The extension analysis compares current alcohol use between students with and without other risk behaviors.

The extension does not prove that cigarette use or physical fighting causes alcohol use. It only shows whether current alcohol use is statistically associated with the composite risk behavior group in this sample.