# Project Cycle 3: Two-Sample Inference

## Group Information

Group number: 23

Group members:
- 112310326 周朝賢
- 113370203 吳佳虹

## Research Question

Is the proportion of current alcohol use different between male and female students?

## Dataset

This project uses the `YRBS_2007.csv` dataset.

The original dataset is stored in:

`data/raw/YRBS_2007.csv`

The cleaned dataset is stored in:

`data/processed/cycle3_cleaned_alcohol_gender.csv`

## Variables

### Group Variable

Original variable:

`WhatIsYourSex`

Final recoded variable:

`sex_group`

Groups:

- Female
- Male

### Response Variable

Original variable:

`CurrentAlcoholUse`

Final recoded variable:

`current_alcohol_use`

Recoding rule:

- 0 = did not currently use alcohol
- 1 = currently used alcohol

For `CurrentAlcoholUse`, code 1 was recoded as 0, and codes 2 to 7 were recoded as 1.

## Statistical Method

Because the response variable is binary, this project compares two proportions.

The main statistical method used is:

Two-proportion z-test

Welch's two-sample t-test was not used because Welch's t-test is used for comparing two means of a quantitative response variable. In this project, the response variable is binary, so the appropriate method is a two-proportion z-test.

## Main Results

The estimated proportion of current alcohol use was:

- Female students: 0.4458
- Male students: 0.4577

The estimated difference in proportions was calculated as:

Male proportion - Female proportion

Result:

0.0119

This means that male students had about 1.19 percentage points higher current alcohol use than female students in this sample.

The 95% confidence interval for the difference was:

-0.0054 to 0.0292

The two-proportion z-test result was:

- z statistic: 1.3442
- p-value: 0.1789

## Conclusion

At the 0.05 significance level, we fail to reject the null hypothesis.

There is not enough statistical evidence to conclude that the proportion of current alcohol use is different between male and female students.

Because the data come from an observational survey, this result should be interpreted as an association, not as a causal relationship.

## Extra Analysis

An extra practical significance analysis was also included.

The observed difference in proportions was about 1.19 percentage points, and the relative risk was about 1.03.

This suggests that the observed difference between male and female students was small in practical size.

## Project Structure

```text
project-cycle-3/
  README.md

  data/
    raw/
      YRBS_2007.csv
    processed/
      cycle3_cleaned_alcohol_gender.csv

  notebooks/
    01_data_cleaning.ipynb
    02_descriptive_visuals.ipynb
    03_inference.ipynb
    04_extra_analysis.ipynb

  outputs/
    figures/
      bar_chart_alcohol_by_gender.png
      ci_plot_difference_alcohol_by_gender.png
      stacked_bar_alcohol_status_by_gender.png

    tables/
      summary_table_alcohol_by_gender.csv
      inference_table_alcohol_by_gender.csv
      effect_size_table_alcohol_by_gender.csv

    summary/
      final_summary.md

  report/
    cycle3_infographic_slide.pptx
    cycle3_infographic_slide.pdf

  references/
    variable_notes.md