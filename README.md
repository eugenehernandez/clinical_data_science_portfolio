# SDTM → ADaM: Clinical Data Transformation Walkthrough

**[View rendered vignette →](https://eugenehernandez.github.io/clinical_data_science_portfolio/sdtm_to_adam_vignette.html)**

An R Markdown vignette I built while working through the CDISC ADaM
Implementation Guide. The goal was to get hands-on with the derivation
conventions — BASE join-back, ADY no-day-zero rule, flag variable behavior —
before applying them to real study data.

## What it covers

Simulated two-arm RCT (Drug A 10 mg vs. Placebo, 12-week hypertension trial).
Starts from SDTM-structured source data (DM + VS domains), builds ADSL and
ADVS following BDS conventions, runs six structural QC checks, then produces
a Table 1, change-from-baseline figures, treatment difference table, and an
age-group subgroup plot.

Key derivations: AGEGR1/AGEGR1N, TRTSDT date conversion from ISO 8601,
SAFFL/ITTFL population flags, AVAL from VSSTRESN, BASE via join-back on
ABLFL, CHG/PCHG, ADY (no day zero), ANL01FL.

## Files

| File | Description |
|------|-------------|
| `sdtm_to_adam_vignette.Rmd` | Source — fully reproducible, no external data needed |
| `sdtm_to_adam_vignette.html` | Knitted output — readable without R installed |

## Running it

```r
install.packages(c("dplyr", "tidyr", "lubridate", "ggplot2",
                   "gtsummary", "kableExtra", "rmarkdown"))
```

Open the `.Rmd` in RStudio and click Knit, or:

```r
rmarkdown::render("sdtm_to_adam_vignette.Rmd")
```

## References

- CDISC ADaM Implementation Guide v1.3
- CDISC SDTM Implementation Guide v3.4
- FDA Study Data Technical Conformance Guide (2022)
