# relative-age-effect-olympic-football
Reproducible Python analysis of the Relative Age Effect in men's and women's Olympic football (1996–2021).
# Relative Age Effect in Olympic Football

## Overview

This repository contains a reproducible data analysis project investigating the **Relative Age Effect (RAE) in Olympic football**.

The project examines football participation records from the Olympic Games between **1996 and 2021**, with particular attention to differences between male and female players and changes in the magnitude of the RAE across Olympic editions.

The analysis was developed in Python as part of a broader project combining sports science research with reproducible data science workflows.

## Research Questions

The project addresses the following questions:

1. Is the Relative Age Effect present among Olympic football players?
2. Does the magnitude and distribution of the RAE differ between male and female players?
3. Has the RAE changed across Olympic editions between 1996 and 2021?

## Dataset

The original dataset contained **3,918 participation records** from Olympic football tournaments.

A systematic data-audit and cleaning procedure was performed to identify missing or implausible birth dates, duplicated records, and structural inconsistencies.

After data validation:

- **3,914 records** were eligible for the RAE analysis;
- **2,365 records** were classified as male;
- **1,549 records** were classified as female.

The analytical unit is an **Olympic participation record**. Therefore, an athlete who participated in more than one Olympic edition may contribute more than one observation.

> Raw individual-level data are not publicly distributed in this repository. The repository focuses on the analytical workflow, reproducible code, aggregated results, and visualizations.

## Relative Age Effect

Birth dates were classified into four calendar-based quartiles:

- **Q1:** January–March
- **Q2:** April–June
- **Q3:** July–September
- **Q4:** October–December

Observed distributions were compared with a day-corrected theoretical distribution:

| Birth quartile | Expected proportion |
|---|---:|
| Q1 | 24.71% |
| Q2 | 24.91% |
| Q3 | 25.19% |
| Q4 | 25.19% |

The statistical workflow included:

- Chi-square goodness-of-fit tests;
- standardized residuals;
- Cohen's *w* as an effect-size measure;
- sex-stratified RAE analyses;
- chi-square test of independence for sex × birth quartile;
- Cramér's *V*;
- edition-specific RAE analyses;
- Spearman correlations between Olympic year and RAE magnitude.

## Main Findings

A statistically significant RAE was identified in the overall sample, although its magnitude was small.

The overall birth distribution showed greater representation in the first two quartiles and lower representation in Q4:

- Q1: **28.31%**
- Q2: **27.11%**
- Q3: **24.04%**
- Q4: **20.54%**

The overall goodness-of-fit analysis resulted in **χ²(3) = 63.724, p < .001, Cohen's w = .128**.

RAE patterns also differed between male and female participation records. The association between sex and birth-quarter distribution was statistically significant but weak (**χ²(3) = 11.273, p = .010, Cramér's V = .054**).

Temporal analyses suggested different trajectories between the male and female Olympic tournaments. Among male records, more recent Olympic editions tended to show greater RAE magnitude, whereas no statistically significant temporal association was identified among female records.

## Project Structure

```text
relative-age-effect-olympic-football/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── 01_data_audit_and_rae_analysis.ipynb
│
├── figures/
│
└── results/
```

## Analysis Workflow

The project follows a reproducible analytical workflow:

**Raw data → Data audit → Data cleaning → Variable construction → Exploratory analysis → Statistical analysis → Visualization → Interpretation**

Particular attention was given to maintaining a distinction between **data auditing**, **data cleaning**, and **statistical analysis**.

## Tools

The analysis was conducted primarily using:

- Python
- pandas
- NumPy
- SciPy
- Matplotlib
- Google Colab
- Git/GitHub

## Reproducibility

The main analytical notebook is available in the `notebooks/` directory and can be opened directly in Google Colab.

The notebook documents the analytical workflow from data validation to the final statistical analyses.

Individual-level raw data are intentionally excluded from the public repository. Consequently, full reproduction from the original data requires access to the source dataset.

## Research Context

This project combines **sports science**, **football research**, and **data science** to investigate selection patterns in elite international sport.

The analysis is also being developed as part of an academic study examining sex differences and historical changes in the Relative Age Effect in Olympic football.

## Author

**João Paulo Lopes da Silva**

Researcher and Professor  
Sports Science | Exercise Physiology | Data Analysis

## Project Status

🚧 **Ongoing research project**

Data auditing, cleaning, primary statistical analyses, and temporal analyses have been completed. Further documentation and manuscript development are in progress.
