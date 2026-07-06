# Mobile Game Retention and A/B Testing Analysis

## Project Overview

This project analyzes a mobile game A/B test from **Cookie Cats**, where players were randomly assigned to one of two versions:

- `gate_30`: the first gate appears at level 30
- `gate_40`: the first gate appears at level 40

The goal is to evaluate whether moving the gate from level 30 to level 40 improves player engagement and retention.

## Tools Used

- Python
- Power BI
- pandas
- SciPy
- statsmodels

## Dataset

The dataset contains **90,189 player records** with the following fields:

| Column | Description |
|---|---|
| `userid` | Unique player ID |
| `version` | A/B test group: `gate_30` or `gate_40` |
| `sum_gamerounds` | Total game rounds played by each player |
| `retention_1` | Whether the player returned after 1 day |
| `retention_7` | Whether the player returned after 7 days |

## Analysis Workflow

1. Checked missing values, duplicate users, and group balance.
2. Compared player engagement using average and median game rounds.
3. Calculated Day-1 and Day-7 retention rates for each test group.
4. Used statistical testing to evaluate whether retention differences were significant.
5. Built a Power BI dashboard to summarize player behavior and A/B test results.

## Key Metrics

| Metric | Gate 30 | Gate 40 | Difference | Result |
|---|---:|---:|---:|---|
| Day-1 Retention | 44.82% | 44.23% | +0.59 pp | Not significant |
| Day-7 Retention | 19.02% | 18.20% | +0.82 pp | Significant |
| Median Game Rounds | 17 | 16 | +1 | Borderline |

## Key Findings

- The two test groups were relatively balanced, with **44,700 players** in `gate_30` and **45,489 players** in `gate_40`.
- `gate_30` showed slightly higher Day-1 retention than `gate_40`, but the difference was not statistically significant.
- `gate_30` showed significantly higher Day-7 retention than `gate_40`.
- Median game rounds were slightly higher for `gate_30`, suggesting marginally stronger engagement.
- Moving the gate from level 30 to level 40 did not improve long-term retention.

## Recommendation

Based on the A/B test results, the product team should **keep the gate at level 30** to support stronger long-term player retention.

## Dashboard Preview

### Player Engagement Overview

![Player Engagement Overview](Player%20Engagement%20Overview.png)

### A/B Test Results

![A/B Test Results](AB%20Test%20Results.png)

## Files

- `cookie_cats.csv` — original dataset
- `Mobile_Games_Retention_and_A_B_Testing_Analysis.ipynb` — Python analysis notebook
- `Player Engagement Overview.png` — Power BI dashboard page 1
- `AB Test Results.png` — Power BI dashboard page 2

## Limitations

- The dataset does not include monetization metrics such as ARPU or revenue.
- The analysis focuses on retention and engagement, not full player lifetime value.
- One extreme outlier was found in game rounds, so median rounds were used alongside average rounds for interpretation.

## Portfolio Summary

This project demonstrates the use of Python and Power BI to analyze mobile game player behavior, evaluate an A/B test, monitor retention KPIs, and provide a product recommendation based on data.
