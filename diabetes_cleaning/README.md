# Diabetes Surveillance Indicators - Data Cleaning and Summary

## Overview

This project reads a messy public health dataset, cleans it, and produces summary tables using R and the tidyverse. It is the Phase 1 deliverable of a broader clinical data science portfolio (R_CDISC_Portfolio) built to demonstrate reproducible data workflows relevant to clinical and pharmaceutical programming.

The focus is the data preparation itself. Real public health data arrives with empty columns, redundant fields, and suppressed values, and this project shows a clean, documented pass from raw file to analysis-ready tables.

## Data source

The data comes from the CDC U.S. Chronic Disease Indicators, published on data.cdc.gov.

https://data.cdc.gov/Chronic-Disease-Indicators/U-S-Chronic-Disease-Indicators/hksd-2xuw

A fixed copy of the dataset is stored in the `data/` folder so the analysis reproduces the same results regardless of later revisions to the source. The original download URL is recorded in a comment inside the analysis document.

## Getting the data

The source CSV exceeds GitHub's file-size limit and is not stored here.
Download it from the link above into a `data/` folder in this project,
then render the analysis document.

## What the analysis does

- Reads the raw CDC Chronic Disease Indicators file (all topics)
- Filters to the diabetes topic
- Drops columns that are empty across all diabetes rows
- Converts column names to snake_case
- Keeps the CDC footnote fields so suppressed values can be explained
- Produces four summary tables
  - Age-adjusted diabetes prevalence by state
  - National prevalence trend over the available years
  - National prevalence by sex over time
  - Prevalence by demographic group (sex, race and ethnicity)

## Tools

Built with R 4.6.0, the tidyverse, janitor, gt, Quarto, and renv for environment reproducibility.

## Repository structure

```
.
├── diabetes_cleaning.qmd     the analysis document
├── renv.lock                 pinned package versions
├── README.md
└── *.Rproj                   RStudio project file
```

## Reproducing this analysis

1. Clone or download the repository
2. Open the project file in RStudio
3. Run `renv::restore()` to install the exact package versions used here
4. Render `diabetes_cleaning.qmd` to produce the report

## Future dataset ideas

Planned extensions move toward drug-level data on the GLP-1 and semaglutide theme, which is a harder wrangling challenge and a closer match to clinical programming work.

- Medicare Part D prescriber data for Ozempic and Wegovy prescribing patterns
- FDA FAERS adverse-event reports for semaglutide

## Author

Eugene Hernandez
github.com/eugenehernandez/
