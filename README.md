# European Banking Risk Intelligence Platform

## Overview

The **European Banking Risk Intelligence Platform** is a data-driven analytical project designed to monitor banking sector risk across selected European countries. It combines bank-level supervisory disclosures, macroeconomic indicators, and selected annual report metrics to assess relative bank resilience and construct an initial multi-factor risk ranking.

This project was developed as a portfolio-oriented banking risk analytics case, with a focus on capital strength, macro-financial pressure, asset quality, and profitability.

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

## How to Run

Clone the repository, install the required packages, and run the scripts in numerical order:

```bash
git clone https://github.com/elnurqurb4nov/European-Banking-Risk-Intelligence-Platform.git
cd European-Banking-Risk-Intelligence-Platform
pip install -r requirements.txt

python scripts/01_macro_data_collection.py
python scripts/02_bank_panel_build.py
python scripts/03_cet1_analysis.py
python scripts/04_macro_pressure_score.py
python scripts/05_npl_proxy_build.py
python scripts/06_roa_integration.py
python scripts/07_final_risk_scoring.py
