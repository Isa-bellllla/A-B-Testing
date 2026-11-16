# Cookie Cats A/B Testing | Player Retention Analysis

### Evaluating the Impact of Gate Placement on Player Retention

**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Statsmodels  
**Skills:** A/B Testing, Experiment Design, Exploratory Data Analysis, Hypothesis Testing, Statistical Inference, Product Analytics

## Project Overview

Cookie Cats is a mobile puzzle game in which players encounter progression gates that require them to wait before continuing.

This project analyzes an A/B experiment comparing two gate configurations:

- **Control Group (`gate_30`):** The first gate appears at Level 30.
- **Treatment Group (`gate_40`):** The first gate appears at Level 40.

The objective is to determine whether delaying the first gate improves player retention by reducing early gameplay interruptions.

Using data from 90,189 players, this project evaluates the impact of gate placement on Day-7 retention and translates statistical findings into actionable product recommendations.

## Business Problem

Progression gates introduce friction into the gaming experience. While delaying a gate may allow players to enjoy longer uninterrupted gameplay, an earlier gate may encourage players to return after a waiting period.

**Key Business Question:**

Does moving the first gate from Level 30 to Level 40 improve player retention, or does the change negatively affect long-term engagement?

The analysis aims to support a data-driven decision about whether the new gate configuration should be implemented.

## Experiment Design

### Control and Treatment Groups

| Group | Configuration | Sample Size |
|---|---|---:|
| Control | Gate at Level 30 | 44,700 |
| Treatment | Gate at Level 40 | 45,489 |
| **Total** | | **90,189** |

### Proposed Experiment Setup

For a real-world implementation, the experiment would target players who were active during the previous week and had not yet reached Level 30.

Eligible users would be randomly assigned at the user level to one of two configurations, with a planned 50/50 allocation across iOS and Android platforms.

The proposed experiment would use a 14-day enrollment period followed by a 7-day observation window to capture Day-7 retention for all enrolled users.

*Note: This is a retrospective case study using an existing public dataset. The proposed eligibility criteria, experiment duration, and platform coverage cannot be independently verified from the available data.*

## Success Metrics

| Category | Metric | Purpose |
|---|---|---|
| Primary | Day-7 Retention Rate | Evaluate sustained player retention |
| Secondary | Day-1 Retention Rate | Measure short-term retention |
| Secondary | Average Game Rounds | Evaluate gameplay engagement |
| Secondary (Proposed) | Early-Level Completion Rate | Assess player progression |
| Secondary (Proposed) | Session Abandonment Rate | Investigate player disengagement |
| Guardrail (Proposed) | Revenue per User (ARPU) | Monitor monetization impact |
| Guardrail (Proposed) | Purchase Conversion Rate | Detect changes in purchasing behavior |
| Guardrail (Proposed) | Crash-Free User Rate | Monitor product reliability |

The available dataset supports direct analysis of Day-1 retention, Day-7 retention, and game rounds. Other metrics are included as recommendations for future experiment instrumentation.

## Dataset

**Source:** [Cookie Cats A/B Testing — Kaggle](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)

## Key Findings

### Day-7 Retention

The treatment group exhibited lower Day-7 retention than the control group.

| Statistical Result | Value |
|---|---:|
| Z-statistic | -3.1644 |
| Two-sided p-value | ≈ 0.00155 |
| Significance Level | 0.05 |
| Statistical Decision | Reject H₀ |
| Observed Direction | Lower retention in `gate_40` |

The results indicate a statistically significant difference in Day-7 retention between the two configurations.
