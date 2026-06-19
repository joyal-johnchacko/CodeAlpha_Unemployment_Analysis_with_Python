# India Unemployment Analysis (2019–2020): COVID-19 Impact Study

A Python-based exploratory data analysis (EDA) of state-wise unemployment in India, examining the impact of the COVID-19 lockdown on Rural and Urban employment trends.

## Overview

This project analyzes monthly unemployment data across 28 Indian states from May 2019 to June 2020, with a focus on quantifying the economic shock caused by the COVID-19 lockdown (effective March 25, 2020). The analysis compares pre- and post-lockdown unemployment rates, breaks down the impact by Rural vs Urban areas, and identifies the states most affected.

## Dataset

| Attribute | Details |
|---|---|
| **Source** | CMIE (Centre for Monitoring Indian Economy), via Kaggle |
| **Coverage** | 28 Indian states |
| **Time period** | May 2019 – June 2020 |
| **Frequency** | Monthly |
| **Granularity** | Rural and Urban split per state |

### Columns

| Column | Description |
|---|---|
| `State` | Name of the Indian state |
| `Date` | Date of observation (end of month) |
| `Frequency` | Reporting frequency (Monthly) |
| `Unemployment_Rate` | Estimated unemployment rate (%) |
| `Employed` | Estimated number of employed people |
| `Labour_Participation_Rate` | Estimated labour participation rate (%) |
| `Area` | Rural or Urban |

## Objectives

- Clean and prepare raw unemployment data for analysis
- Explore unemployment trends across states, regions, and time
- Quantify the impact of COVID-19 on national unemployment
- Compare Rural vs Urban unemployment shocks
- Identify the states hit hardest by the lockdown
- Present insights relevant to economic and social policy

## Methodology

1. **Data Cleaning** — Standardized column names, removed fully blank rows, parsed dates, and stripped whitespace from text fields.
2. **Exploratory Analysis** — Summary statistics, state and area counts, date range validation.
3. **COVID-19 Impact Analysis** — Split the dataset at the lockdown date (March 25, 2020) and compared average unemployment before and after.
4. **Rural vs Urban Comparison** — Measured the differential impact of the lockdown across area types.
5. **State-Level Ranking** — Identified states with the highest average and peak unemployment rates.
6. **Visualization** — Generated trend lines, comparative charts, and a heatmap to illustrate patterns over time and geography.

## Key Findings

- **National impact:** Average unemployment rose significantly following the March 2020 lockdown compared to the prior year's baseline.
- **Urban areas were hit harder than Rural areas**, both in absolute pre-lockdown levels and in the size of the post-lockdown increase — likely because urban employment is more concentrated in factories, offices, and retail, which shut down completely, while rural areas retained some agricultural work as a buffer.
- **Certain states experienced extreme spikes** in specific months, far exceeding the national average, indicating uneven regional impact.
- The unemployment spike began immediately after the lockdown announcement and showed signs of gradual recovery in the following months.

## Tech Stack

- **Python 3**
- **pandas** — data loading, cleaning, and aggregation
- **matplotlib** — core visualizations
- **seaborn** — statistical plots (heatmap)

## How to Run

```bash
pip install pandas matplotlib seaborn
python unemployment_final.py
```

Make sure to update the file path in `pd.read_csv("unemployment.csv")` to match your local dataset location before running.

## Visualizations Included

1. National unemployment rate trend (with lockdown marker)
2. Rural vs Urban unemployment trend comparison
3. Top 10 states by average unemployment rate
4. Unemployment rate heatmap (State × Month)

## Policy Relevance

The findings highlight the need for:
- Targeted economic relief for urban informal-sector workers
- State-specific intervention for the most heavily impacted regions
- Stronger rural employment safety nets (e.g., MGNREGA-style programs) as a buffer during future economic shocks
- Continued monitoring of labour participation rates, not just unemployment, to capture "discouraged worker" effects

## Author

Joyal John Chacko
B.Tech Computer Science & Engineering, Government Model Engineering College (KTU)
