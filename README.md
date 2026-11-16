# Analysis code, data and figures

Code, data and figures for an analysis of severe injury rates by industry
sector in the United States (OSHA Severe Injury Reports, 2015-2024).

## Files

| File | Content |
|---|---|
| `analysis_code.txt` | Complete R code, saved as plain text |
| `analysis_data.xlsx` | Analysis data: reports and employment by sector and year, sector totals with the Michigan reporting counts, and the jurisdiction table |
| `fig1_rank_intervals.png` | Rank intervals of hospitalization rates |
| `fig2_rank_bounds.png` | Rank bounds without reporting data |
| `fig3_agriculture.png` | Sensitivity to agricultural employment |
| `figS1_pairwise.png` | Pairwise comparisons of sectors |

## Code flow

| Step | What it does |
|---|---|
| 0 | Setup: folders, packages, helper functions |
| 1 | Download and clean the injury reports and the employment data |
| 2 | Select federal-jurisdiction states; reported rates and ranks |
| 3 | Simulation of rank uncertainty under unequal reporting |
| 4 | Tipping ratios for pairs of sectors and rank bounds |
| 5 | Hospitalization outcome; sensitivity to agricultural employment |
| 6 | Tables and figures |
| 7-9 | Robustness checks |

## How to run

1. Install R (version 4 or later) and copy the code into an R script.
2. Edit `base_candidates` in step 0 so that it points to a folder on your machine.
3. Run the code from top to bottom.

The code downloads the public source data itself and caches it. Random seeds
are fixed, so results are reproducible.

## Data sources

- OSHA Severe Injury Reports: <https://www.osha.gov/severe-injury-reports>
- BLS Quarterly Census of Employment and Wages: <https://www.bls.gov/cew/>
- Published Michigan linkage studies of employer reporting
