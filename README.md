# environmental-attitudes-regression
# Understanding College Students’ Pro-Environmental Behavior (Regression Reproduction + Extension)

**Project type:** Reproduction & extension of a published study (PLOS ONE, 2024)

## Overview
This project reproduces and extends the analysis from *“The impact of environmental education at Chinese universities on college students’ environmental attitudes”* (PLOS ONE, 2024). The study uses the **Theory of Planned Behavior (TPB)** to model how:
- **Subjective Norms (SN)**
- **Perceived Behavioral Control (PBC)**
- **School Curriculum Education (SCE)**  
predict **Environmental Attitudes (EA)**.

## Data
- Survey dataset: **398 respondents** and **34 variables**
- Constructs: EA, SN, PBC, SCE measured via 5-point Likert items  
- Demographics: gender, degree level, hometown, monthly living expenses

(See `docs/Questionnaire.docx` for the full item wording.)

## Methods
- Reliability: Cronbach’s alpha (overall scale α ≈ 0.918)
- EDA: descriptive stats + correlations
- Models:
  - Multiple Linear Regression: `EA ~ SN + PBC + SCE`
  - Extension: interaction terms (SN×PBC, SN×SCE, PBC×SCE)
  - Extension: Logistic Regression for high EA (EA ≥ 4)

## Key Results (Highlights)
### Linear Regression
All TPB predictors were statistically significant:
- SN (β ≈ 0.377, p < 0.001)
- SCE (β ≈ 0.347, p < 0.001)
- PBC (β ≈ 0.146, p ≈ 0.002)

Interpretation: **Subjective norms and curriculum education were the strongest predictors of EA**, with PBC smaller but still significant.

### Extension: Interaction Terms
Interaction terms were **not significant** (p > 0.55), suggesting **additive effects** rather than interactions.

### Extension: Logistic Regression (EA ≥ 4)
- SN increased odds of high EA by ~4×
- SCE increased odds of high EA by ~5×
- PBC was positive but marginal (p ≈ 0.076)

## Repository Guide
- `code/` contains the RMarkdown for cleaning and modeling
- `data/` contains cleaned data artifacts (if included)
- `report/En_project.pdf` contains the final presentation/report
- `paper/paper.pdf` contains the reference article

## How to Run
1. Open `code/data_cleaning.Rmd` and run to generate the cleaned dataset.
2. Open `code/Project_test.Rmd` and knit/run to reproduce models and outputs.



## Reference
Li, Y., Yang, D., & Liu, S. (2024). *The impact of environmental education at Chinese Universities on college students’ environmental attitudes.* PLOS ONE.
