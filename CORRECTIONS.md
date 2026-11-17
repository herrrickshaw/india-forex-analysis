# Corrections and data refresh (2026-10-23)

## What was wrong: every trade total in this repo is exactly 2x

The trade figures in the nine analysis documents were produced by summing the
TradeStat-Eidb commodity sheets **including the sheet's own grand-total row**
("India's Total Export" / "India's Total Import"). The total row is counted on top
of the line items it already adds up, so each sum is twice the true value.

Evidence, checked against the descriptive sibling repo
[`india-trade-data-analysis`](https://github.com/herrrickshaw/india-trade-data-analysis)
(`data/tradestat_hsn_export_import_2018-19_to_2025-26.json`, DGCI&S TRADESTAT,
US$ million, retrieved 2026-07-18):

| Figure in this repo (before) | Sibling repo, matching fiscal year | Ratio |
|---|---|---|
| "2020" exports $583.6B | FY2020-21 exports $291.8B | 2.000 |
| "2022" exports $902.1B (`EXPORT_INSIGHTS_SUMMARY.md` in `india-trade-export-analysis`) | FY2022-23 exports $451.1B | 2.000 |
| "2023" exports $875.4B | FY2024-25 exports $437.7B | 2.000 |
| "2023" imports $1,442.4B | FY2024-25 imports $721.2B | 2.000 |
| "2023" deficit -$567.0B | FY2024-25 deficit -$283.5B | 2.000 |

The same workbook total, $437,704.58M, appears as the "India's Total Export" row of
`india-trade-export-analysis/EXTENDED_ANALYSIS_2020_2026.csv`, which is exactly the
sibling's FY2024-25 value ($437,704.5M).

**Period label:** the workbook this repo calls "2023" matches FY2024-25
($437,704.5M), not FY2023-24 ($437,072.1M). The repo's "2020-2023 / 3 year"
framing (and the CAGR built on it) therefore cannot be trusted as labelled; the
source workbook is not in the repo, so its own period header could not be checked.

## Corrected figures (US$ billion, merchandise, DGCI&S TRADESTAT)

Full series: [`data/india_merchandise_trade_totals_FY2018-19_to_FY2025-26.csv`](data/india_merchandise_trade_totals_FY2018-19_to_FY2025-26.csv)
(from the sibling repo, retrieved 2026-07-18; FY2025-26 is provisional, source data last updated 19 May 2026).

| Fiscal year | Exports | Imports | Balance |
|---|---|---|---|
| 2018-19 | 330.1 | 514.1 | -184.0 |
| 2019-20 | 313.4 | 474.7 | -161.3 |
| 2020-21 | 291.8 | 394.4 | -102.6 |
| 2021-22 | 422.0 | 613.1 | -191.0 |
| 2022-23 | 451.1 | 716.0 | -264.9 |
| 2023-24 | 437.1 | 678.2 | -241.1 |
| 2024-25 | 437.7 | 721.2 | -283.5 |
| 2025-26 (provisional) | 441.7 | 776.0 | -334.3 |

(Balance = exports minus imports, computed from the rounded totals.)

## What is withdrawn

These depend on the 2x base and are **not** restated here because the commodity
workbooks are not in the repo and projections cannot be recomputed from them:

- "2023" exports $875.4B / imports $1,442.4B / deficit -$567.0B, and the 2020 base $583.6B.
- The 2026 projections ($1.31T exports, $2.08T imports, -$769.5B deficit) and the
  scenario deficits (-$750B / -$765B / -$820B), the "7.3x worse than pre-pandemic",
  "+218% export growth" and "+279% import growth" headlines, and the monthly trade
  drain figures.
- The "10.8 months import cover" ratio is not reproducible from any figure in the
  repo. Using the corrected data: latest RBI reserves $675.2B (week ended 10 Jul 2026)
  against FY2025-26 provisional imports of $776.0B is about 10.4 months of imports
  (own arithmetic: 675.157 / (776.0137 / 12)).
- The qualitative direction (imports growing faster than exports) holds on the corrected
  series: FY2018-19 to FY2025-26 imports +51.0% vs exports +33.8% (own arithmetic from the table above).

## Refresh: latest figures available from sibling repos (not from new collection)

| Item | Value | Period / date | Source |
|---|---|---|---|
| Merchandise exports | $441.7B | FY2025-26 (provisional) | `india-trade-data-analysis`, TRADESTAT, retrieved 2026-07-18 |
| Merchandise imports | $776.0B | FY2025-26 (provisional) | same |
| Merchandise balance | -$334.3B | FY2025-26 (provisional) | same; PIB cites -$333.19B (cross-validation file in the sibling repo) |
| RBI total reserves, latest | $675.2B | week ended 10 Jul 2026 | RBI Weekly Statistical Supplement via sibling `rbi_forex_reserves_2015-01_to_2025-06.json` (`web_extension`) |
| RBI total reserves, all-time high | $728.5B | 27 Feb 2026 | same |
| RBI total reserves, trough since | $666.9B | 26 Jun 2026 (-8.5% from peak) | same |
| USD/INR spot | 96.37 | 17 Jul 2026 | sibling README, RBI rate series |

Discrepancies with this repo's other claims, left unedited but flagged:
the "$691.11B (March 2026)" reserves figure does not appear in the sibling weekly
series (27 Mar 2026: $688.1B); the "$426B in 2019-20" reserves figure differs from the
sibling's MoSPI/RBI monthly series (Mar 2020: $477.8B); the "-$105B 2019-20 deficit"
is closer to FY2020-21 (-$102.6B) than to FY2019-20 (-$161.3B).

## Not refreshed

The user's cloud reference-data copy was checked and holds no India trade, RBI or
forex series (only Damodaran and Fama-French reference files), so it contributed nothing.
The fiscal/debt documents (budget, borrowing, interest burden) were not re-sourced.
