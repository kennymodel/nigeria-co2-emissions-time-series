# Time Series Modelling and Forecasting of CO₂ Emissions in Nigeria (1980-2024)

Final year project, Department of Statistics, University of Ibadan.
Author: Victor Kehinde. Supervisor: Dr. Otekurin.

## What this project does

It models and forecasts Nigeria's CO₂ emissions using 45 years of annual data. Nigeria emitted about 136 million tonnes of CO₂ in 2024. The project asks what drives emissions in the long run and how well simple models forecast them.

Objectives:
1. Describe the trend in emissions from 1980 to 2024.
2. Test for a long-run relationship using the ARDL bounds test.
3. Estimate long-run elasticities and the speed of adjustment.
4. Forecast to 2030 and give policy recommendations.

## Data

Annual data, 1980 to 2024 (45 observations), all in natural logs.

| Variable | Source |
|---|---|
| CO₂ emissions | Global Carbon Budget, via Our World in Data |
| Population | World Bank, World Development Indicators |
| GDP per capita (constant 2015 US$) | World Bank, World Development Indicators |
| Total energy supply, converted to energy per capita | Our World in Data (Energy Institute, Smil, US EIA) |

## Methods

- Stationarity checks: ADF and KPSS tests, ACF and PACF plots
- ARIMA (Box-Jenkins) as a benchmark forecasting model
- ARDL bounds test (Pesaran, Shin and Smith, 2001) with an error-correction term
- Diagnostics: Ljung-Box, Jarque-Bera, VIF
- Forecast check on a hold-out period, 2020 to 2024
- Tools: Python, pandas, NumPy, matplotlib, statsmodels, Jupyter

## Key results

- Bounds test F-statistic is 5.10, above the 1% upper bound, so a long-run relationship exists.
- Error-correction term is -0.47: about 47% of any gap closes each year.
- Long-run elasticities: population 2.03 (significant), GDP per capita -1.13 (significant at 5%), energy per capita -0.42 (not significant).
- On the 2020 to 2024 hold-out, ARIMA(0,1,0) with drift had a MAPE of 4.86%, against 9.73% for the ARDL model.
- ARIMA forecast: about 138 million tonnes in 2025 rising to about 149 million in 2030, with very wide 95% intervals.

## Limitations

Only 45 observations, a short 5-year hold-out, national totals only, and unclear order of integration for population. Structural breaks were not modelled.

## Files

- `PROJECT ANALYSIS.ipynb`: the full analysis in Python
- Charts (PNG): time plots, scatter plots, growth chart, ACF and PACF
- `Project 1-5 (Completed) (1).pdf`: the complete project report

## How to run

1. Install Python and Jupyter.
2. Install the packages: `pip install pandas numpy matplotlib statsmodels`
3. Place the data files in the same folder as the notebook.
4. Open `PROJECT ANALYSIS.ipynb` and run the cells from top to bottom.
