# Project Cycle 3: Two-Sample Inference

## Group Information

Group number: 23

Group members:

- 112310326 周朝賢
- 113370203 吳佳虹

## Research Question

Current Alcohol Use by Sex Group and Other Risk Behavior Group

## Dataset

This project uses the `YRBS_2007.csv` dataset.

- Raw data: `data/raw/YRBS_2007.csv`
- Cleaned data: `data/processed/cycle3_cleaned_alcohol_gender.csv`
- Cleaned data: `data/processed/extension_cleaned_risk_behavior_alcohol.csv`

## Main Variables

### Group Variable

- Original variable: `WhatIsYourSex`
- Recoded variable: `sex_group`
- Groups: Female and Male

### Response Variable

- Original variable: `CurrentAlcoholUse`
- Recoded variable: `current_alcohol_use`

Recoding rule:

- 0 = did not currently use alcohol
- 1 = currently used alcohol

For `CurrentAlcoholUse`, code 1 was recoded as 0, and codes 2 to 7 were recoded as 1.

## Main Statistical Method

Because the response variable is binary, this project compares two proportions.

The main method used was a two-proportion z-test.

Welch's two-sample t-test was not used because this project compares two proportions, not two means.

## Main Results

The estimated proportion of current alcohol use was:

- Female students: 0.4458
- Male students: 0.4577

The estimated difference was calculated as:

Male proportion - Female proportion = 0.0119

This means that male students had about 1.19 percentage points higher current alcohol use than female students in this sample.

Two-proportion z-test results:

- 95% confidence interval: -0.0054 to 0.0292
- z statistic: 1.3442
- p-value: 0.1789

## Main Conclusion

At the 0.05 significance level, we fail to reject the null hypothesis.

There is not enough statistical evidence to conclude that the proportion of current alcohol use is different between male and female students.

The observed difference was also small in practical size.

Because the data come from an observational survey, the result should be interpreted as an association, not as a causal relationship.

---

# Extension Analysis: Other Risk Behaviors

## Extension Research Question

Is the proportion of current alcohol use different between students with other risk behaviors and students without other risk behaviors?

## Extension Group Definition

Other risk behavior was defined as either:

- current cigarette use, or
- physical fighting

The two groups were:

- Students with other risk behaviors
- Students without other risk behaviors

The response variable was still current alcohol use.

## Extension Method

The extension also used a two-proportion z-test because it compares two proportions.

## Extension Results

The estimated proportion of current alcohol use was:

- Students with other risk behaviors: 0.6625
- Students without other risk behaviors: 0.2825

The estimated difference was calculated as:

Other risk behavior group - No other risk behavior group = 0.3800

This means that students with other risk behaviors had about 38.00 percentage points higher current alcohol use than students without other risk behaviors.

Two-proportion z-test results:

- 95% confidence interval: 0.3633 to 0.3967
- z statistic: 41.5471
- p-value: less than 0.001

## Extension Conclusion

At the 0.05 significance level, we reject the null hypothesis for the extension analysis.

This suggests that current alcohol use is statistically associated with other risk behaviors in this sample.

Compared with the main analysis, the extension result showed a much larger difference. The gender difference in current alcohol use was small and not statistically significant, while the difference between students with and without other risk behaviors was large and statistically significant.

Because the data come from an observational survey, this extension result should also be interpreted as an association, not as a causal relationship.

---

# Project Structure

```text
project-cycle-3/
  README.md

  data/
    raw/
      YRBS_2007.csv
    processed/
      cycle3_cleaned_alcohol_gender.csv
      extension_cleaned_risk_behavior_alcohol.csv

  notebooks/
    01_data_cleaning.ipynb
    02_descriptive_visuals.ipynb
    03_inference.ipynb
    04_extension_risk_behavior_group.ipynb

  outputs/
    figures/
      bar_chart_alcohol_by_gender.png
      ci_plot_difference_alcohol_by_gender.png
      extension_bar_chart_risk_behavior_alcohol.png

    tables/
      summary_table_alcohol_by_gender.csv
      inference_table_alcohol_by_gender.csv
      extension_summary_table_risk_behavior_alcohol.csv
      extension_inference_table_risk_behavior_alcohol.csv

    summary/
      final_summary.md

  report/
    cycle3_infographic_slide.pdf

  references/
    variable_notes.md