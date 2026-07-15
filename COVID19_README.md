# COVID-19 Trend Analysis & Forecasting

Analysis of global and India-level COVID-19 case trends, with a time-series forecasting model predicting confirmed cases 7 days ahead.

## Objective

- Visualize global and India-level COVID-19 trends (confirmed, recovered, deaths, active cases)
- Analyze infection and recovery rate patterns over time
- Build a time-series forecasting model (Prophet) to predict confirmed cases 7 days into the future, with confidence intervals

## Dataset

- **Source:** Johns Hopkins University CSSE COVID-19 time-series data (public GitHub repository)
- Daily cumulative confirmed cases, deaths, and recovered cases by country, from the start of the pandemic

## Approach

1. **Data Loading** — pulled real-time historical data directly from the JHU CSSE public dataset.
2. **Data Processing** — aggregated country-level data into global and India-specific time series; computed daily new cases and active cases from cumulative totals.
3. **Visualization** — interactive Plotly charts showing cumulative trends (confirmed/recovered/deaths/active) over time.
4. **Forecasting** — built a Prophet time-series model on global confirmed cases, producing a 7-day-ahead forecast with 95% confidence intervals.

## Results

- Global and India trend visualizations covering the full pandemic timeline
- A working 7-day forecast of global confirmed cases, with upper/lower confidence bounds, validated against the model's own fit on historical data

## Tech Stack

`Python` · `pandas` · `Plotly` · `Prophet` (Facebook's time-series forecasting library) · `requests`

## How to Run

1. Install dependencies: `pip install pandas plotly prophet requests`
2. Run all cells in `COVID19_Analysis.ipynb` top to bottom (data is pulled live from the JHU GitHub repository, no local file needed)

## Key Takeaway

This project demonstrates an end-to-end time-series workflow: pulling and cleaning real-world data, exploratory visualization, and applying a proper forecasting model (Prophet) rather than a naive projection — including honestly reporting model uncertainty via confidence intervals.
