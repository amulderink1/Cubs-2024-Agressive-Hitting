# Cubs 2024 Swing Aggression Analysis

This project looks at how swing habits for Chicago Cubs hitters relate to their offensive performance during the 2024 season. The analysis uses Statcast data (from Baseball Savant) and player performance statistics (from FanGraphs), pulled using the pybaseball library.

## Project Focus

The main question for this project is whether more aggressive hitters perform better or worse.

Swing metrics analyzed:
- Swing%: Percentage of total pitches swung at
- O-Swing% (chase rate): Percentage of swings at pitches outside the strike zone
- 1st Pitch Swing%: Percentage of plate appearances where the batter swung at the first pitch

Performance metrics analyzed:
- Batting Average (AVG)
- On-Base Percentage (OBP)
- Slugging Percentage (SLG)
- Weighted On-Base Average (wOBA)

## Methods

- Used pybaseball to pull pitch-level Statcast data for the Cubs 2024 season.
- Filtered for Cubs hitters using MLBAM IDs.
- Calculated Swing%, O-Swing%, and 1st Pitch Swing% from Statcast data.
- Merged swing metrics with season-long performance stats from FanGraphs.
- Compared swing tendencies to performance using correlation analysis and regression plots.

## Findings

- Hitters with higher O-Swing% (chasing pitches out of the zone) tended to have lower wOBA, suggesting that over-aggressive approaches negatively impact performance.
- 1st Pitch Swing% showed weaker correlation to overall offensive performance.
- Overall Swing% was not strongly tied to wOBA.

## Files Included

- `cubs_2024_swing_metrics.csv`: Full dataset of Cubs hitters with swing and performance metrics.
- `cubs_2024_swing_aggression_full.csv`: Summary of swing aggression data.
- Jupyter Notebook containing the full code and visualizations.

## Tools Used

- Python
- pybaseball
- pandas
- seaborn
- matplotlib
