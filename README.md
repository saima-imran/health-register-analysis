# health-register-analysis
Population-level health data analysis simulating Swedish national register data — Python
# Swedish Health Register Analysis — Python
**Author:** Saima Imran  
**Date:** April 2026  
**Language:** Python (pandas, numpy, matplotlib, seaborn)  
**Relevance:** Population-level health data analysis relevant to CRITICAL AI

---

## Project Overview

Swedish national health registers — such as the National Patient Register (NPR) and SmiNet — contain millions of patient records linking diagnoses, treatments, and outcomes across the entire population. Analysing these registers at scale requires computational methods for data wrangling, population stratification, temporal trend analysis, and outcome assessment.

This project simulates a Swedish health register dataset of 500 patient records and demonstrates a complete population-level analysis pipeline — from data creation and exploration through visualisation and summary reporting. The dataset structure mirrors real Swedish register data including ICD-10 diagnosis codes, Swedish regional identifiers, admission years, and patient outcomes.

---

## Dataset Description

| Variable | Description |
|----------|-------------|
| patient_id | Unique Swedish patient identifier (SE000001 format) |
| age | Patient age in years (18–89) |
| sex | Male / Female |
| region | Swedish region (Stockholm, Västra Götaland, Skåne, Uppsala, Östergötland) |
| diagnosis_code | ICD-10 code (J18, E11, I21, C34, J44, I10, F32, M54) |
| diagnosis_name | Full diagnosis name |
| admission_year | Year of hospital admission (2019–2023) |
| length_of_stay | Number of days in hospital |
| outcome | Patient outcome (Recovered, Ongoing treatment, Referred, Deceased) |
| age_group | Stratified age group (18-30, 31-50, 51-70, 71+) |

**Total records:** 500  
**Time period:** 2019–2023  
**Regions covered:** 5 Swedish regions

---

## ICD-10 Diagnoses Included

| Code | Diagnosis |
|------|-----------|
| J18 | Pneumonia |
| E11 | Type 2 Diabetes |
| I21 | Acute Myocardial Infarction |
| C34 | Lung Cancer |
| J44 | COPD |
| I10 | Hypertension |
| F32 | Depression |
| M54 | Back Pain |

---

## Methods

### Step 1 — Dataset Creation
A realistic simulated Swedish health register dataset was generated using numpy and pandas. ICD-10 codes, Swedish regional identifiers, and realistic outcome probabilities (65% recovered, 20% ongoing, 10% referred, 5% deceased) were used to create a representative dataset.

### Step 2 — Population-Level Visualisation
Four charts were produced:

**Chart 1 — Diagnosis Distribution by Swedish Region**
A grouped bar chart showing how different diagnoses are distributed across the five Swedish regions. Enables identification of regional health patterns and potential geographic disparities in disease burden.

**Chart 2 — Patient Distribution by Age Group**
A bar chart stratifying the 500 patients into four age groups (18-30, 31-50, 51-70, 71+). Shows that the 31-50 age group has the highest hospital admission rate in this dataset, while the youngest group (18-30) has the fewest admissions — consistent with typical hospital utilisation patterns.

**Chart 3 — Hospital Admissions 2019-2023**
A time series line chart tracking total hospital admissions per year from 2019 to 2023. Shows temporal trends in healthcare utilisation — in a real dataset this chart would reveal the impact of COVID-19 on hospital admissions.

**Chart 4 — Patient Outcomes Pie Chart**
A pie chart showing the distribution of patient outcomes: 64.4% Recovered, 18.8% Ongoing treatment, 10.4% Referred, 6.4% Deceased. These proportions are consistent with realistic mixed-diagnosis hospital cohort data.

### Step 3 — Summary Statistics Report
A structured population health report was generated including mean age, sex distribution, average length of hospital stay by diagnosis, and recovery rates stratified by age group.

---

## Key Findings

- **Total patients:** 500 (266 Female, 234 Male)
- **Age range:** 18–89 years | Mean age: 53.6 years
- **Longest hospital stay:** Lung Cancer (16.5 days) — clinically expected
- **Most common diagnosis:** Acute Myocardial Infarction (81 patients)
- **Most affected region:** Östergötland
- **Overall recovery rate:** 64.4%
- **Recovery rate lowest in 18-30 group (57.4%)** — potentially reflecting acute presentations in younger patients
- **Data ready for longitudinal register linkage**

---

## Relevance to Research

This project demonstrates core competencies required for health data science research in Sweden:

- **ICD-10 coding** — understanding and working with international disease classification
- **Swedish register data structure** — patient IDs, regional codes, longitudinal time series
- **Population stratification** — age groups, sex, region
- **Temporal trend analysis** — hospital admissions over time
- **Outcome analysis** — recovery rates by demographic subgroup
- **FAIR data principles** — reproducible, documented, publicly shareable methodology

These skills are directly relevant to the CRITICAL AI project at Umeå University (harmonising nationwide clinical microbiology data) and to precision medicine register-based research at Karolinska Institutet.

---

## Tools and Libraries

| Library | Purpose |
|---------|---------|
| pandas | Data creation, cleaning, groupby analysis |
| numpy | Random data generation, numerical operations |
| matplotlib | Chart creation — bar, line, pie charts |
| seaborn | Statistical visualisation styling |

---

## Files

- `health_register_analysis.ipynb` — main Jupyter notebook
- `health_register_analysis.png` — population health visualisation
- `README.md` — this file

---

## How to Run

```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook
# Open health_register_analysis.ipynb and run all cells
