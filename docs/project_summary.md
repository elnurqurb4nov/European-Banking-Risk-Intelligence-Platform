# Project Summary

## European Banking Risk Intelligence Platform

This project is a data-driven analytical platform designed to monitor banking sector risk across selected European countries. It integrates bank-level supervisory disclosures, macroeconomic indicators, and selected annual report metrics in order to compare banks, evaluate capital resilience, and construct an initial multi-factor risk ranking.

## Project Objective

The main objective of the project is to measure risk levels in the European banking sector, identify major bank-specific and macro-financial risk drivers, and provide a structured analytical framework for monitoring relative vulnerability across banks and countries.

## Sample

The project focuses on a selected sample of 10 banks across 6 European countries:

- Latvia
- Lithuania
- Estonia
- Poland
- Finland
- Sweden

The bank-level analytical focus is primarily concentrated on 2024–2025, while the macroeconomic layer covers 2020–2025.

## Data Sources

### Bank-level sources
- EBA EU-wide Transparency Exercise disclosures
- Selected annual reports for ROA extraction
- Manual proxy construction for selected asset-quality indicators

### Macro-level sources
- World Bank API

## Main Variables

### Bank-level indicators
- CET1 ratio
- CET1 change (2024 to 2025)
- NPL proxy for selected banks
- ROA for selected banks

### Macro indicators
- GDP growth
- Inflation
- Unemployment
- Macro pressure score

## Methodology

The project was built in several stages:

1. Macro data collection from the World Bank API
2. Construction of a bank-year panel structure
3. Integration of CET1 data
4. CET1 comparison and capital change analysis
5. Construction of a macro pressure score
6. Identification of NPL proxy values for selected banks
7. Extraction of ROA values from selected annual reports
8. Construction of a final upgraded risk score

## Risk Scoring Logic

The final upgraded risk score combines four dimensions:

- Capital strength
- Macro-financial pressure
- Asset-quality proxy where available
- Profitability weakness where available

Higher CET1 and higher ROA reduce risk, while higher macro pressure and higher NPL proxy increase risk.

## Key Findings

- Bank Polska Kasa Opieki and Nordea Bank Abp ranked as the most vulnerable institutions under the final upgraded framework.
- OP Osuuskunta and Citadele banka appeared as the most resilient institutions in the sample.
- Sweden and Latvia showed relatively stronger capital positions in the CET1-based analysis.
- The project moved beyond a simple capital ratio comparison by introducing macro stress and selective bank-specific profitability and asset-quality layers.

## Limitations

This is still a portfolio-oriented analytical project rather than a full institutional risk system.

Main limitations:
- NPL proxy was identified only for selected banks
- ROA was integrated only for selected banks
- The current version does not yet include a full profitability and liquidity layer for all banks
- Dashboard development is not fully integrated into the repository yet

## Suggested Next Steps

- Add more bank-level profitability variables
- Expand NPL coverage across the full sample
- Add liquidity indicators such as LCR
- Build a Power BI dashboard
- Extend the model toward a more complete banking risk monitoring platform

