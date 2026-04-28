# European Banking Risk Intelligence Platform

> A data-driven banking risk analytics project for comparing selected European banks using capital adequacy, macroeconomic pressure, asset quality, and profitability indicators.

---

## Overview

The **European Banking Risk Intelligence Platform** is a portfolio-oriented banking risk analytics project developed to compare the relative vulnerability of selected European banks.

The project integrates bank-level supervisory data from the **European Banking Authority (EBA)**, macroeconomic indicators from the **World Bank API**, and selected financial metrics from annual reports. These inputs are combined into a transparent multi-factor composite risk score covering capital adequacy, macroeconomic pressure, asset quality, and profitability.

The purpose of the project is not to produce a regulatory stress test or an official bank rating. Instead, it demonstrates how public supervisory and macroeconomic data can be transformed into a structured risk monitoring workflow using Python and Power BI.

---

## Research Question

**Can a transparent multi-factor scoring framework be used to compare relative vulnerability among selected European banks?**

The project answers this question by combining four dimensions:

- Capital adequacy
- Macroeconomic pressure
- Asset quality
- Profitability

This approach provides a broader view than a simple capital ratio comparison.

---

## Key Findings

Based on the current sample and scoring framework:

- **Highest risk scores:** Bank Polska Kasa Opieki and Nordea Bank Abp ranked highest within this project’s composite risk framework.
- **Stronger combined profiles:** OP Osuuskunta and Citadele banka showed stronger results across the selected capital, macroeconomic, and profitability indicators.
- **Capital positions:** Latvia and Sweden showed relatively stronger CET1 positions within the selected sample.
- **Macro pressure:** Baltic countries experienced elevated macroeconomic pressure during the 2022–2024 period, mainly due to inflation and unemployment dynamics.
- **Asset quality:** NPL proxy indicators, where available, helped refine the ranking beyond capital adequacy alone.

These findings should be interpreted as relative comparisons within this limited project sample, not as official supervisory conclusions.

---

## Sample

The project covers **10 banks** across **6 countries**.

| Country | Banks |
|---|---|
| Latvia | Citadele banka, ABLV Bank |
| Lithuania | Šiaulių bankas |
| Estonia | LHV Group |
| Poland | Bank Polska Kasa Opieki, mBank |
| Finland | OP Osuuskunta, Nordea Bank Abp |
| Sweden | Swedbank, Handelsbanken |

Time coverage:

- **Bank-level data:** mainly 2024–2025
- **Macroeconomic data:** 2020–2025

---

## Data Sources

### Bank-Level Data

| Source | Data Used |
|---|---|
| EBA EU-wide Transparency Exercise | CET1 ratios, risk-weighted assets |
| Annual reports | NPL proxy indicators, ROA |

### Macro-Level Data

| Source | Indicators |
|---|---|
| World Bank API | GDP growth, inflation, unemployment |

---

## Methodology

The project was developed through seven sequential stages:

```text
Stage 1  →  Macroeconomic data collection using World Bank API
Stage 2  →  Bank-year panel construction
Stage 3  →  CET1 data integration and change analysis
Stage 4  →  Country-level macro pressure score construction
Stage 5  →  NPL proxy identification and integration
Stage 6  →  ROA extraction from annual reports
Stage 7  →  Final composite risk scoring and bank ranking
