# European Banking Risk Intelligence Platform

## Overview

The **European Banking Risk Intelligence Platform** is a data-driven analytical project designed to monitor banking sector risk across selected European countries. It combines bank-level supervisory disclosures, macroeconomic indicators, and selected annual report metrics in order to assess relative bank resilience and construct an initial multi-factor risk ranking.

This project was developed as a portfolio-oriented banking risk analytics case, with a focus on capital strength, macro-financial pressure, and selected asset-quality and profitability indicators.

---

## Project Objective

The core objective of the project is to:

- measure relative banking sector risk across selected European banks,
- identify important bank-specific and macro-financial drivers,
- compare banks and countries using a structured analytical framework,
- and build an initial upgraded composite banking risk score.

---

## Sample

The project covers **10 banks** across **6 countries**:

- Latvia
- Lithuania
- Estonia
- Poland
- Finland
- Sweden

The bank-level analytical layer is focused mainly on **2024–2025**, while the macroeconomic layer spans **2020–2025**.

---

## Data Sources

### Bank-level data
- **EBA EU-wide Transparency Exercise**
- Selected **annual reports**
- Manual identification of selected **NPL proxy** and **ROA** values

### Macro-level data
- **World Bank API**
  - GDP growth
  - inflation
  - unemployment

---

## Main Indicators

### Bank-level
- CET1 ratio
- CET1 change
- NPL proxy (selected banks)
- ROA (selected banks)

### Macro-level
- GDP growth
- inflation
- unemployment
- macro pressure score

---

## Methodology

The project was developed in the following stages:

1. Collection of macroeconomic data from the World Bank
2. Construction of a bank-year panel
3. Integration of CET1 data
4. CET1 comparison and 2024–2025 change analysis
5. Construction of a country-level macro pressure score
6. Manual NPL proxy integration for selected banks
7. ROA extraction from annual reports for selected banks
8. Final upgraded composite risk scoring and bank ranking

---

## Final Risk Framework

The final upgraded risk score combines:

- **CET1-based capital risk**
- **macro-financial pressure**
- **NPL proxy risk** where available
- **ROA-based profitability risk** where available

This makes the framework stronger than a simple capital ratio comparison and allows for a more balanced initial banking risk ranking.

---

## Key Findings

Some of the main findings from the current version include:

- **Bank Polska Kasa Opieki** and **Nordea Bank Abp** ranked as the most vulnerable institutions under the final upgraded framework.
- **OP Osuuskunta** and **Citadele banka** appeared as the most resilient institutions in the sample.
- CET1 analysis showed relatively stronger capital positions in **Latvia** and **Sweden**.
- The project demonstrates how capital, macro conditions, profitability, and asset-quality signals can be combined into an initial banking risk monitoring framework.

---

## Repository Structure

```text
European-Banking-Risk-Intelligence-Platform/
│
├─ README.md
├─ .gitignore
│
├─ data/
│  └─ processed/
│     ├─ final_analysis_dataset_with_roa.csv
│     ├─ final_upgraded_risk_score.csv
│     ├─ bank_risk_ranking_final.csv
│     ├─ cet1_change_analysis.csv
│     └─ macro_pressure_score_filled.csv
│
├─ outputs/
│  ├─ final_bank_risk_ranking_advanced.png
│  ├─ cet1_dumbbell_chart.png
│  ├─ risk_vs_cet1_scatter.png
│  ├─ macro_pressure_by_country.png
│  └─ cet1_bank_average.png
│
├─ scripts/
│  ├─ 01_macro_data_collection.py
│  ├─ 02_bank_panel_build.py
│  ├─ 03_cet1_analysis.py
│  ├─ 04_macro_pressure_score.py
│  ├─ 05_npl_proxy_build.py
│  ├─ 06_roa_integration.py
│  └─ 07_final_risk_scoring.py
│
└─ docs/
   └─ project_summary.md
