# Project Cycle 3: Gender and Current Alcohol Use

## Group Information

Group members:

- 112310326 周朝賢
- 113370203 吳佳虹

## Research Question

Is the proportion of current alcohol use different between male and female students?

## Dataset

This project uses the `YRBS_2007.csv` dataset.

## Variables

- Group variable: `WhatIsYourSex`
- Response variable: `CurrentAlcoholUse`
- Extension variable: `InWhatGradeAreYou`

## Data Cleaning and Recoding

For the main analysis, observations with missing or invalid values in `WhatIsYourSex` or `CurrentAlcoholUse` were removed.

`CurrentAlcoholUse` was recoded into a binary variable:

- `0 = no current alcohol use`
- `1 = current alcohol use`

Recoding rule:

- original code `1` = no current alcohol use
- original codes `2–7` = current alcohol use

For the grade-level extension, `InWhatGradeAreYou` was also cleaned and recoded:

- `1 = 9th grade`
- `2 = 10th grade`
- `3 = 11th grade`
- `4 = 12th grade`

Code `5` was excluded from the grade-level extension because it represents an other or ungraded category.

## Method

Because the response variable is binary, a two-proportion z-test was used to compare the current alcohol use proportions between male and female students.

The difference was defined as:

```text
Male proportion - Female proportion
```

Significance level:

```text
alpha = 0.05
```

## Main Results

| Group | Sample Size | Current Alcohol Users | Proportion |
|---|---:|---:|---:|
| Female | 6425 | 2864 | 44.58% |
| Male | 6234 | 2853 | 45.77% |

Main inference results:

- Difference in proportions, Male − Female: `0.0119`
- Difference in percentage points: `1.19 percentage points`
- 95% confidence interval: `-0.54% to 2.92%`
- z statistic: `1.3442`
- p-value: `0.1789`

## Main Conclusion

At `alpha = 0.05`, we fail to reject the null hypothesis.

There is not enough statistical evidence to conclude that the proportion of current alcohol use differs between male and female students.

Although the male sample proportion is slightly higher than the female sample proportion, the difference is small: only `1.19 percentage points`.

## Extension Analysis: Grade-Level Comparison

As an extension, we compared current alcohol use proportions between male and female students within each grade level. This was used as a descriptive extension, not as a new formal hypothesis test.

The purpose of this extension was to check whether the overall gender pattern was consistent across grade levels.

| Grade Level | Female % | Male % | Male − Female Difference |
|---|---:|---:|---:|
| 9th grade | 40.30% | 34.49% | -5.82 percentage points |
| 10th grade | 42.11% | 43.23% | +1.11 percentage points |
| 11th grade | 44.46% | 50.03% | +5.58 percentage points |
| 12th grade | 50.92% | 55.00% | +4.07 percentage points |

The extension shows that the gender pattern is not exactly the same across all grades. Female students had a higher current alcohol use proportion in 9th grade, while male students had higher proportions from 10th to 12th grade.

This adds context to the main z-test result. The main test shows that the overall gender difference is not statistically significant, while the extension suggests that the overall result may hide some grade-level variation.

## Figures and Outputs

Main outputs include:

- `outputs/tables/summary_table_alcohol_by_gender.csv`
- `outputs/tables/inference_table_alcohol_by_gender.csv`
- `outputs/tables/effect_size_table_alcohol_by_gender.csv`
- `outputs/tables/grade_level_alcohol_by_gender_summary.csv`
- `outputs/tables/grade_level_gender_difference.csv`
- `outputs/figures/bar_chart_alcohol_by_gender.png`
- `outputs/figures/grade_level_alcohol_by_gender.png`
- `outputs/figures/grade_level_gender_difference.png`
- `outputs/summary/final_interpretation.md`
- `outputs/summary/extension_grade_level_summary.md`

## Project Structure

```text
project-cycle-3/
├── README.md
├── data/
│   ├── raw/
│   │   └── YRBS_2007.csv
│   └── processed/
│       ├── cycle3_cleaned_main.csv
│       └── cycle3_cleaned_grade_extension.csv
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_main_analysis.ipynb
│   ├── 03_extension_grade_level.ipynb
│   └── 04_outputs_and_summary.ipynb
├── outputs/
│   ├── figures/
│   │   ├── bar_chart_alcohol_by_gender.png
│   │   ├── grade_level_alcohol_by_gender.png
│   │   └── grade_level_gender_difference.png
│   ├── tables/
│   │   ├── summary_table_alcohol_by_gender.csv
│   │   ├── inference_table_alcohol_by_gender.csv
│   │   ├── effect_size_table_alcohol_by_gender.csv
│   │   ├── grade_level_alcohol_by_gender_summary.csv
│   │   └── grade_level_gender_difference.csv
│   └── summary/
│       ├── final_interpretation.md
│       ├── extension_grade_level_summary.md
│       └── one_slide_text_draft.md
├── report/
    └──onepage_ppt.png
└── references/
    └── variable_notes.md
```

## Note

This project uses observational survey data. Therefore, the findings should be interpreted as association, not causation.
