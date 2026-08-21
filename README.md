# Clinical Data Science Portfolio

A collection of R projects built around clinical and public health data, created as part of a move toward pharmaceutical and CRO statistical programming. Each project emphasizes reproducible workflows that run from raw data to analysis-ready output, using R, the tidyverse, and modern reporting tools.

## Projects

### SDTM to ADaM Clinical Data Transformation

An R Markdown vignette built while working through the CDISC ADaM Implementation Guide. It simulates a two-arm hypertension trial (Drug A 10 mg versus Placebo, 12 weeks), starts from SDTM-structured source data (DM and VS domains), and builds ADSL and ADVS datasets following BDS conventions. It runs six structural QC checks and produces a Table 1, change-from-baseline figures, a treatment difference table, and an age-group subgroup plot.

Key derivations include AGEGR1 and AGEGR1N, TRTSDT date conversion from ISO 8601, SAFFL and ITTFL population flags, AVAL from VSSTRESN, BASE via join-back on ABLFL, CHG and PCHG, ADY with no day zero, and ANL01FL. The vignette is fully reproducible and needs no external data.

- [View the rendered vignette](https://eugenehernandez.github.io/clinical_data_science_portfolio/sdtm_to_adam/sdtm_to_adam_vignette.html)
- [SDTM to ADaM data dictionary](https://eugenehernandez.github.io/clinical_data_science_portfolio/sdtm_to_adam/SDTM_to_ADaM_data_dictionary.html)
- [SDTM-IG 3.4 domain reference guide](https://eugenehernandez.github.io/clinical_data_science_portfolio/sdtm_to_adam/SDTM_Domain_Reference_Guide.html)

The source and knitted output live in the `sdtm_to_adam/` folder.

### Diabetes Surveillance Indicators Cleaning

A Quarto project that reads the CDC U.S. Chronic Disease Indicators dataset, filters it to diabetes, cleans it, and produces four summary tables. The focus is a documented, reproducible pass from a messy public file of nearly 400,000 rows to analysis-ready tables, with janitor for the cleaning, gt for the tables, and renv pinning the exact package environment.

- [View the rendered report](https://eugenehernandez.github.io/clinical_data_science_portfolio/diabetes_cleaning/diabetes_cleaning.html)

The project lives in the `diabetes_cleaning/` folder, which has its own README.

## Tools

R 4.6.0, the tidyverse, janitor, gt, gtsummary, kableExtra, Quarto, R Markdown, and renv for environment reproducibility.

## Author

Eugene Hernandez

[github.com/eugenehernandez/](https://github.com/eugenehernandez/)
