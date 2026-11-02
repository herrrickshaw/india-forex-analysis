# India external account and forex analysis (FY 2019-20 to FY 2026-27)

A set of nine written analyses of India's foreign-exchange reserves, merchandise trade balance, government
debt and fiscal capacity for the post-pandemic period, with projections to FY 2026-27. The repository is
Markdown only: there is no code, no data files and no notebooks. It is intended for policy readers and
analysts who want a structured narrative with a decision matrix, not a reproducible data pipeline.

> Status: archived snapshot. All documents are dated 25 June 2026 and have not been updated since.
> Figures are the authors' compilations from Government of India budget documents, RBI reserve reports and
> TradeStat; the underlying source files are **not** included in this repository. Not investment advice.

## What it does
- Compares export growth 2020-2023 (+44%, $623B to $898B, 12.96% CAGR) across 14,980+ HS commodities and projects 2026-27 exports at $1.31T (doc 1).
- Breaks the trade deficit down by commodity and runs three scenarios (base / bull / bear) for FY 2025-26 and FY 2026-27 (doc 2).
- Assesses FX reserve adequacy from the March 2026 RBI position ($691.11B, 10.8 months import cover, 79.9% FCA / 16.7% gold) and rates it AMBER (doc 3).
- Reconciles an earlier ~$300B tax-revenue estimate against the official 2026-27 budget figure of $530.5B (+77% correction) (doc 4).
- Tracks debt receipts, the 2026-27 maturity wall ($65.8B) and the refinancing share of borrowing (17% to 32%) (doc 5).
- Sets out a year-by-year deterioration timeline (best year FY 2019-20, worst projected FY 2026-27), a three-scenario policy outlook and a monitoring dashboard (docs 6, 7, 9).

## Quick start
There is nothing to install or run. Clone and read, or open the files on GitHub.

```bash
git clone https://github.com/herrrickshaw/india-forex-analysis.git
cd india-forex-analysis
open 9_EXECUTIVE_SUMMARY_COMPREHENSIVE.md   # the policy brief; start here
```

Suggested reading paths (from `ANALYSIS_INDEX.md`):

| Audience | Order |
|---|---|
| Quick overview (30 min) | `README.md`, then parts 1-3 of doc 9 |
| Policy readers (1-2 h) | doc 9 in full; decision matrix (part 8) and dashboard (part 9) |
| Analysts (4-6 h) | docs 2, 3, 4, 5, 7 |
| Strategic planners (3-4 h) | docs 6, 3, 9 |

For plain-language use with an AI assistant see [`HOW_TO_USE_WITH_AI.md`](HOW_TO_USE_WITH_AI.md).

## How it works
The documents build on each other in numbered order: verified trade data (doc 1) feeds the deficit
projections (doc 2), which drive the reserve-adequacy assessment (doc 3). Docs 4 and 5 add the fiscal side
(tax revenue, debt). Docs 6 and 7 place everything on a 2019-2027 timeline. Doc 8 describes a cross-validation
framework against four PDF sources, and doc 9 is the executive brief that collects the scenarios, decision
matrix and recommendations. `ANALYSIS_INDEX.md` lists every document's sections and key metrics.

## Repository layout
| Path | Purpose |
|---|---|
| `1_EXTENDED_COMPARISON_2020_2026.md` | Export growth by commodity, 2026-27 projection |
| `2_IMPORT_EXPORT_ANALYSIS_2025_26.md` | Trade balance, deficit scenarios |
| `3_RBI_RESERVES_vs_TRADE_DEFICIT_ANALYSIS.md` | FX reserve adequacy (March 2026 snapshot) |
| `4_BUDGET_ESTIMATES_VS_ANALYSIS_RECONCILIATION.md` | Tax-revenue correction against the 2026-27 budget |
| `5_DEBT_BORROWING_TRENDS_ANALYSIS.md` | Debt receipts, refinancing burden, interest costs |
| `6_FIVE_YEAR_POST_PANDEMIC_COMPARISON.md` | 2020-2026 arc, what got worse / better |
| `7_YEAR_ON_YEAR_TRENDS_DETERIORATION_ANALYSIS.md` | Year-by-year timeline, best and worst years |
| `8_MULTI_SOURCE_INTEGRATION_ANALYSIS.md` | Cross-validation framework against budget annexes and NCAER research |
| `9_EXECUTIVE_SUMMARY_COMPREHENSIVE.md` | Policy brief: scenarios, decision matrix, dashboard, recommendations |
| `ANALYSIS_INDEX.md` | Per-document section list, coverage matrix, reading paths |
| `HOW_TO_USE_WITH_AI.md` | How to read the repo with an AI assistant |

## Data sources
As cited inside the documents. None of these files is tracked in the repository.

| Source | What is taken | Access route | Caveat |
|---|---|---|---|
| Receipt Budget 2026-27, Union Budget 2026-27 analysis and annexes (Annex 268, Annex 9) | Tax revenue, debt receipts, maturity profile | indiabudget.gov.in PDFs | Read manually; not re-extracted here |
| RBI Foreign Exchange Reserves reports, Oct 2025 to Mar 2026 | Reserve level and composition | rbi.org.in | Snapshot as of March 2026 |
| TradeStat (DGCI&S / Ministry of Commerce) | Commodity-level exports and imports, 14,980+ HS lines | tradestat.commerce.gov.in | Figures converted to USD by the authors |
| NCAER Working Paper 180 | Economic-research cross-check | ncaer.org | Doc 8 describes the expected integration |

## Limitations and known issues
- Snapshot only: compiled 25 June 2026; the documents themselves say FY 2025-26 final trade data (July 2026) and FY 2026-27 interest costs were not yet available.
- No source data, spreadsheets or code are included, so the numbers cannot be regenerated from this repository.
- Headline figures are not fully consistent between documents: the trade deficit is given as -$567B (2023-24) and -$769.5B (2026-27 projected) in docs 2, 6 and 7, but as -$850B (2025-26) in doc 9. Treat the deficit series as indicative, not reconciled.
- The deficit and reserve-cover figures should be checked against official RBI/DGCI&S releases before being quoted; they have not been independently verified here.
- Doc 8 is a framework for cross-validating against the four listed PDFs; it records expected rather than completed checks.
- "Confidence levels" quoted in the documents are the authors' judgement, not statistical confidence intervals.

## Related repositories
- [india-trade-data-analysis](https://github.com/herrrickshaw/india-trade-data-analysis) — descriptive trade and macro datasets (TradeStat HSN series, RBI reserves, USD/INR) with charts.

## Licence
No licence file yet — all rights reserved. The underlying government data remains subject to its publishers' terms.
