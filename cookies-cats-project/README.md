# Cookie Cats A/B Test Analysis

An A/B testing project analyzing whether moving the first gate in the mobile game Cookie Cats from level 30 to level 40 affects player retention and engagement.

## Experiment Overview

Players were randomly assigned to one of two groups:

- `gate_30`: the first gate appeared at level 30.
- `gate_40`: the first gate appeared at level 40.

The dataset contains 90,189 players and records their game rounds, Day 1 retention, and Day 7 retention.

## Hypotheses

For the primary metric, Day 7 retention:

- **H₀:** Day 7 retention is the same for the `gate_30` and `gate_40` groups.
- **H₁:** Day 7 retention differs between the two groups.

Day 1 retention and game rounds were also analyzed as secondary metrics.

## Analysis

- Prepared the dataset and checked for missing values and duplicate player IDs.
- Compared retention rates using the Chi-square test.
- Compared game rounds using the two-sided Mann–Whitney U test.
- Used a significance level of **α = 0.05**.

## Key Findings

- **Day 7 retention:** 19.02% for `gate_30` and 18.20% for `gate_40` (**p = 0.0016**). The difference was statistically significant, favoring `gate_30`.
- **Day 1 retention:** 44.82% for `gate_30` and 44.23% for `gate_40` (**p = 0.0750**). The difference was not statistically significant at the 5% level.
- **Game rounds:** The groups had similar average rounds; the Mann–Whitney U test did not find a statistically significant difference at the 5% level (**p = 0.0509**).

Based on the primary metric, the results do not show an improvement in Day 7 retention from moving the gate to level 40.

## Tools

- Python
- pandas, NumPy, SciPy, Matplotlib, and Seaborn
- Excel

## Files

- `Cookie_cats_game_projects.ipynb` — Data preparation and statistical analysis
- `cookie_cats.xlsx` — Dataset
- `BÁO CÁO PHÂN TÍCH GAME COOKIE CATS.pdf` — Project report

## Note

One player with 49,854 game rounds was excluded as an extreme outlier in the notebook. The report recommends a sensitivity check that retains this player for the retention tests and excludes the record only from the game-rounds analysis.
