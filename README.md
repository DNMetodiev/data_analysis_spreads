# Exploratory Data Analysis of Financial Spreads

This project focuses on analyzing financial spread data for symbols such as `US30` and `USD/JPY`. The primary objectives include exploring the distribution, time-series trends, hourly patterns, and detecting anomalies in `avg_spread`. The analysis provides actionable insights and recommendations for alert thresholds based on spread variability.

## Overview

The project analyzes a dataset containing financial spread data, focusing on symbols such as `US30` and `USD/JPY`. The goal is to:
- Understand distribution patterns of `avg_spread`.
- Identify hourly and symbol-specific trends.
- Detect and visualize outliers.
- Provide insights for actionable alert thresholds.

## Dataset Description

- **File Name:** `spreads.csv`
- **Key Columns:**
  - `quote_hour`: Timestamp of the data point.
  - `symbol`: Financial instrument (e.g., US30, USD/JPY).
  - `avg_spread`: Average spread for the given symbol and hour.
- **Preprocessing:**
  - Converted `quote_hour` to datetime format.
  - Verified and aligned timestamps.
  - Filled missing data with a chronological order.

## Key Features of the Analysis

1. **Distribution Analysis:**
   - Visualized the distribution of `avg_spread` using histograms.
   - Compared spread variability across symbols.

2. **Time-Series Trends:**
   - Analyzed trends in `avg_spread` over time for each symbol.
   - Identified periodic patterns and variability.

3. **Hourly Trends:**
   - Created a heatmap to visualize spread variability by hour and symbol.

4. **Outlier Detection:**
   - Detected anomalies using statistical techniques like Z-scores.
   - Highlighted outliers in time-series plots.

5. **Recommendations:**
   - Defined thresholds for alert systems based on spread variability.

## Visualizations

- **Histogram of Average Spread:**
  - Distribution of `avg_spread` for different symbols.
- **Time-Series Line Plots:**
  - Trends in spread over time by symbol.
- **Hourly Heatmap:**
  - Spread variability by hour for each symbol.
- **Outlier Scatter Plot:**
  - Visualization of anomalies in `avg_spread`.

## Findings

### Distribution of `avg_spread`
- `US30` exhibits greater variability and higher average spreads compared to `USD/JPY`.
- `USD/JPY` has a more stable distribution with fewer extreme values.

### Time-Series Trends
- Spreads show periodic fluctuations over time, with specific symbols (e.g., `US30`) experiencing spikes during certain hours.

### Hourly Trends
- Heatmap revealed patterns such as higher spreads for `US30` during early mornings and late afternoons.

### Outliers
- Anomalies align with high-volatility periods, often influenced by external market events.

## Recommendations

1. **Threshold-Based Alerts:**
   - Use Z-scores to identify significant deviations.
   - Recommended thresholds:
     - **US30:** Mean ± 2 standard deviations.
     - **USD/JPY:** Mean ± 2 standard deviations.

2. **Hourly Monitoring:**
   - Focus on high-variability periods for each symbol.

3. **Anomaly Detection Workflow:**
   - Input real-time data and flag anomalies for further investigation.

4. **Visual Dashboards:**
   - Create real-time line charts with flagged anomalies.


