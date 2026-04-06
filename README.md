# UK Gilt Market Dynamics Through the Inflation Cycle 2016–2026

**Independent research project — Thomas Sumner, April 2026**

## Research Question

Did UK gilt markets systematically underprice the inflation surge of 2021–2022, and how did the Truss episode reveal the compounding effect of fiscal risk on a market already repricing monetary policy?

## Structure

| Notebook | Section |
|---|---|
| 01_data_collection | Data pulls — BoE, FRED, yfinance |
| 02_yield_curve | Yield curve construction, slope measures, carry and roll-down |
| 03_inflation_expectations | Breakeven inflation, real yield decomposition, transitory narrative |
| 04_international_comparison | UK vs US vs Germany, OLS regression, spread decomposition |
| 05_truss_case_study | Event study, LDI portfolio simulation, BoE intervention |
| 06_current_environment | Current snapshot, fiscal comparison, portfolio scenarios |
| 07_visualisations | Publication quality charts |

## Data Sources

- **Bank of England** Statistical Interactive Database — nominal and index-linked gilt yields
- **DMO** (Debt Management Office) — gilt issuance data
- **FRED** (Federal Reserve Bank of St. Louis) — US Treasury yields, TIPS, German Bund, macro variables
- **ONS** — UK CPI/RPI
- **yfinance** — ETF price series, GBPUSD

## Key Analytical Contributions

- Yield curve construction across 2yr, 5yr, 10yr, 30yr maturities from raw BoE data
- Nominal yield decomposition into real yield and inflation expectations components
- OLS regression decomposing the gilt-Treasury spread against macroeconomic drivers
- Event study of the September 2022 Truss mini-budget using z-score methodology
- Stylised LDI portfolio simulation illustrating the forced-selling doom loop
- Carry and roll-down analysis across different curve environments