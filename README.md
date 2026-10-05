# Pneumonia Culture and Antimicrobial Resistance Study
**Epidemiological Analysis of 327 Pneumonia Patients — Livingstone University Teaching Hospital (LUTH), Zambia**

Built by Grace Eso — Medical Laboratory Scientist & Healthcare Data Analyst

---

## Overview

An end-to-end epidemiological analysis of bacterial culture and antimicrobial susceptibility data from 327 pneumonia patients at a university teaching hospital in Zambia. The study compares pathogen distribution and resistance patterns between Community-Acquired Pneumonia (CAP) and Hospital-Acquired Pneumonia (HAP), with full statistical analysis including chi-square tests, confidence intervals, and logistic regression.

This project was commissioned as a freelance statistical analysis engagement. The analysis pipeline, code, and visualisations are shared here as a portfolio demonstration of healthcare data science skills. The underlying patient dataset is not included.

---

## Key Findings

| Finding | Result |
|---|---|
| Total patients | 327 |
| No pathogen isolated | 58.4% (95% CI: 53.0–63.6) |
| Most common pathogen | *Klebsiella pneumoniae* (10.1%) |
| Highest resistance | Ampicillin (75.0%) |
| Lowest resistance | Imipenem (0.0%) and Meropenem (2.6%) |
| CAP vs HAP difference | χ² = 60.61, p < 0.001 (**statistically significant**) |

### Key Clinical Observations
- **Klebsiella pneumoniae** was significantly more prevalent in CAP (24 cases) than HAP (9 cases)
- **Pseudomonas aeruginosa** was predominantly hospital-acquired (12 HAP vs 2 CAP cases)
- **Carbapenems retained high susceptibility** — important for treatment guidance in resource-limited settings
- **Ampicillin, co-trimoxazole, and penicillin** showed high resistance rates — empirical use should be reconsidered
- No statistically significant association between pathogen distribution and sex (p = 0.496) or age group (p = 0.411)

### Methodological Decisions
- **Cefpodoxine excluded** from resistance charts — tested in only 1 patient (100% resistance from a single case is not statistically meaningful)
- **"No pathogen isolated"** reported separately — not included in pathogen distribution charts to avoid misrepresenting it as a bacterial species

---

## Analysis Pipeline

### Methods Used
- **Prevalence analysis** with 95% Wilson confidence intervals
- **Chi-square tests** for pathogen distribution across sex, age group, and pneumonia type
- **Logistic regression** attempted for HAP predictors — model did not converge due to insufficient variability in predictor variables; chi-square used as alternative and documented transparently
- **Antimicrobial susceptibility profiling** by organism and antibiotic class
- **CAP vs HAP resistance comparison**

### Tools and Technologies
- Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels)
- Power BI (interactive dashboard)
- Google Colab
- Excel (data cleaning and export)

---

## Repository Structure

```
pneumonia-culture-resistance-luth/
│
├── Clement_Antibiotics.ipynb     # Main analysis notebook (data loading cell uses placeholder)
├── dashboard/
│   └── Pneumonia_Dashboard.pdf   # Power BI dashboard export
│
└── README.md
```

**Note:** The underlying patient dataset is not included in this repository. The notebook demonstrates the full analytical pipeline — data cleaning, prevalence calculations, chi-square testing, logistic regression, and visualisation.

---

## Dashboard

An interactive Power BI dashboard was built to visualise all findings including:
- Patient demographics (age, sex, pneumonia type)
- Most common bacterial pathogens
- Antibiotic resistance rates
- CAP vs HAP pathogen comparison

**Dashboard link:** [View on OneDrive](https://1drv.ms/u/c/b02b818ce2a60f3c/IQBxMWou4QdATIiRf1NyYo9mATJvZt-Bh2zKdE18n-YeThI?e=9B4XpC)

---

## Clinical Relevance

This project demonstrates how routine microbiology laboratory data from African teaching hospitals can be transformed into actionable epidemiological insights using open-source tools — without expensive infrastructure.

Key implications:
- Empirical treatment with ampicillin, co-trimoxazole, or penicillin is not recommended based on current resistance rates
- Carbapenems should be preserved for confirmed resistant cases given their retained efficacy
- CAP and HAP require distinct empirical treatment approaches given significantly different pathogen profiles
- Systematic analysis of routinely generated laboratory data can support antimicrobial stewardship in resource-limited settings

---

## About

This analysis was independently conducted as a freelance statistical engagement, as part of a broader research interest in applying data science to clinical microbiology and infectious disease surveillance in African healthcare settings.

**Author:** Grace Eso | Medical Laboratory Scientist | Healthcare Data Analyst
**GitHub:** [github.com/Eso3011](https://github.com/Eso3011)
**Contact:** esograce96@gmail.com
