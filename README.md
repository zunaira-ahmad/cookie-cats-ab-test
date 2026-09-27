## Mobile Games A/B Testing - Cookie Cats

Cookie Cats is a mobile puzzle game that has levels with one specific level being the 'gate' pauses player from progressing further unless they wait or pay for it. An A/b Testing Analysis will help us determine whether moving a mobile game level from gate 30 to gate 40 affects player retention.

## Business Question:

Should the gate be moved from level 30 to level 40?

## Dataset:

[Mobile Games A/B Testing — Cookie Cats](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)
(Kaggle) — 90,189 players randomly assigned to `gate_30` (control) or `gate_40` (treatment), with day-1 and day-7 retention tracked per player.

## Methodology:

1. Setup
    Importing all libraries and checking the data visually.

2. Exploratory Data Analysis:
    Analyzing the data by checking for missing values, outliers, any inconsistent data. 

3. Check Sample Ratio Mismatch (SRM):
   Verify the two groups are equally randomnly distributed before moving forward with the testing.
   
4. Hypothesis Testing: Two-Proportion Z-Test¶
    Perform testing to determine whether the true retention rate differs in both groups or not.
    
## Recommendation and Conclusion

    Results:

    | Metric | gate_30 | gate_40 | Abs. diff | Relative lift | p-value | 95% CI |
    |---|---|---|---|---|---|---|
    | Day-1 retention | 44.82% | 44.23% | 0.59pp | 1.34% | 0.0744 | (-0.06pp, 1.24pp) |
    | Day-7 retention | 19.02% | 18.20% | 0.82pp | 4.51% | **0.0016** | (0.31pp, 1.33pp) |

    - Retention Day 1: Since p-value>0.05 and the confidence interval barely contains 0, the results are not statistically significant.

    - Retention Day 7: Since p-value<0.05 and the confidence interval is above 0, the results are statistically significant.
    
    Recommendation:
    
    **Do not move the gate from level 30 to level 40.** 
    
    The change shows no retention benefit and measurably reduces 7-day retention by an estimated 0.3-1.3 percentage points (~4.5% relative decline). Recommend keeping the gate at its current position.

