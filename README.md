# UK Gilt Market Dynamics Through 2016–2026

**Independent research project - Thomas Sumner, March - April 2026**

---

## Overview

This project analyses UK gilt market dynamics from 2016 to 2026 using daily data from the Bank of England, ONS, and FRED. It constructs the UK gilt yield curve, decomposes yields into real and inflation components, runs an OLS regression decomposing the gilt-Treasury spread against macroeconomic drivers, and conducts an event study of the September 2022 Truss mini-budget crisis.

---

## Key Findings

**1. Markets rejected the transitory narrative in July 2021 - five months before the BoE acted**

The 5yr breakeven inflation rate crossed a 3.5% threshold on a sustained basis in July 2021 - five months before the BoE's first rate hike. This threshold reflects the BoE's 2% CPI target plus the structural RPI basis (~100bps) and a modest inflation risk premium. Bank Rate was 0.05% and realised CPI was 3.22%. The gilt market had stopped believing inflation was transitory before the BoE acknowledged it

**2. The gilt sell-off had two analytically distinct phases**

The gilt sell-off of 2021–2022 had two analytically distinct phases with very different portfolio implications.

In 2021, nominal yields rose 85bps while real yields moved just 11bps - the entire move was driven by rising breakeven inflation. Index-linked gilts partially protected portfolios.

In 2022, real yields surged 284bps as the BoE hiking cycle delivered genuine monetary tightening. Both nominal and index-linked gilts fell simultaneously - no hiding place in duration at any maturity.

**3. Long duration destroyed value over the decade**

Annual total return decomposition across 2016–2025, using full DCF pricing on a constant maturity par bond:

| Maturity | Cumulative Return 2016–2025 |
|---|---|
| 2yr | +11.87% |
| 5yr | +7.52% |
| 10yr | +3.38% |
| 30yr | **−2.06%** |

The 2022 inflation shock completely reversed the conventional case for long duration outperformance - over a full decade, the 30yr gilt produced a negative cumulative return.

**4. OLS regression identifies a persistent UK fiscal risk premium**

The gilt-Treasury spread moves for two reasons: global factors affecting all sovereign bond markets, and UK-specific factors like fiscal credibility and sterling weakness. 

An OLS regression against four macroeconomic drivers - GBPUSD, UK-US inflation differential, VIX, and BoE-Fed rate differential - explains 56% of spread variation. The BoE-Fed rate differential dominates (t-stat 9.32), confirming monetary policy divergence as the primary systematic driver. The residuals isolate the UK-specific risk premium:

- Post-Brexit 2016–17: negative residuals - UK gilts a safe haven, yielding below fundamentals
- Truss Sep 2022: +76bps unexplained - fiscal credibility shock
- Mid-2023: +107bps peak - persistent fiscal risk premium larger than the Truss spike itself
- 2024–26: residuals remain positive - fiscal premium not fully unwound despite the BoE 
  cutting cycle, with the 30yr at 5.63% exceeding both the Truss peak and the October 
  2023 cycle high

The shift from negative residuals in 2016–17 to persistently positive residuals post-2022 quantifies how international investors' perception of UK sovereign risk changed - from safe haven to fiscally stressed market.

**5. September 2022: When the Gilt Market Broke**

The BoE intervention on 28 September 2022 produced a 112.8bp fall in the 30yr gilt yield in a single day - the largest single-day move in the dataset and 16.2 standard deviations from normal market behaviour. For context, a 5σ move has a probability of less than 0.00003% under normal market conditions. 

The mini-budget itself (23 September) produced moves of +5.1σ on the 2yr and +5.6σ on the 5yr - statistically impossible under normal conditions. The maturity pattern of z-scores reveals which force dominated each day: the short end led initially as markets priced emergency BoE tightening, then the long end dominated as the LDI doom loop drove forced gilt selling.The long end was driven by leveraged pension funds forced to sell gilts to meet variation margin calls - a liquidity crisis, not a solvency crisis, that required the BoE to act as buyer of last resort.

---

## Project Structure

| Notebook | Content |
|---|---|
| 01_data_collection | All data pulls — BoE, FRED, yfinance. Clean and save |
| 02_yield_curve | Yield curve construction, slope measures, total return decomposition |
| 03_inflation_expectations | Breakeven inflation, real yield decomposition, transitory narrative |
| 04_international_comparison | UK vs US vs Germany, OLS regression, spread decomposition |
| 05_truss_case_study | Event study, LDI portfolio simulation, BoE intervention |
| 06_current_environment | Current snapshot, fiscal comparison, portfolio scenario analysis |
| 07_visualisations | Publication quality charts |

**Folder structure:**
- `/data/raw` — source files, not committed to GitHub
- `/data/processed` — cleaned CSVs, not committed to GitHub
- `/outputs/charts` — all publication charts
- `/diary` — project diary entries

---

## Charts

**UK Gilt Yield Curve Evolution 2016–2026**
![Yield Curve](outputs/charts/p01_yield_curve_evolution.png)

**Annual Total Return Decomposition by Maturity**
![Total Return](outputs/charts/p02_annual_total_return.png)

**Breakeven Inflation vs Realised CPI**
![Inflation Expectations](outputs/charts/p03_inflation_expectations.png)

**Transitory Narrative Threshold Analysis**
![Transitory Threshold](outputs/charts/p04_transitory_threshold.png)

**International Comparison and OLS Regression Residuals**
![International](outputs/charts/p05_international_regression.png)

**Truss Mini-Budget Event Study**
![Truss](outputs/charts/p06_truss_event_study.png)

**Current Environment vs Historical Context**
![Current](outputs/charts/p07_current_environment.png)

---

## Data Sources

| Source | Data | Series |
|---|---|---|
| Bank of England | UK nominal gilt spot curve (2yr, 5yr, 10yr, 30yr) | BoE Statistical Interactive Database |
| Bank of England | UK real gilt spot curve (5yr, 10yr, 30yr) | BoE Statistical Interactive Database |
| Bank of England | UK inflation curve (5yr, 10yr, 30yr) | BoE Statistical Interactive Database |
| ONS | UK CPI — series D7BT | MM23 |
| FRED | US Treasury yields | DGS2, DGS5, DGS10, DGS30 |
| FRED | US TIPS real yields and breakevens | DFII5, DFII10, T10YIE |
| FRED | German Bund 10yr | IRLTLT01DEM156N |
| FRED | Policy rates — Fed Funds, ECB | FEDFUNDS, ECBDFR |
| FRED | Macro variables — VIX, GBPUSD | VIXCLS, DEXUSUK |

All data sourced via free public APIs and official government statistical releases. No Bloomberg or paid data terminal used.

---

## Methodology Notes

- **Spot curves over redemption yields** - BoE modelled zero coupon spot curves used throughout - coupon-independent and maturity-specific.
- **Total return decomposition** - full DCF pricing formula (not duration approximation), constant maturity par bond, semi-annual coupon convention. Captures convexity - material for large yield moves
- **Breakeven inflation** - derived from BoE nominal minus real spot curves. RPI basis (~100bps above CPI) means figures overstate CPI-equivalent expectations. No independent cross-check available - UK inflation swap data not freely accessible
- **OLS regression** - monthly frequency, levels specification. Stationarity not formally tested - results interpreted as descriptive. Low R² on yield-policy betas (0.03–0.07) confirms term premium dominates monetary policy in explaining gilt yield variation
- **Event study** - z-scores relative to Jan–Sep 2022 pre-event window. Assumes approximately normally distributed daily yield changes - fat tails in practice mean true rarity of extreme moves is even greater than z-scores imply
- **LDI simulation** - stylised illustrative example. Real LDI structures varied in leverage, instrument type, and margin mechanics. Purpose is to illustrate the liquidity crisis mechanics numerically

---