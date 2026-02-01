# Dataset Source Evaluation (2024–2026)

This document tracks all datasets considered for the Delhi COPD project,
along with their credibility, limitations, and intended usage.

The goal is to avoid blind data usage and ensure medical and analytical integrity.

---

## Category A: Health Outcome Data (COPD)

This category captures disease burden, hospitalizations, and mortality related
to COPD or chronic respiratory conditions in Delhi.

The intent is to understand trends and signals — not individual-level diagnosis.

---

## Category B: Environmental Exposure Data (Air Quality)

This category captures ambient air pollution indicators relevant to
long-term respiratory outcomes in Delhi.

The goal is to study exposure trends, not short-term forecasting.

### A1. National Health Profile (NHP) – India

- Publisher: Central Bureau of Health Intelligence (CBHI), Govt. of India
- Type: Aggregated morbidity & mortality statistics
- Coverage: Annual (latest editions extend into 2024+)
- Geography: State-level (Delhi included)

Why this matters:
- Official government reporting
- Medically curated
- Stable definitions over years

Limitations:
- Not Delhi-ward level
- COPD often grouped under respiratory diseases

Status: Credible, usable for trend validation

### A2. National Family Health Survey (NFHS)

- Publisher: Ministry of Health & Family Welfare
- Type: Population health survey
- Coverage: Periodic (NFHS-5, upcoming NFHS-6 signals)
- Geography: State-level, urban/rural splits

Why this matters:
- Strong methodology
- Widely cited in medical literature
- Useful for demographic context

Limitations:
- Not disease-specific for COPD
- Lag between survey rounds

Status: Supportive, not primary

### A3. Global Burden of Disease (GBD) – India Respiratory Data

- Publisher: IHME (Lancet-backed consortium)
- Type: Modeled disease burden estimates
- Coverage: Yearly estimates up to recent years
- Geography: State-level (India focus)

Why this matters:
- Peer-reviewed methodology
- Used in top journals
- COPD explicitly modeled

Limitations:
- Modeled, not raw clinical data
- Not Delhi city granular

Status: High credibility, analytical reference

### B1. Central Pollution Control Board (CPCB) – AQI & Pollutant Data

- Publisher: Central Pollution Control Board, Govt. of India
- Type: Ground-station air quality measurements
- Coverage: Daily (historical data available)
- Geography: City-level, multiple stations across Delhi

Key pollutants:
- PM2.5, PM10
- NO2, SO2, CO, O3

Why this matters:
- Primary official source for air quality in India
- Directly relevant to COPD literature
- Station-level granularity enables aggregation logic

Limitations:
- Missing values common
- Station coverage varies by year

Status: Primary exposure dataset

### B2. OpenAQ (Delhi Aggregated Air Quality)

- Publisher: OpenAQ (aggregated from CPCB and global sources)
- Type: Cleaned, standardized air quality data
- Coverage: Daily / hourly
- Geography: City-level with station metadata

Why this matters:
- Easier programmatic access
- Consistent schema across years
- Useful for reproducible pipelines

Limitations:
- Derived source (not original authority)
- Depends on upstream CPCB availability

Status: Secondary, engineering-friendly source

### B3. WHO Air Quality Database (Contextual Reference)

- Publisher: World Health Organization
- Type: Annual air pollution summaries
- Coverage: Multi-year
- Geography: City-level (Delhi included)

Why this matters:
- International benchmarking
- Public health framing

Limitations:
- Annual aggregation only
- Not suitable for temporal modeling

Status: Contextual validation only