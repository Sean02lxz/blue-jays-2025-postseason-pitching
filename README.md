# Toronto Blue Jays 2025 Postseason Pitching Analysis

## Project Overview

This data science project examines the Toronto Blue Jays' pitching performance during the 2025 MLB postseason.

**Main Research Question:**

How effectively did Toronto Blue Jays pitchers perform during the 2025 postseason relative to their salaries, workloads, and opposing teams?

## Research Questions

### RQ1 — Salary Efficiency
How did Blue Jays pitchers perform compared with similarly paid postseason pitchers?

Three benchmarking methods were implemented:
- V1: Salary quartile median
- V2: 10 nearest-salary peers
- V3: PA-weighted nearest-salary benchmark

### RQ2 — Workload Comparison
How did Blue Jays pitchers perform compared with teammates who faced similar numbers of qualifying plate appearances?

We examined workload-matched pitchers and used bootstrapping to estimate uncertainty in performance differences.

### RQ3 — Series-Level Performance
How did Toronto's pitchers perform compared with opposing pitchers during each postseason series?

We analyzed the:
- ALDS against the New York Yankees
- ALCS against the Seattle Mariners
- World Series against the Los Angeles Dodgers

## Tools and Methods

**Technologies:** Python, Jupyter Notebook, Pandas, NumPy, Matplotlib, and SciPy.

**Statistical methods:**
- Exploratory Data Analysis (EDA)
- Weighted On-Base Average (wOBA) calculations
- Salary-based benchmarking
- Spearman rank correlation
- Bootstrap confidence intervals

## Key Findings

- Salary showed no statistically significant monotonic association with postseason wOBA allowed among the 63 qualifying pitchers (Spearman ρ = 0.0375, p = 0.7706).
- Workload-based comparisons showed that pitchers with similar qualifying plate appearances could have different observed performances.
- Toronto recorded lower wOBA allowed than its opposing pitching staffs in all three postseason series, but the 95% game-level bootstrap confidence intervals included zero.

These findings are exploratory and should be interpreted cautiously due to the limited postseason sample sizes.

## Data Sources

- MLB Statcast / Baseball Savant — 2025 postseason pitch-by-pitch data.
- [2025 MLB Contract Efficiency](https://github.com/leo-sykucki/2025-mlb-contract-efficiency) — Cot's-derived salary records.
- [2025 MLB Payroll Evaluation](https://github.com/Owen-Quast/war-and-payroll-evaluation-2025) — supplementary salary records.
- FanGraphs, Baseball Almanac, and The Baseball Cube — additional salary references.

Original third-party datasets are not redistributed in this repository. They must be obtained separately in accordance with their providers' terms.

## Project Deliverables

- Jupyter Notebook containing data preparation, visualizations, benchmarks, and statistical analysis.
- Interactive dashboard presenting the results of the three research questions.
- Final report documenting the methodology, findings, limitations, and recommendations.

## Limitations

This project focuses on a single postseason. Differences in sample sizes, pitcher roles, opposing lineups, and salary data sources may affect the comparisons.

This is an academic project and is not affiliated with Major League Baseball or the Toronto Blue Jays.
