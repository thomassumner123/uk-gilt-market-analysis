# UK Gilt Market Dynamics 2016–2026
## A Fixed Income Research Note

**Thomas Sumner** | Independent Research | April 2026

---

## Executive Summary

This note analyses UK gilt market dynamics across a decade of extraordinary volatility:
from the post-financial crisis low rate era through Brexit, COVID, the worst inflation
surge in forty years, and a mini-budget crisis that brought the gilt market to the brink
of systemic dysfunction.

The analysis draws on daily data from the Bank of England, ONS, and FRED across five
areas: yield curve construction and total return decomposition, inflation expectations
and real yield analysis, international comparison and regression analysis, the Truss
mini-budget case study, and current environment and scenario analysis.

Five findings stand out:

**Markets rejected the transitory inflation narrative in July 2021 - five months before
the BoE acted.** The 5yr breakeven inflation rate crossed a 3.5% threshold on a
sustained basis in July 2021, when Bank Rate was 0.05% and realised CPI was 2.02%.
The gilt market stopped believing inflation was transitory before the BoE acknowledged
it publicly.

**The gilt sell-off had two analytically distinct phases with different portfolio
implications.** In 2021, nominal yields rose 85bps while real yields moved just 11bps -
an inflation expectations story where index-linked gilts offered partial protection. In
2022, real yields surged 284bps as the hiking cycle delivered genuine monetary
tightening. Both nominal and index-linked gilts fell simultaneously - there was no hiding 
place in duration at any maturity.

**Long duration destroyed value over the decade.** Annual total return decomposition
using full DCF pricing shows the 30yr gilt produced a cumulative return of −2.06% over
2016–2025, against +11.87% for the 2yr. The 2022 inflation shock completely reversed
the conventional case for long duration outperformance over long holding periods.

**An OLS regression identifies a persistent UK fiscal risk premium.** Decomposing the
gilt-Treasury spread against four macroeconomic drivers - GBPUSD, UK-US inflation
differential, VIX, and the BoE-Fed rate differential - explains 56% of spread variation.
The residuals isolate what macro factors cannot explain: a shift from negative residuals
post-Brexit (UK gilts a safe haven, yielding below fundamentals) to a persistent positive
risk premium of 60–107bps post-2022 that remains only partially unwound today.

**The Truss mini-budget of September 2022 produced the most extreme gilt market
moves in the dataset.** The mini-budget day (23 September) saw the short end reprice
by more than five standard deviations from normal daily moves - consistent with
markets immediately pricing emergency BoE tightening in response to the fiscal
loosening. The BoE intervention on 28 September produced a 112.8bp fall in the 30yr
gilt yield in a single day - the largest single-day move in the dataset and more than
three times larger than the next most extreme event. The pattern of moves across maturities
tells the story: the short end led on the way up as markets priced emergency tightening, then the 
long end dominated as leveraged pension funds were forced to sell gilts to meet cash margin calls.
The result was a liquidity crisis requiring central bank intervention to break.

---

*Data: Bank of England Statistical Interactive Database, ONS, Federal Reserve (FRED).
Full methodology and code available in the project notebooks.*

*[View project on GitHub](https://github.com/thomassumner123/uk-gilt-market-analysis)*

---

## 1. Yield Curve Dynamics and Total Returns

The UK gilt yield curve entered 2016 in the final stages of post-financial crisis
repression - the 10yr yielding 1.96%, the 30yr at 2.74%, and real yields deeply
negative across all maturities. Over the following decade the curve would experience
Brexit, a global pandemic, the sharpest inflation surge in forty years, and a
near-systemic fiscal crisis. By March 2026 the 30yr gilt yielded 5.63% - the highest
level in the full dataset and a world away from the suppressed yields of the low rate era.

### From Suppression to Steepening - The Curve's Journey

The curve spent 2016–2021 in a broadly flat, low-yield configuration. Brexit in June
2016 produced a brief safe-haven rally - yields fell sharply on the day as investors
sought the relative security of UK government debt - before gradually recovering.
COVID in March 2020 produced the opposite dynamic: an initial flight to safety driving
yields to historic lows, followed by the BoE's emergency asset purchase programme
anchoring yields at near-zero levels through 2020 and into 2021.

The 2yr gilt yield fell below zero in 2020 - negative nominal yields on short-dated
government debt, a phenomenon that would have been unthinkable in any prior decade.
The 30yr remained positive but compressed to around 0.7% at its trough. In yield
curve terms the curve was unusually flat, reflecting both the BoE's forward guidance
and the market's belief that rates would remain low for an extended period.

![Yield Curve](https://raw.githubusercontent.com/thomassumner123/uk-gilt-market-analysis/main/outputs/charts/p01_yield_curve_evolution.png)
*Chart 1: UK gilt yield curve evolution 2016–2026 (Panel A) and curve slope measures
(Panel B). Events A–E mark: Brexit vote (Jun 2016), COVID lockdown (Mar 2020),
BoE first hike (Dec 2021), Truss mini-budget (Sep 2022), BoE cuts begin (Aug 2024).*

The inflection came in 2021. As inflation rose through the spring and summer, all four
maturities began moving higher - but at different speeds and for different reasons, as
discussed in Section 2. The hiking cycle that began in December 2021 accelerated the
move. By September 2022 the 2yr had risen from near-zero to 3.52% and the 30yr from
0.7% to 3.72% - before the Truss mini-budget drove a further violent repricement.

The curve slope - measured here as both the 2/10 spread and the 5/30 spread -
tells an equally important story. The curve inverted in 2022 as markets priced
aggressive near-term BoE tightening while capping long-end yields on growth concerns.
The 2/10 spread reached −1.0% at its most inverted point in late 2022 - a level not
seen in decades. By 2026 the curve had re-steepened sharply to +0.66% on the 2/10
spread, but driven by the long end rising not the short end falling - a bear steepening
during a cutting cycle, which is analytically unusual and directly reflects the fiscal risk
premium identified in Section 3.

### Duration Risk - What the Returns Actually Show

Yield levels tell you what the market was pricing. Total returns tell you what investors
actually experienced. The two are not the same - a bond with a rising yield loses price
value even as it pays coupons, and the interaction between price return, coupon income,
and roll-down produces total returns that often differ substantially from what yield
moves alone would suggest.

Total returns were decomposed using full DCF pricing on a constant maturity par bond
with semi-annual coupon convention - the standard for UK gilts. This approach captures
convexity correctly, which matters significantly for large yield moves. A duration
approximation would materially understate the price losses on long-dated gilts in 2022.

![Total Return](https://raw.githubusercontent.com/thomassumner123/uk-gilt-market-analysis/main/outputs/charts/p02_annual_total_return.png)
*Chart 2: Annual total return decomposition by maturity 2016–2025. Bars show coupon
income (green), roll-down (orange), and price return (blue/red). Line shows total return.
Cumulative returns shown in each panel title.*

The results are striking. Across the full 2016–2025 period:

| Maturity | Cumulative Return |
|---|---|
| 2yr | +11.87% |
| 5yr | +7.52% |
| 10yr | +3.38% |
| 30yr | −2.06% |

The conventional case for long duration - that holding longer-maturity bonds produces
higher returns over time through the term premium - was completely overturned by the
inflation cycle. The 30yr gilt produced a negative cumulative return over a full decade.
The 2yr outperformed by nearly 14 percentage points.

2022 was the critical year. The 30yr produced a total return of −44.7% in a single
calendar year - a loss of nearly half the bond's value in twelve months. The 10yr
returned −19.0%. Even the 2yr, with its much lower duration, returned −2.1%. There
was no hiding place in gilts of any maturity during 2022, though the shorter end
offered dramatically better protection.

The decomposition reveals an important nuance. In most years, coupon income provides
a steady positive contribution - the drag comes entirely from price return when yields
rise. In 2022, the price return component was so large and negative that it overwhelmed
not just the coupon income but the entire cumulative gains of prior years for long
maturities. This is the core lesson of the decade for fixed income portfolio management:
duration is not a free lunch. In an inflationary environment with rising real yields,
long duration destroys value - and does so faster than most portfolio managers had
modelled.

The roll-down component - the return earned as a bond approaches maturity and
rolls down a positively sloped yield curve - was broadly positive in the 2016–2021
period when the curve was upward sloping. It turned negative during the inversion of
2022–2023. This reinforces the case for shorter duration positioning during inversion
episodes, not just on price return grounds but on roll-down grounds too.

---

## 2. Inflation Expectations and the Transitory Narrative

The central analytical question of the inflation cycle was not whether inflation would
rise - it was whether it would stick. The transitory narrative, embraced by central banks
on both sides of the Atlantic through 2021, held that the post-COVID inflation surge
reflected temporary supply chain disruptions that would self-correct without sustained
monetary tightening. The gilt market's verdict on this narrative, and when exactly it
delivered that verdict, is the most important analytical finding in this project.

### Reading Inflation Expectations from the Gilt Market

Breakeven inflation rates - derived from the BoE's nominal and real spot curves -
provide a market-based measure of inflation expectations. Two caveats apply
throughout: UK index-linked gilts are indexed to RPI rather than CPI, meaning
breakevens overstate CPI-equivalent expectations by approximately 100bps; and
breakevens embed an inflation risk premium alongside pure expectations. With these
in mind, the 5yr breakeven is the most policy-relevant measure for assessing whether
the gilt market believed the transitory narrative.

### When Did the Market Stop Believing?

A threshold of 3.5% was used to identify a sustained breach of anchored inflation
expectations. This reflects the BoE's 2% CPI target plus the structural RPI basis of
approximately 100bps and a modest inflation risk premium. Levels below this are
consistent with anchored expectations given the measurement issues noted above.

![Transitory Threshold](https://raw.githubusercontent.com/thomassumner123/uk-gilt-market-analysis/main/outputs/charts/p04_transitory_threshold.png)
*Chart 3: UK 5yr breakeven inflation rate against the 3.5% transitory narrative threshold.
The sustained breach in July 2021 is marked - five months before the BoE's first rate hike.*

The 5yr breakeven crossed 3.5% on a sustained basis in July 2021. At that point Bank
Rate was 0.05%, realised CPI was 2.02%, and the BoE's August 2021 Monetary Policy
Report still described inflation as transitory. The first rate hike would not come until
December 2021, five months later. The gilt market had stopped believing the transitory
narrative before the BoE acknowledged it.

This is not a criticism of the BoE's analytical framework. Central banks deliberately
avoid reacting to potentially temporary price level shocks, and the August 2021 MPC
minutes reflect a genuine analytical debate about inflation persistence. But it is an
important empirical finding: market-implied inflation expectations were signalling
sustained above-target inflation at a point when the official narrative remained
transitory.

A sensitivity analysis confirms the robustness of the July 2021 finding. All thresholds
between 3.5% and 4.0% identify the sustained breach in H2 2021. Thresholds below
3.5% capture the structural RPI premium rather than genuine de-anchoring. The July
2021 date is stable across reasonable threshold assumptions.

### The Real Yield Decomposition - Two Phases

Breakeven inflation captures inflation expectations. Real yields capture the degree of
monetary tightening. Decomposing nominal yields into these two components reveals
something the headline yield move obscures: the 2021–2022 gilt sell-off was not one
event but two analytically distinct episodes with different drivers and very different
portfolio implications.

![Inflation Expectations](https://raw.githubusercontent.com/thomassumner123/uk-gilt-market-analysis/main/outputs/charts/p03_inflation_expectations.png)
*Chart 4: Panel A shows breakeven inflation rates and realised CPI 2016–2026. Panel B
shows the nominal yield decomposed into real yield and breakeven components.
The extended period of negative real yields is shaded.*

**Phase 1 - 2021: An inflation expectations story**

In 2021 the UK 10yr nominal yield rose approximately 85bps. Over the same period the
10yr real yield moved just 11bps. The overwhelming majority of the move was driven
by rising breakeven inflation, with markets pricing higher future inflation rather than 
higher future real rates.

Index-linked gilts offered substantial protection during 2021 as a result. As nominal
yields rose on inflation expectations, real yields remained stable, meaning index-linked
gilt prices held up while conventional gilt prices fell. Investors who recognised the
inflation expectations nature of the 2021 move and rotated into index-linked gilts
would have been materially better positioned going into 2022.

**Phase 2 - 2022: A real yield story**

The character of the sell-off changed dramatically in 2022. Real yields surged
approximately 284bps as the BoE's hiking cycle moved from 0.25% in December 2021
to 3.5% by year-end. This was no longer about inflation expectations but genuine
monetary tightening delivering higher real interest rates across the economy.

The portfolio implication reversed equally dramatically. Index-linked gilts, which had
offered protection in 2021, provided no shelter in 2022. Rising real yields reduce the
present value of inflation-linked cash flows just as rising nominal yields reduce the
value of conventional gilt cash flows. Both instruments fell simultaneously. There was
no hiding place in duration of any kind.

This two-phase character is analytically important and practically under-appreciated.
Commentary on the 2021–2022 gilt sell-off frequently treats it as a single episode. The
real yield decomposition shows it was two distinct repricing events requiring different
portfolio responses. This distinction mattered significantly for realised returns.

### Incomplete Re-anchoring - Where Are We Now?

By March 2026 the 10yr breakeven stood at 3.53%, above the 3.5% threshold that
marked the original de-anchoring in July 2021. This is despite the BoE having raised
Bank Rate to 5.25% and subsequently cut back toward neutral. Realised CPI stood at
2.8% in February 2026, above target and declining only slowly.

The 5yr5yr forward inflation rate - the implied five-year inflation rate starting five
years from now, derived from the 5yr and 10yr breakeven rates - provides a cleaner
read of long-run expectations by stripping out near-term distortions. This measure rose
sharply through 2021–2022 and has remained elevated, suggesting the market's concern
extends beyond near-term CPI prints to where inflation settles structurally.

The incomplete re-anchoring has direct implications for gilt market pricing. A central
bank that cannot credibly commit to returning inflation to target cannot credibly anchor
long-end yields. The current 30yr gilt yield of 5.63% partly reflects this credibility gap,
alongside the fiscal risk premium discussed in the next section.

---

## 3. International Context and the UK Fiscal Risk Premium

UK gilt yields do not move in isolation. They are pulled by global forces - US Treasury
yields, risk sentiment, monetary policy divergence - and pushed by UK-specific factors
like fiscal credibility and sterling dynamics. Separating these two forces is analytically
important. A yield move driven by global repricing tells a different story, and has
different portfolio implications, than one driven by a deterioration in UK sovereign risk.

### Co-movement and Divergence

The 10yr gilt yield tracked US Treasuries and German Bunds broadly through the
low-rate era of 2016–2021. All three moved lower through COVID, all three began
rising as inflation emerged in 2021, and all three repriced sharply higher through 2022
as central banks tightened. The global nature of the inflation shock meant that much
of the gilt sell-off reflected forces common to all developed market sovereign bond
markets rather than anything specific to the UK.

![International Comparison](https://raw.githubusercontent.com/thomassumner123/uk-gilt-market-analysis/main/outputs/charts/p05_international_regression.png)
*Chart 5: Panel A shows 10yr government bond yields for UK, US, and Germany 2016–2026.
Panel B shows OLS regression residuals - the unexplained UK-specific risk premium.
Positive residuals indicate UK gilts yielding above what macro factors predict.*

The divergence from global factors is visible in specific episodes. Following the Brexit
vote in June 2016, UK gilt yields fell relative to US Treasuries as investors treated
gilts as a safe haven and priced the growth consequences of EU exit. This safe-haven
dynamic persisted through 2016 and into 2017. The September 2022 Truss mini-budget 
produced the opposite: a sharp UK-specific spike in gilt yields with no corresponding move 
in US Treasuries or German Bunds, reflecting a pure fiscal credibility shock rather than a
global repricing event.

### Decomposing the Gilt-Treasury Spread

To separate global from UK-specific drivers systematically, an OLS regression was run
with the gilt-Treasury spread - the difference between the UK 10yr gilt yield and the
US 10yr Treasury yield - as the dependent variable. Four macroeconomic drivers were
included as explanatory variables: GBPUSD, the UK-US 10yr inflation differential, VIX
as a measure of global risk sentiment, and the BoE-Fed rate differential.

The regression explains 56% of spread variation over the 2016–2026 sample period.
The BoE-Fed rate differential is the dominant driver, with a coefficient of 0.64 and a
t-statistic of 9.32 - confirming that monetary policy divergence between the UK and
US is the primary systematic driver of cross-country yield spreads. GBPUSD is also
significant, with a coefficient of −2.64 and a t-statistic of −4.33, reflecting the
relationship between sterling weakness and gilt underperformance. VIX is not
statistically significant at conventional levels, suggesting that global risk-off episodes
do not systematically widen or compress the gilt-Treasury spread once monetary policy
divergence is controlled for.

The regression is run in levels rather than changes, and stationarity is not formally
tested. Results are therefore interpreted as descriptive rather than causal - the
regression identifies empirical associations rather than structural relationships.

### The Residuals - Isolating the UK Risk Premium

The residuals from the regression capture what the four macro drivers cannot explain.
A positive residual means UK gilts are yielding more than the model predicts given
current macro conditions - an unexplained UK-specific premium. A negative residual
means gilts are yielding less than predicted - a safe-haven discount.

Four distinct episodes emerge from the residual series:

**Post-Brexit 2016–17: negative residuals.** Following the referendum, UK gilts
consistently yielded below what macro factors predicted. Markets were treating the UK
as a safe haven relative to the political uncertainty in continental Europe and pricing
the growth drag of Brexit as deflationary rather than inflationary. The gilt-Treasury
spread was compressed relative to fundamentals.

**Truss episode September 2022: +76bps unexplained.** At the peak of the mini-budget
crisis the residual reached +76bps - UK gilts yielding three quarters of a percentage
point more than the model predicted after controlling for monetary policy divergence,
sterling, and global risk appetite. This is the quantified fiscal credibility shock: the
pure UK-specific premium that emerged when markets lost confidence in the
government's fiscal framework.

**Mid-2023: +107bps peak.** The largest unexplained residual in the dataset occurred
not at the peak of the Truss crisis but in mid-2023, several months after the immediate
political shock had passed. This is analytically significant. The Truss episode triggered
a re-rating of UK sovereign risk that persisted and in fact deepened as markets
absorbed the scale of the UK's structural fiscal challenge. The fiscal risk premium was
larger and more persistent than the acute shock that catalysed it.

**2024–26: ongoing positive residuals.** Despite the BoE cutting rates and the
political situation stabilising under successive governments, the regression residuals
remain positive through to the end of the sample. The fiscal risk premium has not
fully unwound. The 30yr gilt at 5.63% as of March 2026 exceeds both the Truss peak
of 4.85% and the October 2023 cycle high of 5.04% - the highest in the full dataset -
reflecting a market that continues to demand elevated compensation for UK sovereign
risk beyond what monetary policy divergence alone can explain.

The evolution from negative residuals in 2016–17 to persistently positive residuals
post-2022 quantifies a structural shift in how international investors perceive UK
sovereign risk. The UK gilt market has moved from safe haven to fiscally stressed
sovereign over the course of the decade - a transition that the regression residuals
make analytically visible and empirically measurable.

### Portfolio Implications

The fiscal risk premium has direct implications for fixed income portfolio construction.
If the premium is structural rather than cyclical - reflecting genuine concern about
UK debt sustainability rather than temporary political noise - it argues for persistent
underweight positioning in long-dated gilts relative to US Treasuries and German Bunds.
The regression finding that sterling weakness accompanies gilt underperformance
further suggests that hedging sterling exposure is important when holding UK long-end
duration in an international portfolio context.

The current environment, with the BoE cutting rates while 30yr yields rise, is the clearest
expression of this dynamic. Monetary policy easing is being overwhelmed by the fiscal
risk premium at the long end. Until that premium compresses, conventional duration
extension strategies in UK gilts face a structural headwind that yield levels alone do
not capture.

---

## 4. September 2022: When the Gilt Market Broke

The Truss mini-budget of 23 September 2022 produced the most extreme gilt market
moves in the dataset. Understanding why requires separating three distinct but
overlapping forces: the fiscal credibility shock, the monetary policy repricing, and the
LDI doom loop. Each dominated at different points across the crisis week, and the
maturity pattern of daily yield moves reveals which force was in control on each day.

### Background - A Market Already Under Stress

The mini-budget did not arrive in a vacuum. By mid-2022 the BoE had already begun
its hiking cycle and inflation was running at 10.1%. Markets were repricing UK monetary
policy aggressively throughout the year.

Critically, the market had already begun pricing Truss-specific fiscal risk before the
formal announcement. The government's decision to publish the fiscal statement
without an accompanying OBR forecast, combined with signals from the leadership
contest of significant unfunded tax cuts, had pushed the 30yr yield from 2.43% on
1 August to 3.72% by 22 September - a 129bp move before a single line of the budget
had been delivered. The full market impact of the Truss fiscal episode should therefore
be measured from the August baseline rather than the day before the announcement.

### The Event Study

Daily yield changes were measured against the standard deviation of normal daily
moves over the pre-event window of January to September 2022. This produces a
standardised score for each day - how many times larger than a typical daily move
was that day's yield change.

This approach has an important limitation worth stating explicitly. Financial returns
have fat tails as extreme moves occur more frequently than a normal distribution
predicts. The standardised scores therefore cannot be interpreted as precise probability
statements. What they provide is a clean relative measure: how did each day in the
crisis week compare to the pre-event baseline, and which maturities moved most on
each day? It is this maturity pattern, rather than the absolute size of the scores, that
carries the most analytical weight.

![Truss Event Study](https://raw.githubusercontent.com/thomassumner123/uk-gilt-market-analysis/main/outputs/charts/p06_truss_event_study.png)
*Chart 6: Panel A shows UK gilt yields by maturity through the crisis period. Panel B
shows UK vs US 10yr yields with the period of UK yielding above US shaded. Panel C
shows daily yield change scores relative to the pre-event window of January to
September 2022.*

### Three Phases - Three Forces

**Mini-budget day and the immediate aftermath (23–26 September): monetary policy
repricing dominates**

On the mini-budget day itself the short end moved more than the long end. The 2yr
and 5yr recorded larger standardised moves than the 10yr and 30yr. This is
counterintuitive for a fiscal shock, as conventional wisdom suggests unfunded tax cuts
should hit the long end hardest through higher term premium and supply concerns.
The short end leading reflects something different: markets immediately pricing
emergency BoE tightening in response to the inflationary fiscal loosening. The gilt
market was pricing a policy response of aggressive rate hikes to offset the fiscal stimulus.

Panel B of Chart 6 shows UK 10yr gilt yields crossing above US 10yr Treasury yields
during this period - a UK-specific move with no equivalent in the US market,
confirming the domestic nature of the shock. The gilt-Treasury spread widened sharply
in a matter of days, directly visible in the regression residuals discussed in Section 3.

**27 September: the LDI doom loop**

By the third day of the crisis the maturity pattern reversed sharply. The 30yr recorded
a far larger standardised move than the 2yr, with the long end now driving the market.
This shift marks the point at which the LDI doom loop became the dominant force.

Liability-driven investment funds used by UK pension schemes to hedge long-duration
liabilities held leveraged positions in long-dated gilts, typically through gilt repos and
interest rate swaps. These instruments required daily variation margin payments in cash
when yields moved against the fund. As 30yr yields rose sharply, funds faced margin
calls they could not meet from cash reserves - their assets were fully invested. To
raise cash they sold gilts. Multiple funds doing this simultaneously drove yields higher,
which triggered further margin calls, which forced further selling.

A stylised illustration clarifies the mechanics. A fund with £100m of equity supporting
£300m of gilt exposure through 3x leverage faced a mark-to-market loss of
approximately £53m on a 113bp yield move - more than half its equity in a matter of
days. More critically, it faced £53m of variation margin cash demands within 24 hours,
requiring approximately £65m of distressed gilt sales at depressed prices to raise the
necessary cash. Multiplied across dozens of similarly positioned funds selling into the
same market simultaneously, the selling pressure became self-reinforcing.

**28 September: the BoE intervention**

On 28 September the BoE announced it would purchase up to £65bn of long-dated
gilts, acting as buyer of last resort to break the forced selling spiral. The 30yr yield
fell 112.8bps in a single day - the largest single-day move in the full dataset and more
than three times larger than the next most extreme event.

The BoE did not need to deploy the full £65bn. The announcement of a guaranteed
buyer was sufficient to stop the forced selling as funds no longer faced a one-sided
market and could meet margin calls without further distressed gilt sales. By end of
October 2022, following Kwarteng's dismissal and the reversal of the fiscal package,
30yr yields had returned to approximately 3.49% - below even the pre-budget day
level of 3.72%, though well above the August clean baseline of 2.43%.

### What the Crisis Reveals

The Truss episode illustrates two things that are not visible from monthly yield data
or headline commentary.

First, leverage transforms a market stress event into a systemic event. Without the
LDI leverage, pension funds facing rising yields would have experienced mark-to-market
losses but no forced selling. The leverage, and the daily variation margin mechanics
it entailed, converted a fiscal credibility shock into a near-systemic liquidity crisis
requiring central bank intervention to break.

Second, the crisis was fundamentally about the speed of cash demands rather than
solvency. Pension funds were not insolvent - their liabilities also fell as yields rose,
maintaining funding ratios broadly. The problem was that variation margin calls
demanded cash within 24 hours on funds with no liquid reserves. This distinction
matters: it explains why the BoE's announcement of a guaranteed buyer was sufficient
to break the loop without the funds needing to be recapitalised. A liquidity crisis can
be resolved by providing liquidity. A solvency crisis cannot.

---

## 5. Current Environment and Portfolio Implications

The UK gilt market in March 2026 presents a paradox. The BoE is actively cutting rates,
having begun its easing cycle in August 2024, yet gilt yields are at their highest level
in the full 2016–2026 dataset and the highest among G7 countries. The 30yr gilt yields
5.63% - above both the Truss peak of 4.85% and the October 2023 cycle high of 5.04%.
Understanding why requires drawing together the threads from the preceding sections
and connecting them to the specific dynamics of March 2026.

### The Current Yield Curve in Historical Context

The table below places current gilt yields against five reference points across the
decade.

| | Pre-Truss Aug 2022 | Truss Peak Sep 2022 | Yield Peak Oct 2023 | Cuts Begin Aug 2024 | Current Mar 2026 |
|---|---|---|---|---|---|
| 2yr | 1.67% | 4.53% | 4.61% | 3.92% | 4.28% |
| 10yr | 1.85% | 4.43% | 4.58% | 3.86% | 4.94% |
| 30yr | 2.27% | 4.85% | 5.04% | 4.50% | **5.63%** |
| 2/10 spread | +0.18% | −0.10% | −0.03% | −0.06% | +0.66% |
| 10yr breakeven | 3.60% | 3.37% | 3.56% | 3.47% | 3.53% |
| 10yr real yield | −1.75% | +1.06% | +1.01% | +0.39% | **+1.42%** |

Three observations define the current environment.

The 30yr yield at 5.63% is the highest in the dataset, exceeding even the acute
stress of the Truss episode. This is not a post-crisis hangover. It reflects a structural
repricing of UK sovereign risk that has continued to develop long after the immediate
political shock passed, consistent with the persistent regression residuals identified
in Section 3.

The 10yr real yield at +1.42% is also the highest in the dataset, a complete reversal
from the deeply negative real yields of the QE era. In January 2021 the 10yr real yield
stood at −2.98%. The 440bp swing in real yields over five years represents one of the
most dramatic shifts in the real cost of UK government borrowing in modern history.
For fixed income investors, positive real yields on gilts represent a genuine change in
the opportunity set - gilts now offer positive real returns for the first time since the
pre-QE era.

The 10yr breakeven inflation rate at 3.53% remains above the 3.5% threshold
identified in Section 2 as consistent with anchored inflation expectations, despite the
BoE having delivered a full hiking cycle. UK CPI stood at 2.8% in February 2026. The
last mile of disinflation is proving difficult and the market is not yet pricing a credible
return to target.

![Current Environment](https://raw.githubusercontent.com/thomassumner123/uk-gilt-market-analysis/main/outputs/charts/p07_current_environment.png)
*Chart 7: Panel A shows the yield curve shape at key historical dates. The current curve
sits above all historical reference points at the long end. Panel B shows the 2yr and
30yr yields across the full sample with the cutting cycle shaded.*

### Two Stories: Short End and Long End

The short end and long end of the gilt curve tell different stories in the current
environment, driven by different forces operating over different timescales.

At the short end, the BoE cutting cycle broadly achieved its intended effect through
late 2024 and into early 2026 - the 2yr yield was roughly flat as delivered cuts were
absorbed by markets and the rate path was broadly priced. The picture changed
sharply in March 2026. The US-Iran conflict, beginning in late February 2026,
drove an oil price shock that materially complicated the UK inflation outlook. The BoE's
March 2026 MPC meeting then delivered a significant hawkish surprise. Markets had
expected the MPC to signal a pause; instead the committee signalled an openness to
hiking. The shift in policy expectations was extraordinary in its speed and market-implied 
Bank Rate expectations for end-2026 moved 115bps in a single month, swinging from 
pricing approximately 50bps of further cuts to pricing 60bps of hikes. The 2yr yield spiked 
sharply higher through March as a result, ending the sample period at 4.28%.

The BoE's hawkish pivot reflects the scarring effect of the 2021–2022 inflation
episode - the very dynamic documented in Section 2 of this note. Having been
criticised for being too slow to tighten in 2021, the MPC signalled it would err on the
side of caution and tighten sooner rather than later in response to the energy shock,
in order to keep inflation expectations anchored. The institutional memory of the
transitory narrative failure is directly shaping current policy communication. Whether
this represents appropriate caution or a policy error - hiking into a weakening
economy facing a supply-side shock - remains actively debated. The concern is that
tightening into a fragile growth environment would be unambiguously negative for
forward growth without necessarily resolving the inflation shock, which is supply-side
rather than demand-driven.

At the long end the story is different and longer-running. Three structural forces have
driven the 30yr from 4.50% when cuts began to 5.63% as of March 2026 - a 113bp
move that predates the March geopolitical shock and cannot be explained by it alone.

The fiscal risk premium identified in Section 3 has not unwound. Regression residuals
remain persistently positive through to the end of the sample, suggesting the market
continues to demand excess compensation for UK sovereign risk beyond what monetary
policy divergence alone justifies. The DMO issued over £270bn of gilts in 2024–25,
creating a supply overhang that keeps the term premium elevated regardless of BoE
policy at the short end. The March geopolitical shock adds a further dimension here:
if the government were to provide fiscal support to offset the energy price shock to
consumers, breaking its fiscal rules in the process,that would be directly bearish
for gilt yields through both higher issuance and renewed fiscal credibility concerns,
echoing the dynamics of 2022.

Incomplete inflation re-anchoring prevents the long end from rallying independently.
A market pricing a 10yr breakeven inflation rate of 3.53% is implicitly saying it does
not fully believe the BoE will return inflation to 2% on a sustained basis. The
geopolitical shock has reinforced this scepticism - energy-driven inflation in March
2026 pushes breakevens higher and makes the re-anchoring story harder to tell
credibly.

Global term premium has also risen. US Treasury yields have remained elevated as
markets absorb the fiscal implications of the US deficit trajectory. Given the
relationship between UK and US long-end yields identified in Section 3, global term
premium provides a persistent structural headwind to any UK long-end rally.

### Portfolio Scenario Analysis

Three scenarios frame the key risks and positioning implications over a 12-month
horizon from March 2026. Yield moves are judgement-based estimates informed by
historical episodes in the dataset. Empirical estimation of yield curve sensitivity to
policy rate changes was attempted but produced statistically unreliable results,
reflecting that monetary policy explains only a small fraction of monthly gilt yield
variation at this frequency. The resolution of the geopolitical situation as of the data
cut-off adds material uncertainty to the probability distribution across all three
scenarios.

**Scenario 1: Soft landing (base case)**
Energy prices fall back from their March 2026 spike as geopolitical tensions ease.
Inflation falls toward 2.5% by end-2026 as services inflation moderates and the energy
shock proves temporary. The BoE does not hike in April and resumes cutting toward
neutral at around 3.25–3.50% by mid-2027. UK growth is modest but positive and the
fiscal position is broadly stable. The curve bull-steepens as the short end retraces
the March spike and prices further cuts. The long end remains elevated - term premium
persists even in the benign scenario. Short end move calibrated to approximately 50bps
of additional cuts from current levels, partially reversing the March 2026 repricing.

| Maturity | Current | Move | Implied |
|---|---|---|---|
| 2yr | 4.28% | −50bps | 3.78% |
| 5yr | 4.41% | −35bps | 4.06% |
| 10yr | 4.94% | −20bps | 4.74% |
| 30yr | 5.63% | +10bps | 5.73% |

Positioning: long 2yr and 5yr to capture the reversal of the March repricing as
energy prices stabilise and the BoE resumes cutting. Underweight 30yr - term
premium limits any long-end rally even in the base case. Neutral on index-linked gilts
as partial inflation re-anchoring reduces but does not eliminate their relative attraction.

**Scenario 2: Stagflation re-emergence (downside risk)**
The geopolitical shock proves more persistent than assumed in the base case. Energy
prices remain elevated and feed through into services inflation, pushing CPI back
toward 4–5%. The BoE hikes in April and potentially beyond, despite weak growth.
UK growth stagnates as higher rates compound the energy price squeeze on consumers.
The fiscal position deteriorates as tax revenues disappoint. The curve bear-flattens
as the short end reprices further hikes while growth fears cap the long-end move.
This scenario is a direct continuation and deepening of the dynamics already visible
in the March 2026 data. Yield moves calibrated to approximately one-third of the
2021–2022 inflation re-emergence episode, reflecting a less severe shock from an
already elevated starting point.

| Maturity | Current | Move | Implied |
|---|---|---|---|
| 2yr | 4.28% | +75bps | 5.03% |
| 5yr | 4.41% | +50bps | 4.91% |
| 10yr | 4.94% | +35bps | 5.29% |
| 30yr | 5.63% | +20bps | 5.83% |

Positioning: short duration across the curve. Overweight index-linked gilts - the
10yr breakeven inflation rate of 3.53% is likely underpricing the risk of a genuine
inflation re-emergence at 4–5%. If inflation rebounds, breakeven inflation rates would
reprice significantly higher and index-linked gilts would outperform conventional gilts.

**Scenario 3: Fiscal stress (tail risk)**
Gilt issuance overwhelms demand as the government breaks its fiscal rules to provide
energy price support, triggering renewed fiscal credibility concerns. Term premium
reprices sharply at the long end. OBR forecasts deteriorate and international investors
demand higher compensation for UK sovereign risk. The BoE faces the worst of both
worlds - hiking to contain inflation while fiscal loosening undermines long-end
credibility. The curve bear-steepens sharply. Long-end moves motivated by the Truss
episode, where the 30yr moved approximately 258bps from the August 2022 clean
baseline to peak, and by the regression residuals showing 60–107bps of persistent
unexplained UK risk premium. The scenario assumes a slow grind rather than a sudden
shock, with 100bps at the 30yr as the central estimate.

| Maturity | Current | Move | Implied |
|---|---|---|---|
| 2yr | 4.28% | −25bps | 4.03% |
| 5yr | 4.41% | +15bps | 4.56% |
| 10yr | 4.94% | +60bps | 5.54% |
| 30yr | 5.63% | +100bps | 6.63% |

Positioning: maximum short duration at the long end. Overweight 2yr versus 30yr
as a steepening trade. A 30yr yield of 6.63% would represent a new historical extreme,
above any observation in the 2016–2026 dataset, and would constitute a new
sovereign risk regime for the UK gilt market.

In all three scenarios the 30yr remains elevated or rises further. Even the base case
implies a 30yr yield of 5.73%. A meaningful compression in long-end yields requires
either a credible fiscal consolidation that reduces the term premium, a sustained
de-escalation of geopolitical risk that allows energy prices to fall back, or a growth
shock severe enough to force aggressive BoE easing - none of which is the base case
as of March 2026.

---

*This note was produced independently as a research project. All data sourced from
the Bank of England Statistical Interactive Database, ONS, and Federal Reserve (FRED).
Full code, data methodology, and notebooks available at:*
*[github.com/thomassumner123/uk-gilt-market-analysis](https://github.com/thomassumner123/uk-gilt-market-analysis)*