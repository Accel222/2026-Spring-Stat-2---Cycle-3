# Variable Notes for Cycle 3

## Research Question

Is the proportion of current alcohol use different between male and female students?

## Main Variables

### Group Variable: `WhatIsYourSex`

Original coding used in this project:
- `1 = Female`
- `2 = Male`

Recoded variable:
- `sex_group = Female / Male`

### Response Variable: `CurrentAlcoholUse`

Original coding used in this project:
- `1 = no current alcohol use`
- `2–7 = current alcohol use`

Recoded variable:
- `current_alcohol_use = 0` means no current alcohol use
- `current_alcohol_use = 1` means current alcohol use

## Extension Variable: `InWhatGradeAreYou`

Used for descriptive grade-level comparison.

Coding used in the extension:
- `1 = 9th grade`
- `2 = 10th grade`
- `3 = 11th grade`
- `4 = 12th grade`

Code `5`, missing values, and invalid values are not used in the grade-level extension.

## Cleaned Output Files

- `data/processed/cycle3_cleaned_main.csv`
- `data/processed/cycle3_cleaned_grade_extension.csv`
